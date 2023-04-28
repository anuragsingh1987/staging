```mermaid
graph LR
    A(Start) --> B(Is the data structured or unstructured?)
    B --> C{Structured?}
    C --> |Yes| D(Is it relational data?)
    D --> E{Do you need to perform complex queries?}
    E --> |Yes| F[Choose Cloud SQL for MySQL or PostgreSQL]
    E --> |No| G[Choose Cloud Firestore or Cloud Datastore for NoSQL]
    D --> H{Do you need to support transactions?}
    H --> |Yes| I[Choose Cloud Spanner]
    H --> |No| J[Choose Cloud Firestore or Cloud Datastore for NoSQL]
    C --> |No| K(Is it time-series data?)
    K --> |Yes| L[Choose Cloud IoT Core or Cloud Pub/Sub with InfluxDB or OpenTSDB]
    K --> |No| M[Choose a database based on other requirements]
    B --> N{Unstructured?}
    N --> |Yes| O{Do you need to support text search?}
    O --> |Yes| P[Choose Cloud Firestore or Cloud Datastore]
    O --> |No| Q[Choose a database based on other requirements]
    N --> |No| R{Do you need to store and process large volumes of data?}
    R --> |Yes| S[Choose Bigtable or BigQuery]
    R --> |No| T[Choose a database based on other requirements]
    T --> Z(End)
    Q --> Z(End)
    S --> Z(End)
    F --> Z(End)
    G --> Z(End)
    I --> Z(End)
    J --> Z(End)
    L --> Z(End)
    P --> Z(End)
    M --> Z(End)

    style F fill:lightgreen,stroke:#333,stroke-width:1px;
    style G fill:lightgreen,stroke:#333,stroke-width:1px;
    style I fill:lightgreen,stroke:#333,stroke-width:1px;
    style J fill:lightgreen,stroke:#333,stroke-width:1px;
    style L fill:lightgreen,stroke:#333,stroke-width:1px;
    style P fill:lightgreen,stroke:#333,stroke-width:1px;
    style S fill:lightgreen,stroke:#333,stroke-width:1px;

```



```mermaid
graph LR
    A(Start) --> B(Is the data structured or unstructured?)
    B --> C("fa:fa-twitter for peace")
    C --> |Yes| D(Is it relational data?)
    D --> E{Do you need to perform complex queries?}
    E --> |Yes| F[Choose a relational database like MySQL, Oracle, or Microsoft SQL Server]
    E --> |No| G[Choose a NoSQL database like MongoDB, Cassandra, or Redis]
    D --> H{Do you need to support transactions?}
    H --> |Yes| I[Choose a relational database like MySQL, Oracle, or Microsoft SQL Server]
    H --> |No| J[Choose a NoSQL database like MongoDB, Cassandra, or Redis]
    C --> |No| K(Is it time-series data?)
    K --> |Yes| L[Choose a time-series database like InfluxDB or OpenTSDB]
    K --> |No| M[Choose a database based on other requirements]
    B --> N{Unstructured?}
    N --> |Yes| O{Do you need to support text search?}
    O --> |Yes| P[Choose a NoSQL database like MongoDB or Elasticsearch]
    O --> |No| Q[Choose a database based on other requirements]
    N --> |No| R{Do you need to store and process large volumes of data?}
    R --> |Yes| S[Choose a data warehousing database like Amazon Redshift or Snowflake]
    R --> |No| T[Choose a database based on other requirements]
    T --> Z(End)
    Q --> Z(End)
    S --> Z(End)
    F --> Z(End)
    G --> Z(End)
    I --> Z(End)
    J --> Z(End)
    L --> Z(End)
    P --> Z(End)
    M --> Z(End)
```
