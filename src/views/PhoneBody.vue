<template>
    <ion-content :fullscreen="true" class="ion-padding" :filters="filters" :posts="posts">
        <VuegramPost />
    </ion-content>
</template>

<script>
import { IonContent } from '@ionic/vue';
import VuegramPost from '../components/VuegramPost.vue';
import filters from '../data/filters';
import posts from '../data/posts';

export default {
    components: { VuegramPost, IonContent },

    data() {
        return {
            filters,
            posts
        }
    },
}
</script>