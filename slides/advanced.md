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
	
<img src="img/access-control-org.png" style="background:none; border:none; box-shadow:none;"/>

----

## Gestion des accès pour une organisation
<img src="img/console-admin.png" style="background:none; border:none; box-shadow:none;"/>

----

## Creation d'un projet
* Project Id : 6 à 30 caracteres
* Services account :
	* Doit être présent au niveau de l'organisation ou un folder
	* Doit avoir le role Project Creator

----

## Creation d'un projet
* Resource Manager, permet la gestion des folders 

![resources](img/manage-resources.png)

----

## La facturation
![resources](img/billing-gcp.png)

----

## Le reporting
![resources](img/billing-gcp2.png)

----

## SKU
Les SKU sont des codes d'identification des services GCP
[SKU description](https://cloud.google.com/skus/legacy-ids)

----

## Billing exports & Budget alerts
* Export de la facturation 
	* Bigquery
	* Bucket (<b>DEPRECATED</b>)
* Alerting
	* Billing account
	* Project
![resources](img/gcp-alerting.png)
![resources](img/gcp-alerting2.png)

