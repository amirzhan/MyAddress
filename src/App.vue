<template>
  <div id="app">
  	<h4 class="header-word">Мои адреса</h4>
    <AddressInfo />
  </div>
</template>

<script>
import AddressInfo from './components/AddressInfo'

export default {
  name: 'App',
  components: {
    AddressInfo
  },
  data () {
  	return {
  		items: [
  			{
  				name: 'Данияр Кудайбергенов',
  				address: {
  					city: 'Алматы',
  					street: 'ул. Жарокова,97',
  					phoneNumber: '+8 777 777 7777'
  				}
  			},
  			{
  				name: 'adfhs',
  				address: {
  					city: 'Астана',
  					street: 'ул. Жарокова,97',
  					phoneNumber: '+8 777 777 7777'
  				}
  			}
  		]
  	}
  }
}
</script>


