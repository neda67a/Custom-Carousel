
<template>
  <div class="carousel">
      <slot></slot>
      <button  @click="next" class="next">&#x2192;</button>
      <button  @click="prev" class="prev">&#8592;</button>
      <button  @click="next" class="down">&#8595;</button>
  </div>
</template>

<script>

export default {
    date(){
        return {

        }
    },

    methods:{
        next(){
            this.$emit('next');
        }, 

        prev(){
            this.$emit('prev');
        }
    }
}
</script>

<style>

    .carousel{
        position: relative;
        width: 1030px;
        overflow: hidden;
        margin: 0 auto;
    }

    button{
        position: absolute;
        height: 40px;
        width: 45px;
        top: 40%;
        border:none;
        background-color:  rgba(0, 0, 0, 0.603);
        color: #fff;
        font-size: 30px;
    }

    .next{
        right: 0;
    }
    .prev{
        left: 0;
    }

    .down{
        display: none;
          left:44%;
        top: 100%;
        transform: translate(-50%, -50px);
    }
   button:focus, 
   button:hover{
        outline: none;
        cursor: pointer;
        background-color: rgba(128, 128, 128, 0.932);
    }

    @media (max-width: 600px) {

    .carousel {
      width: 600px;
      height: 600px;
      padding: 0 37px 0 37px;

    }

     .next,.prev{
         display: none;
     }
     .down{
         display: block;
       
     }
   }

</style>
