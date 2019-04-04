# Jobs

## Get All Jobs

`GET /ats/api/jobs`

| Parameter | Default | Description                                           |
|-----------|---------|-------------------------------------------------------|
| include   |         | Possible values: `account`         |
| fields    |         | Possible values: `title`, `location`, `industry`, `skills`, `description`, `requirements`, `benefits`, `created_at` |
| sort      |         | Possible values: `created_at`, `title` |
| page      |         | Possible values: `something`       |
| filter    |         | Possible values: `draft`, `published`        |

> RESPONSE:

```
HTTP/1.1 200 OK
Content-Type: application/vnd.api+json
```

```json
{
  "links": {
    "self": "http://example.com/articles"
  },
  "data": [
    {
      "id":"1",
      "type":"job",
      "attributes":{
        "title":"Software Engineer",
        "location":"Athens, Greece",
        "industry":"Software",
        "skills":"Ruby, Java, JS, SQL",
        "description":"<html-encoded-description>",
        "requirements":"<html-encoded-requirements>",
        "benefits":"<html-encoded-benefits>",
        "created_at": "2018-08-10T08:39:36.985Z"
      }
    },
    {
      "id": "2",
      "type": "job",
      "attributes":{
          "title": "Product Manager",
          "location": "Boston, MA, USA",
          "industry": "IT",
          "skills": "product, agile",
          "description": "<html-encoded-description>",
          "requirements": "<html-encoded-requirements>",
          "benefits": "<html-encoded-benefits>",
          "created_at": "2018-08-12T22:31:39.101Z"
      }
    }
  ]
```

> Code footer text here

Some more text here.


## Get A Job

` GET /ats/api/jobs/:id`

| Parameter | Default | Description                                           |
|-----------|---------|-------------------------------------------------------|
| id        |         | The job identifier                                    |
| fields    |         | https://jsonapi.org/format/#fetching-sparse-fieldsets |

> RESPONSE

```
HTTP/1.1 200 OK
Content-Type: application/vnd.api+json
```

```json
{
  "id": "1",
  "type": "job",
  "attributes": {
    "title": "Software Engineer",
    "location": "Athens, Greece",
    "industry": "Software",
    "skills": "Ruby, Java, JS, SQL",
    "description": "<html-encoded-description>",
    "requirements": "<html-encoded-requirements>",
    "benefits": "<html-encoded-benefits>"
  },
  "relationships": {
    "account":{
      "data": {
        "id":"1",
        "type":"account"
      }
    }
  }
}
```

## Create A Job

## Update A Job
