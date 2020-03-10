<script>
	let visible = false;

	function typewriter(node, { speed = 50 }) {
		const valid = (
				node.childNodes.length === 1 &&
				node.childNodes[0].nodeType === 3
		);

		if (!valid) {
			throw new Error(`This transition only works on elements with a single text node child`);
		}

		const text = node.textContent;
		const duration = text.length * speed;

		return {
			duration,
			tick: t => {
				const i = ~~(text.length * t);
				node.textContent = text.slice(0, i);
			}
		};
	}
</script>

<label>
	<input type="checkbox" bind:checked={visible}>
	visible
</label>

<main>
	<nav style="background-color: #f3f3f3">
		<ul>
			<li>Overview </li>
			<li>Features </li>
			<li>Video </li>
			<li>Reviews </li>
			<li>Screenshots </li>
			<li>Overview </li>
		</ul>
	</nav>
{#if visible}
	<h1 in:typewriter>Show your mobile apps with James!</h1>
	<p in:typewriter>It's a mobile app landing page designed with material design in core. Present your app the best way it deserves.</p>
{/if}
</main>

<style>
	:global(body) {
		background-image: url(https://i0.wp.com/www.techgrapple.com/wp-content/uploads/2016/09/Black-Wallpaper-in-2K-Resolution.jpg?fit=2560%2C1440&ssl=1);
		background-color: #616266;
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}



	h1 {
		color: #996600;
		font-size: 4em;
		font-weight: 100;
	}

	p{
		color: #996600;
	}

	ul {
		list-style-type: none;
		margin: 0;
		padding: 0;
	}

	li {
		float: right;
		list-style-type: none;
		margin: 0 3vw;
	}

	nav{
		width: 100vw;
		color: #996600;
	}



	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
