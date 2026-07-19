# Spotify Data Pipeline

A personal data engineering project that demonstrates an end-to-end data pipeline using the Spotify Web API and AWS.

The project extracts data from the Spotify Web API, transforms the API responses into structured datasets, stores them in Amazon S3, and enables SQL-based analytics through Amazon Athena.

## Running the Project

1. Install the required dependencies.

```bash
pip install pandas requests boto3
```

2. Configure your Spotify API credentials.

```python
client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"
```

3. Configure your AWS credentials.

4. Open the notebook and execute all cells sequentially.

## Querying the Data

After the datasets are uploaded to Amazon S3, they can be queried using SQL in Amazon Athena.
