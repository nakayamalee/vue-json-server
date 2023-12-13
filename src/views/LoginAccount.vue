<script>

export default {
  data() {
    return {
      userData: {
        email: '',
        password: '',
      },
    };
  },
  methods: {
    submitData() {
      console.log('fire');
      // fetch('http://localhost:3000/login', {
      //   method: 'POST',
      //   headers: {
      //     'Accept': 'application/json',
      //     'Content-Type': 'application/json',
      //   },
      //   body: JSON.stringify({ ...this.userData }),
      // })
      //   .then(res => res.json())
      //   .then(data => {
      //     sessionStorage.setItem('accessToken', data.accessToken);
      //   })
    },
  },
};
</script>

<template>
  <section id="register">
    <form class="flex flex-col gap-3" @submit.prevent="submitData()">
      <label>
        帳號:
        <input v-model="userData.email" type="email" name="email" required>
      </label>
      <label>
        密碼:
        <input v-model="userData.password" type="password" name="password" required>
      </label>
      <div class="btns">
        <button type="submit">登入</button>
        <button type="">返回</button>
      </div>
    </form>
  </section>
</template>

<style lang="scss" scoped>
#register {
  .btns {
    @apply flex gap-3;
  }
  input {
    @apply text-black;
  }
}
</style>