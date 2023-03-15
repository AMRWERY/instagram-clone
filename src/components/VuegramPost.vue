<template>
    <ion-item>
        <ion-avatar slot="start">
            <img :src="post.userImage" />
        </ion-avatar>
        <ion-label>Item Avatar</ion-label>
    </ion-item>

    <ion-content class="ion-padding">
        <ion-img src="https://ionic-docs-demo-v6.vercel.app/assets/madison.jpg"></ion-img>
    </ion-content>
</template>
  
<script>
import { IonAvatar, IonItem, IonLabel, IonContent, IonImg } from '@ionic/vue';

export default {
    components: { IonAvatar, IonItem, IonLabel, IonContent, IonImg },

    props: {
        post: Object
    },
};
</script>
