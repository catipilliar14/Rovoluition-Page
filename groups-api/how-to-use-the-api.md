# How to use the API

### Start Using the Module:

#### **HTTPS Must be enabled!!** <a href="#https-must-be-enabled-4" id="https-must-be-enabled-4"></a>

First we need to create a new Project on [RovolutionLogistics](https://logistics.rovolution.me/)\
1.) [RovolutionLogistics - Dashboard](https://logistics.rovolution.me/dashboard), you may need to sign in with Discord!\
2.) Click create new project!

![](https://doy2mn9upadnk.cloudfront.net/uploads/default/optimized/4X/b/f/e/bfebc9d1046bf2ca907dfb5b7116569f2fd4e422\_2\_690x316.png)

3.) Enter a project name, and then click next!\
4.) Now select Roblox API

![](https://doy2mn9upadnk.cloudfront.net/uploads/default/optimized/4X/9/4/6/94656b3d4d96f082d51618496d468b334cb1beb2\_2\_690x315.png)

\
\
5.) Now enter your Ranking accounts Roblox token, in Roblox User Token box. To get your token follow the guide below!

![](https://doy2mn9upadnk.cloudfront.net/uploads/default/optimized/4X/1/a/8/1a8039ffd5348922647a6f56f0991a223b917a97\_2\_690x304.png)

6.) Now click download the code snippet, this will automatically add your API key and Project ID, you can open this in notepad or go to Roblox and right click on ServerScriptService and select `Insert from File` and insert it!

***

### Get Roblox Login Token: <a href="#get-roblox-login-token-5" id="get-roblox-login-token-5"></a>

**Roblox tokens are what unlocks an account, they allow users to spend your Robux, trade your items and edit your games! Please always use a alternate Roblox account and never share your token!** If you know what you are doing please continue the guide below:

{% hint style="warning" %}
**NOTICE:** You will need to use a VPN set to London due to Roblox's Continent lock with Cookies. You should use an incognito browser and then close the browser rather than logging out.
{% endhint %}

{% hint style="danger" %}
**WARNING:** You should not use your **personal** Roblox account for the bot. You should use an **alternate** which you do not use.&#x20;
{% endhint %}

#### Click the padlock on the address bar! <a href="#click-the-padlock-on-the-address-bar-6" id="click-the-padlock-on-the-address-bar-6"></a>

[![image](https://doy2mn9upadnk.cloudfront.net/uploads/default/optimized/4X/b/2/8/b280c5e220bdb0dc78eb58630b3b5e8bcab714bf\_2\_597x500.jpeg)](https://doy2mn9upadnk.cloudfront.net/uploads/default/original/4X/b/2/8/b280c5e220bdb0dc78eb58630b3b5e8bcab714bf.jpeg)

#### Then click Cookies: <a href="#then-click-cookies-7" id="then-click-cookies-7"></a>

![image](https://doy2mn9upadnk.cloudfront.net/uploads/default/original/4X/5/4/a/54ab37d054f34552c03be7704fe404b596e01185.png)

#### Find this cookie: <a href="#find-this-cookie-8" id="find-this-cookie-8"></a>

[![image](https://doy2mn9upadnk.cloudfront.net/uploads/default/optimized/4X/6/8/a/68a507575f7b1d9199bc7c22acd5214ec9c66ffa\_2\_624x499.png)](https://doy2mn9upadnk.cloudfront.net/uploads/default/original/4X/6/8/a/68a507575f7b1d9199bc7c22acd5214ec9c66ffa.png)

#### Select all: <a href="#select-all-9" id="select-all-9"></a>

[![image](https://doy2mn9upadnk.cloudfront.net/uploads/default/optimized/4X/8/b/0/8b0c82c1cdae0571957cd77312a0790db2b1ad6a\_2\_425x500.png)](https://doy2mn9upadnk.cloudfront.net/uploads/default/original/4X/8/b/0/8b0c82c1cdae0571957cd77312a0790db2b1ad6a.png)\
And then copy the cookie into Rovolution Logistics!



### Using the API Wrapper:

#### Example code:

```
-- Example using the Rovolution API --
local Rovolution_Module = require(9520664531).default -- Default because of the way the wrapper is written

local ProjectID = "TEST_PROJECT_ID"
local API_KEY = "TEST_API_KEY"

local API = Rovolution_Module.new(ProjectID, API_KEY)

-- Now we can talk to the API

-- For example promote a user
local groupID = 7535264 -- Rovolution Group
local userID = 3152860974 -- A test account

API:PromoteUser(groupID, userID)
```

#### Current wrapper functions:

The wrapper exposes 5 functions, we aim to implement more.

```
API:PromoteUser(groupID, userID)
API:DemoteUser(groupID, userID)
API:AcceptJoinRequest(groupID, userID)
API:RejectJoinRequest(groupID, userID)
API:ExileUser(groupID, userID)
API:SetRank(groupID, userID, rank)
```

### Using the API without the Wrapper:

Base URL - [https://roblox.rovolution.me/api/v1/roblox-api/](https://roblox.rovolution.me/api/v1/roblox-api/)

Only **POST** requests accepted!

Example lua code

```
local HttpService = GetService("HttpService")
local json_Serialised = HttpService:JSONEncode({
            projectID = "ENTER_PROJECT_KEY_HERE",
			apiKey = "ENTER_API_KEY_HERE",
			data = {
                   groupID = "ENTER_GROUP_TO_PROMOTE_IN",
                   userID = "ENTER_USER_USERID",
            },
}) 
HttpService:PostAsync("https://roblox.rovolution.me/api/v1/roblox-api/promoteUser", json_Serialised)
```

#### API Routes:

* checkKey
* promoteUser
* demoteUser
* exileUser
* acceptJoinRequest
* denyJoinRequest
* setRank

### Contributions:

Contributions are always welcome, [github.com/RovolutionTeam/Rovolution-Roblox-API-Wrapper](https://github.com/RovolutionTeam/Rovolution-Roblox-API-Wrapper) We are using Roblox-TS to convert TS to LUA.

### Further Assistance:

If you require any further assistance with the Ranking API you can join the [Rovolution Support server](https://discord.com/invite/2bMg4evVWz).&#x20;
