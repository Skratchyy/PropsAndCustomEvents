<template>
  <div id="inputs">
    <div id="input">
      <label>Username</label>
      <input type="text" v-model="newName" @input="changeName">
    </div>
    <div id="input">
      <label>Age</label>
      <input type="text" v-model="newAge" @input="changeAge">
    </div>
  </div>
</template>

<script>
export default {
  emits: ['change-name', 'change-age'],
  data(){
    return {
      newName: '',
      newAge: ''
    }
  },
  methods: {
    changeName(){
      this.$emit('change-name', this.newName);
    },
    changeAge(){
      this.$emit('change-age', this.newAge);
    }
  }
}
</script>