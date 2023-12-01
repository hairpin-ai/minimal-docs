*Settings
========

This section will describe how you settings your theme.

* * *

##### [](#change-default-settings)Change Default Settings

Remove `local storage` when you change settings.

    <SettingsProvider
      defaultSettings={{
        themeMode: 'light', // 'light' | 'dark'
        themeDirection: 'ltr', //  'rtl' | 'ltr'
        themeContrast: 'default', // 'default' | 'bold'
        themeLayout: 'vertical', // 'vertical' | 'horizontal' | 'mini'
        themeColorPresets: 'default', // 'default' | 'cyan' | 'purple' | 'blue' | 'orange' | 'red'
        themeStretch: false,
      }}
    />

src/App.js, src/app/layout.js

* * *

##### [](#base-theme)Base Theme

    export default function ThemeProvider({ children }: Props) {
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
     
      const theme = createTheme(memoizedValue as ThemeOptions);
     
      theme.components = componentsOverrides(theme);
     
      return (
        <MuiThemeProvider theme={theme}>
          <CssBaseline />
          {children}
        </MuiThemeProvider>
      );
    }

src/theme/index.js

* * *

##### [](#dark-mode-option)Dark Mode Option

    export default function ThemeProvider({ children }: Props) {
      const settings = useSettingsContext();
     
      const memoizedValue = useMemo(
        () => ({
          palette: palette(settings.themeMode),
          shadows: shadows(settings.themeMode),
          customShadows: customShadows(settings.themeMode),
          shape: { borderRadius: 8 },
          typography,
        }),
        [settings.themeMode]
      );
     
      const theme = createTheme(memoizedValue as ThemeOptions);
     
      theme.components = componentsOverrides(theme);
     
      return (
        <MuiThemeProvider theme={theme}>
          <CssBaseline />
          {children}
        </MuiThemeProvider>
      );
    }

src/theme/index.js

* * *

##### [](#right-to-left-option)Right-To-Left Option

    export default function ThemeProvider({ children }: Props) {
      const settings = useSettingsContext();
     
      const memoizedValue = useMemo(
        () => ({
          palette: palette('light'),
          shadows: shadows('light'),
          customShadows: customShadows('light'),
          direction: settings.themeDirection,
          shape: { borderRadius: 8 },
          typography,
        }),
        [settings.themeDirection]
      );
     
      const theme = createTheme(memoizedValue as ThemeOptions);
     
      theme.components = componentsOverrides(theme);
     
      return (
        <MuiThemeProvider theme={theme}>
          <RTL themeDirection={settings.themeDirection}>
            <CssBaseline />
            {children}
          </RTL>
        </MuiThemeProvider>
      );
    }

src/theme/index.js

* * *

##### [](#presets-option)Presets Option

    export default function ThemeProvider({ children }: Props) {
      const settings = useSettingsContext();
     
      const presets = createPresets(settings.themeColorPresets);
     
      const memoizedValue = useMemo(
        () => ({
          palette: {
            ...palette('light'),
            ...presets.palette,
          },
          customShadows: {
            ...customShadows('light'),
            ...presets.customShadows,
          },
          shadows: shadows('light'),
          shape: { borderRadius: 8 },
          typography,
        }),
        [presets.customShadows, presets.palette]
      );
     
      const theme = createTheme(memoizedValue as ThemeOptions);
     
      theme.components = componentsOverrides(theme);
     
      return (
        <MuiThemeProvider theme={theme}>
          <CssBaseline />
          {children}
        </MuiThemeProvider>
      );
    }

src/theme/index.js

* * *

##### [](#contrast-option)Contrast Option

    export default function ThemeProvider({ children }: Props) {
      const settings = useSettingsContext();
     
      const contrast = createContrast(settings.themeContrast, settings.themeMode);
     
      const memoizedValue = useMemo(
        () => ({
          palette: {
            ...palette('light'),
            ...contrast.palette,
          },
          customShadows: {
            ...customShadows('light'),
          },
          shadows: shadows('light'),
          shape: { borderRadius: 8 },
          typography,
        }),
        [contrast.palette]
      );
     
      const theme = createTheme(memoizedValue as ThemeOptions);
     
      theme.components = merge(componentsOverrides(theme), contrast.components);
     
      return (
        <MuiThemeProvider theme={theme}>
          <CssBaseline />
          {children}
        </MuiThemeProvider>
      );
    }

src/theme/index.js

* * *

##### [](#localization)Localization

Combined with settings here: [multi-language](/multi-language)

[https://mui.com/material-ui/guides/localization/](https://mui.com/material-ui/guides/localization/)

    export default function ThemeProvider({ children }: Props) {
      const { currentLang } = useLocales();
     
      const memoizedValue = useMemo(
        () => ({
          palette: palette('light'),
          shadows: shadows('light'),
          customShadows: customShadows('light'),
          shape: { borderRadius: 8 },
          typography,
        }),
        []
      );
     
      const theme = createTheme(memoizedValue as ThemeOptions);
     
      theme.components = componentsOverrides(theme);
     
      const themeWithLocale = useMemo(
        () => createTheme(theme, currentLang.systemValue),
        [currentLang.systemValue, theme]
      );
     
      return (
        <MuiThemeProvider theme={themeWithLocale}>
          <CssBaseline />
          {children}
        </MuiThemeProvider>
      );
    }

src/theme/index.js

* * *

##### [](#full)Full

    export default function ThemeProvider({ children }: Props) {
      const { currentLang } = useLocales();
     
      const settings = useSettingsContext();
     
      const presets = createPresets(settings.themeColorPresets);
     
      const contrast = createContrast(settings.themeContrast, settings.themeMode);
     
      const memoizedValue = useMemo(
        () => ({
          palette: {
            ...palette(settings.themeMode),
            ...presets.palette,
            ...contrast.palette,
          },
          customShadows: {
            ...customShadows(settings.themeMode),
            ...presets.customShadows,
          },
          direction: settings.themeDirection,
          shadows: shadows(settings.themeMode),
          shape: { borderRadius: 8 },
          typography,
        }),
        [
          settings.themeMode,
          settings.themeDirection,
          presets.palette,
          presets.customShadows,
          contrast.palette,
        ]
      );
     
      const theme = createTheme(memoizedValue as ThemeOptions);
     
      theme.components = merge(componentsOverrides(theme), contrast.components);
     
      const themeWithLocale = useMemo(
        () => createTheme(theme, currentLang.systemValue),
        [currentLang.systemValue, theme]
      );
     
      return (
        <MuiThemeProvider theme={themeWithLocale}>
          <RTL themeDirection={settings.themeDirection}>
            <CssBaseline />
            {children}
          </RTL>
        </MuiThemeProvider>
      );
    }

src/theme/index.js

* * *

###### [](#related-files)Related files:

*   `src/App.js` or `src/app/layout.js`
*   `src/components/settings`


