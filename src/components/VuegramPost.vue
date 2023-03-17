<template>
    <ion-item>
        <ion-avatar slot="start">
            <img :src="post.userImage" />
        </ion-avatar>
        <ion-label>{{ post.username }}</ion-label>
    </ion-item>

    <ion-content class="ion-padding">
        <ion-img :src="post.postImage"></ion-img>
        <div class="image-container" :class="post.filter" :style="{ backgroundImage: 'url(' + post.postImage + ')' }">
        </div>

        <div class="content">
            <div class="heart">
                <ion-icon :icon="heart" size="large" :class="{ 'heart': this.post.hasBeenLiked }" @click="like"></ion-icon>
            </div>
            <p class="likes">{{ post.likes }} likes</p>
            <p class="caption"><span>{{ post.username }}</span> {{ post.caption }}</p>
        </div>
    </ion-content>
</template>
  
<script>
import { IonAvatar, IonItem, IonLabel, IonContent, IonImg, IonIcon } from '@ionic/vue';
import { heart } from 'ionicons/icons';

export default {
    components: { IonAvatar, IonItem, IonLabel, IonContent, IonImg, IonIcon },

    props: {
        post: Object
    },

    data() {
        return {
            heart
        }
    },

    methods: {
        like() {
            // eslint-disable-next-line vue/no-mutating-props
            this.post.hasBeenLiked ? this.post.likes-- : this.post.likes++;
            // eslint-disable-next-line vue/no-mutating-props
            this.post.hasBeenLiked = !this.post.hasBeenLiked;
        }
    }
};
</script>
