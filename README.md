[![Stories in Ready](https://badge.waffle.io/geosolutions-it/evo-odas.png?label=ready&title=Ready)](https://waffle.io/geosolutions-it/evo-odas)
# EVO-ODAS 

In this github repo can be found the source code for the ingestion system of the evo-odas project organized in 3 main folders.

## Airflow

The Airflow folder contains the python source code of the custom Operators and DAGs for the ingestion of the Sentinel 1 and 2 data.

## metadata-ingestion

The `metadata-ingestion` folder contains the python code to feed a database used as storage from the OpenSearch plugin for Geoserver.`

* manages OpenSearch Collections and Products
* extracts metadata from Sentinel 1 and 2 SAFE packages
* stores the search parameters 
* generate and stores the OGC links
* generate and store html description

Note that this code will probably wrapped in a Airflow custom Operator(s) to be used during the ingestion process. (So it will be moved in the `Airflow` folder)

## nifi-processors

It contains a [NiFi](https://nifi.apache.org/) custom processr implementation to run the GdalWarp utility.

This is an experiment for the NiFi evaluation as evo-odas workflow engine. 

Read also [this](https://github.com/geosolutions-it/evo-odas/wiki/NiFi-watchers-review) wiki page and have a look at [this](https://docs.google.com/spreadsheets/d/1JT4qdj47SlGxhD9viVAe4UcsW_USira8Lh5HhSpZ60c/edit#gid=409340717) document if you are interested in the workflow engine evaluation topic
