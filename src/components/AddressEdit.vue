<template>
	<div v-if="isCreate" class="address-card create-address">
		<div class="address-edit__header">
			<div class="address-edit__header-text">Создание нового адреса в Алматы</div>
			<div class="icon-close"></div>
		</div>
		<div class="create-address__divider"></div>
		<div class="create-address__form">
			<div v-for="(item,index) in items" :key="index" class="create-address__form-item">
				{{item}}
				<input type="text">
			</div>
		</div>
		<button class="create-address__button">Сохранить</button>
	</div>
	<div v-else class="delete-address address-card">
		<div class="address-edit__header">
			<div class="address-edit__header-text">Подтвердите удаление</div>
			<div class="icon-close"></div>
		</div>

		<div class="address-card__divider"></div>

		<div class="address-card__info">
			<div class="delete-address__item">{{address.city}}</div>
			<div class="delete-address__item">{{address.street}}</div>
			<div class="delete-address__item">{{address.phoneNumber}}</div>
			<button class="delete-address__button">Удалить</button>
		</div>
	</div>
</template>

<script>
export default {
  props: {
  	isCreate: Boolean,
		address: Object
  },
  data () {
  	return {
  		items: [
  			'ФИО',
  			'Номер телефона',
  			'Улица',
  			'Дом',
  			'кв./офис'
  		]
  	}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
