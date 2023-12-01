*Mock Server
===========

We provide some simple examples on how to set up a mock API so you can work in your localhost.

* * *

##### [](#usage-in-localhost)Usage in Localhost

**Step 1:**

Download resource inside the `MOCK_API.md`.

    Minimal_Typescript
      ├── MOCK_API.md
      ├── ...

**Step 2:**

Start project `minimal-api-dev` folder.

Make sure you are running on the correct port `http://localhost:3000`.

    yarn install
    yarn dev

**Step 3:** Update `.env` in your current project.

    // CRA
    REACT_APP_HOST_API=http://localhost:3000
    REACT_APP_ASSETS_API=http://localhost:3000
     
    // Vite.Js
    VITE_HOST_API=http://localhost:3000
    VITE_ASSETS_API=http://localhost:3000
     
    // Next.Js
    NEXT_PUBLIC_HOST_API=http://localhost:3000
    NEXT_PUBLIC_ASSETS_API=http://localhost:3000

cra-js, vite-js, next-js...

* * *

##### [](#usage-on-production)Usage on Production

**Step 1:**

In `next.config.js` of `minimal-api-dev`.

    const nextConfig = {
      reactStrictMode: true,
      env: {
        DEV_API: 'http://localhost:3000',
        PRODUCTION_API: 'https://your-domain.vercel.app',
      },
    };
     
    export default nextConfig;

next.config.js

**Step 2 :**

Push source code `minimal-api-dev` to your github.

  
  

**Step 3 :**

Deploy on your [vercel.com](https://dev.to/ohdylan/nextjs-series-7-deploying-the-web-page-to-vercel-for-free-from-github-repo-1mob).

**Step 4:**

Update `.env` in your current project.

    // CRA
    REACT_APP_HOST_API=https://your-domain.vercel.app
    REACT_APP_ASSETS_API=https://your-domain.vercel.app
     
    // Vite.Js
    VITE_HOST_API=https://your-domain.vercel.app
    VITE_ASSETS_API=https://your-domain.vercel.app
     
    // Next.Js
    NEXT_PUBLIC_HOST_API=https://your-domain.vercel.app
    NEXT_PUBLIC_ASSETS_API=https://your-domain.vercel.app

cra-js, vite-js, next-js...

