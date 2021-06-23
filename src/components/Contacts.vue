<template>
  <p class="contact">
    <i :class="`${singleContact.family} ${singleContact.type}`"></i>
    {{ singleContact.text }}
  </p>
</template>

<script>
export default {
  name: "Contacts",
  props: {
    singleContact: Object,
  },
};
</script>

<style lang="scss">
@import '../scss/variables';
    .contact {
        color: $grey;
        margin: 10px 0;

        i {
          margin-right: 5px;
        }
    }
</style>