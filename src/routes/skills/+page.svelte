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
		<h1>{key}:</h1>
		<ul>
			{#each value as item}
				<li>{item}</li>
			{/each}
		</ul>
	</div>
{/each}

<style>
	.card {
		background-color: rgba(135, 135, 135, 0.803);
		margin: 10px;
		border-radius: 5px;
		min-width: 300px;
		box-shadow: inset 0px -3px 5px rgb(255 255 255 / 64%), 0px -3px 10px 5px black;
		flex-direction: column;
		max-width: 250px;
		padding: 20px;
	}
	h1 {
		font-family: Pont;
		font-size: x-large;
		color: rgb(255, 255, 255);
		text-shadow: 0px 2px 3px black;
	}
	ul {
		font-family: Comfy, sans-serif;
		list-style: none;
		display: flex;
		flex-wrap: wrap;
		padding: 10px;
		justify-content: center;
	}
	li {
		text-shadow: 0px 1px 0px black;
		margin: 5px;
		padding: 5px 10px;
		border-radius: 20px;
		background-color: #494949;
		color: white;
		box-shadow: 0px 3px 3px black;
		box-shadow: 0px -1px 3px black, inset -0px -3px 5px rgba(255, 255, 255, 0.44);
	}

	@media (max-width: 600px) {
		.card {
			max-width: 400px;
		}
	}
</style>
