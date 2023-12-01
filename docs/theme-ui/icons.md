*Icons
=====

* * *

##### [](#material-icon)Material Icon

[https://mui.com/components/material-icons/](https://mui.com/components/material-icons/)

    import AdbIcon from '@mui/icons-material/Adb';
    import AddIcon from '@mui/icons-material/Add';
    import AppleIcon from '@mui/icons-material/Apple';
    import AccountCircleIcon from '@mui/icons-material/AccountCircle';
    import AirplanemodeActiveIcon from '@mui/icons-material/AirplanemodeActive';
     
    function App() {
      return (
        <>
          <AdbIcon color="action" />
          <AddIcon color="disabled" />
          <AccountCircleIcon color="error" />
          <AirplanemodeActiveIcon color="inherit" />
          <AppleIcon color="primary" />
          <AppleIcon color="secondary" />
        </>
      );
    }

* * *

##### [](#iconify-icon)Iconify Icon

[https://iconify.design/icon-sets](https://iconify.design/icon-sets)

    import Iconify from 'src/components/Iconify';
     
    function App() {
      return (
        <>
          <Iconify icon="eva:clock-fill" sx={{ color: 'primary.main' }} />
          <Iconify icon="eva:charging-fill" sx={{ color: 'secondary.main' }} />
          <Iconify icon="eva:alert-circle-fill" sx={{ color: 'info.main' }} />
          <Iconify icon="eva:color-palette-fill" sx={{ color: 'warning.main' }} />
          <Iconify icon="eva/arrow-circle-down-fill" sx={{ color: 'error.main' }} />
        </>
      );
    }

* * *

##### [](#local-icon)Local Icon

    import SvgColor from 'src/components/svg-color';
     
    function App() {
      return (
        <>
          <SvgColor src="/assets/icons/browser-edge.svg" sx={{ color: 'primary.main' }} />
          <SvgColor src="/assets/icons/browser-edge.svg" sx={{ color: 'secondary.main' }} />
          <SvgColor src="/assets/icons/elephant.svg" sx={{ color: 'info.main' }} />
          <SvgColor src="/assets/icons/json-logo.svg" sx={{ color: 'success.main' }} />
          <SvgColor src="/assets/icons/love-camera.svg" sx={{ color: 'warning.main' }} />
          <SvgColor src="/assets/icons/shield.svg" sx={{ color: 'error.main' }} />
        </>
      );
    }

* * *

###### [](#reference)Reference:

*   [https://minimals.cc/components/foundation/icons](https://minimals.cc/components/foundation/icons)


