<template>
  <div class="container">
    
  </div>
</template>

<script>
export default {
  data () {
    return {
      alink: true,
      url: '',
      deviceType: ''
    }
  },

  mounted () {
    this.url = this.$ua.deviceType()
    this.deviceType = this.$ua.os()
    this.chooseDevice()
  },

  methods: {
    chooseDevice () {
      if ((this.url === 'smartphone' && this.deviceType === 'iPhone') || (this.url === 'smartphone' && this.deviceType === 'iPad')) {
        window.location.href = 'https://liff.line.me/1656026908-31A2jyx9';
      } if (this.url === 'pc') {
        return 'https://liff.line.me/1656023598-jbmRQA1P'
      } if (this.url === 'smartphone' && this.deviceType === 'Android') {
        window.location.href = 'https://liff.line.me/1656023598-jbmRQA1P';
    }
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
