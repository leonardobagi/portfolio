<script>
	import ButtonWIcon from "./ButtonWIcon.svelte";
</script>

<div style="width: 100vw; height: 90vh;" />
<header>
	<h1>Olá</h1>
	<h3>Eu sou Leonardo Bagi, um mero menino de 14 anos.</h3>
	<div class="btn-manager">
		<ButtonWIcon text="Twitter" style="link" icon="<i class='fa-brands fa-twitter'></i>" />
		<ButtonWIcon text="Instagram" style="danger" icon="<i class='fa-brands fa-instagram'></i>" />
		<ButtonWIcon text="GitHub" style="dark" icon="<i class='fa-brands fa-github'></i>" />
	</div>
</header>

<style>
	header {
		background-image: linear-gradient(to bottom right, #5e5ef7, #65f3c4);
		width: 100vw;
		height: 90vh;
		top: 0;
		left: 0;
		right: 0;
		position: absolute;

		color: white;
	}

	h1 {
		padding-top: 25vh;
		padding-left: 12vw;
		font-size: 3.5rem;
	}

	h3 {
		padding-left: 10vw;
		font-size: 1.75rem;
	}

	.btn-manager {
		padding-left: 10vw;
		padding-top: 5vh;
		display: flex;
		gap: 3vh;
		flex-direction: column;
	}

	@media screen and (max-width: 990px) {
		h1 {
			font-size: 12vw;
		}
		h3 {
			font-size: 7vw;
		}
	}
</style>
