<template>
  <div>
    <div v-if="loading">
      <p>Loading...</p>
    </div>
    <div v-else>
      <p class="joke">{{ joke }}</p>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  data() {
    return {
      message: 'My new tab page',
      joke: '',
    };
  },

  mounted() {
    axios.get('https://icanhazdadjoke.com/', { headers: { Accept: 'application/json' } }).then(res => {
      this.joke = res.data.joke;
      this.loading = false;
    });
  },
};
</script>

<style scoped>
p {
  font-size: 20px;
}
body {
  height: 98vh;
  text-align: center;
  color: #353638;
  font-size: 22px;
  line-height: 30px;
  font-family: Merriweather, Georgia, serif;
  background-size: 200px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.joke {
  max-width: 800px;
}
</style>
