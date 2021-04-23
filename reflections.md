## Reflections

Curious how to pull the funtionality from this lab into my current codebase . . .

I think I will need to:

+ Add the following code to my weather component :

````javascript
// Goes in at the top to allow the cahe file to load 

const cache = require('./cache.js');
//-------------------------------------------------------------------//
// Somewhere around my weather handling but before my weather function is called in . . . 

if (cache[key] && (Date.now() - cache[key].timestamp < 50000)) {
    console.log('Cache hit');
  } else {
    console.log('Cache miss');
    cache[key] = {};
    cache[key].timestamp = Date.now();
    cache[key].data = superagent.get(url).query(queryParams)
    .then(response => parseWeather(response.body));
  }
  
  return cache[key].data;
}

function parseWeather(weatherData) {
  try {
    const weatherSummaries = weatherData.data.map(day => {
      return new Weather(day);
    });
    return Promise.resolve(weatherSummaries);
  } catch (e) {
    return Promise.reject(e);
  }
}

class Weather {
  constructor(day) {
    this.forecast = day.weather.description;
    this.time = day.datetime;
  }
}
````

+ Create a newfile called cache.js :

```javascript
'use strict';

module.exports = { };
```
