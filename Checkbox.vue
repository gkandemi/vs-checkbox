<template>
  <div>
    <label class="checkbox">
      <input
        v-model="status"
        type="checkbox">
      <span class="checkbox" :class="checkboxMainClass">
        <span :class="checkboxToggleClass"></span>
    </span>
      <span class="text" v-if="text" :class="checkboxTextClass">
        {{ text }}
    </span>
    </label>
  </div>
</template>
<script>
  export default {
    props: [
      "value", "text","color"
    ],
    data() {
      return {
        status: false
      }
    },
    created() {
      this.status = this.value;
    },
    watch: {
      status(value) {
        this.$emit("input", value);
      }
    },
    computed : {
      checkboxMainClass(){
        if(this.color != null && this.status){
          return this.color;
        }
      },
      checkboxToggleClass(){
        if(this.color != null && this.status){
          return this.color + "-toggle";
        }
      },
      checkboxTextClass(){
        if(this.color != null && this.status){
          return this.color + "-text-color";
        }
      },

    }
  }
</script>
<style scoped>
  label.checkbox input {
    position: absolute;
    left: -9999px;
  }

  label.checkbox .text {
    font: 12px/14px sans-serif;
    color: #666;
    position: relative;
    top: -3px;
    padding-left: 10px;
  }

  label.checkbox .checkbox {
    display: inline-block;
    width: 36px;
    height: 14px;
    border-radius: 14px;
    background: rgba(0, 0, 0, .26);
    position: relative;
    transition: 300ms background;
  }

  label.checkbox .checkbox span {
    width: 20px;
    height: 20px;
    position: absolute;
    top: -3px;
    left: 0;
    background: #fff;
    box-shadow: 0 1px 5px 0 rgba(0, 0, 0, .4);
    border-radius: 50%;
    transition: 300ms left, background;
  }

  label.checkbox input:checked + .checkbox {
    background: #83b1f4;
  }

  label.checkbox input:checked + .checkbox span {
    background: #4285f4;
    left: 16px;
  }

  label.checkbox input:checked + .checkbox + .text {
    color: #4285f4;
  }

  .success{
    background-color: #D5EDDB!important;
  }
  .success-toggle{
    background-color: #27a043 !important;
  }
  .success-text-color{
    color: #155724!important;
  }

  .primary{
    background-color: #cce5ff!important;
  }
  .primary-toggle{
    background-color: #0055ca !important;
  }
  .primary-text-color{
    color: #004085!important;
  }

  .secondary{
    background-color: #e2e3e5!important;
  }
  .secondary-toggle{
    background-color: #525f63 !important;
  }
  .secondary-text-color{
    color: #383d41!important;
  }

  .info{
    background-color: #d1ecf1!important;
  }
  .info-toggle{
    background-color: #0d7d8a !important;
  }
  .info-text-color{
    color: #0c5460!important;
  }
  .warning{
    background-color: #fff3cd!important;
  }
  .warning-toggle{
    background-color: #bd9804 !important;
  }
  .warning-text-color{
    color: #856404!important;
  }
  .danger{
    background-color: #f8d7da!important;
  }
  .danger-toggle{
    background-color: #b02333 !important;
  }
  .danger-text-color{
    color: #721c24!important;
  }
</style>
