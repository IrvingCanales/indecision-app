<template>
  <div>
      <h1>Let the computer helps to you</h1>
      
      <input v-model="option" placeholder="Enter option">
      <button  v-on:click="addOption()" >Add</button>
      <ul id="example-1">
            <li v-for="item in options" v-bind:key="item">
                {{ item }}
            </li>
        </ul>
  </div>
</template>

<script>
export default {
    data: function(){
      return {
          option: '',
          options: []
      }
    },
    methods:{
        addOption(){
            
            if(this.options.indexOf(this.option)>-1)
                alert('This already exists');
            else{
                this.options.push(this.option);                
            }

            this.option=''
            
        }
    },
}
</script>

<style>

</style>