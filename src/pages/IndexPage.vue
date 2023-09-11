<template>
  <q-page class="flex flex-center">
     <form
        class="form-submit"
        @submit.prevent="login"
      >

      <div class="logo">
        <img src="https://convicti.com.br/assets/images/r_footer-logo.webp" />

      </div>
      <label class="white label-form">E-mail</label>
      <div class="input-form">

        <q-input
          color="secondary"
          bg-color="white"
          v-model="form.email"
          autocomplete="true"
          filled
          placeholder="admin@admin"
        />
      </div>
      <label class="white label-form">Password</label>
      <div class="input-form">

        <q-input
          color="secondary"
          bg-color="white"
          v-model="form.password"
          autocomplete="true"
          filled
          placeholder="admin@admin"
        />
      </div>

      <q-btn
        color='bg-secondary'
        label="Entrar"
        class="full-width bg-secondary button-submit"
        type="submit"
      />

     </form>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  email: '',
  password: '',
})

</script>

<style>
.form-submit{
  max-width:556px;
  width:100%;
  display:flex;
  flex-direction: column;
  gap:16px;
}

.logo{
  display:flex;
  align-items: center;
  justify-content: center;
}

.logo img {
  width:70%;
  margin-bottom:120px;
}

.label-form {

    color:white;
    font-size:18px;

}

.button-submit{
  height:50px;
  margin-top:16px;
}



</style>
