# *Data Engineering Internship at TE Connectivity*

# Event-Driven System Design for Data Pipeline Implementation

## Overview
This project, titled **"Event-Driven System Design for Data Pipeline Implementation,"** was part of my Professional Final Assignment (PFA) internship at **TE Connectivity** in Tanger.  
The goal was to design and implement an efficient data pipeline for the manufacturing process by streaming, processing, and visualizing data in real-time.

The pipeline streams data from two Excel files, updated periodically via **Robotic Process Automation (RPA)**, into a **ClickHouse** data lakehouse using **Kafka**. The first file tracks machine interruptions, and the second records the quality of produced pieces.  
Key metrics such as **Machine Availability** and **Scrap Rate** are calculated from this data and visualized on real-time dashboards to support decision-making.

## Objectives
1. Automate the extraction of Excel files ("Interactions" and "Confirmations") using **UiPath RPA** tools.
2. Stream data into an event-driven pipeline using **Apache Kafka**.
3. Implement a scalable **ClickHouse** lakehouse architecture for data storage and processing.
4. Build **data marts** to store key performance metrics like Machine Availability and Scrap Rate.
5. Develop real-time **Angular dashboards** to visualize actionable insights.
6. Improve operational efficiency and decision-making through real-time analytics.


## Architecture
Below is the architecture of the implemented solution:

![architecture_solution](https://github.com/user-attachments/assets/69133f27-2dbc-49a5-a5cd-09025d00f6c4)


### Explanation of Components:
1. **Sourcing Layer:**
   - Data files ("Interactions" and "Confirmations") are periodically extracted and updated using **UiPath**.

2. **Streaming Layer:**
   - **Apache Kafka** serves as the backbone for data streaming.
   - Integration with **FastAPI** and **FastStream** ensures efficient event management.

3. **Data Lakehouse Layer:**
   - **ClickHouse** is utilized as a high-performance lakehouse for storing raw, staging, and transformed tables.
   - The ELT (Extract -> Load -> Transform) paradigm is applied for data processing.

4. **Data Marts Layer:**
   - Pre-aggregated metrics such as Machine Availability and Scrap Rate are stored in data marts for analytics.

5. **Visualization Layer:**
   - Real-time dashboards are built using **Angular** and **Python**, showcasing key metrics like availability and scrap rate.

## Technical Stack

| Component          | Technology Used         |
|--------------------|-------------------------|
| **Automation**     | UiPath                  |
| **Streaming**      | Apache Kafka, FastAPI, FastStream |
| **Storage**        | ClickHouse              |
| **Orchestration**  | Docker                  |
| **Visualization**  | Angular, Python         |

## Methodology
The project follows an **ELT (Extract -> Load -> Transform)** approach:
1. **Extract:** Data is extracted from Excel files via UiPath and streamed to Kafka topics.
2. **Load:** Raw data is loaded into ClickHouse lakehouse tables.
3. **Transform:** Data transformations are performed within ClickHouse to calculate Machine Availability and Scrap Rates.

## Implementation Details
1. **Data Extraction:**
   - Automated using **UiPath** to handle periodic updates in Excel files.

2. **Data Streaming:**
   - Kafka topics are used to stream raw data to ClickHouse.
   - **FastAPI** and **FastStream** manage smooth integration between Kafka and data pipelines.

3. **Data Transformation:**
   - Transformation logic is implemented directly in ClickHouse for deriving metrics.

4. **Dashboards:**
   - Dashboards display metrics like Machine Availability, Scrap Rate, and Production Trends in real-time.

## Results
The project successfully implemented a robust and scalable data pipeline. Key outcomes include:
- Real-time insights into machine availability and scrap rates.
- Enhanced operational efficiency in the manufacturing process.
- Angular dashboards that enable data-driven decision-making.

## Challenges and Limitations
- **Privacy Policies:** The raw data and dashboard results cannot be shared publicly.
- **Integration Complexity:** Combining tools like Kafka, ClickHouse, and FastStream required rigorous testing.
- **Latency:** Maintaining low latency in streaming pipelines for real-time visualization.

## Future Work
1. **Predictive Analytics:** Implement advanced metrics like Overall Equipment Effectiveness (OEE) and predictive maintenance models.
2. **Interactive Dashboards:** Add drill-down capabilities and real-time alerting features.
3. **System Integration:** Connect the pipeline with ERP and MES systems for a comprehensive view of the manufacturing process.
4. **Data Quality Assurance:** Enhance validation and error-detection mechanisms in data processing.

## Learning Experience
- Hands-on experience with **event-driven architecture** using Kafka.
- Proficiency in tools like **ClickHouse**, **Polars**, and **Ibis** for data processing.
- Practical knowledge in building real-time dashboards using **Angular**.
- Integration of multiple technologies using **Docker Compose**.

## Conclusion
This project demonstrated the power of combining modern data streaming, processing, and visualization tools to create a scalable and efficient manufacturing data management system.  
The knowledge gained during this internship has provided a strong foundation for future advancements in data engineering and real-time analytics.

## Contact
For any queries regarding this project, feel free to reach out:
- **Name:** Loubna Boukayoua
- **Role:** Data Engineer Intern
- **Company:** TE Connectivity


