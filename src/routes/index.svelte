<script context="module">
	export const prerender = true;
</script>

<script>
	import Counter from '$lib/Counter.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="container">
	<div class="container-body">
		<h1>
			Adventure Together	
		</h1>
		<p>
			Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placerat id potenti faucibus nec, rhoncus, vulputate vitae. Dictum rutrum ut cras nullam porta id dolor arcu, quis.
		</p>
	</div>
	<div class="container-image">
		<img class="box" src="./img/box.png" alt="">
		<img class="astro" src="./img/astronoutIcon.png" alt="">
	</div>
	
	<div class="container-mobile">
		<div class="content-mobile">
			<h1>
				Adventure Together	
			</h1>
			<p>
				Lorem ipsum dolor sit amet, consectetur adipiscing elit. Placerat id potenti faucibus nec, rhoncus, vulputate vitae. Dictum rutrum ut cras nullam porta id dolor arcu, quis.
			</p>
		</div>
		<!-- <div class="mobile-img">
			<img class="image-mobile" src="./img/mobile-illustration.svg" alt="">
		</div> -->
	</div>

</div>

<style>
	.container {
		display: flex;
		position: relative;
		overflow: hidden;
	}

	.container-body {
		padding-top: 150px;
		padding-left: 80px;
		width: 40%;
		height: 100%;
		color: var(--pure-white);
		z-index: 1;
	}

	.container-body h1 {
		font-size: 72px;
		font-weight: 700;
		line-height: 79.2px;
	}

	.container-body p {
		font-size: 18px;
		font-weight: 500;
		line-height: 27px;
	}

	.container-image {
		position: fixed;
		width: 100%;
		height: 100%;
		/* top: -140px; */
		right: -300px;
		z-index: -2;
	}

	.box {
		z-index: -1;
		top: 0px;
		left: 0px;
		/* position: relative; */
		/* width: 100%; */
		/* height: 100%; */
	}

	.astro {
		position: absolute;
		z-index: 0;
		left: 245px;
  		top: 150px;
	}

	.container-mobile {
		display: none;
	}

	@media screen and (max-width: 768px) {
		.container-body {
			display: none;
		}
		.container-image {
			display: none;
		}

		.container {
			width: 100%;
		}

		.container-mobile {
			/* position: relative; */
			display: flex;
			color: var(--pure-white);
			width: 100%;
			height: 100%;
			background-image: url("/img/mobile-illustration.svg");
			background-repeat: no-repeat;
			background-position: center;
			background-attachment: fixed;
			background-size: cover;
		}

		.content-mobile {
			position: relative;
			margin-top: 300px;
			padding-left: 30px;
			width: 100%;
			height: 100%;
			
		}

		.container-mobile h1 {
			width: 60%;
			font-size: 48px;
			line-height: 52.8px;
			font-weight: 700;
		}

		.container-mobile p {
			width: 55%;
			font-size: 12px;
			line-height: 18px;
			font-weight: 500;
		}

	}

</style>
