# Gold channel api document
## Table of Contents
- [Authentication](#authentication)
  - [Google Login](#google-login)
  - [Mobile Login](#mobile-login)
- [Home Page](#home-page)


## Authentication

### Google Login
### Google Login Redirect

#### URL
`POST /api/v1/auth/google`

#### Description
Google redirect url and get token to authenticate

#### Request parameters
- 

#### Show validarion error
- 

#### Response (status 200)
- 


### Google Login Handel callback

#### URL
`POST /auth/google/callback`

#### Description
Google callback with token to authenticate

#### Request parameters
- `callback_token` (string): Google token.(required)

#### Show validarion error
```json  
{
    "success": false,
    "message": {
        "callback_token": [
            "The callback token field is required."
        ]
    }
}
```

#### Response (status 200)
```json
{
  "success": true,
  "message": "Login successful",
  "token": "your_bear_token"
}
```

### Mobile Login

## Home Page





