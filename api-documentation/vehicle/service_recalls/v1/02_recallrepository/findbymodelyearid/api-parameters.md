---
layout: api-documentation
title : 'Get Vehicle Recalls by Car Model Year ID'
title_active_left_menu: 'Service: Recalls'
title_parent: Api documentation

amount_version: 1
title-endpoint: 'Get Vehicle Recalls by Car Model Year ID'
spec: service_recalls
version: v1
api: vehicle
dropdown-link: 'v1/api/maintenance/recallrepository/findbymodelyearid'


level: 4
description_edpoint: 'Get Vehicle Recalls by Car Model Year ID'
title_md : Parameters
number: 2

---

###Parameters

| Parameter  | Description                           | Possible Values   | Default Value | Required |
|:-----------|:--------------------------------------|:----------------- |:------------- |:-------- |
| modelyearid | The car model year ID | See the [Spec: Model/Year](/api-documentation/vehicle/spec_model_year/v2/) resource | | Yes |
| fmt        | Response format                       | json              | json          | Yes      |
| api_key    | Vehicle API key                       |                   |               | Yes      |
