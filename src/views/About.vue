<template>
  <v-content>
   <div class="staticHero">
       <v-img
      
      src="../assets/images/img13.jpg"
    >
    <v-row align="end" class="lightbox white--text pa-2 fill-height">
      <v-col>
       <v-container>
          <div class="headline hidden-xs-only">About Us</div>
       </v-container>
      </v-col>
    </v-row>
    </v-img>
    </div> 
    <div class="block">
      <v-container>
        <p>cccccccc cccccccccc cccccccccccc cccccccccccc cccccccccc ccccccccccccc cccccccccccc cccccccccc ccccccccccc </p>
      </v-container>
    </div>
    <div class="block">
      <v-container>
        <h2 class="text-center">Our Teams</h2>
        <v-row>
          <v-col v-for="item in items" :key="item.id" cols="12" sm="4">
            <v-card 
    flat
    class="mx-auto"
  
  >
    <v-img
      class="white--text align-end"
     :src="item.src"
    >
    </v-img>

    <v-card-text class="text--primary- text-center">
      <div class="title">{{item.name}} </div>
<p>{{item.title}} </p>
    </v-card-text>

  </v-card>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </v-content>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'About',
    data() {
      return {
          items: [
            {
              id:1,
              src: require("../assets/images/team1.jpg"),
              name:'Peter Jack',
              title:'Manager'
            },
              {
              id:2,
              src: require("../assets/images/team2.jpg"),
              name:'adam ge',
              title:'jongos'
            },
              {
              id:3,
              src: require("../assets/images/team3.jpg"),
              name:'oper',
              title:'babuuuu'
            },
          ]
      };

  }
 
};

</script>
