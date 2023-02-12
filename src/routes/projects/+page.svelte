<div class="project">
	<div class="head">
		<h2>Poke Play Pen</h2>
		<a href="https://github.com/codingMustache/pokemon-play-pen">
			<img class="github-logo" src="github-mark.png" alt="github-logo" />
		</a>
	</div>
	<div class="content">
		<img class="project-pic" src="portfolio/pokepp.webp" alt="project" />
		<div class="project-desc">
			<ul>
				<li>
					Implemented new features into the legacy code base following the existing structure,
					seamlessly integrated features while keeping consistent styling.
				</li>
				<li>
					Used Axios to parse JSON objects dynamically while interacting with both internal and
					external APIs
				</li>
				<li>Used advanced CSS techniques on raw images to render into styled-component themes.</li>
				<li>
					Played a vital role in organization of the teams feature planning and implementation.
				</li>
			</ul>
		</div>
	</div>
</div>
<div class="project">
	<div class="head">
		<h2>New Home</h2>
		<a href="https://github.com/codingMustache/NewHome">
			<img class="github-logo" src="github-mark.png" alt="github-logo" />
		</a>
	</div>
	<div class="content">
		<img class="project-pic" src="./portfolio/newhome.webp" alt="project" />
		<div class="project-desc">
			<ul>
				<li>Displayed dynamic content with React based on the user's interactions.</li>
				<li>Setup authentication using Passport.js with a Google strategy.</li>
				<li>Implemented private messaging among users.</li>
				<li>Used React Router for dynamic client-side rendering.</li>
				<li>Implemented proper security in rendering users private messages.</li>
			</ul>
		</div>
	</div>
</div>
<div class="project">
	<div class="head">
		<h2>Hole Dat</h2>
		<a href="https://github.com/codingMustache/holeDat">
			<img class="github-logo" src="github-mark.png" alt="github-logo" />
		</a>
		<a href="holedat.com">
			<img class="github-logo" src="website-icon.png" alt="github-logo" />
		</a>
	</div>
	<div class="content">
		<img class="project-pic" src="portfolio/holedat.webp" alt="project" />
		<div class="project-desc">
			<ul>
				<li>Setup authorization for users with passport.js and Google OAuth Strategy.</li>
				<li>Rendered a map with markers and dynamic popups using react-mapbox-gl.</li>
				<li>Made API calls for reverse/geocoding coding to the mapbox API.</li>
				<li>Built out a comment section to handle user interactions.</li>
				<li>Used ORM Sequelize to query Postgres database managed in AWS RDS.</li>
				<li>Developed pagination on a feed of user created content.</li>
				<li>Displayed dynamic chart data with ChartJS based on count queried from database.</li>
				<li>Deployed app to AWS EC2, used reverse proxies with NGINX and Certbot.</li>
			</ul>
		</div>
	</div>
</div>

<div class="footer" />

<style>
	h2 {
		font-family: Pont;
		font-size: larger;
		text-shadow: 1px 1px 1px black;
	}
	.project {
		background-color: rgba(105, 105, 105, 0.803);
		margin: 5px;
		padding: 20px;
		border-radius: 5px;
		box-shadow: inset 3px -3px 5px rgb(255, 255, 255), 2px -3px 5px black;
		min-width: 200px;
		max-width: 500px;
	}
	ul {
		list-style: circle;
		text-shadow: 1px 1px 1px black;
		padding: 20px;
		color: white;
		font-family: Pont;
	}

	.head {
		padding: 5px;
		display: flex;
		background-color: #494949;
		color: white;
		border-radius: 5px;
		justify-content: space-evenly;
		align-items: center;
		box-shadow: 0px -1px 3px black, inset 0px -3px 5px rgb(255 255 255 / 44%);
	}
	.head img {
		background-color: rgba(164, 162, 162, 0.803);
		padding: 3px;
		border-radius: 100px;
		box-shadow: inset 1px -1px 2px white, 1px -1px 3px black;
		cursor: pointer;
		width: 30px;
	}
	.project-pic {
		object-fit: cover;
		width: 100%;
		height: 200px;
		margin: 5px;
		border-radius: 10px;
		border: 1px solid white;
		box-shadow: 5px 5px 5px black;
	}
	.footer {
		height: 100px;
	}
	@media (max-width: 600px) {
		.project {
			min-width: 90%;
		}
		.project-pic {
			width: 100%;
		}
	}
</style>
