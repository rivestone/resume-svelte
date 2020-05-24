<script>
const photo = './static/photo.jpg';
</script>

<main>
	<h1>Ksenia Dolganova</h1>
	<h2>Front-end developer</h2>
	<img
		class="photo"
		src={photo}
		alt="Ksenia's photo"
		width="140"
		height="auto">
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
