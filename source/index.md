---
title: School Wellness API Reference

language_tabs:
  - html

toc_footers:
  - <a href='http://schoolwellness.herokuapp.com'>School Wellness</a>
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:

search: true
---

# Introduction

School Wellness provides an interface to view cafeteria health inspection report data for DC Public Schools.

# Schools

## Get All Schools

```json
[
  {
  "id": 1,
  "name": "ANACOSTIA SENIOR HIGH SCHOOL",
  "address": "1601 16th ST SE",
  "createdAt": "2015-08-27T19:33:18.734Z",
  "updatedAt": "2015-08-27T19:33:18.734Z"
  },
  {
  "id": 2,
  "name": "ACHIEVEMENT PREP",
  "address": "1500 MISSISSIPPI AVE SE",
  "createdAt": "2015-08-27T19:33:18.734Z",
  "updatedAt": "2015-08-27T19:33:18.734Z"
  }
]
```

This endpoint retrieves all schools.

### HTTP REQUEST

`GET http://schoolwellness.herokuapp.com/schools`

## Get One School
```json
{
"id": 1,
"name": "ANACOSTIA SENIOR HIGH SCHOOL",
"address": "1601 16th ST SE",
"createdAt": "2015-08-27T19:33:18.734Z",
"updatedAt": "2015-08-27T19:33:18.734Z"
}
```

This endpoint retrieves one school

### HTTP REQUEST

`GET http://schoolwellness.herokuapp.com/schools/<ID>`

### URL PARAMTERS

Parameter | Description
--------- | -----------
ID|The ID of the school to retrieve|

# Health Reports

## Get One School's Health Report
```json
{
"id": 1,
"riskCategory": 2,
"numberCritical": 1,
"numberNoncritical": 4,
"createdAt": "2015-08-27T19:33:18.845Z",
"updatedAt": "2015-08-27T19:33:18.845Z",
"schoolId": 1,
"name": "ANACOSTIA SENIOR HIGH SCHOOL",
"address": "1601 16th ST SE"
}
```

This endpoint retrieves one school health report

### HTTP REQUEST

`GET http://schoolwellness.herokuapp.com/schools/<ID>/health-report`

### URL PARAMETERS

Parameter | Description
--------- | -----------
ID|The ID of the school to retrieve|
