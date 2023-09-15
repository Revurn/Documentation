---
title: Revurn Documentation

language_tabs: # must be one of https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='https://revurn.com/app/account/applications'>Generate a Token</a>

includes:
  - errors

search: true

code_clipboard: true

meta:
  - name: description
    content: Information on how you can interact with the Revurn API
---

# Introduction
Welcome to the developer documentation for interacting with the Revurn API. This guide is designed to provide you with comprehensive insights into seamlessly integrating Revurn's powerful features into your applications. 

# Revurn API
This part of the documentation will display how you can interact with Revurn's API

## User Details
Returns details about a Revurn User

```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));
const UserID = "REVURN_USER_ID";

fetch(`https://revurn.com/api/v1/user/${userId}`, {
  method: 'GET',
  headers: {
    'Authorization': 'YOUR_REVURN_TOKEN',
    'Content-Type': 'application/json',
  },
})
  .then(response => {
    if (!response.ok) {
      throw new Error(`Revurn Error, Status Code: ${response.status}`);
    }
    return response.json();
  })
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error(error);
  });
```

```python
import requests

USER_ID = "REVURN_USER_ID"
url = f'https://revurn.com/api/v1/user/{USER_ID}'
headers = {
    'Authorization': "YOUR_REVURN_TOKEN",
    'Content-Type': 'application/json',
}

response = requests.get(url, headers=headers)

if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print(f"Revurn Error, Status Code: {response.status_code}")
    print(response.text)
```

## Guild Information
Returns details about a Revurn Guild

```javascript
const fetch = (...args) => import('node-fetch').then(({default: fetch}) => fetch(...args));
const GuildID = "REVURN_GUILD_ID";

fetch(`https://revurn.com/api/v1/guilds/${GuildID}`, {
  method: 'GET',
  headers: {
    'Authorization': 'YOUR_REVURN_TOKEN',
    'Content-Type': 'application/json',
  },
})
  .then(response => {
    if (!response.ok) {
      throw new Error(`Revurn Error, Status Code: ${response.status}`);
    }
    return response.json();
  })
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error(error);
  });
```

```python
import requests

GUILD_ID = "REVURN_GUILD_ID"
url = f'https://revurn.com/api/v1/guilds/{GUILD_ID}'
headers = {
    'Authorization': "YOUR_REVURN_TOKEN",
    'Content-Type': 'application/json',
}

response = requests.get(url, headers=headers)

if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print(f"Revurn Error, Status Code: {response.status_code}")
    print(response.text)
```
