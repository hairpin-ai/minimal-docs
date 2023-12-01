*Deployment
==========

Each server has different functionality and deployment configuration.

Make sure you have configured it correctly according to your service provider's instructions.

* * *

##### [](#vercel)Vercel

Vercel ready to deploy has strong support for Next.js so we encourage you to use it to deploy your project.

[Preview](https://minimals.cc/)

* * *

##### [](#netlify)Netlify

[Preview](https://netlify-minimals-ui.netlify.app/)

**CRA**

*   Create file `_redirects` in `public` folder.
*   Create file `netlify.toml` in root project.

    /*    /index.html   200

\_redirects

  

    [build]
      command = "yarn build"
      publish = "build"

netlify.toml

**Next.js**

*   Update in `package.json`.
*   Create file `netlify.toml` in root project.
*   Connect with git and deploy.

      "scripts": {
        "dev": "next dev",
        "build": "next build",
        "start": "next start",
        "build-netlify": "next build && cp -r .next _next && mv _next .next/",
      },

package.json

  

    [build]
      command = "npm run build-netlify"
      publish = ".next"
     
    [[plugins]]
      package = "@netlify/plugin-nextjs"

netlify.toml

* * *

##### [](#azure)Azure

*   [CRA](https://www.youtube.com/watch?v=3wF99gvBFcw)
*   [Next.js](https://learn.microsoft.com/en-us/azure/static-web-apps/deploy-nextjs-hybrid)

* * *

##### [](#firebase)Firebase

[Preview](https://fir-minimals-ui.firebaseapp.com/)

*   [CRA](https://www.knowledgehut.com/blog/web-development/deploying-react-app-to-firebase)
*   [Next.js](https://medium.com/nerd-for-tech/lets-deploy-a-next-js-app-with-firebase-hosting-e070b3aecd04)

* * *

##### [](#heroku)Heroku

*   [CRA](https://stackabuse.com/how-to-deploy-a-react-app-to-heroku/)
*   [Next.js](https://elements.heroku.com/buildpacks/mars/heroku-nextjs)

* * *

##### [](#app-platform)App Platform

*   [CRA](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-react-application-to-digitalocean-app-platform)
*   [Next.js](https://docs.digitalocean.com/tutorials/app-nextjs-deploy/)

* * *

##### [](#vite)Vite

[https://vitejs.dev/guide/static-deploy.html](https://vitejs.dev/guide/static-deploy.html)

 