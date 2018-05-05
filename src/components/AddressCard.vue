<template>
	
	<div class="address-card">
		<div v-if="add" class="add-new-address"> 
			<div class="address-card__header-text">Добавить новый адрес</div>
			<div class="address-card__info">
				<div class="address-card__icon">					
					<div class="address-card__icon_home"></div>
					<div class="address-card__icon_home2"></div>
					<div class="address-card__icon_door"></div>
					<div class="address-card__icon_add"></div>
					<div class="address-card__icon_add2"></div>
				</div>
			</div>
		</div>
		<div v-else class="existing-address"> 
			<div class="address-card__header">
				<div class="existing-address__name">{{name}}</div>
				<div class="existing-address__icon_close">
					<div class="existing-address__icon_close1"></div>
					<div class="existing-address__icon_close2"></div>
				</div>	
			</div>
			<div class="address-card__divider" />
		
			<div class="address-card__info">
				<div class="address-card__item">{{address.city}}</div>
				<div class="address-card__item">{{address.street}}</div>
				<div class="address-card__item">{{address.phoneNumber}}</div>
				<div class="address-card__item"><a class="address-card__item_edit" href="#">Редактировать</a></div>
			</div>
		</div>
	</div>
	
</template>

<script>
export default {
  props: {
  	add: Boolean,
	name: String,
	address: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

