_Note: I completed this issue for Oregon State University as part of CS 464. I did not submit a pull request for this as I did not get great specifications for what they were looking for in the repo.  I feel that this would qualify to solve their issue on cors proxy documentation._

## **Cloudflare Cors Proxy Documentation**
Project: Notesnook - https://github.com/streetwriters/notesnook

Author: Amy Mummert

Description: Documentation for Cors Proxy - Notesnook

## What is Cors?
Cors stands for Cross-Origin Resource Sharing. "Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources. CORS also relies on a mechanism by which browsers make a "preflight" request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request." https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS 

## What is a Cors Proxy?
Cors proxy allows users to bypass Cors errors and get the data we need.

## Cloudflare Workers
Cloudflare is a serverless application that allows us to deploy instantly. 

"Cloudflare Workers are a platform for enabling serverless functions to run as close as possible to the end user" - https://www.cloudflare.com/learning/serverless/what-is-serverless/          

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/streetwriters/cors)


_It is recommended that you deploy your own instance instead of using the default one. This is also better for your privacy. It takes just 5 minutes to deploy._

## How To Create A Cloudflare Worker
1. Create Cloudflare Account 
2. Select Workers & Pages > Create Application
2. Select Create Worker > Deploy

## Cloudflare Worker Prerequisites
`install npm`

`install Node.js`

## Usage:

```
<proxy-url>/<resource-url>

```

## Examples

```
https://cors-proxy.url/https://api.github.com/repos/streetwriters/notesnook/releases/tags/v2.2.4

```

## Legal
Copyright (c) 2022 Streetwriters (Private) Limited.

Licensed under GNU General Public License version 3.
