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
	{name: "Nsellaspb.ru", description: "registering for training courses platform and ordering medical equipment", link: "http://nsellaspb.ru/", tags: ['HTML','Adaptive CSS','Angular', 'Webpack']},
	{name: "Beautyhome.me", description: "cosmetics store", link: "https://beautyhome.me/", tags: ['']},
	{name: "Rezerv-chita.ru", description: "electronics and home appliance store", link: "http://rezerv-chita.ru", tags: ['']},
	{name: "Pumparts.ru", description: "shop of spare parts and accessories for industrial pumping systems", link: "https://pumparts.ru/", tags: ['']}
];
</script>
<div class="container-wrapper">
	<div class="container">
		<h1>Ksenia Dolganova</h1>
		<h2>Front-end developer</h2>
		<img
			class="photo"
			src={photo}
			alt="Ksenia's photo"
			width="140"
			height="auto">
		<div class="resume-block">
		  <h3>Social links</h3>
			<Socials {socials}/>
		</div>
		<div class="resume-block">
			<h3>Skills</h3>
			<ul>
				{#each skills as skill}
					<li>{skill}</li>
				{/each}
			</ul>
		</div>
		<div class="resume-block">
		  <h3>Projects</h3>
			<Projects {projects}/>
		</div>
	</div>
</div>

<style>
	:global(body) {
		font-family: "Lucida Console";
	}
	.container-wrapper {
		padding: 1em;
	}
	.container {
		text-align: center;
		max-width: 500px;
		margin: 0 auto;
	}
	@media (max-width: 640px) {
		.container {
			width: 300px;
		}
	}
	h1{
		font-size: 2.2em;
	}
	:global(h3){
		font-size: 25px;
		margin: 40px 0 15px;
	}
	:global(ul) {
		padding: 0;
		list-style-type: none;
	}
	:global(li) {
		margin-bottom: 5px;
		font-family: "Verdana", sans-serif;
	}
	li{
		font-size: 18px;
	}
</style>
