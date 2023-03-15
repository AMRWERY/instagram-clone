<template>
    <ion-footer>
        <ion-toolbar>
            <ion-icon :icon="home" size="large"></ion-icon>
            <ion-icon :icon="add" slot="end" size="large"></ion-icon>
        </ion-toolbar>
    </ion-footer>
</template>

<script>
import { IonFooter, IonToolbar, IonIcon } from '@ionic/vue';
import { home, add } from 'ionicons/icons';

export default {
    components: { IonFooter, IonToolbar, IonIcon },

    data() {
        return {
            home,
            add
        }
    },
}
</script>

<style scoped>
ion-footer {
    position: absolute;
    bottom: 0;
}
</style>