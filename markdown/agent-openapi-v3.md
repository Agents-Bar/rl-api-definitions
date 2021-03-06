---
title: Agents Bar - Agent v0.1.1
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="agents-bar-agent">Agents Bar - Agent v0.1.1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Agents Bar compatible Agent entity

<h1 id="agents-bar-agent-default">Default</h1>

## api_get_agent_info_agent_get

<a id="opIdapi_get_agent_info_agent_get"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /agent \
  -H 'Accept: application/json'

```

```http
GET /agent HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/agent',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/agent',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/agent', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/agent', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/agent", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /agent`

*Api Get Agent Info*

Describes agent.

Provides summary information of the agent.
The method should be relatively light.

> Example responses

> 200 Response

```json
{
  "model": "string",
  "hyperparameters": {},
  "last_active": "2019-08-24T14:15:22Z",
  "discret": true
}
```

<h3 id="api_get_agent_info_agent_get-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|[AgentInfo](#schemaagentinfo)|

<aside class="success">
This operation does not require authentication
</aside>

## api_post_agent_agent_post

<a id="opIdapi_post_agent_agent_post"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /agent \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /agent HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "model_type": "string",
  "obs_space": {
    "dtype": "string",
    "shape": [
      0
    ],
    "low": 0,
    "high": 0
  },
  "action_space": {
    "dtype": "string",
    "shape": [
      0
    ],
    "low": 0,
    "high": 0
  },
  "model_config": {},
  "network_state": "string",
  "buffer_state": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/agent',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/agent',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/agent', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/agent', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/agent", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /agent`

*Api Post Agent*

Create agent.

The agent is reused by other methods. There is no "update" method to agent's interal state
so in case it needs changes it should be deleted and recreated.

> Body parameter

```json
{
  "model_type": "string",
  "obs_space": {
    "dtype": "string",
    "shape": [
      0
    ],
    "low": 0,
    "high": 0
  },
  "action_space": {
    "dtype": "string",
    "shape": [
      0
    ],
    "low": 0,
    "high": 0
  },
  "model_config": {},
  "network_state": "string",
  "buffer_state": "string"
}
```

<h3 id="api_post_agent_agent_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AgentCreate](#schemaagentcreate)|true|none|

> Example responses

> 201 Response

```json
null
```

<h3 id="api_post_agent_agent_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Successful Response|Inline|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="api_post_agent_agent_post-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## api_delete_agent_agent__agent_name__delete

<a id="opIdapi_delete_agent_agent__agent_name__delete"></a>

> Code samples

```shell
# You can also use wget
curl -X DELETE /agent/{agent_name} \
  -H 'Accept: application/json'

```

```http
DELETE /agent/{agent_name} HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/agent/{agent_name}',
{
  method: 'DELETE',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.delete '/agent/{agent_name}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('/agent/{agent_name}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','/agent/{agent_name}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent/{agent_name}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "/agent/{agent_name}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /agent/{agent_name}`

*Api Delete Agent*

Deletes agent and all related attribute. A hard reset.

Agent name (reference) is necessary to prevent accidental deletion.

<h3 id="api_delete_agent_agent__agent_name__delete-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|agent_name|path|string|true|none|

> Example responses

> 422 Response

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}
```

<h3 id="api_delete_agent_agent__agent_name__delete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Successful Response|None|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<aside class="success">
This operation does not require authentication
</aside>

## api_get_agent_state_agent_state_get

<a id="opIdapi_get_agent_state_agent_state_get"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /agent/state \
  -H 'Accept: application/json'

```

```http
GET /agent/state HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/agent/state',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/agent/state',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/agent/state', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/agent/state', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent/state");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/agent/state", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /agent/state`

*Api Get Agent State*

Retruns agent's state.

The state should be sufficient to fully describe and reconstruct the agent.
It might be that in some situations the reconstructed agent doesn't produce
the exact same output, e.g. due to internal randomness, but statistically
they need to be the same.

> Example responses

> 200 Response

```json
{
  "model": "string",
  "state_space": {},
  "action_space": {},
  "encoded_config": "string",
  "encoded_network": "string",
  "encoded_buffer": "string"
}
```

<h3 id="api_get_agent_state_agent_state_get-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|[AgentStateJSON](#schemaagentstatejson)|

<aside class="success">
This operation does not require authentication
</aside>

## api_get_agent_last_active_agent_last_active_get

<a id="opIdapi_get_agent_last_active_agent_last_active_get"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /agent/last_active \
  -H 'Accept: application/json'

```

```http
GET /agent/last_active HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/agent/last_active',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/agent/last_active',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/agent/last_active', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/agent/last_active', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent/last_active");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/agent/last_active", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /agent/last_active`

*Api Get Agent Last Active*

Returns timestamp of agent's latest usage.

> Example responses

> 200 Response

```json
"2019-08-24T14:15:22Z"
```

<h3 id="api_get_agent_last_active_agent_last_active_get-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|string|

<aside class="success">
This operation does not require authentication
</aside>

## api_get_agent_hparasm_agent_hparams_get

<a id="opIdapi_get_agent_hparasm_agent_hparams_get"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /agent/hparams \
  -H 'Accept: application/json'

```

