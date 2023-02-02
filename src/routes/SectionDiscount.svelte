<script>
	import discountImg from '$lib/assets/50off.webp';
</script>

<section class="offer wrapper">
	<div class="container discount-applied row">
		<div class="discount-applied__img">
			<img src={discountImg} alt="50% de desconto" />
		</div>
		<div class="discount-applied__text">
			<span class="discount-title text-featured">Seu desconto de 50% foi aplicado!</span>
			<span class="discount-text"
				><span class="text-featured">Oferta limitada:</span> ComfyPolar está disponível por
				<span class="crossed">R$100</span>
				<span class="text-success">R$48,99</span>
				<span class="text-info">(50% de desconto por unidade)</span></span
			>
		</div>
	</div>
</section>

<style lang="scss">
	.offer {
        margin-top: 2rem;
		.discount-applied {
			flex-wrap: wrap;
			.discount-applied__img {
				display: block;
				margin: 0 auto;
				max-width: 100px;
			}

			.discount-applied__text {
				display: flex;
				flex-direction: column;
				justify-content: space-around;
				gap: 1em;
				.discount-title {
					display: block;
					font-size: var(--step-2);
				}

				.discount-text {
					display: block;
					font-size: var(--step-1);
				}
			}
		}
	}

	@media only screen and (min-width: 480px) {
		.offer {
			.discount-applied {
                flex-wrap: nowrap;
			}
		}
	}
</style>
