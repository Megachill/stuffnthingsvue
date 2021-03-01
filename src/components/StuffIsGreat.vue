<template>

  <div>

    <h3 v-if="bStuffIsHappening">
      Stuff is happening...
    </h3>

    <h3 v-if="!bStuffIsHappening">
      Nothings happening...
    </h3>

    <p>Email: {{ form.email }}</p>

    <form>
      <div>
        <label for="email">EMail</label>
        <input type="text" id="email" v-model="form.email" placeholder="your email">
      </div>

      <div>
        <label for="password">Password</label>
        <input type="password" id="password" v-model="form.password" placeholder="password plx">
      </div>
    </form>

  </div>

</template>
<script>
export default {
  name: "stuffisgreat",
  data() {
    return {
      bStuffIsHappening: true,
      form: {
        email: '',
        password: '',
      }
    }
  },
}
</script>
