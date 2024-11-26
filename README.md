# TinoTesting
Setup Trino on docker and setup multiple connectors with it.

So Basically, what I did was I wanted to use trino an attach multiple connectors and transfer data between them and make life easier.

I added Trino, with catalogs
1. Clickhouse -> Is used for analytics
2. PostgreSQL -> Is used to store Facts, Dimensions and Lookup Tabeles (you can use it for whatever you want)
3. DeltaLake -> Use it for you lakehouse

So Basically what you do is that you dump your data inside DeltaLake. You write quereis for you Facts, Dimensions and Lookup Tables in PostgreSQL.
Here we levergae the power of trino, as in a single query we can tranfer data from DeltaLake to PostgreSQL.
Then we can write the Aggregated Tables inside Clickhouse.
