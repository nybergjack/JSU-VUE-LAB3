<script setup>
import AppButton from "../components/AppButton.vue";
</script>

<template>
  <div class="card text-center">
    <div class="card-body">
      <!-- recive the props from HomePage -->
      <h5 class="card-title">{{ option.cardTitle }}</h5>
      <p class="card-text">{{ option.cardDescription }}</p>
      <!-- reuse custom button with custom properties -->
      <AppButton color="primary" size="medium" padding="p-large"
        >{{ option.cardButton }}
      </AppButton>
    </div>
  </div>
</template>

<script>
export default {
  components: {
    AppButton,
  },
  props: {
    option: Object,
  },
  /* props: {
    title: String,
    desc: String,
    btnLable: String,
  }, */
};
/* const props = defineProps({
  title: String,
  description: String,
}); */
</script>

<style>
.card-text {
  margin-bottom: 2rem;
}
</style>
