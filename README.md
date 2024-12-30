# Data Engineering Internship at TE Connectivity

## Overview

This repository contains the documentation and resources for my Professional Final Assignment (PFA) internship at TE Connectivity.  
The internship focused on designing and implementing an end-to-end data engineering solution for streaming, processing, and visualizing data.

NOTE: Due to privacy policies, the raw data and dashboard results cannot be shared.

## Objectives

1. Automate the extraction of Excel-based data files ("Interactions" and "Confirmations") using robotic process automation (RPA).
2. Implement an event-driven data streaming pipeline with Apache Kafka.
3. Develop a scalable data lakehouse architecture using ClickHouse for storage and processing.
4. Build data marts to store key performance metrics such as **Availability** and **Scrap Rate**.
5. Create visualization dashboards for actionable insights.

## Architecture

Below is the architecture of the implemented solution:

![architecture_solution](https://github.com/user-attachments/assets/69133f27-2dbc-49a5-a5cd-09025d00f6c4)


### Explanation:

1. **Sourcing Layer:**
    - Data files ("Interactions" and "Confirmations") are extracted and updated periodically via **UiPath** RPA tools.

2. **Streaming Layer:**
    - **Apache Kafka** is used for data streaming between components.
    - Integration with **FastAPI** and **FastStream** for efficient handling of events.

3. **Data Lakehouse Layer:**
    - **ClickHouse** serves as the lakehouse for storing raw, staging, and transformed tables.
    - Transformation logic follows the **E-L-T** paradigm (Extract -> Load -> Transform).

4. **Data Marts Layer:**
    - Key metrics, such as Availability and Scrap Rate, are calculated and stored in data marts for analysis.

5. **Visualization Layer:**
    - Analytical dashboards are created using **Python** and **Angular**.

## Technical Stack

| Component          | Technology Used         |
|--------------------|-------------------------|
| **Automation**     | UiPath                  |
| **Streaming**      | Apache Kafka, FastAPI, FastStream |
| **Storage**        | ClickHouse              |
| **Orchestration**  | Docker                  |
| **Visualization**  | Python, Angular         |

## Implementation Details

1. **Data Extraction:**
    - Automated using UiPath to handle periodic updates in Excel files.
    
2. **Data Streaming:**
    - Kafka topics were configured to stream raw data to the ClickHouse lakehouse.
    - FastAPI and FastStream ensured smooth integration between Kafka and the processing pipelines.

3. **Data Transformation:**
    - Staging tables in ClickHouse were used to store raw data.
    - Transformation logic was implemented within ClickHouse for deriving key metrics.

4. **Data Marts:**
    - Designed to store pre-aggregated metrics for Availability and Scrap Rate.

5. **Dashboards:**
    - Created to visualize data for decision-making.
    - Dashboards include filters, charts, and tables for better insights.

## Challenges and Limitations

- **Privacy Concerns:** The enterprise data cannot be shared in this repository.
- **Complex Pipelines:** Integration of multiple tools required rigorous testing and debugging.
- **Latency:** Ensuring low latency in streaming pipelines for real-time insights.

## Contact

For any queries regarding this project, feel free to reach out:
- **Name:** Loubna Boukayoua
- **Role:** Data Engineer Intern
- **Company:** TE Connectivity

