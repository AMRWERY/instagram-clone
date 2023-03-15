<template>
    <ion-header>
        <ion-toolbar>
            <ion-title><ion-icon :icon="logoInstagram"></ion-icon> Vue-Gram</ion-title>
        </ion-toolbar>
    </ion-header>
</template>

<script>
import { IonHeader, IonToolbar, IonTitle, IonIcon } from '@ionic/vue';
import { logoInstagram } from 'ionicons/icons';

export default {
    components: { IonHeader, IonToolbar, IonTitle, IonIcon },

    data() {
        return {
            logoInstagram
        }
    }
}
</script>

<style scoped>
ion-title {
    font-family: 'Lobster', cursive;
    font-size: 30px;
}
</style>