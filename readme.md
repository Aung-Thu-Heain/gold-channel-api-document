# Gold channel api document
## Table of Contents
- Authentication
  - [Google Login](#google-login)
  - [Mobile Login](#mobile-login)
  - [Logout](#logout)
- Home
  - [Banner](#banner)
  - [Recently Add](#recently-add)
  - [Top rated movies](#top-rated-items)





## Google Login

#### URL
`GET /api/v1/auth/google`

#### Description
Google redirect url and get token to authenticate


### Google Login Handel callback

#### URL
`GET /auth/google/callback`

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

## Mobile Login


## Logout
### URL
`POST /logout`

#### Description
Logout user

#### Headers
- `Authorization` : Bearer Token
#### Response (status 200)
```json
{
  "success": true,
  "message": "Logout successfull",
}
```


## Banner
#### URL
`POST /home-banner`

#### Description
Home banner

#### Response (status 200)
```json
{
  "success": true,
  "message": "Banner list reterived successfully",
  "data": "banner_list"
}
```


## Recently Add
#### URL
`POST /recently-add`

#### Description
Recently added videos and tv shows

#### Response (status 200)
```json
{
  "success": true,
  "message": "Recently added items reterived successfully",
  "data": "item_list"
}
```


## Top rated items
#### URL
`POST /top-rated/{type}`

#### Description
type = movie | tvshow

#### Response (status 200)
```json
{
  "success": true,
  "message": "Recently added {type} reterived successfully",
  "data": "item_list"
}
```





