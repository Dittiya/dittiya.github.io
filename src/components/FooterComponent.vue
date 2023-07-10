<script>
async function getConfig() {
  const response = await fetch("https://raw.githubusercontent.com/Dittiya/dittiya.github.io/master/public/config.json")
  const json = response.json()
  return json
}

export default {
  data() { return { version: null } },
  created() {
    this.fetchData()
  },
  methods: {
    async fetchData() {
      const config = await getConfig()
      this.version = config.version
    }
  }
}
</script>

<template>
  <footer class="position-absolute bottom-0 start-0 end-0">
    <div class="container-flex">
      <h6 class="text-dark-emphasis">v{{ version }}</h6>
    </div>
  </footer>
</template>
