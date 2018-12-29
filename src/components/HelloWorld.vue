<template>
  <div class="hello">
   <websocket/>
  </div>
</template>

<script>
import websocket from "@/components/websocket"
export default {
  name: 'HelloWorld',
  components:{
    websocket
  },
  data () {
    return {
     
    }
  },
  mounted(){
     this.$axios
        .post("http://112.64.170.158:9117/Service1.svc/HistoryThermalData")
        .then(res => {
        console.log(res)
        })
        .catch(error => {
          console.log(error);
        });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
