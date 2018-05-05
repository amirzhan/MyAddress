<template>
  <div class="address-block">
	  <div class="address-info">
		  
		  <AddressCard v-for="(item, index) in items" :key="index" :address="item.address" :name="item.name" :add="item.add" />
	  		
	  </div>
	  <div class="address-edit">
	  	<AddressEdit :isCreate="true"/>
	  	<AddressEdit :isCreate="false" :address="items[0].address"/>
	  </div>
	</div>
</template>

<script>
import AddressCard from '@/components/AddressCard'
import AddressEdit from '@/components/AddressEdit'

export default {
  components: {
  	AddressCard,
  	AddressEdit
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
  				},
  				add: true
  			},
  			{
  				name: 'Данияр Кудайбергенов',
  				address: {
  					city: 'Алматы',
  					street: 'ул. Жарокова,97',
  					phoneNumber: '+8 777 777 7777'
  				},
  				add: false
  			},
  			{
  				name: 'adfhs',
  				address: {
  					city: 'Астана',
  					street: 'ул. Жарокова,97',
  					phoneNumber: '+8 777 777 7777'
  				},
  				add: false
  			}
  		]
  	}
  }
}
</script>

