 # ETL vs ELT
 ## Data Pipeline : series of steps that move data from raw source to where it can be stored, cleaned and analyzed. ETL and ELT are two methods of preparing pipelines.
 * ETL(Extract Transform and Load) : Transformrd to a separate server before loading into data  warehouse.
 * ELT (Extract Load and Transformed) : Raw data loaded to ware house and then transformed.
# ETL
* Data is extracted from raw source.
* Used in systems where strict data validation, compliance and pre_processing are required.
* Best for structured and smaller datbase
* originated in 1970s
* slower ingestion - transformed and used - Batch processing - with fixed schemas and validation rule
* Does not retain raw data giving fewer opportunities for reanalysis
* strong compliance, securuity and governance controls
* Higher infrastructure and maintenance cost
* less flexible, predefined transformation
* real time analysis is challenging
* Banking, healthcare and insurance where strict data rules compliance
# ELT
* Designed for modern cloud based solutions where scalability and flexibility are key.
* designed for cloud warehouses like Snowflake, BigQuery, Redshift
* Handles structured, semistructured and unstructured data
* leverages scalable comute resources to process large dataset quickly
* supports real time or near real time analysis - raw data is uploaded
* flexible allowing changes based on business needs(for future analysis)
* retains original data best for audits, exploration and AI/ML Application(Data exploration)
* Lower cost with clod scalability
* e-commerce, social media and IoT platforms
# Batch Processing
Technique where data is collected and stored over a period of time. Processed as a single unit or batch instead of being processed immediately. 
* Data is collected from various sources
* Data is formed into batches - batches satisfying certain criteria (data till midnight/ 10000 data )
* different from real time as data is analyzed  only when the condition of batches are satisfied ( not like real time data where the data is processed instantly)
* The pipeline process the entire batch at once
* processed data is stored in a database, file or to other sysytem for future use
* 

