<template>
  <v-app dark>
    <v-card class="container mt-6">
      <v-card-title class="text-center justify-center">
        <v-img
          max-height="200"
          max-width="400"
          :src="require('assets/img/blanca.png')"
        ></v-img>
      </v-card-title>

      <v-tabs centered> 
        <v-tab v-for="tab in tabs" :key="tab.title" :to="tab.to">{{ tab.title }}</v-tab>
      </v-tabs>

      <v-card-text>
        <Nuxt />
      </v-card-text>

      <v-footer class="text-center justify-center">
        <span>© 2022 | Jesús Serrano Medrano</span>
        <v-container>
          <v-btn
            v-for="icon in icons"
            :key="icon.id"
            :href="icon.link"
            target="_blank"
            icon
          >
            <v-icon :color="icon.color" size="24px">
              {{ icon.icon }}
            </v-icon>
          </v-btn>
        </v-container>
      </v-footer>
    </v-card>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      tabs: [
        {
          title: 'Inicio',
          to: '/'
        },
        {
          title: 'Cofrade',
          to: '/cofrade'
        },
        {
          title: 'Naturaleza',
          to: '/naturaleza'
        },
        {
          title: 'Viajes',
          to: '/viajes'
        },
        {
          title: 'Nocturna',
          to: '/nocturna'
        },
        {
          title: 'Deportes',
          to: '/deportes'
        }
      ],
      icons: [
        {
          id: 1,
          icon: 'mdi-facebook',
          color: '#4267B2',
          link: 'https://m.facebook.com/jesus.sm96/'
        },
        {
          id: 2,
          icon: 'mdi-instagram',
          color: '#e4405f',
          link: 'https://instagram.com/jesus.sm96'
        },
      ],
    }
  }
}
</script>
