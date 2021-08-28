<template>
  <section
    id="services"
    class="overflow-hidden"
  >
    <v-row
      class="accent"
      no-gutters
    >
      <v-col
        class="hidden-sm-and-down"
        md="6"
      >
        <v-img
          :src="require('@/assets/circuit.jpg')"
          height="100%"
        />
      </v-col>

      <v-col
        class="text-center pa-5"
        cols="12"
        md="6"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <v-col cols="12">
            <base-bubble-2
              style="transform: translateX(55%)"
            />
            <base-heading class="info--text">
              Values
            </base-heading>

            <base-text>
              Life long quick learner. <br/>
              Adding value to people's life through technology.<br/>
            </base-text>
          </v-col>

          <v-col
            v-for="(service, i) in services"
            :key="i"
            class="text-center mb-3"
            md="6"
          >
            <v-avatar
              class="elevation-6 mb-2"
              color="#69A1BB"
              size="100"
              tile
            >
              <v-icon
                dark
                size="70"
                v-text="service.icon"
              />
            </v-avatar>

            <base-text>
              <div
                class="mb-2"
                v-text="service.name"
              />
              <div v-html="service.blurb" />
            </base-text>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </section>
</template>

<script>
  export default {
    name: 'Services',

    data: () => ({
      services: [
        {
          name: 'Research',
          icon: 'mdi-library',
          blurb: 'Keep up to date with technology',
        },
        {
          name: 'Leadership',
          icon: 'mdi-pencil-outline',
          blurb: 'Applying technology to solve problems',
        },
        {
          name: 'Development',
          icon: 'mdi-cogs',
          blurb: 'Practice skills to keep them sharp',
        },
        {
          name: 'Team Oriented',
          icon: 'mdi-human-queue',
          blurb: 'Always better to work in groups,<br/>More brain power bigger goals',
        },
      ],
    }),
  }
</script>
