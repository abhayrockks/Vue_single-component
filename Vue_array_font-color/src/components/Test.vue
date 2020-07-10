<template>
  <div id="testing">
    <div v-bind:style="{color: color_value.color}">{{name}}</div>
    <br />
    <input type="text" v-model="name" />
    <button v-on:click="del">Clear</button>
    <button @click="makeCapital">Caps</button>
    <br />
    <br />
    <select v-model="color_value">
      <option v-for="(col, index) in colors" v-bind:key="index" v-bind:value="{color: col}">{{col}}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Test",
  data: function() {
    return {
      name: "abhay",
      date: false,
      colors: ["red", "yellow", "black", "orange"],
      color_value: {
        color: "black"
      }
    };
  },
  methods: {
    del: function() {
      this.name = "";
    },
    makeCapital: function() {
      this.name = this.name.toUpperCase();
    }
  }
};
</script>

<style>
</style>
