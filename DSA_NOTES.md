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
