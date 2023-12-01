*Typography
==========

Custom global typography inside `src/theme/typography`.

* * *

##### [](#create-react-app-vitejs)Create React App, Vite.js

**Google fonts**

    <!doctype html>
    <html lang="en">
      <head>
        <link rel="preconnect" href="https://fonts.googleapis.com" />
        <link rel="preconnect" href="https://fonts.gstatic.com" />
        <link href="https://fonts.googleapis.com/css2?family=Public+Sans:wght@400;500;600;700;800&display=swap"
          rel="stylesheet" />
        <link href="https://fonts.googleapis.com/css2?family=Barlow:wght@900&display=swap" rel="stylesheet" />
      </head>
    </html>

index.html

  

    const primaryFont = 'Public Sans, sans-serif';
    const secondaryFont = 'Barlow, sans-serif';
     
    const typography = {
      fontFamily: primaryFont,
      h1: {
        fontFamily: primaryFont,
      },
      h2: {
        fontFamily: secondaryFont,
    },
    };

src/theme/typography

**Local fonts**

    <!doctype html>
    <html lang="en">
      <head>
        <link rel="stylesheet" type="text/css" href="%PUBLIC_URL%/fonts/index.css" />
      </head>
    </html>

index.html

  

Create public/fonts

    public/fonts
      ├── index.css
      ├── CircularStd-Medium.otf
      ├── CircularStd-Bold.otf
      ├── Barlow-Medium.ttf
      ├── ...

  

    @font-face {
      font-family: 'CircularStd';
      font-weight: 500;
      font-style: normal;
      src:
        local('CircularStd'),
        url('CircularStd-Medium.otf') format('opentype');
    }
    @font-face {
      font-family: 'CircularStd';
      font-weight: 700;
      font-style: normal;
      src:
        local('CircularStd'),
        url('CircularStd-Bold.otf') format('opentype');
    }
    @font-face {
      font-family: 'Barlow';
      font-weight: 500;
      font-style: normal;
      src:
        local('Barlow'),
        url('Barlow-Medium.ttf') format('truetype');
    }

public/fonts/index.css

**Usage**

    import { secondaryFont } from 'src/theme/typography';
     
    const StyledTextH1 = styled('h1')(({ theme }) => ({
      fontSize: 16,
      fontFamily: theme.typography.fontFamily,
    }));
     
    const StyledTextH2 = styled('h1')({
      fontSize: 16,
      fontFamily: secondaryFont,
    });

* * *

##### [](#nextjs)Next.js

**Google fonts**

[https://nextjs.org/docs/app/building-your-application/optimizing/fonts#google-fonts](https://nextjs.org/docs/app/building-your-application/optimizing/fonts#google-fonts)

    import { Public_Sans, Barlow } from 'next/font/google';
     
    export const primaryFont = Public_Sans({
      weight: ['400', '500', '600', '700', '800'],
      subsets: ['latin'],
      display: 'swap',
      fallback: ['Helvetica', 'Arial', 'sans-serif'],
    });
     
    export const secondaryFont = Barlow({
      weight: ['900'],
      subsets: ['latin'],
      display: 'swap',
      fallback: ['Helvetica', 'Arial', 'sans-serif'],
    });

src/theme/typography

**Local fonts**

[https://nextjs.org/docs/app/building-your-application/optimizing/fonts#local-fonts](https://nextjs.org/docs/app/building-your-application/optimizing/fonts#local-fonts)

Create public/fonts

    public/fonts
      ├── CircularStd-Bold.otf
      ├── CircularStd-Book.otf
      ├── CircularStd-Medium.otf

  

Update src/theme/typography

    import localFont from 'next/font/local';
    import { Barlow } from 'next/font/google';
     
    export const primaryFont = localFont({
      src: [
        {
          path: '../../public/fonts/CircularStd-Book.otf',
          weight: '400',
          style: 'normal',
        },
        {
          path: '../../public/fonts/CircularStd-Medium.otf',
          weight: '500',
          style: 'normal',
        },
        {
          path: '../../public/fonts/CircularStd-Bold.otf',
          weight: '700',
          style: 'normal',
        },
      ],
    });
     
    export const secondaryFont = Barlow({
      weight: ['900'],
      subsets: ['latin'],
      display: 'swap',
      fallback: ['Helvetica', 'Arial', 'sans-serif'],
    });

**Usage**

    import { primaryFont } from 'src/theme/typography';
     
    export default function RootLayout({ children }) {
      return (
        <html lang="en" className={primaryFont.className}>
          <body>
            {children}
          </body>
        </html>
      );
    }

  

    import { primaryFont, secondaryFont } from 'src/theme/typography';
     
    const StyledTextH1 = styled('h1')({
      fontSize: 16,
      fontFamily: primaryFont.style.fontFamily,
    });
     
    const StyledTextH2 = styled('h2')({
      fontSize: 16,
      fontFamily: secondaryFont.style.fontFamily,
    });

* * *

###### [](#reference)Reference:

*   [https://minimals.cc/components/foundation/typography](https://minimals.cc/components/foundation/typography)


