---
layout: api-documentation
title : 'Find Inventories by Style ID'
title_active_left_menu: 'Vehicle Listings'
title_parent: Api documentation

amount_version: 2
title-endpoint: 'Find Inventories by Style ID'
spec: vehicle_listings
version: v2
api: inventory
dropdown-link: '/api/inventory/v2/styles/{styleId}'

level: 3
description_edpoint: 'Find Inventories by Style ID'
title_md : Description
number: 1

---

### Description

Get cars available for sale by style id and ZIP.

### URL

    https://api.edmunds.com/api/inventory/v2/styles/{styleId}?zipcode={zipcode}&fmt=json

### Code Example

    # Get your access token
    curl -i -H 'Content-Type: application/x-www-form-urlencoded' 'https://api.edmunds.com/inventory/token' -X POST -d 'client_id=<api key>' -d 'client_secret=<shared secret>' -d 'grant_type=client_credentials'

    # Response should be something like this
    {"token_type":"bearer","mapi":"2ep93tpnyh6p5hgaxmp6qqsa","access_token":"jw8qpg8a3yprdbbkwvu2yas2","expires_in":3600}

    # With the access_token now available, we can make the call
    # In this example, we want to get a list of cars available for sale, or inventory listings, for all NEW cars at the Santa Monica Audi dealership, which has a dealerhsip ID of 26711
    curl -i -H 'Authorization: Bearer jw8qpg8a3yprdbbkwvu2yas2' 'https://api.edmunds.com/api/inventory/v2/styles/200674795?zipcode=90404&fmt=json'

    # You can make the same call directly in the browser as follows
    curl -i 'https://api.edmunds.com/api/inventory/v2/styles/200674795?zipcode=90404&fmt=json&access_token=jw8qpg8a3yprdbbkwvu2yas2'
