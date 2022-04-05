# NodeJS Applications on Vercel (EJS)

Create `vercel.json` inside of application root folder.

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
  
  ---
  
  Add `app.set('views', __dirname + '/views)` to top of code before `app.set('view engine', 'ejs')`
  
  ---
  
  Remove `.ejs` from all `res.render()` functions.
  
  Example: `res.render('index.ejs')` becomes `res.render('index')`
