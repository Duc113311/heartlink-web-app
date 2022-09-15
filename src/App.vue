<template>
  <div class="h-screen w-full p-3">
    <!-- <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/login">Login</router-link>
    </nav> -->
    <router-view />
  </div>
</template>
<script>
import { fireStoreCore, collection, getDocs } from "./configs/firebase";
export default {
  setup() {
    async function getUser() {
      const citiesCol = collection(fireStoreCore, "users");
      const citySnapshot = await getDocs(citiesCol);
      const cityList = citySnapshot.docs.map((doc) => doc.data());
      console.log(cityList);
      return cityList;
    }

    getUser();
  },
};
</script>
