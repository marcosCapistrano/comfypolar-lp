<script>
	import homem1 from '$lib/assets/comments/homem1.jpeg';
	import homem2 from '$lib/assets/comments/homem2.jpeg';
	import homem3 from '$lib/assets/comments/homem3.jpeg';
	import homem4 from '$lib/assets/comments/homem4.jpeg';
	import homem5 from '$lib/assets/comments/homem5.jpeg';

	import mulher1 from '$lib/assets/comments/mulher1.jpeg';
	import mulher2 from '$lib/assets/comments/mulher2.jpeg';
	import mulher3 from '$lib/assets/comments/mulher3.jpeg';
	import mulher4 from '$lib/assets/comments/mulher4.jpeg';
	import mulher5 from '$lib/assets/comments/mulher5.jpeg';

	const comments = [
		{
			author: 'Marilia Santos',
			timestamp: 'há 3 horas',
			content: 'Conheço amigos que possuem o produto e recomendam, vou aproveitar a promoção!',
			image: mulher1
		},
		{
			author: 'Rafael Carvalho',
			timestamp: 'há 5 horas',
			content: 'O produto é ótimo, não me arrependo',
			image: homem1
		},
		{
			author: 'Maria Silva',
			timestamp: 'há 7 horas',
			content: 'Eu amei o produto, realmente cumpre o que promete',
			image: mulher2
		},
		{
			author: 'João Santos',
			timestamp: 'há 8 horas',
			content: 'Melhor compra que já fiz, recomendo muito',
			image: homem2
		},
		{
			author: 'Ana Paula',
			timestamp: 'há 10 horas',
			content: 'Não consigo mais viver sem ele, é incrível',
			image: mulher3
		},
		{
			author: 'Carlos Oliveira',
			timestamp: 'há 12 horas',
			content: 'Fiquei surpreso com a qualidade do produto, é excepcional',
			image: homem3
		},
		{
			author: 'Juliana Souza',
			timestamp: 'há 1 dia',
			content: 'Meus amigos ficaram impressionados com os resultados, recomendo',
			image: mulher4
		},
		{
			author: 'Paulo Almeida',
			timestamp: 'há 2 dias',
			content: 'Não poderia estar mais satisfeito com a minha compra',
			image: homem4
		},
		{
			author: 'Bruna Rodrigues',
			timestamp: 'há 3 dias',
			content: 'É simplesmente incrível, eu recomendo',
			image: mulher5
		},
		{
			author: 'Lucas Machado',
			timestamp: 'há 4 dias',
			content: 'O produto é ótimo e a entrega foi rápida, recomendo',
			image: homem5
		}
	];
</script>

<section class="social-proof">
	<div class="wrapper">
		<h1>O que dizem nossos clientes</h1>

		<span class="product__rating">
			<span class="rating__stars"><i>★</i><i>★</i><i>★</i><i>★</i><i>★</i></span>
			(857) avaliações
		</span>

		{#each comments as comment}
			<div class="comment row">
				<div class="profile-pic" >
						<img src={comment.image} />
					</div>
				<div class="comment-content">
					<div class="header">
						<span class="author">{comment.author}</span>
						<span class="timestamp">{comment.timestamp}</span>
					</div>
					<div class="content">
						<p>{comment.content}</p>
					</div>
					<div class="footer">
						<div class="icon-btn">
							<i class="fa-solid fa-thumbs-up" />
							<span>Curtir</span>
						</div>

						<div class="icon-btn">
							<i class="fa-solid fa-reply" />
							<span>Responder</span>
						</div>
					</div>
				</div>
			</div>
		{/each}
	</div>
</section>

<style lang="scss">
	section.social-proof {
		background-color: #fff;
		color: #000;
		padding-top: 2rem;
		padding-bottom: 4rem;
		margin-top: 4rem;

		h1 {
			font-size: var(--step-4);
			text-align: center;
		}

		.product__rating {
			display: block;
			margin-top: 2rem;
			margin-bottom: 1rem;
			font-size: var(--step-2);
			.rating__stars {
				color: #fc0;
				text-shadow: #fc0 0 0 20px;
			}
		}

		.comment {
			margin: 1rem 0;
			border: 1px solid rgba(255,255,255,0.25);
			padding: 1em;
			align-items: center;
			border-radius: 1em;

			&.row {
				flex-wrap: nowrap;
			}

			.profile-pic {
				img {
					border-radius: 100%;
					max-width: 100%;
				}
			}

			.comment-content {
				width: 100%;
				margin-left: 1rem;
			}
		}

		.icon-btn {
			cursor: pointer;
		}

		.header {
			display: inline-flex;
			align-items: baseline;
			gap: 10px;
			margin-bottom: 10px;

			.author {
				font-weight: bold;
			}

			.timestamp {
				font-size: 0.75em;
			}
		}

		.footer {
			display: inline-flex;
			gap: 16px;
			margin-top: 20px;
			.icon-btn {
				display: inline-flex;
				gap: 6px;
			}
		}
	}
</style>
