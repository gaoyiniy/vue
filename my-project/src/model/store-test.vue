<template>
  <div class="store-test">{{count}}</div>
</template>
<script>
    export default{
        name: "store-test",
        computed:{
            count(){
                return this.$store.state.count
            }
        },
    }
</script>