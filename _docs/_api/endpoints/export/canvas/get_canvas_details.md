---
nav_title: "GET: Canvas Details"
article_title: "GET: Canvas Details"
search_tag: Endpoint
page_order: 4
layout: api_page
page_type: reference
description: "This article outlines details about the Canvas Details Endpoint."

---
{% api %}
# Canvas details endpoint
{% apimethod get %}
/canvas/details
{% endapimethod %}

Use this endpoint to export metadata about a Canvas, such as the name, time created, current status, and more.

{% apiref postman %}https://documenter.getpostman.com/view/4689407/SVYrsdsG?version=latest#5188873c-13a3-4aaf-a54b-9fa1daeac5f8 {% endapiref %}

## Rate limit

{% multi_lang_include rate_limits.md endpoint='default' %}

## Request parameters

| Parameter   | Required | Data Type | Description            |
| ----------- | -------- | --------- | ---------------------- |
| `canvas_id` | Required | String | See [Canvas API Identifier]({{site.baseurl}}/api/identifier_types/) |
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

## Example request
{% raw %}
```
curl --location -g --request GET 'https://rest.iad-01.braze.com/canvas/details?canvas_id={{canvas_identifier}}' \
--header 'Authorization: Bearer YOUR-REST-API-KEY'
```
{% endraw %}

## Response

```json
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
{
  "created_at": (string) the date created as ISO 8601 date,
  "updated_at": (string) the date updated as ISO 8601 date,
  "name": (string) the Canvas name,
  "description": (string) the Canvas description,
  "archived": (boolean) whether this Canvas is archived,
  "draft": (boolean) whether this Canvas is a draft,
  "schedule_type": (string) the type of scheduling action,
  "first_entry": (string) the date of first entry as ISO 8601 date,
  "last_entry": (string) the date of last entry as ISO 8601 date,
  "channels": (array of strings) step channels used with Canvas,
  "variants": [
    {
      "name": (string) the name of variant,
      "id": (string) the API identifier of the variant,
      "first_step_ids": (array of strings) the API identifiers for first steps in variant,
      "first_step_id": (string) the API identifier of first step in variant (deprecated in November 2017, only included if the variant has only one first step)
    },
    ... (more variations)
  ],
  "tags": (array of strings) the tag names associated with the Canvas,
  "steps": [
    {
      "name": (string) the name of step,
      "id": (string) the API identifier of the step,
      "next_step_ids": (array of strings) the API identifiers of steps following step,
      "channels": (array of strings) the channels used in step,
      "messages": {
          "message_variation_id": (string) {  // <=This is the actual id
              "channel": (string) the channel type of the message (eg., "email"),
              ... channel-specific fields for this message, see Campaign Details endpoint API Response for example message responses ...
          }
      }
    },
    ... (more steps)
  ],
  "message": (required, string) the status of the export, returns 'success' when completed without errors
}
```

{% alert tip %}
For help with CSV and API exports, visit [Export troubleshooting]({{site.baseurl}}/user_guide/data_and_analytics/export_braze_data/export_troubleshooting/).
{% endalert %}

{% endapi %}
