## Reporting

----

### Billing dans bigquery
* Les informations liées au billing sont <b>exportées en continu dans Bigquery</b>.
	* Table détaillée des coûts journalier, table : <b>gcp_billing_export_v1_<BILLING_ACCOUNT_ID></b>
	* Grille tarifaire, table : <b>cloud_pricing_export</b>
	

----

## Requetes dans bigquery
```sql
SELECT
  invoice.month, service.description,
  ROUND(SUM(cost) + SUM(IFNULL((
        SELECT
          SUM(c.amount)
        FROM
          UNNEST(credits) c),
        0))) AS cost_after_credits
FROM
  `data-analytics-pocs:public.gcp_billing_export_EXAMPL_E0XD3A_DB33F1`
WHERE
  invoice.month = "201906"
GROUP BY
  1,2
ORDER BY 3 DESC;
```

Resultat de la requete bigquery
|Row | month | description | cost_after_credits
| --- | --- | --- |--- |
|1 | 201906 | Compute engine | $1605.00
|2 | 201906 | Cloud Storage | $102.31
|3 | 201906 | App Engine | $1220.76
|4 | 201906 | BigQuery | $73.0
|5 | 201906 | cloud Pub/Sub | $0.0

----

## Visualiser les dépenses avec Google Data Sutdio

Google propose des templates permettant de suivre depuis Google Data Studio les dépenses
![Data Studio](img/Billing-dashboard.png)