*Navigation
==========

* * *

###### [](#desktop)Desktop

src/layouts/main/header.js

    // Change
    <NavDesktop data={navConfig} />
     
    // To
    import { NavBasicDesktop } from 'src/components/nav-basic';
     
    <NavBasicDesktop
      slotProps={{
        rootItem: {
          '& .icon': { display: 'none' },
        },
      }}
      data={[
        {
          title: 'Home',
          icon: <Iconify icon="solar:home-2-bold-duotone" />,
          path: '/',
        },
        { title: 'About us', path: '/about' },
        {
          title: 'Pages1',
          path: '/pages1',
          icon: <Iconify icon="solar:file-bold-duotone" />,
          children: [
            { title: 'FAQs', path: '/pagespages/faqs' },
            { title: 'Pricing', path: '/pagespages/pricing' },
          ],
        },
        {
          title: 'Pages2',
          path: '/pages2',
          icon: <Iconify icon="solar:file-bold-duotone" />,
          children: [
            { title: 'Payment', path: '/pagespages/payment' },
            { title: 'Maintenance', path: '/pages/maintenance' },
          ],
        },
        {
          title: 'Docs',
          icon: <Iconify icon="solar:notebook-bold-duotone" />,
          path: paths.docs,
        },
      ]}
    />

  

**Result:**

###### [](#mobile)Mobile

src/layouts/main/header.js

    // Change
    <NavMobile data={navConfig} />
     
    // To
    <NavMobile
      data={[
        {
          title: 'Home',
          icon: <Iconify icon="solar:home-2-bold-duotone" />,
          path: '/',
        },
        { title: 'About us', path: '/about' },
        {
          title: 'Pages1',
          path: '/pages1',
          icon: <Iconify icon="solar:file-bold-duotone" />,
          children: [
            { title: 'FAQs', path: '/pagespages/faqs' },
            { title: 'Pricing', path: '/pagespages/pricing' },
          ],
        },
        {
          title: 'Pages2',
          path: '/pages2',
          icon: <Iconify icon="solar:file-bold-duotone" />,
          children: [
            { title: 'Payment', path: '/pagespages/payment' },
            { title: 'Maintenance', path: '/pages/maintenance' },
          ],
        },
        {
          title: 'Docs',
          icon: <Iconify icon="solar:notebook-bold-duotone" />,
          path: paths.docs,
        },
      ]}
    />

  

src/layouts/main/nav/mobile/index.js

    import { NavProps, NavBasicMobile } from 'src/components/nav-basic';
     
    <NavBasicMobile data={data} />

  

**Result:**

* * *

###### [](#reference)Reference:

*   [https://minimals.cc/components/extra/navigation-bar](https://minimals.cc/components/extra/navigation-bar)


