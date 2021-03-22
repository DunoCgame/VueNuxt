<template>
  <header class="header">



	<b-navbar type="dark" variant="dark">
	 <!-- Image and text -->
	  <b-navbar variant="faded" type="light">
		<b-navbar-brand href="#">
		  <img src="@/assets/logo.png"  width="30px" heigth="30px"class="d-inline-block align-top" alt="Kitten">
			NuxtWeb
		</b-navbar-brand>
	  </b-navbar>
  
  
  
	  <b-navbar type="dark" variant="dark">
	  
		<b-nav-form @submit.prevent="onSubmit" method="Post" action="From">
		
			<b-form-input id="DataInput" v-model="Search"  class="mr-sm-2" placeholder="Search" ></b-form-input>
		 
			<b-button variant="outline-success" class="my-2 my-sm-0" type="submit" value="Enviar" >Search</b-button>
		
		</b-nav-form>
		
		
	  </b-navbar>
  
  
  
		<b-navbar-nav class="ml-auto">
			<b-nav-item to="/" exact>Home</b-nav-item>
			<b-nav-item to="/about">About</b-nav-item>
			<b-nav-item to="/posts">Posts</b-nav-item>
		</b-navbar-nav>
		
		
		<button @click="showButton"  >click</button>
  </b-navbar>


	
  </header>
</template>

<script>
export default{	
  name:'Navigation',
  data(){
	return{
		Search:null
	} 
  },
  methods:{
	onSubmit(){
			alert(this.Search);
			
			console.log(this.Search);
      }, 
	  showButton(){
				alert("hola");
			}
			
  
  
  }
  
  
}
</script>

<style>
.nuxt-link-exact-active{
	

	font-size:20px;
	
	color:white !important;
	
}
</style>