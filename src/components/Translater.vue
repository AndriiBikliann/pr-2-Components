<template>
   <div>
     <div>
       <h3>Перекладач</h3>
       <label>
         Українська
         <input type="text" v-model="ukrWord" placeholder="Введіть слово українською"/>
       </label>
     </div>
     
     <div>
       <button @click="getTranslateArray">TranslateArray</button><br>
       <button @click="getTranslateObj">TranslateObj</button>
     </div>
     
     <div>
       <span>Переклад: 
         {{ translateWord }}
       </span>
     </div>
   </div>
 </template>
 
 <script>
   export default {
     name : "Translater",
     data() {
       return {
         ukrWord: "",
         translateWord: "",
         translationsArray: [
         {
           en: "Hi",
           ua: "Привіт"
         },
         {
           en: "Bye",
           ua: "Допобачення"
         },
         {
           en: "Pen",
           ua: "Ручка"
         },
         ],
         translationsObj: {
           Привіт: "Hi",
           Допобачення: "Bye",
           Ручка: "Pen",
         },
       };
     },
    methods: {
       getTranslateArray() {
         const trObj = this.translationsArray.find (el => el.ua === this.ukrWord)??{}
         this.translateWord = trObj.en ?? "No word"
       },
       getTranslateObj() {
         this.translateWord = this.translationsObj[this.ukrWord] ?? "No word";
       },
    },
   };
 </script>
 
 <style lang="scss" scoped>
 </style>