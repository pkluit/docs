# Helpful Linux Snippets

The purpose of this document is to provide a place for me to document any helpful Linux commands i've found. This will primarily be singular lines or small multi-line commands. Larger items will have their own documents.

## Index

1. [View Google Cloud BigQuery load job info](#sec_1)

## Snippets

#### 1. View Google Cloud BigQuery load job info <a name="sec_1"></a>

command will need to be run in cloud terminal or cloud SDK
```bash
$ bq --format=prettyjson show -j <job_id>
```
