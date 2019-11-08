<template>
  <div class="home">
    <img style="width:100% " src="../../image/11.png" alt="">
    <img style="width:100% " src="../../image/22.png" alt="">
    <img style="width:100% " src="../../image/33.png" alt="">
  </div>
</template>
<script>
import {mapState,mapActions,mapGetters,mapMutations} from 'vuex'
export default {

  computed:{//为一个对象
    ...mapState("user",["info",'token']),
  
  },
  created() {
    this.inFo(this.token)
  },
  methods: {
    ...mapActions('user',['inFo']),
  }
}
</script>
<style scoped>
 .home {
  height: 100%;
  position: fixed;
 }
</style>