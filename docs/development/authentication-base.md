*Authentication Base
===================

Minimals template that supports authentication methods JWT,Aws Amplify, Auth0, Firebase

* * *

##### [](#jwt)JWT

**Step 1:**

Update `.env`

    REACT_APP_HOST_API=https://api-dev-minimal-v5.vercel.app or your-website-base-URL

.env

**Step 2:**

Update `src/App` or `src/app/layout`

    import { AuthProvider } from 'src/auth/context/jwt';
     
    <AuthProvider>
      {children}
    </AuthProvider>;

src/App or src/app/layout

**Step 3:**

Update `src/auth/hooks/use-auth-context`

    import { AuthContext } from '../context/jwt/auth-context';

src/auth/hooks/use-auth-context

* * *

##### [](#firebase)Firebase

[Flow demo](https://www.dropbox.com/s/4kv2msowsh2yjbv/%5BAuth%5D_firebase.mp4?dl=0)

**Step 1:**

[Create Firestore Database](https://www.dropbox.com/s/almvpoqk3dkscp5/%5BAuth%5D_firestore_collection%20%26%20rules.mp4?dl=0)

Update rule in Cloud Firestore

    service cloud.firestore {
      match /databases/{database}/documents {
        match /{document=**} {
          allow read, write: if request.auth.uid != null;
        }
      }
    }

**Step 2:**

Update `.env`

    REACT_APP_FIREBASE_API_KEY=
    REACT_APP_FIREBASE_AUTH_DOMAIN=
    REACT_APP_FIREBASE_PROJECT_ID=
    REACT_APP_FIREBASE_STORAGE_BUCKET=
    REACT_APP_FIREBASE_MESSAGING_SENDER_ID=
    REACT_APP_FIREBASE_APPID=

.env

**Step 3:**

Update `src/App` or `src/app/layout`

    import { AuthProvider } from 'src/auth/context/firebase';
     
    <AuthProvider>
      {children}
    </AuthProvider>;

src/App or src/app/layout

**Step 4:**

Update `src/auth/hooks/use-auth-context`

    import { AuthContext } from '../context/firebase/auth-context';

src/auth/hooks/use-auth-context.js

* * *

##### [](#amplify)Amplify

[Flow demo](https://www.dropbox.com/s/4bj97w3vi1nw2ck/%5BAuth%5D-amplify.mp4?dl=0)

**Step 1:**

Update `.env`

    REACT_APP_AWS_AMPLIFY_USER_POOL_ID=us-east-1_lz1fF1nlN
    REACT_APP_AWS_AMPLIFY_USER_POOL_WEB_CLIENT_ID=1rlr1111shmclka1111f1v1fcp
    REACT_APP_AWS_AMPLIFY_REGION=us-east-1

.env

**Step 2:**

Update `src/App` or `src/app/layout`

    import { AuthProvider } from 'src/auth/context/amplify';
     
    <AuthProvider>
      {children}
    </AuthProvider>;

src/App or src/app/layout

**Step 3:**

Update `src/auth/hooks/use-auth-context`

    import { AuthContext } from '../context/amplify/auth-context';

src/auth/hooks/use-auth-context.js

* * *

##### [](#auth0)Auth0

[Flow demo](https://www.dropbox.com/s/ldw9tkwjkb0vxss/%5BAuth%5D_auth0.mp4?dl=0)

**Step 1:** [Example settings](https://www.dropbox.com/s/9zwm8svsbl87g2a/auth0-settings.png?dl=0)

Update `.env`

    REACT_APP_AUTH0_CALLBACK_URL=http://localhost:3000/auth/auth0/callback or your-website-base-URL
    REACT_APP_AUTH0_DOMAIN=k1wfhc1k.us.auth0.com
    REACT_APP_AUTH0_CLIENT_ID=za1frltoozwl1H1ye1YC1BQL0eHdmGUD

.env

**Step 2:**

Update `src/App` or `src/app/layout`

    import { AuthProvider } from 'src/auth/context/auth0';
     
    <AuthProvider>
      {children}
    </AuthProvider>;

src/App or src/app/layout

**Step 3:**

Update `src/auth/hooks/use-auth-context`

    import { AuthContext } from '../context/auth0/auth-context';

src/auth/hooks/use-auth-context.js

* * *

##### [](#get-user-info)Get User Info

    // Change
    import { useMockedUser } from 'src/hooks/use-mocked-user';
    const { user } = useMockedUser();
     
    // To
    import { useAuthContext } from 'src/auth/hooks';
    const { user } = useAuthContext();