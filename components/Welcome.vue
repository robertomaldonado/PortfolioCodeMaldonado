<template>
  <section
    id="welcome"
    class="overflow-hidden"
  >
    <v-row no-gutters>
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/person.jpeg')"
          height="100vh"
        />
      </v-col>

      <v-col
        class="align-content-space-between layout wrap"
        cols="12"
        md="6"
        :pa-5="$vuetify.breakpoint.smAndDown"
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateY(25%)"
        />

        <v-row
          align="center"
          justify="center"
        >
          <v-col
            cols="10"
            md="6"
          >
            <base-heading>Roberto Maldonado</base-heading>
            <base-text>
            Software Engineer <br/>
            MSc. Computer Science <br/> <br/>

            Welcome to my portfolio! <br/>
            I'm interested in technology and in the process of software engineering.<br/>
            Always exited for logic challenges, riddles and jigsaw puzzles. <br/><br/>
            This site was created using NuxtJs (VueJs), Vuetify and is hosted in firebase 
            with enabled autodeployment and publishing feature once the build is successful through github actions. <br/>
            Do you want to lern more about this project or myself? Follow my linkedIn.
            </base-text>
            <base-btn 
              class="mt-4" 
              color="primary"
              @click="ToLinkedIn()"
            >
              Let's connect on LinkedIn!
            </base-btn>
          </v-col>
        </v-row>

        <base-bubble-2
          style="transform: rotate(180deg) translate(-200px, -15%)"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default { 
    props: {},
    data() {
      return {}
    },
    methods: {
      ToLinkedIn(){
        window.open("https://www.linkedin.com/in/jrmaldo/", '_blank')
      }
    }
  }
</script>