<h1 align="center">Hosting Express Applications on <img src="./img/vercel-logotype-light.png" height="22px"/></h1> 

Before continuing, make sure you have the Vercel CLI installed. (`npm i -g vercel`)
    
<hr/>

## Step 1: Create the `vercel.json` in the Root Directory.

Create (or download) the `vercel.json` file and inside, put the following (change "src" if you use a different file):

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

## Step 3: Done!

Your application is now running on <img src="./img/vercel-logotype-light.png" height="16px"/> . Just so you know, this is NOT required if using React or another JS framework. You also cannot host Discord bots with this. In that case, I recommend using [Fly](https://fly.io). For free, you can host for around 2000 hours a month (around 3 24/7 applications). Balance DOES reset every month. I also recommend this for hosting your backend instead of Vercel.
