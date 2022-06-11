<template>
  <div
    class="w-11/12 m-auto border border-gray-400 rounded-md h-96 mt-24 mb-6 py-6 px-16 text-gray-600"
  >
    <h1 class="border-b border-gray-200 mb-6">
      Girmiş olduğunuz bilgiler aşağıdadır.
    </h1>
    <div>
      <p>
        <span class="mr-4">Email:</span
        ><span class="text-red-600">{{ this.$route.query.email }}</span>
      </p>
      <p>
        <span class="mr-4">Şifre:</span
        ><span class="text-red-600">{{ this.$route.query.pass }}</span>
      </p>
      <p class="mt-32 text-sm font-light">
        Bu bilgiler her hangi bir yerde saklanmamaktadır. Sadece bilgilendirme
        amaçlı kurulan bir sistemdir.
      </p>
      <p class="mt-4 text-gray-300 font-thin text-sm">
        <a href="https://akgngr.com">akgngr</a>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InstagramSonuc',
  mounted() {
    // eslint-disable-next-line no-unused-expressions
    console.log(this.$route.query)
  },
}
</script>
