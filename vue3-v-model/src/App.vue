<template>
  <div id="app">

    <header>
      Checkbox Slider
    </header>

    <div class="container">
      <checkbox-slider />
      <span>{{ remember_password }}</span>
    </div>
    
  </div>
</template>

<script>
import CheckboxSlider from './components/CheckboxSlider.vue'

export default {

  name: 'App',

  components: { CheckboxSlider },

  data() {
    return {
      remember_password: false
    }
  }

}
</script>

<style>
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

html, body, #app {
    display: inline-block;
    width: 100%;
    height: 100%;
}

body {
    font-family: "Lato";
}

header {
    display: flex;
    width: 100%;
    background: #3d90da;
    padding: 17px;
    color: #fff;
    font-weight: bold;
}

.container {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    width: 100%;
    height: 100%;
}
</style>