<script>
	import Header from '$lib/Layout/Header.svelte';
	import '../app.css';
	import Navbar from '$lib/Layout/SideNav.svelte';
	import Footer from '$lib/Layout/Footer.svelte';
</script>

<div class="container">
	
	<div class="side-menu">
		<Navbar />
	</div>
	<div class="content">
		<Header />
		<div class="content-body">
			<slot />
			<div class="footer">
				<Footer />
			</div>
		</div>
		
	</div>

	<div class="mobile-only">
		<div class="mobile-header">
			<Header/>
		</div>
		<div class="mobile-content">
			<slot/>
		</div>
		<div class="footer-mobile-only">
			<Footer />
		</div>
	</div>
</div>

<footer>
	<!-- <p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p> -->
</footer>

<style>
	.container {
		display: flex;
		width: 100%;
		height: 100vh;
		position: relative;
		/* overflow: hidden; */
	}

	.side-menu {
		/* z-index: 100; */
		/* position: fixed; */
		top: 0;
		height: 100%;
		width: 161px;
	}

	.content {
		height: 100%;
		width: calc(100% - 161px);
		/* overflow-y: auto; */
	}

	.content-body {
		max-width: 100vw;
		width: 100%;
		height: calc(100vh - 100px);
		z-index: -2;
		position: relative;
	}

	.footer {
		z-index: 1;
		position: absolute;
		top: 510px;
		opacity: 0.8;
	}

	.mobile-only {
		display: none;
	}



	@media screen and (max-width: 768px) {
		.container {
			overflow: auto;
			height: 896px;
		}

		.content{
			display: none;
		}
		.side-menu {
			display: none;
		}

		.mobile-only {
			width: 100%;
			display: flex;
			/* justify-content: space-between; */
		}

		.mobile-header {
			position: fixed;
			width: 100%;
			transition: 0.4s;
			top: 0;
			z-index: 99;
			padding: 100px 5px;
		}
		

		.mobile-content{
			display: flex;
			position: relative;
			width: 100%;
			/* z-index: -1; */
			/* flex-direction: column; */
		}

		.footer-mobile-only {
			position: absolute;
			width: 100%;
			top: 800px;
			height: fit-content;
		}
	
		
	}

	/* main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	} */
</style>
