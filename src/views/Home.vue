<template>
  <v-content>
    <Hero/>
    <Galery/>
    <LatestPost/>
  </v-content>
</template>

<script>
// @ is an alias to /src
import Hero from '../components/Hero';
import Galery from '../components/Galery';
import LatestPost from '../components/LatestPost';

export default {
  name: 'Home',
  components: {

    Hero,
    Galery,
    LatestPost,
  
  },
    data() {
      return {
          items: [
          ]
      };

  }
 
};

</script>