```http
GET /agent/hparams HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/agent/hparams',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/agent/hparams',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/agent/hparams', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/agent/hparams', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent/hparams");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/agent/hparams", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /agent/hparams`

*Api Get Agent Hparasm*

Returns hashmap of agent's hyperparameters.

> Example responses

> 200 Response

```json
null
```

<h3 id="api_get_agent_hparasm_agent_hparams_get-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|

<h3 id="api_get_agent_hparasm_agent_hparams_get-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## api_get_agent_loss_agent_loss_get

<a id="opIdapi_get_agent_loss_agent_loss_get"></a>

> Code samples

```shell
# You can also use wget
curl -X GET /agent/loss \
  -H 'Accept: application/json'

```

```http
GET /agent/loss HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/agent/loss',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/agent/loss',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('/agent/loss', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','/agent/loss', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent/loss");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "/agent/loss", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /agent/loss`

*Api Get Agent Loss*

Returns agent's loss values.

By default it only returns the most recent metrics, i.e. single timestamp.
Max timestamp values is based on the agent's intialization.

<h3 id="api_get_agent_loss_agent_loss_get-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|last_samples|query|integer|false|none|

> Example responses

> 200 Response

```json
[
  {
    "property1": 0,
    "property2": 0
  }
]
```

<h3 id="api_get_agent_loss_agent_loss_get-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="api_get_agent_loss_agent_loss_get-responseschema">Response Schema</h3>

Status Code **200**

*Response Api Get Agent Loss Agent Loss Get*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|Response Api Get Agent Loss Agent Loss Get|[object]|false|none|none|
|?? **additionalProperties**|number|false|none|none|

<aside class="success">
This operation does not require authentication
</aside>

## api_post_agent_step_agent_step_post

<a id="opIdapi_post_agent_step_agent_step_post"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /agent/step \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /agent/step HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "obs": [
    0
  ],
  "action": [
    0
  ],
  "next_obs": [
    0
  ],
  "reward": 0,
  "done": true
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/agent/step',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/agent/step',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/agent/step', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/agent/step', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent/step");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/agent/step", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /agent/step`

*Api Post Agent Step*

Feed agent with step information.

The minimum required is the current state and reward.
Some agents, for convinience, might also require passing last action,
auxilary infrmation whether state is terminal (done) and the next state.

By default, the Step is committed to the agent in the request.
In case it's needed to delay committing, e.g. gathering all information first,
one can use `/agent/commit` method.

> Body parameter

```json
{
  "obs": [
    0
  ],
  "action": [
    0
  ],
  "next_obs": [
    0
  ],
  "reward": 0,
  "done": true
}
```

<h3 id="api_post_agent_step_agent_step_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|commit|query|boolean|false|none|
|body|body|[AgentStep](#schemaagentstep)|true|none|

> Example responses

> 200 Response

```json
null
```

<h3 id="api_post_agent_step_agent_step_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<h3 id="api_post_agent_step_agent_step_post-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## api_post_agent_commit_agent_commit_post

<a id="opIdapi_post_agent_commit_agent_commit_post"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /agent/commit \
  -H 'Accept: application/json'

```

```http
POST /agent/commit HTTP/1.1

Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('/agent/commit',
{
  method: 'POST',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.post '/agent/commit',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.post('/agent/commit', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/agent/commit', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent/commit");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/agent/commit", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /agent/commit`

*Api Post Agent Commit*

Commits submitted step into Agent.

Before using this method the data needs to be submitted using `/agent/step`.

> Example responses

> 200 Response

```json
null
```

<h3 id="api_post_agent_commit_agent_commit_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|Inline|

<h3 id="api_post_agent_commit_agent_commit_post-responseschema">Response Schema</h3>

<aside class="success">
This operation does not require authentication
</aside>

## api_post_agent_act_agent_act_post

<a id="opIdapi_post_agent_act_agent_act_post"></a>

> Code samples

```shell
# You can also use wget
curl -X POST /agent/act \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST /agent/act HTTP/1.1

Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '[
  0
]';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('/agent/act',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post '/agent/act',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('/agent/act', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','/agent/act', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("/agent/act");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "/agent/act", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /agent/act`

*Api Post Agent Act*

Infers action based on provided observation.

    

> Body parameter

```json
[
  0
]
```

<h3 id="api_post_agent_act_agent_act_post-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|noise|query|number|false|none|
|body|body|any|true|none|

> Example responses

> 200 Response

```json
{
  "action": 0
}
```

