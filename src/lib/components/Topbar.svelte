<script>
	export let navLinks = [
		{ href: '/', label: 'Home' },
		// TODO: Uncomment the following lines after creating the respective pages
		// { href: '/about', label: 'About' },
		// { href: '/services', label: 'Services' },
		{ href: '/contact', label: 'Contact' }
	];
</script>

<div class="topbar">
	<div class="container">
		<!-- Image and Text container -->
		<div class="logo-container">
			<!-- Flex container for logo and text -->
			<div class="logo">
				<img src="/images/seria-logo-color-outlined.png" alt="Seria Logo" width="60" height="60" />
			</div>
			<div class="site-name">
				Seria <br /> Solutions
			</div>
		</div>
		<nav>
			<ul class="nav-links">
				{#each navLinks as link}
					<li><a href={link.href}>{link.label}</a></li>
				{/each}
			</ul>
		</nav>
	</div>
</div>

<style>
	.topbar {
		background-color: #2463eb;
		color: #ffb400;
		padding: 8px;
		min-width: min-content;
	}

	.container {
		display: flex;
		justify-content: space-between;
		align-items: center;
		max-width: 1200px;
		margin: 0 auto;
	}

	.logo-container {
		display: flex;
		align-items: center;
	}

	.logo {
		padding: 8px;
		flex-shrink: 0;
	}

	.site-name {
		font-size: 1.5rem; /* 2xl */
		font-weight: bold;
		margin-left: 8px;
	}

	nav .nav-links {
		display: flex;
		gap: 16px; /* Space between nav items */
		margin-bottom: 24px;
		margin-left: 24px;
		list-style: none;
		padding: 0;
	}

	nav .nav-links a {
		text-decoration: none;
		color: inherit;
	}

	nav .nav-links a:hover {
		text-decoration: underline;
	}
</style>
