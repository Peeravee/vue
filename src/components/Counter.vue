<template>
<div>
  <div id="example-1">
  <button @click="upFunction" class="btn btn-primary">{{lable}}</button>

  
 

</div>
</div>
</template>

<script>
export default {
 data: function (){
     return{
    counter: 0,
    fsize:50
    }
  },
  props: {
    lable: String
  },
  methods: {
    upFunction: function () {
     this.counter+=1
      this.fsize+=10

     console.log(this.fsize);
      console.log(this.counter);

      // ส่งค่าตัวแปร counter ออกไปผ่านตัวแปร cc
      this.$emit('cc', this.counter)


   },
    downFunction: function () {
     this.counter-=1
      this.fsize-=10

      console.log(this.fsize);
      console.log(this.counter);
      }
  }
}
</script>

<style>

</style>