<h3 id="api_post_agent_act_agent_act_post-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Successful Response|[AgentAction](#schemaagentaction)|
|422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Validation Error|[HTTPValidationError](#schemahttpvalidationerror)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_AgentAction">AgentAction</h2>
<!-- backwards compatibility -->
<a id="schemaagentaction"></a>
<a id="schema_AgentAction"></a>
<a id="tocSagentaction"></a>
<a id="tocsagentaction"></a>

```json
{
  "action": 0
}

```

AgentAction

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|action|any|true|none|none|

anyOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|integer|false|none|none|

or

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|number|false|none|none|

or

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|[integer]|false|none|none|

or

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|[number]|false|none|none|

<h2 id="tocS_AgentCreate">AgentCreate</h2>
<!-- backwards compatibility -->
<a id="schemaagentcreate"></a>
<a id="schema_AgentCreate"></a>
<a id="tocSagentcreate"></a>
<a id="tocsagentcreate"></a>

```json
{
  "model_type": "string",
  "obs_space": {
    "dtype": "string",
    "shape": [
      0
    ],
    "low": 0,
    "high": 0
  },
  "action_space": {
    "dtype": "string",
    "shape": [
      0
    ],
    "low": 0,
    "high": 0
  },
  "model_config": {},
  "network_state": "string",
  "buffer_state": "string"
}

```

AgentCreate

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|model_type|string|true|none|none|
|obs_space|[DataSpace](#schemadataspace)|true|none|none|
|action_space|[DataSpace](#schemadataspace)|true|none|none|
|model_config|object|false|none|none|
|network_state|string(binary)|false|none|none|
|buffer_state|string(binary)|false|none|none|

<h2 id="tocS_AgentInfo">AgentInfo</h2>
<!-- backwards compatibility -->
<a id="schemaagentinfo"></a>
<a id="schema_AgentInfo"></a>
<a id="tocSagentinfo"></a>
<a id="tocsagentinfo"></a>

```json
{
  "model": "string",
  "hyperparameters": {},
  "last_active": "2019-08-24T14:15:22Z",
  "discret": true
}

```

AgentInfo

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|model|string|true|none|none|
|hyperparameters|object|true|none|none|
|last_active|string(date-time)|true|none|none|
|discret|boolean|true|none|none|

<h2 id="tocS_AgentStateJSON">AgentStateJSON</h2>
<!-- backwards compatibility -->
<a id="schemaagentstatejson"></a>
<a id="schema_AgentStateJSON"></a>
<a id="tocSagentstatejson"></a>
<a id="tocsagentstatejson"></a>

```json
{
  "model": "string",
  "state_space": {},
  "action_space": {},
  "encoded_config": "string",
  "encoded_network": "string",
  "encoded_buffer": "string"
}

```

AgentStateJSON

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|model|string|true|none|none|
|state_space|object|true|none|none|
|action_space|object|true|none|none|
|encoded_config|string|true|none|none|
|encoded_network|string|true|none|none|
|encoded_buffer|string|true|none|none|

<h2 id="tocS_AgentStep">AgentStep</h2>
<!-- backwards compatibility -->
<a id="schemaagentstep"></a>
<a id="schema_AgentStep"></a>
<a id="tocSagentstep"></a>
<a id="tocsagentstep"></a>

```json
{
  "obs": [
    0
  ],
  "action": [
    0
  ],
  "next_obs": [
    0
  ],
  "reward": 0,
  "done": true
}

```

AgentStep

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|obs|any|true|none|none|

anyOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|[integer]|false|none|none|

or

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|[number]|false|none|none|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|action|[number]|true|none|none|
|next_obs|any|true|none|none|

anyOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|[integer]|false|none|none|

or

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|[number]|false|none|none|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|reward|number|true|none|none|
|done|boolean|true|none|none|

<h2 id="tocS_DataSpace">DataSpace</h2>
<!-- backwards compatibility -->
<a id="schemadataspace"></a>
<a id="schema_DataSpace"></a>
<a id="tocSdataspace"></a>
<a id="tocsdataspace"></a>

```json
{
  "dtype": "string",
  "shape": [
    0
  ],
  "low": 0,
  "high": 0
}

```

DataSpace

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|dtype|string|true|none|none|
|shape|[integer]|true|none|none|
|low|any|false|none|none|

anyOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|number|false|none|none|

or

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|[number]|false|none|none|

continued

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|high|any|false|none|none|

anyOf

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|number|false|none|none|

or

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|?? *anonymous*|[number]|false|none|none|

<h2 id="tocS_HTTPValidationError">HTTPValidationError</h2>
<!-- backwards compatibility -->
<a id="schemahttpvalidationerror"></a>
<a id="schema_HTTPValidationError"></a>
<a id="tocShttpvalidationerror"></a>
<a id="tocshttpvalidationerror"></a>

```json
{
  "detail": [
    {
      "loc": [
        "string"
      ],
      "msg": "string",
      "type": "string"
    }
  ]
}

```

HTTPValidationError

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|detail|[[ValidationError](#schemavalidationerror)]|false|none|none|

<h2 id="tocS_ValidationError">ValidationError</h2>
<!-- backwards compatibility -->
<a id="schemavalidationerror"></a>
<a id="schema_ValidationError"></a>
<a id="tocSvalidationerror"></a>
<a id="tocsvalidationerror"></a>

```json
{
  "loc": [
    "string"
  ],
  "msg": "string",
  "type": "string"
}

```

ValidationError

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|loc|[string]|true|none|none|
|msg|string|true|none|none|
|type|string|true|none|none|

