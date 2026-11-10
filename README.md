# Claude BigQuery Basics Skill

A practical skill for managing Google BigQuery datasets, tables, and query jobs, with guidance for data ingestion, client libraries, infrastructure, security, and AI-assisted analytics.

## What It Covers

- **Setup:** Enable the BigQuery API and configure datasets and tables.
- **SQL queries:** Run GoogleSQL queries and work with public datasets.
- **CLI operations:** Use the `bq` command-line tool to manage resources and jobs.
- **Client libraries:** Work with BigQuery from Python, Java, Node.js, and Go.
- **MCP integration:** Use the BigQuery remote MCP server and Gemini CLI extension.
- **Infrastructure as Code:** Manage datasets, tables, and reservations with Terraform.
- **IAM and security:** Apply permissions and data governance practices.
- **BigQuery AI and ML:** Connect BigQuery analytics with AI/ML capabilities where applicable.

## Installation

Clone the repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-bigquery-basics-skill.git ~/.claude/skills/bigquery-basics
```

## Quick Start

Enable the API:

```bash
gcloud services enable bigquery.googleapis.com --quiet
```

Create a dataset:

```bash
bq mk --dataset --location=US my_dataset
```

Create a table using a schema file:

```bash
bq mk --table my_dataset.mytable schema.json
```

Run a GoogleSQL query:

```bash
bq query --use_legacy_sql=false \
'SELECT name FROM `bigquery-public-data.usa_names.usa_1910_2013`
 WHERE state = "TX" LIMIT 10'
```

## Using the Skill

Ask Claude for a task such as:

```text
Use the bigquery-basics skill to create a dataset, define a table schema,
and write a GoogleSQL query for my data.
```

## Reference Files

- [Core concepts](references/core-concepts.md)
- [CLI usage](references/cli-usage.md)
- [Client library usage](references/client-library-usage.md)
- [MCP usage](references/mcp-usage.md)
- [Infrastructure as Code](references/iac-usage.md)
- [IAM and security](references/iam-security.md)

For BigQuery AI and ML workflows, the skill also points to the related BigQuery AI and ML skill and its reference materials.
