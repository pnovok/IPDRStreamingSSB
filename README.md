# IPDR Streaming Examples
This repo contains some sample SQL Stream Builder (SSB) jobs to consume and process IPDR messages.

## List of SSB Jobs

1. **Create_IPDR_Table** - This SSB Job with create an IPDR Kafka table and describe it
2. **IPDR_Summary_Select** - This SSB Job will read the data from the Flink table and filter IPDR data stream based on the Service Class field
3. **Hourly_RollUp_Select** - This job will do an hourly roll up of IPDR data stream group by Mac Addr, every 30 second using ROLLUP operator
4. **Create_IPDR_Summary_View** - This SSB job will create a summary view of IPDR usage as tumbling window aggregation over the past 20 seconds upon data arrival grouped by Mac Address
5. **IPDR_Summary_Select** - This SSB job will get IPDR Summary Usage data from the view
6. **IPDR_Summary_Kafka_Sink** - This SBB Job will create an Kafka sink for IPDR summary data and output the data there in JSON format
7. **IPDR_Summary_HDFS_Sink** - This SBB Job will create an HDFS sink for IPDR summary data and output the data there in CSV format

## Usage

To use this repo create a new SSB project called **IPDRStreaming** and go to source control and import the content.
