<template>
  <div class="home">
    <h1>helloWorld</h1>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
    
  },
  data(){
    return {
      loading: true,
      title: 'Global',
      dataDate: '',
      status: '',
      countries: [],
      loadingImage: require('../assets/hourglass.gif')
    }
  },
  methods:{
    async fetchCovidData(){
      const res = await fetch('https://api.covid19api.com/summary')
      const data = await res.json()
      return data;
    }
  },
  async created(){
    const data = await this.fetchCovidData();
    console.log(data );
  }
}
</script>
