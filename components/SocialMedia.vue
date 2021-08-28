<template>
  <div>
    <v-btn
      v-for="(item, i) in items.slice(0, large ? items.length : 2)"
      :key="i"
      :value="item.name"
      fab
      class="ma-2"
      color="info"
      :small="true"
      @click="NavigateToSM(item.name)"
    >
      <v-icon
        dark
        v-text="item.icon"
      />
    </v-btn>
  </div>
</template>

<script>
  export default { 
    props: {
      large: {
        type: Boolean,
        default: false,
      },
    },
    data: () => ({
      items: [
        {
          name: 'LinkedIn',
          icon: 'mdi-linkedin',
        },
        {
          name: 'Github',
          icon: 'mdi-github',
        },
        {
          name: 'Email',
          icon: 'mdi-email',
        },
      ],
    }),
    methods:{
      NavigateToSM(val){
        if(val=="Github"){
          window.open("https://github.com/robertomaldonado", '_blank')
        }
        else if(val=="LinkedIn"){
          window.open("https://www.linkedin.com/in/jrmaldo/", '_blank')
        }
        else if(val=="Email"){
          window.open("mailto:?subject=Contact&body=Hello!");
        }
      }
    }
  }
</script>
