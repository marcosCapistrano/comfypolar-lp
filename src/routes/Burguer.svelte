<div class="burger">
	<div class="burger-item" />
	<div class="burger-item" />
	<div class="burger-item" />
</div>

<style>
	.burger {
		display: flex;
		flex-direction: column;
		width: calc(clamp(1rem, calc(0.63rem + 2.75vw), 1.5rem));
		height: calc(clamp(1rem, calc(0.63rem + 2.75vw), 1.25rem));
		border-radius: 0;
		justify-content: space-between;
        padding: 1px;
	}

	.burger > * {
		height: 13%;
		background: #fff;
	}
</style>
