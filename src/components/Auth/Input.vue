<template>
  <ion-item class="ion-margin-bottom">
    <ion-input :type="type" :placeholder="placeholder"></ion-input>
  </ion-item>
</template>

<script>
export default {
  name: "Input",
  props: [
      'type',
      'placeholder'
  ]
}
</script>

<style scoped>
  ion-item {
    border-radius: 50px;
    height: 55px;
    box-shadow: 1px 8px 8px 0px rgba(0, 0, 0, 0.08);
    --highlight-height: 0px;
  }

  ion-input {
    font-size: 18px;
    --padding-top: 20px;
    --padding-bottom: 15px;
    --padding-start: 5px;
  }

  a {
    font-size: 17px;
    letter-spacing: 0.5px;
    text-decoration: none;
  }
</style>