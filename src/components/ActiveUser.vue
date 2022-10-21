<template>
  <div id="useractive">
    <h2>{{usrName}}</h2>
    <h3>{{usrAge}}</h3>
  </div>
</template>

<script>
export default {
  props: {
    usrName: {
      type: String,
      required: true
    },
    usrAge: {
      type: String,
      required: true
    }
  }
}
</script>