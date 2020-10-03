# Apache Spark Standalone Cluster on Docker

> Originally forked from [https://github.com/cluster-apps-on-docker/spark-standalone-cluster-on-docker](https://github.com/cluster-apps-on-docker/spark-standalone-cluster-on-docker)

This project gives you an **Apache Spark** cluster in standalone mode with a **JupyterLab** interface built on top of **Docker**.
Learn Apache Spark through its **Scala**, **Python** (PySpark) and **R** (SparkR) API by running the Jupyter [notebooks](build/workspace/) with examples on how to read, process and write data.

Start the cluster by typing:
```bash
docker-compose up
```

Run Apache Spark code using the provided Jupyter [notebooks](build/workspace/) with Scala, PySpark and SparkR examples. Finally, stop the cluster by typing `ctrl+c`.

<p align="center"><img src="docs/image/cluster-architecture.png"></p>

## <a name="tech-stack"></a>Tech Stack

- Infrastructure

| Component      | Version |
| -------------- | ------- |
| Docker Engine  | 1.13.0+ |
| Docker Compose | 1.10.0+ |
| Python         | 3.7.3   |
| Scala          | 2.12.11 |
| R              | 3.5.2   |

- Jupyter Kernels

| Component      | Version | Provider                                |
| -------------- | ------- | --------------------------------------- |
| Python         | 2.1.4   | [Jupyter](https://jupyter.org/)         |
| Scala          | 0.10.0  | [Almond](https://almond.sh/)            |
| R              | 1.1.1   | [IRkernel](https://irkernel.github.io/) |

- Applications

| Component      | Version                 | Docker Tag                                           |
| -------------- | ----------------------  | ---------------------------------------------------- |
| Apache Spark   | 2.4.0 \| 2.4.4 \| 3.0.0 | **\<spark-version>**-hadoop-2.7                      |
| JupyterLab     | 2.1.4                   | **\<jupyterlab-version>**-spark-**\<spark-version>** |

> Apache Spark R API (SparkR) is only supported on version **2.4.4**. Full list can be found [here](https://cran.r-project.org/src/contrib/Archive/SparkR/).
