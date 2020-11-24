robots-txt-component
====================
> Lightweight robots.txt parsing component **without any external dependencies** for **Node.js**.

Installation
------------
**NPM**
`npm install @ibragim64/robots-txt-component --save`


Getting started
---------------
Before using the parser, you need to initialize it like below:
```javascript
const RobotsParser = require('@ibragim64/robots-txt-component')
...

let robots = new RobotsParser('https://www.example.com', true) # allowOnNeutral = true
await robots.init() # Will attempt to retrieve the robots.txt file natively and parse it.
```

#### Check for allowance && other usages:
```javascript
let robots = new RobotsParser('https://www.example.com', true) // # allowOnNeutral = true
await robots.init() // # Will attempt to retrieve the robots.txt file natively and parse it.


userAgent = '*'
if (robots.canCrawl(url, userAgent)) { // # Will check the url against all the rules found in robots.txt file
    // # Your logic
}

// # Get the crawl delay for a user agent
let crawlDelay = robots.getCrawlDelay('Bingbot')
```
