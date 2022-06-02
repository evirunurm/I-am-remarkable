<template>
<section class="main-2">
<div class="main-origen-2">
	<div class="main-principal-02">
		<img class="flecha02" src="../images/2flechita.png">
		<img class="estrellitas02" src="../images/estrellas3.png">
		<input  class="main-alias-2" type="text" maxlength="10" placeholder="Name / Alias" size="10">
	</div>
	<SelectCountries/>
	<div class="main-why-2">
		<textarea class="main-input-2" name="textarea" rows="4" minlength="10" size="4" maxlength="200" placeholder="I am remarkable because..."></textarea>
		<p>Max 200 caracters</p>
	</div>
</div>
	<div class="final02">
		<img class="estrellas1" src="../images/2conjuntoestrellas.png">
		<img class="corona2" src="../images/2corona.png">
		<router-link @click="dataLocal" class="button-send-2" to="/Usuario">    Share    </router-link>
	</div>

  </section>
</template>
<script>
    import SelectCountries from '@/components/Form/SelectCountries.vue'
    
    export default {
        name: 'Register',
        components:{
            SelectCountries,
        },
        data() {
            return {
                name: "",
                remarkable: ""
            }
        },
        mounted() {
            this.name = localStorage.name;
            this.remarkable = localStorage.remarkable;
        },
        methods:{
            dataLocal() {
                localStorage.name = this.name;
                localStorage.remarkable = this.remarkable;
                console.log(localStorage);
                           }
        }
    }
</script>


<style>
.container02 {
  box-sizing: border-box;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: radial-gradient(58% 33.05% at top center, rgba(255, 255, 255, 0.94) 46.78%, rgba(135, 237, 255, 0) 102.33%),
    linear-gradient(0deg, #DDE9ED, #DDE9ED);
  overflow-x: hidden;
}

.corner {
  position: absolute;
  top: 0px;
  left: 0px;
}

.header_logo-2 {
  color: #202124;
  font-family: 'Raleway', sans-serif;
  border-radius: 25px;
  text-shadow: gainsboro;
}

.header-message:hover {
  color: royalblue;
}

.main-2 {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 90vw;
  height: 90vh;
  font-size: 10px;
  position: relative;
}

.main-origen-2 {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 5px;
  justify-content: flex-start;
  width: 100%;
  max-width: 500px;
}

.main-principal-02 {
  display: flex;
  flex-direction: column;
  align-items: center;
  box-sizing: border-box;
  position: relative;
  width: 100%;
}

.flecha02 {
  position: absolute;
  right: -7%;
}

.estrellitas02 {
  	position: absolute;
	top: -50%;
}

.main-alias-2 {
  outline: none;
  z-index: 3;
  box-shadow: inset 0px 4px 6px 0px grey,
    0px 2px 3px 0px rgb(255, 255, 255, 0.5);
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
  border-radius: 25px;
  width: 100%;
  /*max-width: 277px;*/
  height: 40px;
  border: none;
  margin-bottom: 25px;
  margin-top: 30px;
  background: rgba(212, 230, 236, 1);
  padding-left: 20px;
  font-size: 14px;
}

.select {
  position: relative;
  box-shadow: inset 0px 4px 6px 0px grey, 0px 2px 3px 0px rgb(255 255 255 / 50%);
  width: 100%;
  height: 44px;
  padding-left: 20px;
  margin-bottom: 25px;
  border: none;
  border-radius: 25px;
  background: rgba(212, 230, 236, 1);
  display: flex;
  align-items: center;
  box-sizing: border-box;
}

/* Reset Select */
select {
  -webkit-appearance: none;
  -moz-appearance: none;
  -ms-appearance: none;
  appearance: none;
  width: 80%;
  background: none;
  border: none;
  outline: none;
  font-size: 1.5em;
}

/* Remove IE arrow */
select::-ms-expand {
  display: none;
}

/* Custom Select */
/* Arrow */
.select::after {
  content: '\25BC';
  position: absolute;
  width: 5.5em;
  height: 100%;
  top: 0;
  right: 0;
  cursor: pointer;
  pointer-events: none;
  display: flex;
  justify-content: center;
  align-items: center;
  -webkit-transition: .25s all ease;
  -o-transition: .25s all ease;
  transition: .25s all ease;
  background-color: rgb(174 190 196 / 42%);
  border-radius: 0px 20px 20px 0px;
}

/* Transition */
.main-country-2:hover::after {
  color: #000000;
}

.main-why-2 {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.main-input-2 {
  outline: none;
  box-sizing: border-box;
  height: 240px;
  border-radius: 25px;
  border: none;
  background: rgba(212, 230, 236, 1);
  box-shadow: inset 0px 2px 6px 0px grey,
    0px 2px 3px 0px rgb(255, 255, 255, 0.5);
  margin-bottom: 10px;
  padding-left: 20px;
  padding-top: 30px;
}

p {
  font-size: 14px;
  float: right;
  align-self: flex-end;
  color: #969696;
  margin: 0
}

input::placeholder {
  margin-left: 20px;
  color: black;
  font-family: 'Roboto Slab';
  font-weight: 800;
}

textarea::placeholder {
  color: black;
  font-family: 'Roboto Slab';
  font-weight: 800;
  resize: none;
}

select {
  color: rgb(0, 0, 0);
  font-family: 'Roboto Slab';
  font-weight: 800;
}

.final02 {
  flex-direction: column;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  width: 100%;
  max-width: 500px;
}

.corona2 {
  max-width: 100px;
	margin-left: 50%;
}

.esterllas1 {
  width: 100%;
  max-width: 328px;
  position: absolute;
}

/*** ESTILOS BOTÓN  ***/
a.button-send-2 {
  background: #0D0C2F;
  color: #fff;
  border: 2px solid #0D0C2F;
  position: relative;
  z-index: 1;
  overflow: hidden;
  display: inline-block;
  text-decoration: none;
  height: 51px;
  font-size: 20px;
  border-radius: 7px 20px 37px 36px;
  text-align: center;
  width: 257px;
  padding: 15px 0 0 0;
}

a.button-send-2:hover {
  	color: #0D0C2F;
	font-weight: bold;
}

a.button-send-2::after {
  content: "";
  background: #fff;
  /* color de fondo hover */
  position: absolute;
  z-index: -1;
  padding: 5px;
  display: block;
  left: -20%;
  right: -20%;
  top: 0;
  bottom: 0;
  transform: skewX(-45deg) scale(0, 1);
  transition: all 0.3s ease;
}

a.button-send-2:hover::after {
  transition: all 0.3s ease-out;
  transform: skewX(-45deg) scale(1, 1);
}
</style>