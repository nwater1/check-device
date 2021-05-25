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

  async created () {
    await inappcheck ()
  },

  methods: {
    inappcheck () {
        // const path = 'github.com/donma/'
        const path = 'www.google.com'
        // https://line.me/ti/p/~@dhamma1000000
        // https://lin.ee/Jqdw87d

        // 如果是 LINE
        // if (navigator.userAgent.includes('Line')) {
        //  location.href = 'https://' + path + '?' + 'openExternalBrowser=1'
        // eslint-disable-next-line brace-style
        // }

        // 如果是 facebook
        //if (navigator.userAgent.includes('FBAV') || navigator.userAgent.includes('FBAN')) {
          // 如果是 Android App
          if (navigator.userAgent.includes('Android')) {
            location.href = 'intent:https://' + path + '#Intent;action=android.intent.action.VIEW;category=android.intent.category.BROWSABLE;component=com.android.browser/com.android.browser.BrowserActivity;end'
            setTimeout(function () {
              location.href = 'intent:https://' + path + '#Intent;action=android.intent.action.VIEW;category=android.intent.category.BROWSABLE;component=com.android.browser/com.android.browser.BrowserActivity;end'
            }, 500)
            // 如果是 IOS APP
          } else if (navigator.platform.match(/iPhone|iPod|iPad/)) {
            document.write('safari or Chrome')
            // location.href = 'googlechromes://' + path
          // location.href = 'safari-https://' + path
          } else {
            location.href = 'https://' + 'www.gmail.com'
          }
        //}
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
