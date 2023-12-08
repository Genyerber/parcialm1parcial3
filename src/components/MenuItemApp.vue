<template>
    <ion-list class="ion-text-end">
      <ion-item href="/">
        <ion-label>Inicio</ion-label>
      </ion-item>
      <ion-item color="primary" v-for="genre in genres" :key="genre.id" :href="`/movies/genre/${genre.id}`">
        <ion-label>{{ genre.name }}</ion-label>
      </ion-item>
    </ion-list>
  </template>
  
  <script>
  import { IonList, IonItem, IonLabel } from '@ionic/vue';
  import MovieServices from "@/services/MovieServices"
  
  export default {
    name: 'MenuItemApp',
    components: {
      IonItem,
      IonList,
      IonLabel
    },
    data() {
      return {
        genres: [{}]
      }
    },
    async created() {
      this.genres = await MovieServices.getGenrers()
    }
  }
  </script>
  
  <style scoped>
  /* Puedes agregar estilos específicos aquí si es necesario */
  </style>
  