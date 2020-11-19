<template>
  <v-form ref="form" v-model="valid" lazy-validation>
    <v-container class="grey lighten-5">
      <v-card class="input-container">
        <v-text-field
          v-model="locations"
          placeholder="Locations"
          :rules="locationRules"
          required
          content-class="custom-input"
        ></v-text-field>
        <v-text-field
          v-model="productionAccountant"
          placeholder="Production Accountant"
          required
        ></v-text-field>
        <v-text-field
          v-model="scriptPages"
          placeholder="Script Pages"
          required
        ></v-text-field>
        <v-text-field
          v-model="ScriptScenes"
          placeholder="Script Scenes"
          required
        ></v-text-field>
        <v-text-field
          v-model="totalMinutes"
          placeholder="Total Minutes"
          :rules="locationRules"
          required
          content-class="custom-input"
        ></v-text-field>
        <v-text-field
          v-model="prep"
          placeholder="Prep (Weeks)"
          required
        ></v-text-field>
        <v-text-field
          v-model="wrap"
          placeholder="Wrap (Weeks)"
          required
        ></v-text-field>
        <v-text-field
          v-model="shoot"
          placeholder="Shoot (Weeks)"
          required
        ></v-text-field>
      </v-card>
    </v-container>
  </v-form>
</template>

<script>
export default {
  name: "VuetifyTest",
  data: () => ({
    locations: "",
    locationRules: [
      (v) => !!v || "Location is required",
      (v) =>
        (v && v.length <= 10) || "Location must be less than 10 characters",
    ],
    productionAccountant: "",
    totalMinutes: "",
    prep: "",
    wrap: "",
    shoot: "",
    ScriptPages: "",
    ScriptScenes: "",
    valid: true,
  }),
  props: {
    msg: String,
  },
};
</script>

<style  lang="scss">
// @import "../global.scss";

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

input {
  background-color: rgba(211, 211, 211, 0.829);
  outline: none;
  border: none;
  border-radius: 2px;
  height: 6vh;
  padding: 0 0.6vw;
  width: 40vw;
  margin: 2vh 2vw;
}
.input-container {
  display: flex;
  flex-wrap: wrap;
  padding: 2vh 2vw;
}
</style>
