<script>
	import { page } from '$app/stores';
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
		<div class="navbar-toggle">
			<img src="./img/IconMode.svg" alt="" />
		</div>
	</div>
	<div class="mobile-only">
		<a href="#" class="header-logo">Xae</a>
		<div class="header-menu">
			<img src="./img/hamburger.svg" alt="" />
		</div>
	</div>
</header>

<style>
	.nav-header {
		position: fixed;
		top: 0;
		width: 100%;
		height: 100px;
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

    .menu-list li a:hover::after{
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
		}
		.menus {
			display: none;
		}

		.mobile-only {
			display: flex;
			width: 100%;
			justify-content: space-between;
			align-items: center;
			padding-top: 50px;
			/* padding-left: 10px; */
		}

		.header-logo {
			font-size: 48px;
			font-weight: 700;
			color: var(--pure-white);
			text-decoration: none;
			padding-left: 50px;
		}

		.header-menu {
			width: 100px;
		}
	}
</style>
