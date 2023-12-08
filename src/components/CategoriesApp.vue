<template>
    <header-app/>
    <ion-content class="detail-container" :fullscreen="true">
        <ion-row class="d-flex justify-content-center">
            <ion-col size="8">
                <h4 class="d-flex justify-content-center">CATEGORIAS DISPONIBLES:</h4>
            </ion-col>
        </ion-row>
        <ion-row class="d-flex justify-content-center">
            <ion-col v-for="(category, index) in categories" :key="index" size="8">
                <card-category-app  :category="category"/>
            </ion-col>
        </ion-row>
    </ion-content>
</template>

<script lang="ts">
import HeaderApp from "@/components/HeaderApp.vue"
import { IonContent, IonRow, IonCol, IonTitle, IonImg, IonList, IonItem, IonButton, IonModal, IonAccordionGroup, IonAccordion, IonBadge } from '@ionic/vue';
import CardCategoryApp from '@/components/CardCategoryApp.vue'
import "@/assets/scss/global.scss"
export default {
    name: 'CategoriesApp',
    components: {
        HeaderApp,
        CardCategoryApp,
        IonContent,
        IonRow,
        IonCol,
        IonTitle,
        IonImg,
        IonList,
        IonItem,
        IonButton, 
        IonModal,
        IonAccordionGroup,
        IonAccordion,
        IonBadge
    },
    data() {
        return {
            categories: [
                {
                    image: '../assets/img/cartelera2.jpeg',
                    name: "CINE",
                    id: 'now_playing',
                    description: ''
                },
                {
                    image: '../assets/img/populares2.jpg',
                    name: "FAMOSAS",
                    id: 'popular',
                },
                {
                    image: '../assets/img/mejorcalifi2.jpg',
                    name: "MAYOR CALIFICACIÓN",
                    id: 'top_rated',
                },
            ]
        }
    }
}
</script>

<style>
</style>