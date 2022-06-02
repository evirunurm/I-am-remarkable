<template>
<div class="containerlandpage">
  <Header />
  <div class="main_title_pg_01">
    #IamRemarkable is a Google initiative empowering women and other underrepresented groups to celebrate their achievements in the workplace and beyond.
  </div>

  <div class="main-center-1">
    <p class="main_message_pg_01"> Tell to the World,</p>
    <img class="main_pic_flecha_pg_01" src="../images/Vector_flecha.svg" alt="" />

    <router-link to="/Formulario" class="btn-01">
      Why are you remarkable?
    </router-link>
  </div>

  <div class="all">
    <img class="main_pic_allPeople_pg_01" src="../images/allPeople.png" />
  </div>
</div>
</template>

<script>
import Header from "@/components/Header.vue";

export default {
  name: "Home",
  components: {
    Header,
  }
};
</script>

<style scoped>

body {
  box-sizing: content-box;
  width: 100%;
  color: #202124;
  font-family: 'Roboto', sans-serif;
  margin: 0px;
  box-sizing: border-box;
  padding: 0px;
}

.containerlandpage {
  box-sizing: border-box;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  background: radial-gradient(112.66% 58.05% at 48.31% -1.3%, rgba(255, 255, 255, 0.54) 16.78%, rgba(174, 200, 207, 0100) 82.33%),
    linear-gradient(0deg, #AEC8CF, #AEC8CF);
  overflow-x: hidden;
  height: 100vh;
}

header {
  width: 100%;
  max-width: 250px;
  margin-top: 90px;
  padding-bottom: 30px;
}

.header_logo {
  width: 100%;
  max-width: 240px;
}

.main_title_pg_01 {
  width: 80%;
  max-width: 1024px;
  padding-left: 10%;
  padding-right: 10%;
  color: rgb(35, 35, 34);
  text-align: center;
  font-weight: 800;
  font-family: 'Roboto Slab';
  font-style: 'Regular';
  font-size: 1em;
  line-height: auto;
}

.main-center-1 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top: 20px;
}

.main_message_pg_01 {
  pointer-events: none;
  color: #9C895D;
  font-size: 1.4em;
  text-align: center;
  font-family: 'Roboto Slab';
  font-weight: 800;
  margin-bottom: 20px;
  margin-right: 50px;
  letter-spacing: 1px;
  ;
}

.main_pic_flecha_pg_01 {
  pointer-events: none;
  align-self: center;
  position: static;
  margin-top: -74px;
  margin-right: -262px;
}

.btn-01 {
  color: aliceblue;
  background: rgba(26, 33, 58, 1);
  border-radius: 40px;
  width: 450px;
  padding: 13px;
  margin-top: -20px;
  font-size: 1.1em;
  font-family: 'Roboto Slab';
  text-align: center;
  text-decoration: none;
  max-width: 250px;
}

.btn-01:hover {
  background: rgba(26, 33, 58, 0.11);
  color: rgba(26, 33, 58, 1);
  font-weight: bold;
  transition: ease-in 0.2s;
}


.main_pic_allPeople_pg_01 {
  width: 100%;
  max-width: 996px;
  max-height: 980px;
}

.main-center-1 {
	margin-top: 50px;
	margin-bottom: 80px;
}

.btn-01 {
	margin-top: 50px;
}



</style>
