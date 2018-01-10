---
title: API Reference

language_tabs: # must be one of https://git.io/vQNgJ
- javascript

toc_footers:
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the create-node-app API! You can access endpoints, which get information on various users in our database.

You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This API documentation page was created with [Slate](https://github.com/lord/slate). Feel free to edit it and use it as a base for your own API's documentation.

# Headers

> When passing in these headers, it should look something like this:

```javascript
  some-request-library({
      url: some-url,
      headers: {
          ...
          'x-token': meowmeowmeow,
          'x-user-id': woofwoof,
      }
  })
```

> Make sure to replace `meowmeowmeow & woofwoof` with your user id and token.

All endpoints will require these headers except for when first creating a user.

We expect these two things so that we can verify that it's actually you.

`x-token: "meowmeowmeow", x-user-id: "woofwoof"`

<aside class="notice">
You must replace <code>meowmeowmeow & woofwoof</code> with your personal token and id.
</aside>

# Users
## Get Or Create A User

> An example POST request will have a payload that looks like

```javascript
{
    "first": "john",
    "last": "doe",
    "email": "jdoe@us.company.com",
    "password": "password"
}
```


> Success response

```json
{
  "id": 2,
  "first_name": "john",
  "last_name": "doe",
  "email": "jdoe@123.com",  
  "created": true
}
```

This endpoint attempts to create a user. If the user already exists, it gets it instead.

### HTTP Request

`POST http://127.0.0.1/user`

## Get User

> Success response

```json
{
  "id": 2,
  "first_name": "john",
  "last_name": "doe",
  "email": "jdoe@123.com",
}
```

This endpoint gets your user details

### HTTP Request

`GET http://127.0.0.1/user`

<aside class="notice">
Custom headers required 
</aside>

## Log In

Coming Soon. This will contain the token that you need.

