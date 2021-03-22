<template>
  <nuxt-link :to="'/posts/' + id">
    <div class="post">
      <p>{{id}}. {{name}}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Post",
  props: ["id", "name"]
};
</script>

<style>
.post{
  background: #2d3436;
  padding: 1rem;
  border: 1px solid whitesmoke;
  margin: 0px;
}

.post:hover{

  border: 1px solid #6c5ce7;
  cursor: pointer;
}
a{
  color: whitesmoke;
}

a:hover{
  color: #6c5ce7;
}
</style>
