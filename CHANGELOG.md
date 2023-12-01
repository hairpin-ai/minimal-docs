

### [](#v560)v5.6.0

###### [](#oct-8-2023)Oct 8, 2023

*   **New** `src/components/nav-basic`.
*   Update `src/components/nav-section`.
*   Update `src/components/mega-menu`.
*   Update `src/theme`.
*   Update `src/auth/guard/auth-guard`.
*   Update `src/auth/guard/guest-guard`.
*   Update `src/locales/use-locales`.
*   Update `<RHFMultiSelect/>`.
*   Remove `<AuthConsumer/>`.
*   Remove `.eslintrc`.
*   Change external style import strategy
*   Temporarily stop supporting `create-react-app` version ([tracking](https://github.com/reactjs/react.dev/pull/5487#issuecomment-1409720741)).
*   Update dependencies.

* * *

### [](#v550)v5.5.0

###### [](#aug-30-2023)Aug 30, 2023

*   Update `src/components/progress-bar` (Next.js version only).
*   Update `src/components/loading-screen/splash-screen.tsx`.
*   Update `src/theme/overrides/components/avatar.tsx`.
*   Update `src/layouts/_common/account-popover.tsx`.
*   Update `src/layouts/_common/searchbar/searchbar.js`.
*   Update `src/sections/chat/view/chat-view.tsx`.
*   Update `src/sections/chat/chat-message-input.tsx`.
*   Update `src/sections/chat/chat-message-item.tsx`.
*   Update `src/sections/chat/chat-nav-item.tsx`.
*   Update `src/sections/kanban/view/kanban-view.tsx`.
*   Fix bug dashboard layout `src/layouts/dashboard/layout.tsx`.
*   Update dependencies.

* * *

### [](#v540)v5.4.0

###### [](#aug-10-2023)Aug 10, 2023

*   Update `src/hooks/use-local-storage.ts`.
*   Update `src/components/settings/context/settings-provider.tsx`.
*   Update `src/sections/checkout/context/checkout-provider.tsx`.
*   Update `src/locales/config-lang.ts`.
*   Update `src/locales/localization-provider.tsx`.
*   Update `src/components/animate/motion-lazy.tsx`.
*   Update `src/components/upload`.
*   Update `src/components/loading-screen/splash-screen.tsx`.
*   Update `src/components/progress-bar` (CRA / Vite version only).
*   Update dependencies.
*   **\[Figma\]** Migrate to [variables](https://help.figma.com/hc/en-us/articles/15339657135383-Guide-to-variables-in-Figma).

* * *

### [](#v530)v5.3.0

###### [](#jul-17-2023)Jul 17, 2023

*   Update `theme` folder.
*   Rename folder `src/routes/hook` => `src/routes/hooks`
*   Fix `Right-to-left` (src/theme/options/right-to-left.tsx).
*   Fix Next.js `Dark mode` (src/theme/next-emotion-cache.tsx).
*   Update dependencies.

* * *

### [](#v520)v5.2.0

###### [](#jul-04-2023)Jul 04, 2023

*   Completely remove redux.
*   Migrate checkout `redux-slice` to `react-context`.
*   Update `src/auth/guard/guest-guard`.
*   Support `dynamic routes` with next `output: 'export`.([tracking](https://github.com/vercel/next.js/issues/48022))
*   Update dependencies.

* * *

### [](#v510)v5.1.0

###### [](#jun-17-2023)Jun 17, 2023

*   Add Vite version.
*   Migrate `redux` to `swr`.
*   Update `src/auth/guard/auth-guard.tsx`.
*   Update `src/layouts/auth/modern.tsx`.
*   Update `src/layouts/dashboard/main.tsx`.
*   Update `src/sections/auth/jwt/jwt-login-view.tsx`.
*   Update `src/sections/auth/jwt/jwt-register-view.tsx`.
*   Update `src/components/nav-section/mini/nav-item.tsx`.
*   Update `src/sections/auth/amplify/amplify-login-view.tsx`.
*   Update `src/sections/auth/firebase/firebase-login-view.tsx`.
*   Update `src/components/nav-section/horizontal/nav-item.tsx`.
*   Update `src/components/settings/drawer/settings-drawer.tsx`.
*   Update dependencies.

* * *

### [](#v500)v5.0.0

###### [](#jun-05-2023)Jun 05, 2023

*   Support `Next.js` appDir version.
*   Add Order pages.
*   Add Job pages.
*   Add Tour pages.
*   Improve the performance.
*   Update project folder structure.
*   Refactor authentication flows.
*   Refactor and simplify project code.
*   Update dependencies.
*   Update Figma.
*   Discontinue support for Sketch files.

* * *

### [](#v430)v4.3.0

###### [](#feb-21-2023)Feb 21, 2023

*   Add `src/components/scroll-progress`.
*   Update `src/components/chart/useChart`.
*   Update some rule in [Yup](https://github.com/jquense/yup/issues/1906) (remove `nullable()`, update types...).
*   Upgrade dependencies to the latest versions.

* * *

### [](#v420)v4.2.0

###### [](#jan-18-2023)Jan 18, 2023

*   Update `src/@types/calendar`.
*   Update `src/pages/dashboard/CalendarPage`.
*   Update `src/sections/@dashboard/calendar`.
*   Update `src/redux/slices/calendar`.
*   Update `src/hooks/useOffSetTop`.
*   Update `src/auth/FirebaseContext`.
*   Update `src/components/scrollbar`.
*   Update `src/sections/home/HomeHero`.
*   Update `src/components/carousel/CarouselDots`.
*   Update `src/components/custom-breadcrumbs/LinkItem`.
*   Update `src/sections/@dashboard/invoice/form/InvoiceAddressListDialog`.
*   Update types `type RHFMultiSelectProps` in `src/components/hook-form/RHFSelect`.
*   Update `import 'simplebar/src/simplebar.css';` =>`import 'simplebar-react/dist/simplebar.min.css';`
*   Update `next.config.js` (Next.js).
*   Update `.eslintignore` (Next.js).
*   Upgrade dependencies to the latest versions.

* * *

### [](#v410)v4.1.0

###### [](#nov-26-2022)Nov 26, 2022

*   **NEW** Support next.js 13.
*   Update `src/components/lightbox/*`.
*   Update `src/components/markdown/*`.
*   Update `src/components/hook-form/*`.
*   Update `src/components/editor/Editor`.
*   Update `src/components/chart/useChart`.
*   Update `src/components/nav-section/mini/NavList`.
*   Update `src/components/custom-avatar/CustomAvatar`.
*   Update `src/components/nav-section/horizontal/NavList`.
*   Update `src/components/date-range-picker/useDateRangePicker`.
*   Update `src/components/loading-screen/LoadingScreen` (cra\_version only).
*   Update `src/redux`.
*   Update `src/theme`.
*   Update `src/App` (cra\_version only).
*   Update `src/index` (cra\_version only).
*   Update eslint.
*   Migrate `react-beautiful-dnd` => `@hello-pangea/dnd`.
*   Migrate `react-image-lightbox` => `yet-another-react-lightbox`.
*   Improve & rename folder structure.
*   Upgrade dependencies to the latest versions.
*   **Design:** Update Sketch v4.

* * *

### [](#v400)v4.0.0

###### [](#oct-15-2022)Oct 15, 2022

*   **NEW** [Home page](https://minimals.cc).
*   **NEW** [General file page](https://minimals.cc/dashboard/file).
*   **NEW** [File manager page](https://minimals.cc/dashboard/files-manager).
*   **NEW** [Components date range picker](https://minimals.cc/components/mui/pickers).
*   **NEW** [Components nav section mini](https://minimals.cc/components/extra/navigation-bar).
*   Add [Calendar filters](https://minimals.cc/dashboard/calendar).
*   Add `Reset Button` when filters [user list](https://minimals.cc/dashboard/user/list).
*   Add `Reset Button` when filters [product list](https://minimals.cc/dashboard/e-commerce/list).
*   Add `Reset Button` when filters [invoice list](https://minimals.cc/dashboard/invoice/list).
*   Add confirmation dialog when deleting item.
*   Add `src/components/hook-form/RHFAutocomplete`.
*   Add `src/components/file-thumbnail`.
*   Update `src/layouts`.
*   Update `src/theme`.
*   Remove `src/components/Page`.
*   Remove `src/components/emoji-picker`.
*   Remove `src/components/SocialsButton`.
*   Remove `src/components/TextIconLabel`.
*   Remove `src/components/CopyClipboard`.
*   Remove `src/contexts/CollapseDrawerContext`.
*   Remove and add some new hooks.
*   Improve & rename folder structure.
*   Upgrade dependencies to the latest versions.
*   **Design:** Update Figma (Sketch no update)

* * *

### [](#v350)v3.5.0

###### [](#jul-04-2022)Jul 04, 2022

*   Support React 18.
*   Resolve warning npm vulnerabilities when install. (React script version / skip if using yarn).
*   Add `src/components/organizational-chart` ([view](https://www.minimals.cc/components/extra/organization-chart/)).
*   Update `theme / overrides`.
*   Update `src/guards/GuestGuard`.
*   Update `src/contexts/AwsCognitoContext` (TS version).
*   Update `src/components/emoji-picker`.
*   Update `src/components/Image`.
*   Update `src/components/Scrollbar` (TS version).
*   Update `src/components/hook-form`.
*   Update `src/components/map`.
*   Update `src/components/nav-section`. (Infinity menu level support)
*   Update `src/layouts/main/MenuDesktop`.
*   Update `src/layouts/main/MenuMobile`.
*   Improve filter products `src/pages/dashboard/EcommerceShop`.
*   Improve invoice create function.
*   Remove `src/utils/mapboxgl`.
*   Improve folder structure.
*   Upgrade some dependencies to the latest versions.

* * *

### [](#v340)v3.4.0

###### [](#apr-11-2022)Apr 11, 2022

*   Add `src/pages/auth/NewPassword`.
*   Add `src/pages/Page403`.
*   Update `/src/components/hook-form/*`.
*   Update `/src/components/nav-section/*`.(support for translation, role based guard)
*   Update `/src/components/settings/*`.
*   Update `/src/components/upload/*`.
*   Update `/src/components/table/*`.
*   Update `/src/components/EmptyContent`.
*   Update `/src/components/Label`.
*   Update `/src/components/MenuPopover`.
*   Update `/src/components/LightboxModal`.
*   Update `/src/components/LoadingScreen`.
*   Update `/src/components/NotistackProvider`.
*   Update `/src/contexts/SettingsProvider`.
*   Update `/src/guards/AuthGuard`.
*   Update `/src/guards/RoleBasedGuard`.
*   Update `/src/hooks/useLocales`.
*   Update `/src/locales/*`.
*   Update `src/pages/dashboard/Kanban`.
*   Update `src/pages/dashboard/GeneralAnalytics`.
*   Update `src/pages/dashboard/GeneralApp`.
*   Update `src/pages/dashboard/GeneralBanking`.
*   Update `src/pages/dashboard/GeneralBooking`.
*   Update `src/utils/jwt.ts`
*   Update `src/config.ts`
*   Improve folder structure
*   Upgrade some dependencies to the latest versions.

* * *

### [](#v330)v3.3.0

###### [](#mar-12-2022)Mar 12, 2022

*   Add `src/components/table/TableSkeleton`.
*   Update `src/components/table/TableMoreMenu`.
*   Change `src/components/table/TableSearchNotFound` => `src/components/table/TableNoData`.
*   Update `src/sections/@dashboard/e-commerce/product-list/ProductTableRow`.
*   Update `src/sections/@dashboard/user/list/UserTableRow`.
*   Update `nextjs_TS/src/sections/@dashboard/invoice/list/InvoiceTableRow`.
*   Update `InvoiceList` page.
*   Update `UserList` page.
*   Update `EcommerceProductList` page.
*   Update `logout`in `src/contexts/Auth0Context`.
*   Demo handle loading `EcommerceProductList` ([https://minimals.cc/dashboard/e-commerce/list/](https://minimals.cc/dashboard/e-commerce/list/)).
*   Upgrade some dependencies to the latest versions.

* * *

### [](#v320)v3.2.0

###### [](#mar-4-2022)Mar 4, 2022

*   Add components `table`.
*   Add hooks `useTable`.
*   Add hooks `useTabs`.
*   Add hooks `useToggle`.
*   Add categories menu mobile in `faqs` page.
*   Add Management Invoice part ([view](https://minimals.cc/dashboard/invoice/list/)).
*   Update `User List` page ([view](https://minimals.cc/dashboard/user/list/)).
*   Update `Product List` page ([view](https://minimals.cc/dashboard/e-commerce/list/)).
*   Upgrade some dependencies to the latest versions.
*   Update design file.

* * *

### [](#v310)v3.1.0

###### [](#feb-24-2022)Feb 24, 2022

*   Support react-scripts v5.0.0 ([migrate to react-script v5.0.0](https://docs-minimals.vercel.app/limitations/react-script-v5)).
    
*   Update `.eslintrc`.
    
*   Update `src/utils/jwt`.
    
*   Upgrade some dependencies to the latest versions.
    
*   Add `src/utils/mapboxgl`.
    
    *   In `src/sections/contact/ContactMap`
    
        import 'src/utils/mapboxgl';
    
*   Fix handdle alert error:
    
    *   In `src/sections/auth/register/RegisterForm`
    *   In `src/sections/auth/login/LoginForm`
    
        setError('afterSubmit', error);
        // to
        setError('afterSubmit', {
          ...error,
          message: error.message,
        });
    
*   Update In `src/layouts/dashboard/navbar/NavbarHorizontal`
    
        const RootStyle = styled('div')(({ theme }) =>({})
        // to
        const RootStyle = styled(AppBar)(({ theme }) =>({})
    

###### [](#nextjs)Next.js

*   Change `import { yupResolver } from '@hookform/resolvers/yup/dist/yup'` to `import { yupResolver } from '@hookform/resolvers/yup'`.

* * *

### [](#v300)v3.0.0

###### [](#dec-23-2021)Dec 23, 2021

*   **NEW** Add Next.JS full version for Javascript.
*   **NEW** Migrate all `formik form` to `react-hook-form`.
*   Add `src/components/hook-form` as fast field support for react-hook-form (use version `2.8.0` if you like working with formik).
*   Add **vertical-layout** with **navbar-horizontal** in settings (apply for dashboard layout only).
*   Update `src/components/nav-section`.
*   Update `src/components/upload`.
*   Update `src/components/MenuPopover`.
*   Update `src/theme/overrides`. (can copy and override).
*   Update `src/theme/shadows` (add value `card`, `dialog`,`dropdown`).
*   Update `src/components/SearchNotFound`.
*   Update `src/contexts/FirebaseContext` (support for firebase v9).
*   Move `src/theme/globalStyles` to `src/theme/overrides/CssBaseline`.
*   Move `components overview` to next.js source.
*   Upgrade some dependencies to the latest versions.

* * *

### [](#v280)v2.8.0

###### [](#dec-14-2021)Dec 14, 2021

*   **NEW** - Add Next.JS full version (TypeScript only).
*   Fix `src/components/settings` on Safari (Can be copied and overwritten).
*   Improve the blog.
*   Improve `src/guards/AuthGuard`.
*   Improve `src/pages/auth/VerifyCode` (support copy and next focus input when type).
*   Update `handleLogout` in `src/layouts/dashboard/header/AccountPopover`.
*   Update `src/theme/overrides/Autocomplete`.
*   Support external link `full_version_TS/src/components/nav-section/NavItem`.
*   Upgrade some dependencies to the latest versions.

* * *

### [](#v270)v2.7.0

###### [](#dec-7-2021)Dec 7, 2021

##### [](#design)Design

*   **Figma** support full dark mode and mobile version ([Learn more](https://www.figma.com/file/x7earqGD0VGFjFdk5v2DgZ/%5BPreview%5D-Minimal-Web))
*   **Sketch** no change

##### [](#code)Code

*   Add `src/components/Image` support lazyload and [aspect ratio](https://minimals.cc/components/image)
*   Add `src/components/TextMaxLine` [(learn)](https://minimals.cc/components/text-max-line)
*   Update and support [nav-section](https://minimals.cc/components/navigation-bar) 3 level item.
*   Update `src/components/LightboxModal`.
*   Update `src/components/SvgIconStyle`.
*   Update `src/components/Scrollbar`.
*   Upgrade `src/routes`.
*   Upgrade `src/layouts`.
*   Update `src/guards/AuthGuard`.
*   Update `src/components/settings`
*   **Update `src/theme` (can copy and replace)**
    *   Remove `src/theme/shape`
    *   `borderRadiusSm => theme.shape.borderRadius * 1.5`
    *   `borderRadiusMd => theme.shape.borderRadius * 2`
*   **Remove `src/components/@material-extend`**
    *   Move `src/components/@material-extend/MAvatar` => `src/components/Avatar`.
    *   Move `src/components/@material-extend/MBreadcrumbs` => `src/components/Breadcrumbs`.
    *   Change `src/components/@material-extend/MFab` => `src/components/animate/FabButtonAnimate`.
    *   Change `src/components/@material-extend/MIconButton` => `src/components/animate/IconButtonAnimate`.
    *   Change `src/components/@material-extend/MHidden` => `src/hooks/useResponsive`.
*   Remove `src/components/LazySize`
*   Remove `src/components/draft`
*   Remove `src/layouts/AuthLayout`
*   **Upgrade `src/components/animate`.**
    *   Wrap `MotionLazyContainer` in `src/App`
    *   Change `<motion.div>` => `<m.div>`/ `<motion.a>` => `<m.a>`...

    // before
    variants = { varFadeInUp }
     
    // after
    variants = {
      varFade({
        distance:120,
        durationIn:1,
        durationOut:0.5,
        easeIn:'easeIn',
        easeOut:'easeInOut',
        }).inUp }

*   Migrate `@iconify/react` to use via API

    // before
    import { Icon } from '@iconify/react';
    import menu2Fill from '@iconify/icons-eva/menu-2-fill';
     
    <Icon icon={menu2Fill} />;
     
    // after
    import Iconify from 'src/components/Iconify';
     
    <Iconify icon="eva:bell-fill" sx={{ width: 20, height: 20, color: 'red' }} />;

*   Improve folder structure
*   Upgrade some dependencies to the latest versions

* * *

### [](#v260)v2.6.0

###### [](#sep-18-2021)Sep 18, 2021

*   Support MUI v5.0.0 official release
    
*   Upgrade dependencies `react-router` [changelog](https://github.com/remix-run/react-router/releases)
    
*   Change dependencies `notistack5` => `notistack`
    
*   Change dependencies `@material-ui/core` => `@mui/material`
    

    // Example
    // Learn more : https://github.com/mui-org/material-ui/blob/master/CHANGELOG.md
    import {Button} from '@material/core'; => import {Button} from '@mui/material';

*   Change dependencies `@material-ui/icons` => `@mui/icons-material`
*   Change dependencies `@material-ui/lab` => `@mui/lab`
*   Change dependencies `@material-ui/styles` => `@mui/styles`
*   Change dependencies `@material-ui/system` => `@mui/system`
*   Change dependencies `@material-ui/utils` => `@mui/utils`
*   Change dependencies `@material-ui/data-grid` \=> `@mui/data-grid`
*   Change `styleProps` => `ownerState`
*   Update `src/theme/globalStyles`
*   Update `src/components/NotistackProvider`
*   Update `src/components/LoadingScreen`
*   Update `src/components/LightboxModal`
*   Update `src/components/BaseOptionChart`
*   Update `src/routes/index`
*   Update `src/theme/overrides`
*   Remove `GlobalStyles` in `src/theme/index`
*   Add `GlobalStyles`, `ProgressBarStyle`, `BaseOptionChartStyle` in `src/App`
*   Upgrade some dependencies to the latest versions
*   More changelog [MUI](https://github.com/mui-org/material-ui/blob/next/CHANGELOG.md)

* * *

### [](#v250)v2.5.0

###### [](#aug-18-2021)Aug 18, 2021

*   Add example for [Form Validation](https://minimals.cc/components/form-validation)
*   Update `src/components/editor/draft`
*   Update `src/components/editor/quill`
*   Update `src/components/RtlLayout`
*   Update `src/utils/formatTime`
*   Update type `src/components/Markdown`
*   Improve version `demo_next` (Issuse css first render)
*   Upgrade some dependencies to the latest versions

* * *

### [](#v240)v2.4.0

###### [](#aug-7-2021)Aug 7, 2021

*   Add page dashboard banking
*   Add page dashboard booking
*   Update landing page
*   Update `src/theme/overrides/Card`
*   Update `src/theme/overrides/Alert`
*   Update `src/theme/overrides/DataGrid`
*   Update `src/components/editor/draft`
*   Update `src/theme/palette`
*   Update `src/theme/typography`
*   Update `src/components/carousel/controls`
*   Update `src/components/Markdown`
*   Update `src/@types/mega-menu`
*   Upgrade some dependencies to the latest versions
*   Replace `faker` dependencies =>`src/utils/mock-data`
*   More changelog [React Material UI](https://github.com/mui-org/material-ui/blob/next/CHANGELOG.md)

* * *

### [](#v230)v2.3.0

###### [](#jul-23-2021)Jul 23, 2021

*   Support MUI v5.0.0-beta.1
*   Support layout stretch in settings
*   Support localization for MUI components [https://next.material-ui.com/guides/localization/#main-content](https://next.material-ui.com/guides/localization/#main-content)
*   Support mini Menu (Dashboard sidebar) [demo](https://simple-minimals.vercel.app/dashboard/one)
*   Add component DataGrid example [demo](https://minimals.cc/components/data-grid)
*   Remove `MButton`, `MTimelineDot`, `MChip`, `MBadge`, `MButtonGroup`, `MCircularProgress`, `MLinearProgress`, `MRadio`, `MSwitch`, `MCheckbox` form `src/components/@material-extend` (MUI v5.0.0-beta.1 is now supported)
*   Changes some illustration
*   Change dependencies `notistack` to `notistack5` (for support MUI v5.0.0-beta.1)
*   Update landing page
*   Upgrade some dependencies to the latest versions

* * *

### [](#v220)v2.2.0

###### [](#jun-25-2021)Jun 25, 2021

*   Add kanban board
*   Upgrade some dependencies to the latest versions

* * *

### [](#v210)v2.1.0

###### [](#may-22-2021)May 22, 2021

*   Add primary color change support
*   Add guard based role support
*   Add page about us
*   Add page contact us
*   Add page faqs
*   Add component mega menu
*   Add method auth auth0
*   Add method auth aws cognito
*   Add `<MHidden>`into `src/components/@material-extend` support v33
*   Update folder simple\_version
*   Update folder simple\_next\_js
*   Update some components from `src/components`
*   Upgrade to react router v6
*   Upgrade dependencies to the latest versions
*   Change some layouts and graphic
*   Migrate some components to the context instead of redux (auth, settings)
*   Improve folder structure
*   Clean code

* * *

### [](#v200)v2.0.0

###### [](#apr-18-2021)Apr 18, 2021

*   Add **Typescript** support
*   Add a simple\_version example for next js
*   Add animation examples
*   Update package.json
*   Upgrade to calendar v5
*   Upgrade dependencies to the latest versions
*   Remove google map
*   Remove recharts
*   Improve routers
*   Improve folder structure
*   Change the directory tree structure
*   Clean code

* * *

### [](#v120)v1.2.0

###### [](#mar-1-2021)Mar 1, 2021

*   Add design Figma source file (variants and auto layout)
*   Add Right-to-Left layout support
*   Add JWT login support (see in doc Authentication)
*   Add simple version
*   Update components override
*   Update `.babelrc`
*   Update `.eslintrc`
*   Update `jsconfig.json`
*   Update `package.json`
*   Upgraded depdendecy
*   Change `import xxx from '~/...'` `to import xxx from 'src/...'`
*   Improve folder structure

* * *

### [](#v110)v1.1.0

###### [](#feb-3-2021)Feb 3, 2021

*   Depdendecy versions `@material-ui` from 5.0.0-alpha.23 to 5.0.0-alpha.24
*   Fix the injection order of the CSS with yarn. JSS and emotion are still cohabitating until v5 reaches a stable version. We need to tell emotion to inject before JSS
*   Fix layout doc `src/layouts/DocsLayout` breakpoints
*   Fix double scroll bar on mobile `src/components/Scrollbars.js`
*   Improvement Carousel implementation

* * *

### [](#v100)v1.0.0

###### [](#jan-26-2021)Jan 26, 2021

Initial release.


