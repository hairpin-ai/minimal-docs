*Routing
=======

This article does not cover the settings in `next.js` because the `next.js` documentation is quite complete [here](https://nextjs.org/docs/app/building-your-application/routing)

* * *

##### [](#create-react-app-vitejs)Create React App, Vite.js

The routing is based on [react-router-dom](https://reactrouter.com/en/main) (version 6).

In this page you will find how to add new routes and how we handle existing routes.

You can find the template's router configuration in `src/routes/sections/index.js` contains all routes of our template.

##### [](#add-a-new-item-navigation)Add a new item navigation

Apply version `CRA`, `Vite.js`, `Next.js`.

    export const navConfig = [
      {
        title: 'Home',
        path: '/',
      },
      {
        title: 'About',
        path: '/about',
      },
      {
        title: 'New Page',
        path: '/new-page',
      },
      {
        title: 'Pages',
        path: '/pages',
        children: [
          {
            subheader: 'Nested',
            items: [
              { title: 'item 1', path: '/pages/item-1' },
              { title: 'item 2', path: '/pages/item-2' },
            ],
          },
        ],
      },
    ];

config-navigation.js

* * *

##### [](#add-a-new-route)Add a new route

Apply version `CRA`, `Vite.js`.

    import { lazy } from 'react';
     
    const NewPage = lazy(() => import('src/pages/NewPage'));
     
    export default function Router() {
      return useRoutes([
        {
          element: (
            <MainLayout>
              <Outlet />
            </MainLayout>
          ),
          children: [
            { path: <HomePage />, index: true }, // => '/'
            { path: 'new-page', element: <NewPage /> }, // => '/new-page'
            {
              path: 'pages',
              children: [
                { element: <Pages />, index: true }, // => '/pages'
                { path: 'color', element: <ColorPage /> }, // => '/pages/color'
              ],
            },
          ],
        },
        {
          element: (
            <DashboardLayout>
              <Outlet />
            </DashboardLayout>
          ),
          children: [
            { path: <DashboardPage />, index: true }, // => '/dashboard'
            { path: 'new', element: <DashboardNewPage /> }, // => '/dashboard/new'
            {
              path: 'user',
              children: [
                { element: <UserPage />, index: true }, // => '/dashboard/user'
                { path: 'list', element: <UserListPage /> }, // => '/dashboard/user/list'
                { path: 'edit', element: <UserEditPage /> }, // => '/dashboard/user/edit'
              ],
            },
          ],
        },
      ]);
    }

src/routes/sections/index.js

* * *

##### [](#usage)Usage

    import Link from '@mui/material/Link';
    import { RouterLink } from 'src/routes/components';
     
    <Link component={RouterLink} href="/new" underline="none" variant="subtitle2">
      Go to About us
    </Link>;

* * *

##### [](#display-with-role)Display with role

[https://minimals.cc/components/extra/navigation-bar](https://minimals.cc/components/extra/navigation-bar)

[https://minimals.cc/dashboard/permission](https://minimals.cc/dashboard/permission)

    const navConfig = [
      {
        subheader: 'Marketing',
        items: [
          {
            title: 'Landing',
            path: '/landing',
            icon: <Iconify icon="carbon:bat" width={1} />,
            roles: ['admin'],
            caption: 'Display only admin role',
          },
          {
            title: 'Services',
            path: '/services',
            icon: <Iconify icon="carbon:cyclist" width={1} />,
            roles: ['admin', 'user'],
          },
        ],
      },
    ];

config-navigation.js

* * *

##### [](#set-the-index-page)Set the index page

Set default page when visit website.

    export default function Router() {
      return useRoutes([
        // Set index page with skip home page
        {
          path: '/',
          element: <Navigate to={PATH_AFTER_LOGIN} replace />,
        },
     
        // Set index page with home page
        {
          path: '/',
          element: (
            <MainLayout>
              <Outlet />
            </MainLayout>
          ),
          children: [{ element: <HomePage />, index: true }],
        },
      ]);
    }

src/routes/sections/index.js
