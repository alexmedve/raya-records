<template>
	<div class="home">
		<AppButton
			v-for="(button, i) in buttons"
			:key="i"
			:text="button.text"
			class="home__button"/>
	</div>
</template>

<script>
	import Button from '@/components/Button.vue';

	export default {
		name: 'Home',
		components: {
			AppButton: Button
		},
		data() {
			return {
				buttons: [
					{
						text: 'Artists'
					},
					{
						text: 'Events'
					},
					{
						text: 'Contact'
					},
					{
						text: 'Radio'
					}
				]
			}
		}
	};
</script>

<style lang="scss">
	.home {
		height: 100%;
		position: relative;
		@include flex-center;
		flex-direction: column;

		&__button {
			margin-bottom: 4rem;
		}
	}
</style>