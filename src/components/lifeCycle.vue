<template>
  <div>
{{count}}
  </div>
  <h1>텍스트</h1>
</template>

<script>
export default{
  data(){
    return {
      count: 0,
    }
  },
  beforeCreate(){
    console.log('beforeCreate', this.count);
    //beforeCreate undefined
  },
  created(){
    console.log('create', this.count);
// create 0
  },
  beforeMount(){
  console.log('beforeMount', document.querySelector('h1'));
  },  
  mounted(){
  console.log('mounted', document.querySelector('h1'));
  },
  methods(){
   test(
    console.log('test')
   )
   },
  }

</script>

<style lang="scss" scoped>

</style>