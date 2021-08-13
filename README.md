# DNS_API with JWT authentication

  This is an implementation of DNS API using FastAPI and JWT Authentication

  FastAPI allows the asynchronous programming and has out-of-the box support for the Swagger docs. JWT authentication is one of the most secure procedure to authenticate.
  Details of Authentication with JWT can be found in the below locations:
  
  ```
  https://jwt.io/introduction

  https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/

  ```
 
   This code is inspired from the JWT authentication example provided by FastAPI docs

## Usage
 
  1. Execute the program in a Linux 
  2. The program runs in 127.0.0.1 with port 5000
  3. Authenticate with the user using the following username and password with 
     POST for /token

  ```
  user: svcacct
  password: secret

  ```

  4. Get the JWT tocken from the above step

  5. Send request with JWT token in the "Authorization: Bearer" token Header
  ```
  Eg..

  curl -X 'GET' \
  'http://127.0.0.1:5000/yahoo.com' \
  -H 'accept: application/json' \
  -H 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJzdmNhY2N0IiwiZXhwIjoxNjI4ODczODQwfQ.7D8qvIMy91Hm-wgr6dEOK6iIUTciLPCeBfpRLDV1Hdk'

  ```

  6. The API provides as response as below:
  
  ```
    
{
  "ipaddress": [
    "74.6.231.21",
    "74.6.231.20",
    "74.6.143.26",
    "74.6.143.25",
    "98.137.11.164",
    "98.137.11.163"
  ]
}

  ```

## Execution  through Swagger docs:

### Authentication/Authorization:

![Authorize in Swagger docs](images/authorize.jpg)
![Authoriziation for svcacct](images/authorize1.jpg)

Execution:
![DNS API docs](images/fastapi_bearer.jpg)

Dependencies:
------------
   - Python 3.6+
   - FastAPI
   - python-jose[cryptography]
   - passlib[bcrypt]




