<template>
  <DialogCard title="Login" :actions="actions">
    <v-text-field label="Username" icon="person" v-model="username"/>
    <v-text-field label="Password" icon="lock" v-model="password"/>
  </DialogCard>
</template>
<script>
export default {
  // overlay: 'default',
  //   asyncData () {
  //         return new Promise(resolve => {
  //           setTimeout(resolve, 3000)
  //         })
  // },
  data () {
    return {
      username: '',
      password: ''
    }
  },
  computed: {
    actions () {
      return {
        login: {
          flat: true,
          text: 'Login',
         handle: () => {
           return new Promise(resolve => {
            setTimeout(resolve, 3000)
            })
          }
        }
      }
    }
  }
}
</script>
