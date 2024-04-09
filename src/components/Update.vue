<template>
  <Header />
  <h1>Hello User, Welcome on Update Restaurant Page</h1>   
  <form class="add">
    <input type="text" name="name" placeholder="Enter Name" v-model="restaurant.name" />
    <input type="text" name="address" placeholder="Enter address" v-model="restaurant.address" />
    <input type="text" name="contact" placeholder="Enter contact" v-model="restaurant.contact" />
    <button type="button" v-on:click="addRestuarant">Add new Restaurant</button>
  </form>
</template>
<script>
import Header from './Header.vue'
export default {
 name: 'Update-vue',
  components:{ 
     Header
},
data()
  {
    return {
      restaurant: {
        name: '',
        address: '',
        contact: ''
      }
    }
  },
   mounted()
      {
        let user = localStorage.getItem('user-info');
        if(!user)
        {
            this.$router.push({name:'Login'})
        }
      }
 }
</script> 