<template>

  <section class="src-components-header">
    <div id="header" :style=" this.$store.state.win ? {background : this.$store.state.pickedColor} : '' ">
      <h1>
        The Great <br>
        <span id="colorDisplay">{{this.$store.state.pickedColor != ''? this.$store.state.pickedColor : 'RGB' }} </span>
        <br>
        Guessing Game
      </h1>  
    </div>

    <Navbar />

  </section>

</template>

<script>
import Navbar from './Navbar.vue'

  export default  {
    name: 'src-components-header',
    props: [],
    components: {
      Navbar
    },
    mounted () {

    },
    data () {
      return {
    
      }
    },
    methods: {
      toggleHeader(event){
        this.win = event
      }
    },
    computed: {

    }
}


</script>

<style scoped lang="css">
  .src-components-header {

  }

   #header {
	transition: all 0.3s;
	background: steelblue;
	text-transform: uppercase;
	text-align: center;
	margin: 0;
	color: white;
  }

  #colorDisplay {
    font-size: 200%;
  }
</style>
