<script>
	let visible = false;
	import LeftComponent from './LeftComponent.svelte'
	import RightComponent from './RightComponent.svelte'
	import Footer from './Footer.svelte'
</script>


<main>
	<section class="bodyContainer">
		<LeftComponent />
		<RightComponent/>
	</section>
	<Footer />
</main>



<style>
	:global(body) {
		/*background-image: url(https://i0.wp.com/www.techgrapple.com/wp-content/uploads/2016/09/Black-Wallpaper-in-2K-Resolution.jpg?fit=2560%2C1440&ssl=1);*/
		background-color: #FFFFFF;
	}
	main {
		display: flex;
		height: 100%;
		flex-direction: column;
		/*background-color: blue;*/
	}

	.bodyContainer {
		display: flex;
		flex: 1;
		justify-content: center;
		align-items: center;
		/*background-color: red;*/
	}

	@media (min-width: 640px) {
		main {

			max-width: none;
		}
	}
</style>
