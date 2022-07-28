<script>
	import { page } from '$app/stores';

	const darkMode = () => {
		console.log('tes');
	};

	const dashboard = [
		{ label: 'Home', href: '/' },
		{ label: 'About', href: 'about' },
		{ label: 'Gallery', href: 'gallery' },
		{ label: 'Contact', href: 'contact' }
	];

	const handleToggle = () => {
		console.log('handle');
	};

	let openToggle = false;
</script>

<header class="nav-header">
	<div class="menus">
		<ul class="menu-list">
			<li class:active={$page.url.pathname === '/'}><a sveltekit:prefetch href="/">Home</a></li>
			<li class:active={$page.url.pathname === '/about'}>
				<a sveltekit:prefetch href="/about">About</a>
			</li>
			<li class:active={$page.url.pathname === '/gallery'}>
				<a sveltekit:prefetch href="/gallery">Gallery</a>
			</li>
			<li class:active={$page.url.pathname === '/contact'}>
				<a sveltekit:prefetch href="/contact">Contact</a>
			</li>
		</ul>
		<div class="navbar-toggle" on:click={darkMode}>
			<img src="./img/IconMode.svg" alt="" />
		</div>
	</div>
	<div class="mobile-only">
		<a href="#" class="header-logo">Xae</a>
		<div class="toggle-menu">
			<div
				class="header-menu"
				on:click={() => (openToggle = !openToggle)}
				class:change={openToggle}
			>
				<img src="./img/hamburger.svg" alt="" />
			</div>
			<div class="sideToggle" class:open={openToggle}>
				<a href="#a" class="closebtn" on:click={() => (openToggle = !openToggle)}>&times;</a>
				<ul>
					{#each dashboard as db}
						<li>
							<a href={db.href}>{db.label}</a>
						</li>
					{/each}
				</ul>
			</div>
			<!-- <div class:open={openToggle}>
				<ul>
					{#each dashboard as db}
						<li>
							<a href={db.href}>{db.label}</a>
						</li>
					{/each}
				</ul>
			</div> -->
		</div>
	</div>
</header>

<style>
	.nav-header {
		position: fixed;
		top: 0;
		width: 100%;
		height: 70px;

	}

	.menus {
		display: flex;
	}

	.menu-list {
		position: absolute;
		top: 10px;
		right: 300px;
	}

	ul {
		color: var(--pure-white);
		list-style: none;
	}

	.menu-list li.active {
		border-bottom: 2px solid var(--pure-white);
	}

	.menu-list li {
		float: left;
	}

	.menu-list li a {
		padding: 25px;
		color: var(--pure-white);
		text-decoration: none;
		position: relative;
	}

	.menu-list li a::after {
		content: '';
		position: absolute;
		/* bottom: 0; */
		left: 50%;
		display: block;
		background: none repeat scroll 0 0 transparent;
		height: 2px;
		width: 0;
		background: #fff;
		transition: width 0.3s ease 0s, left 0.3s ease 0s;
	}

	.menu-list li a:hover::after {
		width: 100%;
		left: 0;
	}
	.navbar-toggle {
		position: absolute;
		top: 20px;
		right: 220px;
		cursor: pointer;
	}

	.navbar-toggle:hover {
		transform: scale(1.5);
	}

	.mobile-only {
		display: none;
	}

	@media screen and (max-width: 768px) {
		.nav-header {
			width: 100%;
			/* background: linear-gradient(289.6deg, #0c0c0c 0%, #2c4550 98.22%); */
		}
		.menus {
			display: none;
		}

		.mobile-only {
			display: flex;
			width: 100%;
			justify-content: space-between;
			align-items: center;
			padding-top: 20px;
			/* background: linear-gradient(289.6deg, #0c0c0c 0%, #2c4550 98.22%); */
			/* padding-left: 10px; */
		}

		.toggle-menu {
			position: relative;
			display: flex;
			margin: auto;
			box-sizing: border-box;
			align-items: center;
		}
		.header-logo {
			font-size: 48px;
			font-weight: 700;
			color: var(--pure-white);
			text-decoration: none;
		}

		.header-menu {
			position: absolute;
			left: 120px;
			width: 100px;
			cursor: pointer;
			display: inline-block;
		}

		.sideToggle {
			height: 100%;
			position: fixed;
			width: 0;
			top: 0;
			right: 0;
			background: linear-gradient(289.6deg, #0c0c0c 0%, #2c4550 98.22%);
			transition: 0.5s;
		}

		.sideToggle a {
			text-decoration: none;
			/* padding: 5px; */
			color: var(--pure-white);
		}

		.sideToggle a:hover {
			color: red;
		}

		.open {
			width: 30%;
		}

		.closebtn {
			position: absolute;
			left: 10px;
		}
        
	}
</style>
