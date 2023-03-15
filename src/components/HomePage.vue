<template>
  <TheHeader />

  <PhoneBody />

  <TheFooter />
</template>

<script>
import TheHeader from '../views/TheHeader.vue';
import PhoneBody from '../views/PhoneBody.vue';
import TheFooter from '../views/TheFooter.vue';

export default {
  components: { TheHeader, PhoneBody, TheFooter },
};
</script>


