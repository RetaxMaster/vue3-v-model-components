<template>
  <div class="checkbox-slider">
      <input :value="modelValue" @change="changeValue" type="checkbox" id="my-slider">
      <label for="my-slider">Recordar contraseña</label>
  </div>
</template>

<script>
export default {

    name: 'CheckboxSlider',

    props: {
        modelValue: {
            type: Boolean,
            required: true
        }
    },

    methods: {

        changeValue() {
            this.$emit("update:modelValue", !this.modelValue)
        }

    }

}
</script>

<style scoped>
/* Checkbox Slider */

.checkbox-slider input {
    display: none;
}

.checkbox-slider label {
    position: relative;
    cursor: pointer;
}

.checkbox-slider label:after {
    content: '';
    display: inline-block;
    width: 11px;
    height: 11px;
    position: absolute;
    top: 3px;
    left: calc(100% + 9px);
    /*Porahora*/background: #fff;
    border-radius: 20px;
    transition: 0.2s all ease;
    -webkit-border-radius: 20px;
    -moz-border-radius: 20px;
    -ms-border-radius: 20px;
    -o-border-radius: 20px;
    -webkit-transition: 0.2s all ease;
    -moz-transition: 0.2s all ease;
    -ms-transition: 0.2s all ease;
    -o-transition: 0.2s all ease;
}

.checkbox-slider label:before {
    content: '';
    display: inline-block;
    width: 30px;
    height: 17px;
    position: absolute;
    left: calc(100% + 5px);
    background: #ccc;
    border-radius: 20px;
    transition: 0.2s all ease;
    -moz-border-radius: 20px;
    -ms-border-radius: 20px;
    -o-border-radius: 20px;
    -webkit-transition: 0.2s all ease;
    -moz-transition: 0.2s all ease;
    -ms-transition: 0.2s all ease;
    -o-transition: 0.2s all ease;
}

.checkbox-slider input:checked + label:after {
    left: calc(100% + 20px);
}

.checkbox-slider input:checked + label:before {
    background: #3d90da;
}

/* ->Checkbox Slider */
</style>
