# Spark Technical Interview: Structured Streaming with Kafka and HDFS

## Exercise Overview:
In the subsequent interview, we would delve deep into a use case to understand the approach for building a simple streaming application. Please note, we don't expect a fully functional code but a comprehensive pseudo code to understand your approach.

### Use Case Description:
1. **Stream Creation**:
   - Develop a Spark Structured Streaming application (either in Python or Scala) to publish some sample data to Kafka.
  
2. **Data Consumption and Storage**:
   - Utilize Spark Structured Streaming (Python or Scala) to read the published data from Kafka.
   - Store this consumed data as Parquet files in HDFS within a designated RAW Zone. You may use a sample XML with nested elements for this task.
  
3. **Data Processing**:
   - Implement an Hourly scheduled Spark Batch process to read from the RAW Zone.
   - Store the processed data as Parquet files in a separate location, termed as the Processed Zone.

### Output Requirements:
- **Project Organization**:
  - Provide a conceptual project folder structure illustrating the organization of scripts, logs, and other relevant files.
  
- **Pseudo Code**:
  - Design sample scripts representing the tasks mentioned in the use case description. These scripts should be pseudo code.
  
- **Key Functionalities**:
  - Kafka Consumption:
    - Offset maintenance.
    - Data de-duplication.
  - XML Parsing:
    - Flatten nested XML structures.
  - Data Validation:
    - Dynamic data validation.
    - Schema validation.
    - Data type validation.
    - Data formatting (like trimming).
  - Fault Tolerance:
    - Comprehensive error handling.
    - Continuous streaming without interruptions.
    - Checkpoint restarts from a specific point.
  - Data Partitioning:
    - Partition the final Parquet data in the Processed Zone based on a date field.

## What We Expect:
1. The primary expectation is to see pseudo code.
2. During our next meeting, we'd like you to present:
   - The main shell script used to submit the Spark job.
   - The Spark program (Python/Scala).
3. Please feel free to refer to GitHub, Google, official Spark documentation, or any other relevant resources to guide your approach.
4. We're mainly interested in your approach. During the interview, a code walk-through will help us understand your choices regarding functions/methods and the reasoning behind them.

**Note**: Please don't hesitate to reach out if you have any questions or need clarifications on the exercise.
