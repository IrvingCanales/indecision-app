<template>
  <div>
      <h1>Let the computer help you choose</h1>
      
      <input v-model="option" placeholder="Enter option">
      <button  v-on:click="addOption()" >Add</button>
      <ul id="options">
            <li v-for="item in options" v-bind:key="item">
                {{ item }}
            </li>
        </ul>
        <button v-if="options.length>0" v-on:click="randomOption()">What should I do?</button>
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
            
        },
        randomOption(){                

                let choose = Math.floor(Math.random() * this.options.length);                
                alert(this.options[choose])
                
        }
    },
}
</script>

<style>

</style>