<template>
	<div id="app">
		<div class="app-container">
			<div class="app-container__banner">
				<h2 class="app-container__title">
					Raya Records
				</h2>
			</div>
			<div class="app-container__view">
				<router-view />
			</div>
		</div>
	</div>
</template>

<style lang="scss">
	//APP VUE STYLING
	.app-container {
		height: 100vh;
		display: grid;
		grid-template-columns: 35% 65%;

		&__banner {
			position: relative;
			background-image: url("./assets/img/landing-page-bg-purple.jpg");
			background-size: cover;
			background-position: center;
		}

		&__title {
			font-size: 3rem;
			letter-spacing: .2rem;
			font-family: $font-display;
			color: $color-white;
			@include abs-center;
		}

		&__view {
			background-color: $color-dark;
		}
	}
</style>

/////HELPER CLASSES

<style module>
	.u-text-align-right {
		text-align: right;
	}
</style>


///GLOBAL STYLE DECLARATIONS

<style lang="scss">
	*,
	*::before,
	*::after {
		margin: 0;
		padding: 0;
		box-sizing: border-box
	}

	html,
	body {
		font-size: 62.5%;
	}

	::-webkit-scrollbar {
		width: 15px;
	}

	/* Track */
	::-webkit-scrollbar-track {
		background: #333740;
	}

	/* Handle */
	::-webkit-scrollbar-thumb {
		background: #888;
	}

	/* Handle on hover */
	::-webkit-scrollbar-thumb:hover {
		background: #555;
	}
</style>