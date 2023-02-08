<script>
	const skills = {
		Languages: ['Javascript', 'Typescript'],
		Frontend: ['HTML', 'CSS', 'JQuery', 'React', 'Svelte', 'AngularJS'],
		Backend: ['NodeJS', 'SvelteKit', 'Express'],
		Build: ['Babel', 'Vite', 'Webpack', 'ESLint', 'Prettier', 'GitHub Actions'],
		Database: ['SQLite', 'MySQL', 'Postgres', 'Mongo', 'Mongoose', 'Sequelize'],
		Deployment: ['EC2', 'RDS', 'Digital Ocean', 'Nginx', 'Certbot'],
		Style: ['Sass', 'Styled Components', 'Bootstrap', 'MUI'],
		Misc: [
			'Axios',
			'Agile',
			'SCRUM',
			'MapBox',
			'MomentJS',
			'Cherrio',
			'Multer',
			'Chart.js',
			'Passport'
		],
		Software: ['PGAdmin', 'Gimp', 'InkScape', 'Procreate'],
		'Image Mgmt': ['HIEC/HIEF2Any', 'Cloudinary', 'Browser Image Compression', 'Swiper']
	};

	//bable webpack  esLint Prettier github actions
</script>

{#each Object.entries(skills) as [key, value]}
	<div class="card">
		<h1>{key}</h1>
		<ul>
			{#each value as item}
				<li>{item}</li>
			{/each}
		</ul>
	</div>
{/each}

<style>
	.card {
		flex-direction: column;
		max-width: 250px;
		padding: 20px;
	}
	h1 {
		font-family: 'Baloo 2';
		font-size: x-large;
		color: yellow;
		text-shadow: 0px 2px 3px black;
	}
	ul {
		font-family: 'Zen Maru Gothic', sans-serif;
		list-style: none;
		display: flex;
		flex-wrap: wrap;
		padding: 10px;
	}
	li {
		text-shadow: 0px 1px 0px black;
		margin: 5px;
		padding: 3px 5px;
		border-radius: 20px;
		background-color: yellow;
		box-shadow: 0px 3px 3px black;
	}
	@media (max-width: 600px) {
		.card {
			max-width: 400px;
		}
	}
</style>
