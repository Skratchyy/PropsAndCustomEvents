<template>
  <section>
    <div id="user-Data">
  <user-data v-on:change-name="changeUserName"
             v-on:change-age="changeUserAge"
  ></user-data>
    </div>
    <div>
  <active-user :usr-name="currentName"
               :usr-age="currentAge"
  ></active-user>
    </div>
  </section>
</template>

<script>
export default {
  data(){
    return {
      currentName: 'Skratchyy',
      currentAge: '19'
    }
  },
  methods: {
    changeUserName(newName){
      this.currentName = newName
    },
    changeUserAge(newAge){
      this.currentAge = newAge
    }
  }
}
</script>


<style>
*{
  font-family: Arial;
  margin: 0;
  color: #333;
}
section {
  width: 50%;
  margin: 3rem auto;
  display: flex;
  justify-content: center;
}

#inputs {
  display: inline-grid;
}
#input{
  width: 60%;
  display: inline;
  margin: 1rem;
}
#useractive{
  margin: 1rem;
}
#useractive h2{
  margin-top: 20px;
  margin-bottom: 3.5rem;
}
</style>