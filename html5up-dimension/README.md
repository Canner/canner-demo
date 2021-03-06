# HTML5Up-dimension canner Demo

canner demo using HTML5Up-dimension theme

> This project use Firebase realtime database, learn more: https://docs.canner.io/docs/start-quick-firebase.html

## Live Demo: https://flamelin-f64b2.firebaseapp.com

## Steps

#### 1. Create a new project at Firebase

and enable `Anonymous` login in `Authentication -> Sign-in method`.

#### 2. Install [Firebase Tool](https://github.com/firebase/firebase-tools)
#### 3. Install `@canner/cli`

```
npm i -g @canner/cli
```

#### 4. Create project at Canner
#### 5. Update `public/index.html` & `canner.schema.js` Firebase config.


**index.html**

```js
  var config = {
    apiKey: "API_KEY",
    authDomain: "AUTH_DOMAIN",
    databaseURL: "DATABASE_URL",
    projectId: "PROJECT_ID",
    storageBucket: "STORAGE_BUCKET",
    messagingSenderId: "MESSAGING_SENDER_ID"
  };
```

and **canner.schema.js - utils.js**

```js
const myDefultConnector = new FirebaseRtdbAdminConnector({
  projectId: "<Project ID>"
});
```

#### 6. Download firebase private key

go to "settings > service account" download private key, and put it in `cert/firebase` folder.

> Learn more http://docs.canner.io/docs/start-quick-firebase.html

#### 7. Deploy your website on [Firebase hosting](https://firebase.google.com/docs/hosting/)

Select project

```
  firebase init
```

Deploy host

```
  firebase deploy
```

#### 8. Deploy your data to Firebase, and schema to Canner through Canner cli tool.

Deploy schema

```
  canner script:deploy
```

Import data

```
  canner data:import
```

### Credits:
    - HTML5Up:
        - see `./LICENSE.txt`

    - Demo Images:
        - Unsplash (unsplash.com)

    - Icons:
        - Font Awesome (fortawesome.github.com/Font-Awesome)

    - Other:
        - jQuery (jquery.com)
        - html5shiv.js (@afarkas @jdalton @jon_neal @rem)
        - Respond.js (j.mp/respondjs)
        - Skel (skel.io)
