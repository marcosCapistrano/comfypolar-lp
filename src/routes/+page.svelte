<script>
	// @ts-nocheck
	import logo from '$lib/assets/logo.webp';
	import product from '$lib/assets/product.webp';
	import discountImg from '$lib/assets/50off.webp';
	import SectionOffer from './SectionOffer.svelte';
	import SectionDiscount from './SectionDiscount.svelte';
	import SocialSection from './SocialSection.svelte';
</script>

<svelte:head>
	<title>ComfyPollar</title>
</svelte:head>

<header class="wrapper">
	<img src={logo} alt="ComfyPolar" />
</header>

<section class="hero">
	<div class="wrapper-big row">
		<div class="col product-img">
			<img src={product} alt="três mulheres usando ComfyPolar" />
		</div>
		<ul class="col bullets">
			<li>Protege as pernas do frio e do congelamento</li>
			<li>Melhora a sua circulação sanguínea</li>
			<li>Limão, confortável e macio como um xadrez</li>
			<li>Durável graças ao seu design rosqueável e resistente</li>
			<li>Chique e elegante, combina com todas as suas roupas</li>
			<li>Fácil de manter e não requer engomar</li>
		</ul>
	</div>
</section>

<SectionDiscount/>
<SectionOffer />
<SocialSection />


<style lang="scss">
	header {
		padding-top: 0.5rem;
		padding-bottom: 0.5rem;
		img {
			margin: 0 auto;
			display: block;
			max-width: 350px;
		}
	}

	.hero {
		margin-top: 2rem;
		.product-img {
			margin: 0 auto;
		}

		.bullets {
			margin: 0 auto;

			li {
				background-color: #f3f3f3;
				border: 1px solid rgba(0, 0, 0, 0.1);
				font-size: var(--step-1);
				font-weight: bold;
				text-align: center;
				padding: 0.5em;
				margin-bottom: 0.5em;
			}
		}
	}

	@media only screen and (min-width: 900px) {
		.hero {
			.product-img {
				width: 49%;
			}

			.bullets {
				width: 49%;

				.li {
					padding: 0.5em 1em;
				}
			}
		}
	}
</style>
