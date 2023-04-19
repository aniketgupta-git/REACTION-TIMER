<template>
  <h3>THE SCORE IS {{ this.score }} ms </h3>
  <h3>You are {{ rank }}</h3>
</template>

<script>
export default {
    props: ['score'],
    data(){
        return{
            rank : null
        }
    },
    mounted(){
       if(this.score < 300){
            this.rank = "Khiladi"
       }else if (this.score < 500 ){
            this.rank = "Average"
       }else{
         this.rank = "Anadi" 
       }
    }
}
</script>

<style>

</style>