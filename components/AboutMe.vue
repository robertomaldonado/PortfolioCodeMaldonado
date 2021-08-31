<template>
  <section
    id="about"
    class="overflow-hidden"
  >
    <v-row
      class="white"
      no-gutters
    >
      <v-col
        class="pa-5"
        cols="12"
        md="6"
      >
        <base-bubble-1 style="transform: translate(5%, -5%)" />
        <base-heading class="info--text">
          About Me
        </base-heading>
        <base-text class="mb-5">
          Passionate for technology<br>
          Always eager to learn new things<br>
          Be productive with available resources
        </base-text>
        <base-subheading class="info--text">
          Education
        </base-subheading>
        <base-text class="mb-5">
          My short trip on education: <br>
        </base-text>
        <v-alert
          outlined
          color="black"
          class="mb-12"
        >
          <v-row
            v-for="(ed, i) in education"
            :key="i"
            style="color: black;"
          >
            <v-col
              cols="8"
            >
              <b>{{ed.institution}}</b>
            </v-col>
            <v-col
              class="text-right"
              cols="4"
            >
              {{ed.year}}
            </v-col>
            <v-row>
            <v-col
              cols="8"
              class="ml-4"
            >
              {{ed.degree_level}}
            </v-col>
            <v-col 
              cols="12"
              class="text-right mt-n15"
            >
              <v-img
                class="image-container mr-4"
                :src="require(`@/assets/${ed.ilogo}`)"
              />
            </v-col>
            </v-row>
            <v-progress-linear
              value=100
              color="black"
              height="4"
            />
          </v-row>
        </v-alert>
        <base-subheading class="info--text">
          Technical skills
        </base-subheading>
        <base-text class="mb-5">
          Skills I have developed (but not limited to): <br>
        </base-text>
        <v-alert
          outlined
          color="info"
          class="mb-10"
        >
          <v-row
            v-for="(skill, i) in skills"
            :key="i"
            style="color: #69A1BB"
          >
            <v-col
              cols="6"
              v-text="skill.name"
            />
            <v-col
              class="text-right"
              cols="6"
              v-text="`${skill.value}%`"
            />
            <v-progress-linear
              :value="skill.value"
              color="info"
              height="8"
            />
          </v-row>
        </v-alert>
      </v-col>
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/rock-pile.jpeg')"
          height="100%"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    data: () => ({
      skills: [
        {
          name: 'Python, Flask, Javascript (NuxtJs, VueJs, Vuetify), NoSQL, Google Cloud Platform, git',
          value: 100,
        },
        {
          name: 'C/C++, C#, R, Typescript, React, Angular, pandas, numpy, ffmpeg, devOps, CI/CD, gnuplot, bigQuery, mongoDB, nodeJs, express, npm, yarn, terraform, docker, kubernetes, Twilio, REST APIs',
          value: 80,
        }
      ],
      education: [
        {
          id: 1,
          institution: 'Florida State University',
          degree_level: 'M.Sc. Computer Science',
          year: "Tallahasse, FL | 2019",
          ilogo: "fsulogo.png"
        },
        {
          id: 2,
          institution: 'Universidad San Francisco de Quito',
          degree_level: 'B.S. Computer Science',
          year: "Quito, Ecuador | 2015",
          ilogo: "usfqlogo.jpeg"
        }
      ],
    }),
  }
</script>

<style>
.image-container { 
  width:75px;
  height:75px;
  float: right;
}
</style>