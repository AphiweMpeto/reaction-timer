<template>
<div>
  <p>reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
  </div> 
</template>

<script>
export default {
    props:['score'],
    data() {
        return {
            rank: null, 
        }
    },
    mounted() {
        if (this.score < 250){
            this.rank = 'Ninja Fingers'}
            else if (this.score < 480){
                this.rank = 'Rapid Reflexes'
            } else{
                this.rank = "snail pace.."
            }
        }
    }


</script>

<style>
.rank{
    font-size: 1.4em;
    color:rgb(85, 185, 152) ;
    font-weight: bold;
}

</style>