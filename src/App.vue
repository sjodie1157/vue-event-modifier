<template>
  <div>
    <form @submit="sendInfo">
      <div>
        <label>
          Enter a value:
        </label>
        <input type="text" placeholder="Enter a value" v-model="currValue" @keyup="popUpMessage(currValue)">
      </div>
      <div>
        <h2>
          List of entered values
        </h2>
        <ul v-show="listOfValues.length">
          <li v-for="data, index in listOfValues" :key="index">
            <p>{{ data }} @ position {{ index }}</p>
          </li>
        </ul>
      </div>
      <button type="submit">Display</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
