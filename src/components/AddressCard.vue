<template>

	<div class="address-card">
		<div class="add-new-address" v-if="add">
			<div class="address-card__header-text">Добавить новый адрес</div>
			<div class="address-card__info">
				<div class="address-card__icon">
					<div class="address-card__icon_home"></div>
				</div>
			</div>
		</div>
		<div class="existing-address" v-else>
			<div class="address-card__header">
				<div class="existing-address__name">{{name}}</div>
				<div class="icon-close"></div>
			</div>
			<div class="address-card__divider"></div>
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
