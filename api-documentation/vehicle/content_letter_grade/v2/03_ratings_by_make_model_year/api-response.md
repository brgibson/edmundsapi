---
layout: api-documentation
title : 'Get All Rating Details Reviews for the Given Make/Model/Year'
title_active_left_menu: "Content: Letter Grade Rating"
title_parent: Api documentation

amount_version: 1
title-endpoint: 'Get All Rating Details Reviews for the Given Make/Model/Year'
spec: content_letter_grade
version: v2
api: vehicle
dropdown-link: 'api/vehicle/v2/{make}/{model}/{year}/grade'


level: 4
description_edpoint: 'Get All Rating Details Reviews for the Given Make/Model/Year'
title_md : Response format
number: 3

---

###Response format

#### JSON Response

    {
        "reviews": [
            {
                "make": {object},
                "model": {object},
                "style": {object}, 
                "id": {integer},
                "year": {integer},
                "date": {date},
                "grade": {string},
                "summary": {style}
            }
            ...
        ],
        "reviewsCount": {integer}
    }

| Property                      | Description                                           | Visibility                |
|:------------------------------|:------------------------------------------------------|:------------------------- |
| make                          | The car make                                          | Edmunds, Partners, Public |
| model                         | The car model                                         | Edmunds, Partners, Public |
| style                         | The car style                                         | Edmunds, Partners, Public |
| id                            | The review id                                         | Edmunds, Partners, Public |
| year                          | The car model year                                    | Edmunds, Partners, Public |
| date                          | The date of this review                               | Edmunds, Partners, Public |
| grade                         | The grade assigned by Edmunds's editorial team        | Edmunds, Partners, Public |
| summary                       | The review                                            | Edmunds, Partners, Public |

The <code>make</code> object follows this format:

    {
        "id": {integer},
        "name": {string},
        "niceName": {string}
    }

| Property      | Description                                              | Visibility                |
|:--------------|:---------------------------------------------------------|:------------------------- |
| id            | The Edmunds ID for the car make/brand                    | Edmunds, Partners, Public |
| name          | The name of this car make                                | Edmunds, Partners, Public |
| niceName      | URL-friendly car make/brand name                         | Edmunds, Partners, Public |

The <code>model</code> object follows this format:

    {
        "id": {string},
        "name": {string},
        "niceName": {string},
    }

| Property      | Description                                                    | Visibility                |
|:--------------|:---------------------------------------------------------------|:------------------------- |
| id            | The Edmunds ID for the car model                               | Edmunds, Partners, Public |
| name          | The name of this car model                                     | Edmunds, Partners, Public |
| niceName      | URL-friendly car model name                                    | Edmunds, Partners, Public |

The <code>style</code> object follows this format:

    {
        "id": {integer},
        "name": {string},
        "submodel": {object},
        "trim": {string}
    }

| Property      | Description                                                    | Visibility                |
|:--------------|:---------------------------------------------------------------|:------------------------- |
| id            | The Edmunds ID for the car style                               | Edmunds, Partners, Public |
| name          | The car style name                                             | Edmunds, Partners, Public |
| submodel      | The vehicle submodel (body and modelName info)                 | Edmunds, Partners, Public |
| trim          | The vehicle trim for this car style                            | Edmunds, Partners, Public |

The <code>submodel</code> object follows this format:

    {
        "body": {string},
        "modelName": {string},
        "niceName": {string}
    }

| Property      | Description                                                         | Visibility                 |
|:--------------|:--------------------------------------------------------------------|:-------------------------- |
| body          | The type of car body (e.g. "Sedan", "Hatchback")                    | Edmunds, Partners, Public  |
| modelName     | The name of this submodel (e.g. "Civic Hatchback", "X5 SUV Diesel") | Edmunds, Partners, Public  |
| niceName      | The nice name of this submodel (e.g. "sedan", "diesel")              | Edmunds, Partners, Public  |
