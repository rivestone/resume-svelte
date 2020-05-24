<script>
const photo = './static/photo.jpg';
import Socials from './socials.svelte';
import Projects from './projects.svelte';

const skills = ["Responsive HTML & CSS",
"Sass\ Less\ Stylus",
"Javascript",
"React",
"Gulp\ Webpack"];
const socials = [
	{name: "Github", link: "https://github.com/rivestone"},
	{name: "Telegram", link: "https://t.me/rivestone"},
	{name: "mycoralriver@gmail.com", link: "mailto:mycoralriver@gmail.com"}
];
const projects = [
	{name: "Nsellaspb.ru", description: "online store", link: "http://nsellaspb.ru/", tags: ['HTML','Adaptive CSS','Angular', 'Webpack']},
	{name: "Beautyhome.me", description: "online store", link: "https://beautyhome.me/", tags: ['']},
	{name: "Rezerv-chita.ru", description: "online store", link: "http://rezerv-chita.ru", tags: ['']},
	{name: "Pumparts.ru", description: "online store", link: "https://pumparts.ru/", tags: ['']}
];
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
	<Socials {socials}/>
	<h3>Skills</h3>
	<ul>
		{#each skills as skill}
			<li>{skill}</li>
		{/each}
	</ul>
	<Projects {projects}/>
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
