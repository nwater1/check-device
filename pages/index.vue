<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        check-device
      </h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {


  mounted () {
    this.chooseDevice()
  },

  methods: {
    chooseDevice () {
      if ((this.url === 'smartphone' && this.deviceType === 'iPhone') || (this.url === 'smartphone' && this.deviceType === 'iPad')) {
        window.location.href = 'www.google.com';
      } if (this.url === 'pc') {
        return 'https://page.line.me/?accountId=002sjkcf&openerPlatform=native&openerKey=talkroom:header'
      } if (this.url === 'smartphone' && this.deviceType === 'Android') {
        window.location.href = 'www.google.com';
    }
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
