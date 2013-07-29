---
category: survey
path: '/survey/single/iframe'
title: 'Get a single-use iframe-able survey (new or existing)'
type: 'POST'
params: 'server_url form_id'
codes: [200, 400, 401, 403, 404, 405, 410]
layout: nil
---

### Request

* required parameter **`server_url`** is the url of the OpenRosa server your form is hosted on.
* required parameter **`form_id`** is the ID of the form listed in _SERVER_/formList.
* The headers must include a **valid authentication token**.

```Authentication: basic API_TOKEN:```

### Response

Sends back an object including an single_iframe_url property.

```Status: 200 OK (existing)    Status: 201 OK (new)```
```{
    single_iframe_url:  'https://abcde.enketo.org/webform/single?iframe=true',
    code: '200'
}```