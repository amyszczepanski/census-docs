---
description: This page describes how to use Census with Stripe.
---

# Stripe

## Introduction

In this guide, we will show you how to connect your Stripe instance to [Census](https://www.getcensus.com/) and create your first sync.Prerequisites

* [Create a Free Trial Census Account](https://app.getcensus.com/)
* Have your Stripe account ready
* Have the credential to access to your Warehouse. See our articles for each data warehouse here \([Redshift](https://help.getcensus.com/article/10-configuring-redshift-postgresql-access), [Postgres](https://help.getcensus.com/article/10-configuring-redshift-postgresql-access), [BigQuery](https://help.getcensus.com/article/21-configuring-bigquery-access), [Snowflake](https://help.getcensus.com/article/8-configuring-snowflake-access)\)

## 1. Connect Stripe

* Once you are in Census, Navigate to [Connections](https://app.getcensus.com/connections)
* Click the Add Service button
* Select Stripe in the dropdown list

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/5bb7d5d0042863158cc71f7e/images/5fbc4462cff47e00160bcde2/file-tKjZxmKj6C.png)

Follow Stripe OAuth flow to connect Stripe. Your end state should look something like this 👇

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/5bb7d5d0042863158cc71f7e/images/5fbc451b4cedfd00165b33cf/file-jxnqNJwf5C.png)

## 2. Connect your Data Warehouse

Please follow one of our short guides depending on your data warehouse technology

* [Redshift](https://help.getcensus.com/article/10-configuring-redshift-postgresql-access)
* [Postgres](https://help.getcensus.com/article/10-configuring-redshift-postgresql-access)
* [BigQuery](https://help.getcensus.com/article/21-configuring-bigquery-access)
* [Snowflake](https://help.getcensus.com/article/8-configuring-snowflake-access)

## 3. Create your first Model

Now navigate to the [Model section of our Dashboard](https://app.getcensus.com/models)

Here you will have to write SQL queries to select the data you want to see in Stripe. Here are some ideas of data you should select

* The type of customer
* The attribution of the customer
* Order form data to generate an invoice

Once you have created your model, click save. 

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/5bb7d5d0042863158cc71f7e/images/5f6563834cedfd00173b9a49/file-zg53SxxpoO.png)

## 4. Create your first Sync

No head to the [Sync page](https://app.getcensus.com/syncs) and click the Add Sync button

In the " What data do you want to sync?" section

* For the Connection, select the data warehouse you connected in step 2
* For the Source,  select the model you created in step 3

Next up is the "Where do you want to sync data to?" section

* Pick Stripe as the Connection
* For Object, pick **Customer**

For the " How should changes to the source be synced?" section 

* Select Update or Create
* Pick the right mapping key, it can be Email or any other external id for Customer

Finally, select the fields you want to update in the Mapper in the "Which Fields should be updated?" section

* Here simply map the field from your Stripe instance to the column from your model.

The end result should look something like this

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/5bb7d5d0042863158cc71f7e/images/5fbc4804cff47e0017d34b6d/file-drmWJMVTz9.png)

Click the Next button to see the final preview which will have a recap of what will happen when you start the sync

## 5. Confirm the data is in Stripe

Now go back to your Stripe and go view a Customer Profile that should have been updated. If everything well well, you should see your data in Stripe

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/5bb7d5d0042863158cc71f7e/images/5fbc4ae846e0fb0017fcee63/file-mYnHg4FN41.png)

That's it, in 5 steps, you connect Census to Stripe and started syncing customer & product data from your warehouse to Stripe 🎉

If you have any question or if you have any issues getting started, please contact us via the in-app live chat in the bottom right corner or send us an email at support@getcensus.com

