<template>
  <div class="logout">
    <button @click="logout">ログアウト</button>
  </div>
</template>

<script>
import firebase from '~/plugins/firebase'
export default {
  methods: {
    logout() {
      firebase
        .auth()
        .signOut()
        .then(() => {
          // alert('ログアウトが完了しました')
          this.$router.replace('/')
        })
    },
  },
}
</script>