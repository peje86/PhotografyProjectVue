<template>
  <v-content>
  <div class="staticHero">
       <v-img
      
      src="../assets/images/img14.jpg"
    >
    <v-row align="end" class="lightbox white--text pa-2 fill-height">
      <v-col>
       <v-container>
          <div class="headline hidden-xs-only">Contact Us</div>
       </v-container>
      </v-col>
    </v-row>
    </v-img>
    </div> 

    <div class="block">
      <v-container>
         <v-form
    ref="form"
    v-model="valid"
    lazy-validation
  >
    <v-text-field
      v-model="name"
      :counter="10"
      :rules="nameRules"
      label="Name"
      required
    ></v-text-field>

    <v-text-field
      v-model="email"
      :rules="emailRules"
      label="E-mail"
      required
    ></v-text-field>

    <v-textarea
          v-model="messages"
      :rules="messageRules"
      label="Messages"
      required
        ></v-textarea>

    

    <v-btn
      :disabled="!valid"
      color="success"
      class="mr-4"
      @click="validate"
    >
      Submit
    </v-btn>

    <v-btn
      color="error"
      class="mr-4"
      @click="reset"
    >
      Reset 
    </v-btn>

    
  </v-form>
      </v-container>
    </div>
    <div class="googlemap">
      <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d150446.72129098978!2d110.50785523760418!3d-7.742970087397829!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x54eab584e432360b%3A0x1c3bb99243deb742!2sAmerika%20Serikat!5e0!3m2!1sid!2sid!4v1619454611616!5m2!1sid!2sid" width="100%" height="450" ></iframe>
    </div>
  </v-content>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Contact',
    data: () => ({
      valid: true,
      name: '',
      nameRules: [
        v => !!v || 'Name is required',
        v => (v && v.length <= 10) || 'Name must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
       message: '',
      messageRules: [
        v => !!v || 'Messages is required',
        v =>(v && v.length >= 10) || 'Messages must more 10 character',
      ],
   
    }),

    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
     
    },
 
};
</script>
