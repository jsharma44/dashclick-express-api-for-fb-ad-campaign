# Intoduction

A [Expressjs](https://expressjs.com) API which is using [Facebook Business SDK](https://developers.facebook.com/docs/business-sdk). This is API only. Frontend/client is independent

# Features

-   Manage CURD operation on ad campaign
-   A Minimul API with best code practice
-   I am using [.prettierrc](.prettierrc) file rule to manage coding styles
-   This is a limited feature api just to get started

# Installation

## Before you install

1. Make sure nodejs and npm is installed on your system.
2. For Windows OS follow the nodejs installer
3. For debian based system use following commands

````bash
# Install curl
sudo apt-get install -y curl

# Get nodejs
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -

# Install nodejs

sudo apt-get install -y nodejs

# Confirm  node version
node -v

# Confirm npm is installed
npm -v

## Clone Repo

### Get Source Code in your current directory

```bash
git clone ssh://git@github.com/user/repo.git .
````

## Install Packages

```bash
 npm install
```

## setup

-   Rename [apiKeys.json.example](apikeys.json.example) to apikeys.json
-   Dont worry about security we are not pushing it to repository. We have added it to .gitignore
-   get your [Ad Account ID](https://www.facebook.com/ads/manager/accounts/) and put [apikeys.json](apikeys.json)
-   Get user access token. Right now we are generating a access token from [Graph API Tool Explorer](https://developers.facebook.com/tools/explorer/). Make sure you are getting access token only after granting permission for ad_campaign. Token will expire after 60 minutes you need to reissue again and use them again.
-   In real world application we will get this access token from user consent when user will log into our ad campaign dashboard.

```json
{
    "ad_account_id": "act_<AD_ACCOUNT_ID>",
    "access_token": "<ACCESS_TOKEN>"
}
```

# Serve

To serve this api use

```bash
npm run start
```

if you have nodemon installed globally you can use

```bash
npm run dev
```

Now you can access api at

```bash
http://localhost:3000/campaign/
```

# Available Endpoints

| method | Endpont                            | Required Parameter                  |
| ------ | ---------------------------------- | ----------------------------------- |
| GET    | http://localhost:3000/campaign/    | none                                |
| POST   | http://localhost:3000/campaign/    | name,objective, special_ad_category |
| PUT    | http://localhost:3000/campaign/:id | none                                |
| DELETE | http://localhost:3000/campaign/:id | none                                |
