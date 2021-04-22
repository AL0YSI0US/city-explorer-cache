# City Explorer API [cache]

**Author** : Aloysious

+ [{ `city-explorer Trello Project Board` }](https://trello.com/b/0jJjZi3c/city-explorer-trello-board)

## Architecture

**Languages :** JavaScript | HTML | CSS | Markdown

**Libraries :** Node

**Tools :** VS Code | GitHub | Trello

## Initial condition:

````bash
✔️ cloned repository
✔️ ran `npm init`
✔️ installed the needed dependencies `dotenv`, `express` & `cors`
✔️ created `.env` file
✔️ added weatherbit api key
✔️ got the sever to listen on the correct port 3002
❌ http://localhost:3002/weather printed the following errors:

⚠️ ReferenceError: WEATHER_API_KEY is not defined
    at getWeather (/home/aloysious/codeFellows/301/labs/city-explorer-cache/modules/weather.js:11:10)
    at weatherHandler (/home/aloysious/codeFellows/301/labs/city-explorer-cache/server.js:20:3)
    at Layer.handle [as handle_request] (/home/aloysious/codeFellows/301/labs/city-explorer-cache/node_modules/express/lib/router/layer.js:95:5)
    at next (/home/aloysious/codeFellows/301/labs/city-explorer-cache/node_modules/express/lib/router/route.js:137:13)
    at Route.dispatch (/home/aloysious/codeFellows/301/labs/city-explorer-cache/node_modules/express/lib/router/route.js:112:3)
    at Layer.handle [as handle_request] (/home/aloysious/codeFellows/301/labs/city-explorer-cache/node_modules/express/lib/router/layer.js:95:5)
    at /home/aloysious/codeFellows/301/labs/city-explorer-cache/node_modules/express/lib/router/index.js:281:22
    at Function.process_params (/home/aloysious/codeFellows/301/labs/city-explorer-cache/node_modules/express/lib/router/index.js:335:12)
    at next (/home/aloysious/codeFellows/301/labs/city-explorer-cache/node_modules/express/lib/router/index.js:275:10)
    at cors (/home/aloysious/codeFellows/301/labs/city-explorer-cache/node_modules/cors/lib/index.js:188:7)
```
````


<h2 align="center">⏰ T I M E . E S T I M A T E S</h2>


## ⚙️ **Performance** : Feature One

As a user, I want the application to work with recent results, so that I can see info without the app doing unnecessary API calls.

> Cache external API data in server storage:

**Given** that a user enters a recently **unused** valid location in the input
**When** the user clicks the "Explore!" button
**Then** the API results will be loaded from third-party APIs, and stored in server memory for later retrieval.

**Given** that a user enters a recently **used** valid location in the input
**When** the user clicks the "Explore!" button
**Then** the API results will be returned from a server memory, rather than incurring the delay of repeating the request to third-party APIs.

```sh
Estimate of time needed to complete: 4 hours

Start time: _____

Finish time: _____

Actual time needed to complete: _____
```


## Resources

+ [Node JS Docs](https://nodejs.org/en/)
+ [NPM JS Docs](https://docs.npmjs.com/)
+ [Express JS Docs](http://expressjs.com/en/4x/api.html)
+ [dotenv Docs](https://www.npmjs.com/package/dotenv)


[Reflections ⇒](reflections.md)

---

This work by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/AL0YSI0US/" property="cc:attributionName" rel="cc:attributionURL">AL0YSI0US</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>. <a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />

This license lets others distribute, remix, adapt, and build upon your work, even commercially, as long as they credit you for the original creation. This is the most accommodating of licenses offered. Recommended for maximum dissemination and use of licensed materials.
