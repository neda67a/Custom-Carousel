<template>
  <div class="carouselslideimage">
      <figure v-for="(category) in slides[index]" 
              :key="category">
         <img v-bind:src="category.img">
        <p class="text" > {{ category.description}} </p>
      </figure>
  </div>
</template>

<script>

export default {
    props: ['slides' , 'index'],
    date(){
        return {

        }
    }
}
</script>

<style>

.carouselslideimage figure {
    width: 250px;
    height: 250px;
    float: left;
    padding: 0;
    margin: 0;
    position: relative;
    margin-bottom: 10px;
}

.carouselslideimage figure:not(:last-child){
    margin-right: 10px;
    
   
}
.carouselslideimage img{
    border-radius: 30px;
}

.carouselslideimage img:hover {
   filter: blur(1.5px);
   
}
.text{
    color: white;
    position: absolute;
    bottom: 10px;
    left: 50%;
    transform: translate(-50%, -50%);
   
}
</style>