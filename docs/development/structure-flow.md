*Structure
=========

* * *

    root
      ├── public
      ├── src
          ├── types
          ├── assets
          ├── components
          ├── pages OR app
          ├── hooks
          ├── layouts
          ├── sections
          ├── theme
          ├── utils
          ├── routes
          ├── ...
      ├── next.config.js
      ├── package.json
      ├── ...

* * *

##### [](#remove--clean)Remove & Clean

Depending on the needs of each project, there will be components that are not needed.

Below is the order of precedence for deleting components:

**Step 1:**

Delete unused pages in `/pages`or `/app`.

Example: delete `src/pages/contact-us.tsx`.

**Step 2:**

Create file `.unimportedrc.json`

CRAVite.jsNext.js

    {
      "rootDir": ".",
      "aliases": {
        "src/*": ["./src", "./src/*"]
      },
      "entryFiles": [
        {
          "file": "src/index.tsx",
          "aliases": {
            "src/*": ["./src", "./src/*"]
          },
          "extensions": [".js", ".jsx", ".ts", ".tsx"]
        }
      ],
      "moduleDirectory": ["node_modules"],
      "ignorePatterns": ["**/node_modules/**", "**/*.d.ts"]
    }

**Step 3:**

Find and delete related files.

Run:

    npx unimported --show-unused-files

  

Result:

    ➜  vite-ts npx unimported --show-unused-files
     
           summary               unimported v1.29.1 (node)
    ──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
           entry file          : src/main.tsx
     
           unresolved imports  : 3
           unused dependencies : 6
           unimported files    : 5
     
     
    ─────┬────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
         │ 5 unimported files
    ─────┼────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
       1 │ src/sections/contact/contact-form.tsx
       2 │ src/sections/contact/contact-hero.tsx
       3 │ src/sections/contact/contact-map.tsx
       4 │ src/sections/contact/view/contact-view.tsx
       5 │ src/sections/contact/view/index.ts
    ─────┴────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
     
     
           Inspect the results and run npx unimported -u to update ignore lists
    ➜  vite-ts

* * *

###### [](#reference)Reference:

*   [https://www.npmjs.com/package/unimported](https://www.npmjs.com/package/unimported)

