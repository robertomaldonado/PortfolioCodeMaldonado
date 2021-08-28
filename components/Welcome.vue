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
          :src="require('@/assets/welcome.png')"
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
            Capicola sirloin pork loin, turducken shank cupim rump jerky picanha turkey meatloaf. 
            Tail frankfurter filet mignon meatloaf. 
            Ribeye bresaola porchetta, flank shankle doner sirloin corned beef kielbasa cow strip steak. 
            Kevin ribeye chislic shoulder t-bone ham beef ribs pork chop sausage pancetta sirloin pig. 
            Picanha hamburger chislic tenderloin. <br/> 
            Chicken salami bacon landjaeger capicola, tenderloin chuck rump chislic short loin fatback beef ribs jowl picanha meatball.
            </base-text>
            <base-btn 
            class="mt-4" 
            color="primary"
            nuxt
            to="/otherPage">
              See my work!
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
