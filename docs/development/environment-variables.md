
*Environment Variables
=====================

* * *

##### [](#create-react-app)Create React App

[https://create-react-app.dev/docs/adding-custom-environment-variables/](https://create-react-app.dev/docs/adding-custom-environment-variables/)

Use a prefix `REACT_APP_`

    REACT_APP_MAP=
    REACT_APP_WEBSITE_URL=

.env

  

Usage

    process.env.REACT_APP_MAP;
    process.env.REACT_APP_WEBSITE_URL;

* * *

##### [](#nextjs)Next.js

[https://nextjs.org/docs/api-reference/next.config.js/environment-variables](https://nextjs.org/docs/api-reference/next.config.js/environment-variables)

Use a prefix `NEXT_PUBLIC_`

    NEXT_PUBLIC_MAP=
    NEXT_PUBLIC_WEBSITE_URL=

.env

  

Usage

    process.env.NEXT_PUBLIC_MAP;
    process.env.NEXT_PUBLIC_WEBSITE_URL;

* * *

##### [](#vitejs)Vite.js

[https://vitejs.dev/guide/env-and-mode.html](https://vitejs.dev/guide/env-and-mode.html)

Use a prefix `VITE_`

    VITE_MAP=
    VITE_WEBSITE_URL=

.env

  

Usage

    import.meta.env.VITE_MAP;
    import.meta.env.VITE_WEBSITE_URL;