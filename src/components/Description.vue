<template>
<div>
  <h2>I'm Remarkable because</h2>
  <p>{{ Remarkable }}</p>
  <p class="name">{{ Name }}</p>
</div>
</template>

<script>
//import axios from "axios";

export default {
  name: "Description",

  data() {
    return {
      Remarkable: null,
      Name: null,
      Country: null
    };
  },
  mounted() {
    this.Remarkable = localStorage.getItem("remarkable"),
      this.Country = localStorage.getItem("country"),
      this.Name = localStorage.getItem("name")
  }
};
</script>

<style scoped>
p {
	font-family: 'Roboto Slab';
	font-size: 1rem;
	text-align: left;
	font-weight: bold;
	margin: 10px 0;
}
h2 {
	margin: 10px 0;
}


.name {
	font-weight: normal;
	font-family: 'Sacramento', cursive;
  color: #9C895D;
  font-size: 1.3em;
  top: 10px;
}
</style>
