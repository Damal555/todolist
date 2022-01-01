<template>
  <div class="">
    <input type="text" placeholder="Название задачи" value='' v-model="msg">
    <button type="submit" class="btn" v-on:click='add'>Дополнить</button>
    <ul>
      <li v-for='item in list' :key='item'>{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  data () {
    return {
            msg:"",
            list:[],
    }
  },
   methods : {
     add: function () {
       this.item=this.msg;
       this.list.push (this.item);
       this.msg='';

      console.log(this.list.length);
     }

   }
}
</script>

<style>
</style>
