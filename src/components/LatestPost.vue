<template>
  <v-container>
<div class="block LatestPostBlock">
    <h2 class="text-center">LatestPost</h2>
    <v-row>
        <v-col cols="12" md="4" v-for="item in items" :key="item.id">
            <v-card
     outlined
    class="mx-auto"
    
  >
    <v-img
      class="white--text align-end"
      height="200px"
      :src="item.src"
    >
      <v-card-title>{{item.title}}</v-card-title>
    </v-img>

    <v-card-subtitle class="pb-0">
     {{item.subtitle}}
    </v-card-subtitle>

    <v-card-text class="text--primary">
      <div>{{item.description}} </div>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="primary"
        text
      >
        More
      </v-btn>

    </v-card-actions>
  </v-card>
        </v-col>
    </v-row>
     
</div>
  </v-container>
</template>

<script>
export default {
  name: "LatestPost",

  data() {
      return {
          items: [
              {
                  id: 1,
                  title: "xxx",
                  subtitle: "dddddddddddddddd",
                  description: "vvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvvv ,vvvvvvvv,vvvvvvvv",
                  src: require ("../assets/images/img10.jpg") ,
              },
                 {
                  id:2 ,
                  title: "ccccccc",
                  subtitle: "vvvvv bbbbbb" ,
                  description: "cccccc xxxxxxxxx xxxxxxxx",
                  src: require ("../assets/images/img11.jpg") ,
              },
              {
                  id:3 ,
                  title: "zzzzzzzz",
                  subtitle: "ddddddd bbbbbb" ,
                  description: "cccccc xxxxxxxxx xxxxxxxx",
                  src: require ("../assets/images/img12.jpg") ,
              },

          ]
      }
  },
};
</script>
