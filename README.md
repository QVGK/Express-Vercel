<h1 align="center">Hosting Express Applications on <img src="./img/vercel-logotype-light.png" height="22px"/></h1> 

Before continuing, make sure you have the Vercel CLI installed. (`npm i -g vercel`)
    
<hr/>

## Step 1: Create the `vercel.json` in the Root Directory.

Create (or download) the `vercel.json` file and inside, put the following:

```
{
    "version": 2,
    "builds": [
        {
            "src": "./index.js",
            "use": "@vercel/node"
        }
    ],
    "routes": [
        {
            "src": "/(.*)",
            "dest": "/"
        }
    ]
  }
  ```
  
## Step 2: Deploy VIA Vercel CLI

Run `vercel` in the Root Directory's terminal. Run `vercel --prod` if you've already ran `vercel` and want to deploy to the production branch.
