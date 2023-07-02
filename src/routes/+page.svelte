<script>

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>

		<h2><center>Home Page</center></h2>
<h5>
	Website indexation is the process by 
	which a search engine adds web content to
	 its index. This is done by “crawling” webpages 
	 for keywords, metadata, and related signals that 
	 tell search engines if and where to rank content. 
	 Indexed websites should have a 
	navigable, findable, and clearly 
	understood content strategy.
</h5>


	<h1>Hello and welcome to my site!</h1>
	<a href="/Register">About my site</a>
	<a href="/sverdle">About my site</a>



	<!-- <Counter /> -->
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
