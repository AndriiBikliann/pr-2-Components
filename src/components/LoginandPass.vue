<template>
  <div>
    <label>
      Введіть логін
    <input type="text" v-model="userLogin">
    </label> <br>
    <label>
      Введіть пароль
    <input type="password" v-model="userPass">
    </label> <br>
    <button @click="checkPass">Go</button>
    <span>
      {{authResultMessage}}
    </span>
  </div>
</template>

<script>
export default {
  name: 'LoginandPass',
  data() {
    return {
      userLogin:"",
      userPass :"",
      authResultMessage: null,
      loginBase : [
        {
          login: "Ivan", 
          pass:"111"
          },
        {
          login: "Petro", 
          pass:"222"
          },
        {
          login: "Roma", 
          pass:"333"
          },
        {
          login: "Stas", 
          pass:"444"
          },
      ],
    };
  },
  methods: {
    checkPass() {
      if (
        this.loginBase.some(
          (item) => this.userLogin == item.login && this.userPass == item.pass
        )
      )
      this.authResultMessage = "Вітаємо!"
      else this.authResultMessage = "Некоректний логін або пароль!"
    },
  },
};

</script>


<style scoped> </style>
