<template>
    <ion-menu side="end" content-id="main-content">
      <ion-header>
        <ion-toolbar color="primary">
          <ion-title>Menu</ion-title>
        </ion-toolbar>
      </ion-header>
      <ion-content color="primary" class="ion-padding">
        <menu-item-app />
      </ion-content>
    </ion-menu>
  </template>
  
  <script lang="ts">
  import {
    IonButtons,
    IonContent,
    IonHeader,
    IonMenu,
    IonMenuButton,
    IonPage,
    IonTitle,
    IonToolbar,
    IonList,
    IonItem,
    IonLabel,
  } from "@ionic/vue";
  import MenuItemApp from "./MenuItemApp.vue";
  import { defineComponent } from "vue";
  
  export default defineComponent({
    components: {
      IonButtons,
      IonContent,
      IonHeader,
      IonMenu,
      IonMenuButton,
      IonPage,
      IonTitle,
      IonToolbar,
      IonList,
      IonItem,
      IonLabel,
      MenuItemApp,
    },
  });
  </script>
  