# Workable ATS:API Documentation

## Installation

```sh
bundle install
```

## Run Locally

```sh
bundle exec middleman server
```

## Build and Release

```sh
# Generate the static html
bundle exec middleman build --clean

# Upload to server (S3, github pages etc.)
./deploy.sh
```

## Helpers
You can use this (generator)[http://www.tablesgenerator.com/markdown_tables] for tables.
