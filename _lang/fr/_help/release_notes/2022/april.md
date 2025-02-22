---
nav_title: Avril
page_order: 9
noindex: true
page_type: update
description: "Cet article contient les notes de version d’avril 2022."
---

# Avril 2022

## Messages in-app pour Roku

Braze prend désormais en charge l’envoi des messages in-app à vos utilisateurs sur leurs appareils Roku ! Notez que cela nécessite une configuration SDK supplémentaire et n’est pas disponible « out-of-the-box ». Pour plus d’informations sur l’intégration des messages in-app pour Roku, reportez-vous à [messages in-app Roku]({{site.baseurl}}/developer_guide/platform_integration_guides/roku/in-app_messaging/overview/).

## Mode de filtrage complet pour les prédictions du taux d’attrition et d’achat

Si vous voulez créer immédiatement une nouvelle prédiction, seul un sous-ensemble de filtres de segmentation Braze est pris en charge par défaut. Vous pouvez maintenant activer le Mode de filtrage complet pour activer tous les filtres de segmentation, mais ce mode vous limite à une seule fenêtre lors de la création de la prédiction. Consultez les articles suivants pour en savoir plus :

- [Création d’une prédiction du taux d’attrition]({{site.baseurl}}/user_guide/predictive_suite/predictive_churn/creating_a_churn_prediction/#full-filter-mode)
- [Création d’une prévision d’achat]({{site.baseurl}}/user_guide/predictive_suite/predictive_purchases/creating_a_purchase_prediction/#full-filter-mode)

## Option de reciblage pour les réponses avec mot-clé

Quand vous visualisez des analyses pour une campagne SMS, vous pouvez désormais créer facilement un segment pour recibler les utilisateurs qui ont répondu avec une catégorie spécifique de mots-clés. Pour plus d’informations, consultez [Réponses contenant des mots-clés]({{site.baseurl}}/user_guide/message_building_by_channel/sms/sms_campaign_analytics/#keyword-responses) dans les rapports SMS.

## Meilleures pratiques de collecte de données

Vous êtes-vous déjà demandé quand et comment collecter des données utilisateur si vous traitez à la fois avec des utilisateurs connus et des utilisateurs inconnus ? Nous savons que le cycle de vie d’un profil utilisateur à Braze peut être un peu déroutant, donc nous avons rassemblé les [meilleures pratiques de collecte de données]({{site.baseurl}}/user_guide/data_and_analytics/user_data_collection/best_practices/) pour clarifier les différentes méthodes et les meilleures pratiques de collecte de données pour les utilisateurs nouveaux ou existants.

## Obsolescence de l’API Transifex

Depuis le 7 avril 2022, Transifex a arrêté le support pour les versions 2 et 2.5 de son API pour se concentrer sur la version 3. Après cette date, les versions v2 et v2.5 ne seront plus opérationnelles, et les requêtes associées échoueront. Si vous utilisez l’API Transifex, mettez à jour vos appels de Contenu connecté en conséquence. Reportez-vous à [Transifex]({{site.baseurl}}/partners/message_personalization/localization/transifex/) pour plus d’informations.

## Nouveaux partenariats Braze

### Toovio - Plateforme de données client

Le partenariat entre Braze et [Toovio]({{site.baseurl}}/partners/data_and_infrastructure_agility/customer_data_platform/toovio/) fournit des déclenchements de messages en temps quasi réel, des outils pour stimuler les performances et un accès aux outils avancés de mesure de campagne de Toovio.

### Snowplow - Analyses

L’intégration entre Braze et [Snowplow]({{site.baseurl}}/partners/data_and_infrastructure_agility/analytics/snowplow/) permet aux utilisateurs de transférer des événements de Snowplow vers Braze via le marquage côté serveur de Google Tag Manager. La balise Snowplow Braze vous permet d’envoyer des événements à Braze tout en bénéficiant d’une flexibilité et d’un contrôle accrus :

- Visibilité totale sur toutes les modifications de données
- Capacité à évoluer et à se développer au fil du temps
- Toutes les données restent dans votre cloud privé jusqu’à ce que vous choisissiez de les envoyer
- Configuration simplifiée grâce à de vastes bibliothèques de balises et à l’interface utilisateur familière de Google Tag Manager

Tirez parti des données comportementales enrichies de Snowplow pour effectuer des interactions client efficaces dans Braze et livrer des messages personnalisés en temps réel.

### Clarisights - Analyses

L’intégration entre Braze et [Clarisights]({{site.baseurl}}/partners/data_and_infrastructure_agility/analytics/clarisights/) vous permet d’importer des données issues des campagnes et Canvas de Braze pour tirer parti d’une interface de reporting unifiée pour votre performance et votre marketing de rétention client/système de gestion de la relation client (CRM).

### Wyng - Contenu dynamique

L’intégration entre Braze et [Wyng]({{site.baseurl}}/partners/message_personalization/dynamic_content/wyng/) vous permet de tirer parti des expériences de Wyng pour personnaliser vos campagnes et Canvas Braze. Wyng comprend également un portail de préférences des clients afin que les utilisateurs puissent contrôler les données et les préférences qu’ils partagent avec une marque.

### Grouparoo - Automatisation des workflows

L’intégration entre Braze et [Grouparoo]({{site.baseurl}}/help/release_notes/deprecations/grouparoo) facilite l’opérationnalisation des données stockées dans un entrepôt en les envoyant à Braze. En configurant des calendriers de synchronisation automatique, vous pouvez constamment améliorer vos communications client grâce à des informations actualisées.

### Lexer - Plateforme de données client

L’intégration entre Braze et [Lexer]({{site.baseurl}}/partners/data_and_infrastructure_agility/customer_data_platform/lexer/) vous permet de synchroniser des données entre les deux plateformes. Utilisez vos données Lexer pour créer des segments Braze, ou importez vos propres données dans Lexer pour en extraire de précieuses informations.

### Knak - Orchestration des e-mails

L’intégration entre Braze et [Knak]({{site.baseurl}}/partners/message_orchestration/channel_extensions/email_templates/knak/) permet de créer des e-mails totalement réactifs en quelques minutes ou en heures au lieu de quelques jours ou semaines, et de les exporter en tant que modèles Braze prêts à l’emploi. Knak est conçu pour les marketeurs qui souhaitent mettre à niveau leur création d’e-mails pour les campagnes gérées dans Braze, sans avoir besoin d’agences extérieures ou de codage manuel.