<script>
	
	import logo from '$lib/images/svelte-logo.png';
	
</script>

<header>
	<div class="corner">
		<a href="https://png.pngtree.com/png-vector/20230303/ourmid/pngtree-education-and-college-logo-design-template-vector-png-image_6627789.png">
			<img src={logo} alt="SvelteKit" />
		</a>
	</div>

	<nav class="navbar navbar-expand-lg bg-body-tertiary" style="">
		<div class="container-fluid">
		  
		  <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
			<span class="navbar-toggler-icon"></span>
		  </button>
		  <div class="collapse navbar-collapse" id="navbarSupportedContent">
			<ul class="navbar-nav me-auto mb-2 mb-lg-0">
			  <li class="nav-item">
				<a class="nav-link active" aria-current="page" href="/">Home</a>
			  </li>
			  <li class="nav-item">
				<a class="nav-link active" aria-current="page" href="/Register">Register Here</a>
			  </li>
			  <li class="nav-item">
				 
				<a class="nav-link active" aria-current="page" href="/sverdle">Login Here</a>
			  </li>
			 
			
			
			
		  </div>
		</div>
	  </nav>


</header>

<style>
	header {
		display: flex;
		/* justify-content: space-between; */
		
	}

	.corner {
		width: 3em;
		height: 3em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}
	
</style>
