<script>
	// @ts-nocheck

	export let featured;
	export let image;
	export let text;
	export let priceBefore;
	export let priceNow;
	export let setOfferChoosen;

	export let num;
	export let offerChoosen;

	$: console.log(num, offerChoosen, num === offerChoosen);
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="product container row" class:featured class:choosen={offerChoosen === num} on:click={() => setOfferChoosen(num)}>
	<input type="radio" class="radio" name="choice" bind:group={offerChoosen} on:change={(e) => setOfferChoosen(e.currentTarget.value)} value={num}/>
	<div class="img-container">
		<img src={image} alt="produto" />
	</div>
	<span class="product-details">{text}</span>
	<div class="pricing">
		<span class="price-crossed">{priceBefore}</span>
		<span class="price-featured">{priceNow}</span>
	</div>
</div>

<style lang="scss">
	.product.container.featured {
		background-color: yellow;
		margin-bottom: 1rem;
		margin: 1rem 0 1rem 0;
		position: relative;

		&::before {
			float: left;
			// display: block;
			position: absolute;
			top: -2em;
			left: 0.5em;
			content: 'Melhor Oferta';
			background-color: red;
			padding: 0.75em;
			color: white;
			font-weight: bold;
			border-radius: 1em;
		}
	}

	.product.container {
		align-items: center;
		justify-content: space-between;
		flex-wrap: nowrap;
		gap: 5px;
		margin-left: 1rem;
		margin-right: 1rem;
		margin-bottom: 0.5rem;

        &.choosen {
            border: 2px solid orange;
        }

		.radio {
			max-width: 40px;
			max-height: 40px;
		}

		.img-container {
			border: 1px solid #c5c7d2;
			max-width: 75px;
			// padding: 1em;
		}

		.product-details {
			font-size: var(--step-1);
		}

		.pricing {
			display: flex;
			flex-direction: column;
			align-items: flex-end;
			margin-left: auto;

			.price-crossed {
				font-size: var(--step-1);
				text-decoration: line-through;
				color: grey;
			}

			.price-featured {
				font-size: var(--step-4);
				color: green;
				margin-top: 1rem;
			}
		}
	}
</style>
