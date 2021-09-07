## Concepts avancés

----

### Gestion des accès
* Les projets (pas les folders) sont liés pour la facturation a un (sub)accounts
* Associer les rôles 
	* Creation de billing account : roles/billing.creator
	* Administration des comptes de billing : roles/billing.admin
	* Creation de projet et association au billing account : roles/billing.user
	* Accès à la facturation : roles/billing.viewer
	* Attache / Détache des projets depuis le billing (sub)account : roles/billing.projectManager
	
![Organization](img/access-control-org.png)

----

## Gestion des accès pour une organisation
![accès](img/console-admin.png)

----

## Creation d'un projet
* Project Id : 6 à 30 caracteres
* Services account :
	* Doit être présent au niveau de l'organisation ou un folder
	* Doit avoir le role Project Creator

----

## Creation d'un projet
* Resource Manager, permet la gestion des folders 

![Project](img/manage-resources.png)

----

## La facturation
![Billing](img/billing-gcp.png)

----

## Le reporting
![reporting](img/billing-gcp2.png)

----

## SKU
Les SKU sont des codes d'identification des services GCP
[SKU description](https://cloud.google.com/skus/legacy-ids)

----

## Billing exports
* Export de la facturation 
	* Bigquery
	* Bucket (<b>DEPRECATED</b>)

----

## Budget alerts
* Alerting
	* Billing account
	* Project
![Alerting](img/gcp-alerting.png)
![resources](img/gcp-alerting2.png)

----

## Optimisation des dépenses
* [Sustained use discounts](https://cloud.google.com/compute/docs/sustained-use-discounts) 
* [Committed use discounts](https://cloud.google.com/compute/docs/instances/signing-up-committed-use-discounts)
	* B's : réduction allant jusqu'à 57% 
	* C's : engagement sur 1 ou 3 ans