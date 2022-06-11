<template>
  <div class="login_container">
    <div class="login">
      <img class="mb-4" src="/logo.png" alt="logo" />
      <div class="form-control">
        <span v-if="!email" class="pl-2"
          >Telefon numarası, kullanıcı adı veya e-posta</span
        >
        <input v-model="email" type="text" />
      </div>
      <div class="form-control">
        <span v-if="!pass" class="pl-2">Şifre</span>
        <input
          v-if="!showPass"
          v-model="pass"
          type="password"
          name="pass"
          aria-label="Şifre"
        />
        <input
          v-else
          v-model="pass"
          type="text"
          name="pass"
          aria-label="Şifre"
        />
        <div class="show">
          <button @click="showPassClick">{{ goster }}</button>
        </div>
      </div>
      <button class="btn">Giriş Yap</button>
      <div class="yada">
        <div class="yada-left"></div>
        <div class="yazi">YA DA</div>
        <div class="yada-right"></div>
      </div>
      <div class="flex flex-col items-center justify-center">
        <a class="text-sm mb-2 font-semibold text-blue-900" href="#"
          >Facebook İle Giriş Yap</a
        >
        <a class="text-xs mt-2 font-light text-blue-900" href="#"
          >Şifreni mi unuttun?</a
        >
      </div>
    </div>
    <div class="kayit">
      <span>Hesabın yok mu?</span
      ><a class="text-blue-400 font-semibold" href="#">Kaydol</a>
    </div>
    <div class="my-4 text-center text-sm"><span>Uygulamayı İndir.</span></div>
    <div class="app_logo">
      <img src="/apple.png" alt="apple" /> <img src="google.png" alt="google" />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      email: null,
      pass: null,
      showPass: false,
      goster: 'Göster',
    }
  },
  methods: {
    showPassClick() {
      if (this.showPass === false) {
        this.showPass = true
        this.goster = 'Gizle'
      } else {
        this.showPass = false
        this.goster = 'Göster'
      }
    },
  },
}
</script>
<style scoped>
.login_container {
  @apply w-96 mx-auto;
}
.login {
  @apply w-96 mx-auto border border-gray-300 rounded-sm flex py-6 px-10 flex-col items-center;
}
.form-control {
  @apply flex flex-col w-full py-1 relative;
}
.form-control span {
  pointer-events: none;
  text-overflow: ellipsis;
  transform-origin: left;
  user-select: none;
  white-space: nowrap;
  font-size: 10px;
  @apply text-gray-400 absolute top-4 left-2 overflow-hidden;
}
.form-control input {
  @apply w-full px-4 py-2 border border-gray-300 rounded-md bg-gray-50;
}
.form-control input:focus .form-control span {
  @apply top-0;
}
.show {
  @apply absolute right-2 top-4 text-sm;
}
.btn {
  @apply flex mt-3 bg-blue-500 text-sm text-white w-full justify-center items-center h-8 rounded-md;
}
.yada {
  margin: 10px 40px 18px;
  @apply flex flex-row justify-center items-center mt-3 w-full h-12;
}
.yada-left,
.yada-right {
  background-color: #dbdbdb;
  background-color: rgba(var(--b38, 219, 219, 219), 1);
  -webkit-box-flex: 1;
  -webkit-flex-grow: 1;
  -ms-flex-positive: 1;
  flex-grow: 1;
  -webkit-flex-shrink: 1;
  -ms-flex-negative: 1;
  flex-shrink: 1;
  height: 1px;
  position: relative;
  top: 0.45em;
}
.yada .yazi {
  @apply px-4 text-gray-400 text-sm pt-4 font-bold;
}
.kayit {
  @apply w-96 mx-auto border border-gray-200 rounded-sm mt-6 h-16 text-sm text-gray-600 flex flex-row justify-center items-center gap-1;
}
.app_logo {
  @apply w-96 m-auto flex flex-row gap-3 items-center justify-center;
}
.app_logo {
  @apply w-32;
}
</style>
