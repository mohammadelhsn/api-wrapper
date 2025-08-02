# @mohammadelhsn/api-wrapper

My first package project — a lightweight wrapper for my API, built to learn how to create, publish, and manage JavaScript packages.

> ⚠️ Heads up: This project is no longer maintained because the original API (hosted on Heroku) has been shut down.

## Stack

| Technology | Icon                                                               |
| ---------- | ------------------------------------------------------------------ |
| API        | ![Discord Bots](https://go-skill-icons.vercel.app/api/icons?i=api) |
| NodeJS     | ![NodeJs](https://go-skill-icons.vercel.app/api/icons?i=nodejs)    |
| TypeScript | ![TypeScript](https://go-skill-icons.vercel.app/api/icons?i=ts)    |
| NPM        | ![NPM](https://go-skill-icons.vercel.app/api/icons?i=npm)          |
| Axios      | ![Axios](https://go-skill-icons.vercel.app/api/icons?i=axios)      |

## Example usage:

<details>
<summary>Click to show / hide</summary>

- Javascript

```js
const API = require('@processversion/api-wrapper');
const api = new API('KEY HERE');
```

- Typescript

```ts
import API from '@processversion/api-wrapper';
const api = new API('KEY HERE');
```

API keys can be found through my Discord Bot (WIP). Spamming any of the endpoints is an easy way to get your token revoked and your IP banned. I encourage putting the API key into a .env file or a JSON file and requiring it:

- config.json

```json
{
	"api_key": "KEY HERE"
}
```

```js
const config = require('./config.json');

const API = require('@processversion/api-wrapper');
const api = new API(config.api_key);
```

- Dotenv

```txt
API_KEY=KEY HERE
```

```js
require('dotenv').config(); // npm i dotenv

const API = require('@processversion/api-wrapper');
const api = new API(process.env.API_KEY);
```

- Methods

`new API('API_KEY').Reverse('any string')`

```js
const API = require('@processversion/api-wrapper');
const api = new API('API_KEY');

(async function () {
	const info = await api.Reverse('processversion');

	if (info.success == false) console.log('An error has occurred');

	console.log(info.data.text); // Prints out: noisrevssecorp
})();
```

`new API('API_KEY').Subreddit('subreddit name')`

```js
const API = require('@processversion/api-wrapper');
const api = new API('API_KEY');

(async function () {
	const info = await api.Subreddit('prequelmemes');

	if (info.success == false) console.log('An error has occurred!');

	console.log(info.data.created); // Prints out date the subreddit was created
})();
```

`new API('API_KEY').Reddit('user name')`

```js
const API = require('@processversion/api-wrapper');
const api = new API('API_KEY');

(async function () {
	const info = await api.Reddit('reddit user');

	if (info.success == false) console.log('An error has occurred');

	console.log(info.data.created); // Returns when the user's account was created
})();
```

`new API('API_KEY').Roblox('username')`

```js
const API = require('@processversion/api-wrapper');
const api = new API('API_KEY');

(async function () {
	const info = await api.Roblox('roblox user');

	if (info.success == false) console.log('An error has occurred');

	console.log(info.data.joinDate); // Returns when the user's account was created
})();
```

- Simple Discord Bot example

```js
const {} = require('discord.js');
```

</details>

## Features

- Simple and consistent interface to access my custom API
- Supports all available endpoints of the API with easy-to-use methods
- Handles authentication and request formatting automatically
- Promise-based asynchronous calls for smooth integration
- Built-in error handling with clear messages
- Lightweight and minimal dependencies for fast performance
- Designed to integrate easily with Discord bots or other JavaScript projects
- Modular structure to allow easy updates and adding new endpoints
- Basic usage examples and documentation included

## Status

🚫 Archived – This project is no longer actively developed or maintained. You're welcome to explore, fork, or build upon it for your own projects.
