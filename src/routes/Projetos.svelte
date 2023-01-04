<script lang="ts">
	import { onMount } from "svelte";

	onMount(() => {
		const rbxm = document.querySelector(".rbxmaster")!;
		const cuboMagico = document.querySelector(".cubo-magico")!;
		const kumon = document.querySelector(".kumon")!;

		const btns = [
			document.querySelector("#rbxm-btn"),
			document.querySelector("#cubo-btn"),
			document.querySelector("#kumon-btn"),
		] as HTMLButtonElement[];

		btns.forEach(btn =>
			btn.addEventListener("click", () => {
				switch (btn.id) {
					case "rbxm-btn":
						rbxm.classList.add("visible");

						cuboMagico.classList.remove("visible");
						kumon.classList.remove("visible");
						break;

					case "cubo-btn":
						cuboMagico.classList.add("visible");

						rbxm.classList.remove("visible");
						kumon.classList.remove("visible");

						break;
					case "kumon-btn":
						kumon.classList.add("visible");

						rbxm.classList.remove("visible");
						cuboMagico.classList.remove("visible");
						break;
				}
			}),
		);
	});
</script>

<section>
	<h1>Coisas que eu já fiz da vida</h1>
	<div class="buttons has-addons btn-manager">
		<button class="button is-dark is-outlined is-inverted is-responsive is-medium" id="rbxm-btn">RBXMaster</button>
		<button class="button is-dark is-outlined is-inverted is-responsive is-medium" id="cubo-btn">Cubo Mágico</button>
		<button class="button is-dark is-outlined is-inverted is-responsive is-medium" id="kumon-btn">Kumon</button>
	</div>
	<div class="rbxmaster visible">
		<h2>RBXMaster</h2>
		<p>
			Uma extensão para o site do Roblox, que atualmente integra playlists e algumas utillidades. A extensão costumava
			se chamar "RobloxPromocodeMaster", mas novas ideias vieram e foram adicionadas, então mudei o nome. Com o passar
			do tempo, a funcionalidade de promocodes foi, infelizmente, removida.
		</p>
	</div>
	<div class="cubo-magico">
		<h2>Cubo Mágico</h2>
		<p>
			Em 2018, aprendi a montar o cubo pelo método de camadas, e já me sentia extremamente feliz com isso. Tinha o sonho
			de quebrar o recorde mundial um dia, mesmo tendo tempos de 2-3 minutos. Atualmente, sei o <a
				href="https://cinoto.com.br/cubomagico/principais/fridrich/">método de Fridich</a
			>
			(ou
			<abbr title="Cross, F2L, OLL, PLL">CFOP</abbr>, para os gringos) e consigo tempos de ~35s. Também tenho os cubos
			2x2, 4x4 e 5x5; gosto muito de montar eles todos e sempre conseguir melhorar, realmente me tira do tédio.
		</p>
	</div>
	<div class="kumon">
		<h2>Kumon</h2>
		<p>
			Comecei o kumon de inglês em 2017. Nesse tempo, o nível de inglês que eu tinha era basicamente as palavras que me
			ensinavam na escola. Comecei no estágio 4a e aprendi logo o alfabeto e melhorei muito minha pronúncia. Depois de
			longos 5 anos, os quais eu tinha preguiça de fazer os blocos e já não queria mais, conclui o curso e não me
			arrependo. Ganhei muitas coisas nesse meio tempo, além da gratificação de saber falar bem o idioma estrangeiro.
		</p>
	</div>
</section>

<style>
	*:not(a) {
		color: #eee;
	}

	a {
		color: #3838ff;
	}

	a:hover {
		color: blue;
		transition: 0.2s;
	}

	section {
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		gap: 2em;
		background-color: #333231;
		width: 100vw;
		height: 110vh;
	}

	h1 {
		font-weight: 700;
		font-size: 5.5vw;
	}

	h2 {
		font-weight: 500;
		font-size: 3vw;
	}

	p {
		width: 80vw;
		font-size: 1.4vw;
	}

	button {
		transition: 0.2s;
	}

	.btn-manager {
		display: none;
	}

	@media screen and (max-width: 990px) {
		section {
			height: 90vw;
		}

		h2 {
			font-size: 4vw;
		}
		p {
			font-size: 3vw;
		}

		.btn-manager {
			display: block;
		}

		.rbxmaster:not(.visible),
		.cubo-magico:not(.visible),
		.kumon:not(.visible) {
			display: none;
		}
	}
</style>
