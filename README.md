# Spark Batch Processor Application

This application processes data from a RAW zone to a Processed zone using Spark, while addressing potential issues with small files.

## Description

- The application reads data from specific partitions in the RAW zone, corresponding to today's date.
- It performs schema validation, type validation, and formatting.
- To avoid the small files problem, the application coalesces the data into a reasonable number of files before writing to the destination.
- The processed data is then written to the Processed zone, partitioned by date.

## Pre-requisites

- Apache Spark
- Python 3.x
- pyhocon (for configuration parsing)
- Logging module (for logging operations)

## Configuration

The application requires a configuration file (`application.conf`) with the following parameters:

- `s3.raw-zone-path`: The path to the RAW zone where the data is read from.
- `s3.processed-zone-path`: The path to the Processed zone where the data will be written to.
- `data.xml_schema`: The schema for XML validation.

Ensure these configurations are correctly set before running the application.

## Usage

To run the Batch Processor Application:
`python BatchProcessorApp.py`


## Logging
The application logs its operations, which can be helpful for troubleshooting and monitoring. The logs are saved to logs/batch_processor_app.log.

## Note
Adjust the number of partitions in the coalesce method based on the typical size of your data and your specific requirements to efficiently handle the small files problem.

## Contributors
Ihor Haivan

## License
This project is licensed under the MIT License - see the LICENSE.md file for details.