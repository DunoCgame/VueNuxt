<template>
	<div>
		<Posts
			v-for="post of posts"
			:key="post.id"
			:id="post.id"
			:name="post.name"
			:content="post.content"
		/>
	
	
		<p>
			"Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum."
		</p>
	</div>
</template>

<script>

import axios from "axios";
import Posts from "@/components/Posts";

export default{
		name:"Contenido",
		data() {
			return {
			  posts:[]
			};
		  },
		  async created(){
				const res = await axios.get(
				  "https://jsonplaceholder.typicode.com/comments"
				);
			this.posts = res.data;
		  }
};
</script>
