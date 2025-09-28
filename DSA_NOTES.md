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
#  Stream processing
Continuous and real-time processing of data asits flows in. No delay between data arrival and processing. Latency is low, designed for ongoing and unbounded streams od data, small time windows, use cases - alerting, monitoring.fault tolerance - managed via checkpoints and windowing and more compute intensive-higher price.
Data ingestion : data is continuosly ingested.
real-time processing : each event is processed as it arrives
output delivery : results are pushed immediately to databases or dashboards.
#  Examples
* fraud detection in banking : monitors every transaction
* Real time ride matching(uber and ola) : location of drivers and riders are updated
* real time analytics for E-commerce : track live user behaviours
* social media feeds and notification : provides real time messaages and notification
* Log monitoring and alerting: monitor server logs and application errors in real time
* Online gaming leaderboards : update scores and ranking live as users play
* stock market data and alerts : provide stock prices or transcation for live dashboards
* video live streaming analytics : update the number of viewers
* Smart traffic system : monitor vehicle flows and agjust the traffic
#  Advantages
* data handled as a comntinuous and unbounded flow
* processing is real time and insights are delivered instantly
* Essential for instant decision making (real time recomendations)
* demands hig availability, always on infrastructure
* errors and anomalies detected as they occur, enabling immediate actions
#  Feature engineering, Feature sllection and Feature extraction
Feature engineering : broad process that includes creating new features,transformingexisting ones and selecting the most relevant ones. Enhance the dataset for better model prediction. methods like selection, extraction, transformation and cretion of features.
Feature Selection : a specific technique within feature engineering focused on selecting the most relevant features from the dataset. simplify the model and improve performance by reducing the number of features.Filter, wrappee and embedded are the methods.
Feature extraction : aimed at tranforming existing features into new and more informative ones. Create new features that better capture the underlying data patterns or reduce dimensionality. PCA, ICA and Polynomial features are the method
#  Feature engineering
process of using domain knowledge to extract and transform raw data into features that make machine learning algorithms work efficiently. Involves selectingor creating new features from the existing data to improve the performance.
## key concepts
* feature : a variable or attribute in the dataset that the model will make use for predictions.
* Engineering : process of refining, transforming and creating features to better represent the underlying pattern.
## Importance of feature engineering
* Improves model accuracy : reveals hiddden pattern in data and gives accurate prediction.
* Reduces overfitting : by selecting and transforming features that generalize well across different dataset.
* Simplifies the model : reduces the complexity of model by dropping irrelevant and redundant features, leading tofaster training amnf inferance timing.
* Enhance interpretability : that are meaningfull and well-constructed can make predictions more interpretable.
##  Real world example of feature engineering
* E-commersce recomendation system
#  Filter Methods (Feature selection)
Filter method select features based on statistical measures and do not involve any machine learning algorithms.
##  Common techniques
* Correlation Coefficient : identify the linear relationship between features and target variables. Calculate the pearson correlation cofficient for continuous variables.
* Chi-Square test : teat the independent relation between categorical features and the target variable. Suitable for categorical data.
* ANOVA (Analysis of Vriance) : Compare the means of different groups and determine if the mean of a feature differs significantly from others. Suitable for continuous input and categorical output.
#  Advanced Feature Selection Technique
##  Supervised  Technique
* Filter-based approach : Information gain, chi-square test, Fisher's score, missing value ratio
* Wrapper-based approach : forward selection, backward selection, exhaustic feature selection, recurrcive feature elimination
* Embedded approach : regularization, random forest importance
##  Unsupervised techniques 
* PCA
* ICA
* NMF
* t-SNE
* Autoencoder
#  Techniques for feature extraction
Ivolves transforming the existing feature to new feature that better shows the structure of data. This helps in improving the models performance by better understanding the non-linear relationships, reducing dimensionlityor representing data in a way that is more suitable for the machine learning algorithm.
* Principal component analysis(PCA) : reduces the dimensionality of the data by transforming it into a set of uncorrelated variables called principal components.
* Independent component analysis : separates a multivariable signal into additive, independent components.
* Feature construction : creating new features based on existing ones such that polynomial features , interaction terms etc
* Discretization/Binning : converts continuous bins into categorical bins
*   
  

 
