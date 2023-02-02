<script>
	import Burguer from './Burguer.svelte';
</script>

<div id="navbar">
	<Burguer />
	<span class="navbar-title">NOTÍCIAS</span>
	<svg
		xmlns="http://www.w3.org/2000/svg"
		width="25"
		height="25"
		fill="#f0f0f0"
		viewBox="0 0 256 256"
		><rect width="256" height="256" fill="none" /><circle
			cx="116"
			cy="116"
			r="84"
			fill="none"
			stroke="#f0f0f0"
			stroke-linecap="round"
			stroke-linejoin="round"
			stroke-width="20"
		/><line
			x1="175.4"
			y1="175.4"
			x2="224"
			y2="224"
			fill="none"
			stroke="#f0f0f0"
			stroke-linecap="round"
			stroke-linejoin="round"
			stroke-width="20"
		/></svg
	>
</div>
<div id="advertorial">
	<span class="advertorial-title">ADVERTORIAL</span>
</div>

<style lang="scss">
	#navbar {
		background-color: $primaryColor;
		padding: 0 1rem 0 1rem;

		display: flex;
		align-items: center;
	}

	#navbar .navbar-title {
		color: white;
		flex: 1;
		text-align: center;
		font-size: clamp(1.5rem, calc(1.24rem + 1.3vw), 2.25rem);
		font-weight: 300;
		font-family: 'Open Sans', Arial, Helvetica, sans-serif;
		letter-spacing: -1px;
		padding: 0.5em;
	}

	#navbar .navbar-search {
		width: calc(clamp(1rem, calc(0.63rem + 2.75vw), 1.5rem));
		padding: 1px;
	}

	#advertorial {
		background-color: darken($primaryColor, 10%);
		padding: 0 1rem 0 1rem;

		display: flex;
		align-items: center;
	}

	#advertorial .advertorial-title {
		color: rgb(231, 252, 227);
		flex: 1;
		text-align: center;
		font-size: clamp(0.72rem, calc(0.65rem + 0.35vw), 0.92rem);
		font-weight: 400;
		font-family: 'Open Sans', Arial, Helvetica, sans-serif;
		padding: 0.5em;
	}
</style>
