<template>
  <div id="app"></div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

import Firebase from 'firebase';

let config = {

  apiKey: "AIzaSyA1fAX9P4HSX5_YMNfwm1K27tsA2VXn8J0",
  authDomain: "learnprogramminginvuejs-830dc.firebaseapp.com",
  databaseURL: "https://learnprogramminginvuejs-830dc-default-rtdb.firebaseio.com",
  projectId: "learnprogramminginvuejs-830dc",
  storageBucket: "learnprogramminginvuejs-830dc.appspot.com",
  messagingSenderId: "592997188390",
  appId: "1:592997188390:web:89468bd3a1a0ae2eca77e7",
  measurementId: "G-P3DQRHNECH"

}

let app = Firebase.initializeApp(config);
let db = app.database();
let programmingRef = db.ref('programming');

export default {
  name: "App",
  firebase: {
    programming: programmingRef
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
