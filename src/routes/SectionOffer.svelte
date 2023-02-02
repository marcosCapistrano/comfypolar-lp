<script>
// @ts-nocheck

	import ProductOffer from '$lib/components/ProductOffer.svelte';
	import product3 from '$lib/assets/product3.webp';
	import product2 from '$lib/assets/product2.webp';
	import product1 from '$lib/assets/product1.webp';

	const offers = [
		{
			featured: true,
			image: product3,
			text: 'Compre 3 ComfyPolar, GANHE 2 GRÁTIS',
			priceBefore: 'R$290,00',
			priceNow: 'R$87,00',
			num: "0"
		},
		{
			featured: false,
			image: product2,
			text: 'Compre 2 ComfyPolar, GANHE 1 GRÁTIS',
			priceBefore: 'R$174,00',
			priceNow: 'R$58,00',
			num: "1"
		},
		{
			featured: false,
			image: product1,
			text: '1x ComfyPolar',
			priceBefore: 'R$58,00',
			priceNow: 'R$29,00',
			num: "2"
		}
	];

	let offerChoosen = "0";
	$: console.log(offerChoosen);

	const setOfferChoosen = (num) => {
		offerChoosen = num;
		console.log("oieee")
	}
</script>

<section class="offer wrapper container">
	<span class="step"><strong>Escolha uma oferta</strong></span>
	<span class="warning"
		>Encomende já e recebe <strong>FRETE-GRÁTIS!</strong> (envio em 24h/48h)</span
	>
	<hr />

	<br />
	<form>
		{#each offers as offer}
			<ProductOffer
				featured={offer.featured}
				image={offer.image}
				text={offer.text}
				priceBefore={offer.priceBefore}
				priceNow={offer.priceNow}
				num={offer.num}
				{offerChoosen}
				{setOfferChoosen}
			/>
		{/each}
	</form>

	<a href="" class="btn btn-featured">Ir para o Checkout</a>
</section>

<style lang="scss">
	.offer {
		margin-top: 2rem;

		.step {
			text-align: center;
			display: block;
			font-size: var(--step-2);
			font-weight: bold;
		}

		.warning {
			display: block;
			padding: 1em;
			border-radius: 1em;
			background-color: rgba(120, 250, 150, 0.5);
			margin: 1em auto;
			width: fit-content;

			strong {
				font-weight: bold;
			}
		}
	}
</style>
