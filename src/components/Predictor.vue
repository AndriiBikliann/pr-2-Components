<template>
    <div>
      
      <div>
        <button @click="getPrediction"> Натисніть для передбачення </button>
      </div>
      <div> <span> Ваше передбачення : {{ yourPrediction }} </span> </div>
    
    </div>
</template>

<script>
    export default {
        name : "Predictor",
        data (){
           return {
               yourPrediction: null,
               predictionArr: [
                 "Увас буде хороший день!",
                 "Вам сьогодні пощастить",
                 "Бурні річки тихо течуть",
                 "Іноді краще жувати",
               ]
           };
        },
        methods : {
            getRandom (min, max){
              return min + Math.floor(Math.random)* (max - min + 1)
            },
            getPrediction () {
              const randIndex = this.getRandom(0, this.predictionArr.length-1)
              this.yourPrediction = this.predictionArr[randIndex];
            },
        },
    };
</script>

<style lang="scss" scoped>

</style>