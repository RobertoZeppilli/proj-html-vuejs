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
    .contact {
        color: #8fa1b5;
        margin: 10px 0;

        i {
          margin-right: 5px;
        }
    }
</style>