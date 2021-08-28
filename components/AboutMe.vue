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
        <!-- <base-bubble-1 style="transform: translate(5%, -5%)" /> -->
        <base-heading class="info--text">
          About Me
        </base-heading>
        <base-text class="mb-3">
          Passionate for technology<br>
          Always eager to learn new things<br>
          Be productive with available resources
        </base-text>
        <base-subheading class="info--text">
          Skills
        </base-subheading>
        <base-text class="mb-5">
          Skills which I consider important in the tech industry<br>
        </base-text>
        <v-alert
          outlined
          color="info"
        >
          <v-row
            v-for="(skill, i) in skills"
            :key="i"
            style="color: #69A1BB;"
          >
            <v-col
              class="text-uppercase"
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
          name: 'Python, Javascript(ES6)',
          value: 100,
        },
        {
          name: 'Web Development',
          value: 75,
        },
        {
          name: 'Web Support',
          value: 90,
        },
        {
          name: 'Web Support',
          value: 90,
        },
        {
          name: 'Web Support',
          value: 90,
        },
        {
          name: 'Web Support',
          value: 90,
        },
        {
          name: 'Web Support',
          value: 90,
        },
        {
          name: 'Web Support',
          value: 90,
        },
      ],
    }),
  }
</script>
