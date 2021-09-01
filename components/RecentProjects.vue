<template>
  <section
    id="recent-projects"
    class="overflow-hidden"
  >
    <v-row no-gutters>
      <v-col
        class="gradient-bottom text-center pa-5 white--text"
        cols="12"
        md="6"
      >
        <base-bubble-1
          style="transform: rotate(180deg) translateX(25%)"
        />

        <base-heading>
          Recent Projects
        </base-heading>

        <base-text class="mb-5">
          These are projects I have worked on in my free time. <br/>
          They include some projects done with Js frameworks: VueJs, NuxtJs and ReactJs.<br/>
        </base-text>

        <v-card color="secondary">
          <v-container class="pa-2">
            <v-row>
              <v-col
                v-for="project in projects"
                :key="project.id"
                :value="project.url"
                cols="12"
                md="6"
                @click="GoToProject(project.url)"
              >
                <a>
                  <v-img
                    :src="require(`@/assets/${project.img}.jpeg`)"
                    height="200"
                  />
                  <v-card class="gradient-bottom">
                    <v-card-title align="center">
                      {{project.name}}
                    </v-card-title>
                    <v-card-text>
                      {{project.description}}
                    </v-card-text>
                  </v-card>
                </a>
              </v-col>
            </v-row>
          </v-container>
        </v-card>
      </v-col>

      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/laptop.jpeg')"
          height="100%"
        />
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'RecentProjects',

    data: () => ({
      projects: [
        {
          id:1,
          img: 'glasses',
          url: 'https://github.com/robertomaldonado/LeetHubCode/',
          name: 'LeetCode Challenges',
          description: 'This a link to my GitHub coding solutions for LeetCode'
        },
        {
          id:2,
          img: 'cactus',
          url: 'https://natgarden-ec.web.app/',
          name: 'Natgarden',
          description: 'This is an informative website that uses NuxtJS'
        },
        {
          id:3,
          img: 'stacks',
          name: 'ReactJs Resume',
          url: 'https://maldonado-3ed76.web.app/',
          description: 'This a resume version created with ReactJs'
        },
        {
          id:4,
          img: 'code_js',
          name: 'My Reading Books Blog',
          url: 'https://skylake.web.app/',
          description: 'A simple blog to present my read books and a short review'
        }
      ],
    }),
    methods:{
      GoToProject(url){
        console.log(url)
        window.open(url, '_blank')
      }
    }
  }
</script>
