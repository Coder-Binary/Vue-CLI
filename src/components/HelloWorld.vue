<template>
  <h1>{{ msg }}</h1>
  <button @click="cache">count is: {{ count }}</button>
  <p v-if="show">Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      count:0,
      user_name:null,
      show:true
    }
  },
methods:{
    cache:function(){
      console.log("cache");
      this.show = !this.show;
    }
  },
  beforeCreate(){
    console.log("beforeCreate");
  },
  created(){
    console.log("Create");
  },
  beforeMount(){
    console.log("beforeMount");
  },
  mounted(){
    console.log("mounted");
  },
  beforeUpdate(){
    console.log("BeforeUpdate");
  },
  updated(){
    console.log("Update");
  },
  beforeUnmount(){
    console.log("beforeDestroy");
  },
  unmounted(){
    conole.log("destroyed");
  }
}
</script>
