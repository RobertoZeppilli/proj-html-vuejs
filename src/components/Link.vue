<template>
  <a href="#">{{linktext}}<i class="fas fa-chevron-right"></i></a>
</template>

<script>
export default {
    name: 'Link',
    props: {
        linktext: String
    }
}
</script>

<style lang="scss">
    a {
        text-decoration: none;
        color: #191919;
        

        i {
            margin-left: 5px;
            font-size: 12px;
        }
    }
</style>