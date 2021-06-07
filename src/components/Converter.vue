<template>
    <div>
     <h2> Конвертер </h2>
     <input type="number" v-model="course" placeholder="Введіть курс"> <br>
     <input type="number" v-model="grn" placeholder="Введіть гривні"> <br>
     <input type="number" :value="grn/course" placeholder="Долари">
    </div>
</template>

<script>
    export default {
        name : "Converter",
        data () {
            return {
            course: "",
            grn: ""
            }
        }
    }

</script>










<style lang="scss" scoped>
</style>