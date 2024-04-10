
# Introduction

This is the main deliverable of the Plugin Inventory WG.
You are encouraged to contribute to this list by:

-  Confirming the status of one or more plugins that you're using ("does it work?")
- Adding notes on what elements you see missing (even if the integration is working for you)

## Why?

Flyte is a platform only to the extent it is extensible. Also, it's on the interest of the community to rely on a robust ecosystem of integrations. This assessment is a first step towards finding possible issues on particular integrations and eventually allocate resources to fix them.

## Agents

|  Name | Status   |Reported by |Missing elements (documentation/code)   |  Notes |Date |
|---|---|---|---|---|---|
|  Airflow |   |   |   |   | |
|  ChatGPT |   |   |   |   | |
|  Databricks | (Legacy plugin) Works with issues |Robert Ambrus   |   | [Reported issue](https://github.com/flyteorg/flyte/issues/5203) | 04/09/2024 |
|  BigQuery | (Legacy plugin) Works but could be better |  Jake Dodd |  | Coming from Airflow, most of our SQL was heavily templated using jinja. We worked around this by rendering the query in a function and passing that to the BigQuery Task. But if there was a way to do this with the Task directly. I know you can use BigQuery params, but these don’t support table names being templated, which is the main thing we template | 04/02/2024 |
|MMCloud |   |   |   |   |  |
|  Sensor |   |   |   |   | |
|  Snowflake |   |   |   |   | |  


## Backend plugins
|  Plugin | Does it work?   |Reported by |Missing elements (documentation/code)   |  Notes | Date |
|---|---|---|---|---|---|
|  Athena | Yes | Laura Lin   |  Better documentation | It's not clear how to configure the plugin to get the `athena:StartQueryExecution` permissions |11/03/2023 |
|  AWS Batch|   |   |   |  | |  
|  Dask | Yes  |Len Strand   | Making it easier to scale up the cluster in the task without having to fix the number of resources in the task signature. We have implemented that, but it requires us to use python kubernetes to find the deployment and scale up manually.  | Overall, I think this is a very useful plugin for the work that we do since we use Xarray for many of the inputs/outputs in our data workflows. Some weaknesses are that back to back dask tasks may incur slower startup/shutdown times. If one has an aggressive autoscaler enabled, the time it takes to serialize outputs and wrap up the task may be enough time for resources to be removed from k8s cluster. Then on the next task we have to wait for autoscaler to kick up more nodes. This may contribute to 3+ mins per dask task transition. Not the worst, but something worth mentioning. We have 7+ back to back dask clusters, which means that the minimum amount of time even if not running any code in the task would be 21+ minutes. Overall, I think it is as useful as it is popular in the community. Ray may be preferred by software engineers, but I think dask may more popular with scientists.  |04/10/2024 |
|  Hive |   |   |   | Is this still available?  | |
|  MPI |   |   |   |    |  |
|  KFPytorch | Yes  | Fabio Graetz  |03/22/2024 | 
|  Ray |   |   |   |    | |
|  Spark | Yes  | Frank Shen  | Better documentation  |   | 03/26/2024 |
|  KFTensorflow |   |   |   |  |   |


## flytekit plugins

|  Plugin | Does it work for your use case?   | Reported by|Missing elements (documentation/code) |  Notes |  Date |
|---|---|---|---|---|---|
|  bacalhau |   |   |   |   | |
|  dbt |  Yes |   |  Better documentation |   | 03/27/2024 |
|  dolt | Yes, with issues  |   |  |  [Reported issue](https://github.com/flyteorg/flyte/issues/5074) | 03/19/2024  | 
|  duckdb |   |   |   |  |  |
|  envd (ImageSpec)| Yes  |  | Better documentation  |   | 03/27/2024 |
|flyteinteractive |  No | Alex Beach  | Better documentation  |   | 03/27/2024| 
|  greatexpectations |   |   |   |  |  |
|  huggingface |   |   |   |   |  |
|  identity-aware-proxy |  Yes |Fabio Graetz   |   |  | 03/22/2024 |  
|  huggingface |   |   |   |   |
|  mmcloud |   |   |   |   |  |
|  mlflow | Yes, but it's limited  | Jose Navarro  |   |The main caveat so far is that the plugin renders the training traces only for one task, not the whole experiment.  | 10/31/2023|
|  modin |   |   |   |   | |
|  onnxtensorflow |   |   |   |    | |   
|  onnxscikitlearn |   |   |   |   |  |
|  onnxpytorch |   |   |   |   |  |
|  pandera |   |   |   |   | |
|  papermill |   |   |   |  |  |
|  polars |   |   |   |   | |
|  pydantic |   |   |   |  |  |
|  sqlalchemy | Yes, but it's limited  |Greg Linklater   |   |SQLAlchemyTask it is fine for selects, it does not seem to do much for inserting data.  |  | 11/23/2023 |
|  vaex |   |   |   |   | |
|  whylogs |  Yes | David Espejo  | Better documentation  | Apparently, it's necessary to use the custom Docker image, but this is not mentioned in the docs. |04/08/2024  |



