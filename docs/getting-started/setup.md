*Setup
=====

Simple instructions for integrating into an existing project.

This example builds on **next-app-dir**.

* * *

**Step 1:** Create new app next.js

    npx create-next-app@latest

  

JavaScriptTypeScript

    ✔ What is your project named? … my-app
    ✔ Would you like to use TypeScript? … No
    ✔ Would you like to use ESLint? … No // => Choose "No" to avoid conflicts. You can set up later.
    ✔ Would you like to use Tailwind CSS? … No
    ✔ Would you like to use `src/` directory? … Yes
    ✔ Would you like to use App Router? (recommended) … Yes
    ✔ Would you like to customize the default import alias? … Yes

**Step 2:** Install the required dependencies

JavaScriptTypeScript

    yarn add @emotion/react @emotion/styled @iconify/react @mui/lab @mui/material lodash prop-types

**Step 3:**

Copy `src/components/iconify`

Copy `src/theme`

Remove `src/theme/options`

Update `src/theme/index`

JavaScriptTypeScript

    // src/theme/index.js
     
    'use client';
     
    import PropTypes from 'prop-types';
    import { useMemo } from 'react';
    import CssBaseline from '@mui/material/CssBaseline';
    import { createTheme, ThemeProvider as MuiThemeProvider } from '@mui/material/styles';
    import { palette } from './palette';
    import { shadows } from './shadows';
    import { typography } from './typography';
    import { customShadows } from './custom-shadows';
    import { componentsOverrides } from './overrides';
    import NextAppDirEmotionCacheProvider from './next-emotion-cache';
     
    export default function ThemeProvider({ children }) {
      const memoizedValue = useMemo(
        () => ({
          palette: palette('light'), // or palette('dark')
          shadows: shadows('light'), // or shadows('dark')
          customShadows: customShadows('light'), // or customShadows('dark')
          shape: { borderRadius: 8 },
          typography,
        }),
        []
      );
     
      const theme = createTheme(memoizedValue);
     
      theme.components = componentsOverrides(theme);
     
      return (
        <NextAppDirEmotionCacheProvider options={{ key: 'css' }}>
          <MuiThemeProvider theme={theme}>
            <CssBaseline />
            {children}
          </MuiThemeProvider>
        </NextAppDirEmotionCacheProvider>
      );
    }
     
    ThemeProvider.propTypes = {
      children: PropTypes.node,
    };

**Step 4:** Wrap `<ThemeProvider/>`

    // src/app/layout
     
    import ThemeProvider from 'src/theme';
     
    return (
      <html lang="en">
        <body className={inter.className}>
          <ThemeProvider>{children}</ThemeProvider>
        </body>
      </html>
    );

**Step 5:** Testing

    // src/app/page
     
    import Button from '@mui/material/Button';
    import Stack from '@mui/material/Stack';
     
    export default function Page() {
      return (
        <Stack spacing={1} alignItems="center">
          <Button variant="contained">Button</Button>
          <Button variant="contained" color="primary">
            Button
          </Button>
          <Button variant="contained" color="secondary">
            Button
          </Button>
          <Button variant="contained" color="info">
            Button
          </Button>
          <Button variant="contained" color="success">
            Button
          </Button>
          <Button variant="contained" color="warning">
            Button
          </Button>
          <Button variant="contained" color="error">
            Button
          </Button>
          <Button disabled variant="contained">
            Button
          </Button>
        </Stack>
      );
    }

* * *

###### [](#note)Note:

Should also update other files like:

*   `jsconfig.json`
*   `tsconfig.json`


