<template>
      <div v-show="visibleSlide === index" class="carouselSlide">
        <slot></slot>
      </div>
</template>

<script>

export default {
   props: [ 'visibleSlide', 'index'],

    date(){
        return {

        }
    }
}
</script>

<style>

</style>