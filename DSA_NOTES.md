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
* Latency in batch processing refers to the time delay between when data is collected and when it is actually processed and results are available. Latency is high. Not suitable for immediate use.
* Handles large volume effectively
* data is processed in groups and not individually
* Fault tolerance in batch processing refers to the system’s ability to continue processing correctly even if errors, failures, or interruptions occur during the execution of batch jobs. Easier to retry uses checkpoints and all
* cheaper then real time processing for large volumes
# Advantages of Batch Processsing
* Efficiency at scale : Proscessing large volumes of data all at once, which is often more resource efficient than handling each task individually
* Automated Scheduling : ideal for task that don't require real time processing - run overnight or off peak hours
* Error Handling and Retry Logic : Easier to apply consistent error handing, rollback mechanisms or validation acrosss batches, which improves reliability
* Reduced manual intervention : once automated doesn't require human intervention
* Resource optimization : when data is runned in bulk often large amount ofmemory is required
* Consistency and standadization : ideal for appliying the same logic throughout the dataset
# Limitations of Batch Processing 
 * Delayed results: not apt for time sensitive analysis( fraud detection)- scheduled at time intervals
 * Resource spikes : large bulks require more sources therefore affect the performance at peak times
 * Complex debugging : if error occurs finding it through a bulk job is more difficult than real time processing
 * Limited Flexibility : once a batch starts we have to wait till the next batch to make changes
 * data staleness : the insights are freash as the last batch run bad news if you need current data to make decisions
# Batch processing architecture
Data sources-----Data injestion(scheduled jobs)----Storage level(HDF5,S3,ETC)-----Batch processing(spark, hadoop)---processsed data(DW, DBs, Reports)---BI Tools\reports
#  Common Batch Processsing tools
* Apache Spark
* Apache Hadoop
* Talend
* AWS Glue
* Google Dataflow(batch mode)
* Azure Data Factory
 
