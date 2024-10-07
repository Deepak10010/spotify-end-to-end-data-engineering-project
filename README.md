# spotify-end-to-end-data-engineering-project



The Spotify project involved building a data pipeline to automate the extraction, transformation, and loading (ETL) of music data from Spotify's API into cloud storage for analysis. The project began by creating an application in Spotify's developer platform to access their API, and configuring an AWS environment, which included setting up S3 buckets to store both raw and processed data.

The ETL workflow was managed using AWS Lambda functions. A custom Python script was developed for these Lambda functions, leveraging the Spotipy library to interact with Spotify's API and Pandas for transforming the data. To handle limitations of Lambda, additional layers were added for required libraries. The data transformation involved organizing information about songs, albums, and artists into a structured format, making it ready for analysis.

The project also involved configuring IAM roles to ensure secure communication between AWS services and using environment variables to keep sensitive information secure. AWS Glue was utilized to create metadata tables, enabling the structured data to be queried using Amazon Athena. The pipeline was automated with scheduled triggers for Lambda functions, and the entire process was monitored to ensure successful data ingestion and transformation, including moving processed data to different S3 folders for better data management.

This project allowed for near real-time ingestion and transformation of Spotify data, enabling efficient storage and easy retrieval for analysis, with a focus on using serverless cloud infrastructure to minimize maintenance.
