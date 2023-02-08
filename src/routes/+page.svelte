<div class="card">
	<img src="pfp.JPG" alt="profile-pic" />
	<div class="card-text">
		<h2>Jorge Carvajal</h2>
		<p>
			I am web developer in New Orleans, LA and has a passion for building things for the web. With
			experience in both web development, I enjoys continuing to hone my craft and explore new
			technologies in building for the web.
		</p>
		<button href="">View Resume</button>
	</div>
</div>

<style>
	:global(
			html,
			body,
			div,
			h1,
			h2,
			h3,
			p,
			a,
			big,
			em,
			img,
			small,
			strong,
			center,
			ol,
			ul,
			li,
			form,
			table,
			caption,
			article,
			aside,
			nav,
			summary,
			video
		) {
		margin: 0;
		padding: 0;
		border: 0;
		font-size: 100%;
		font: inherit;
		vertical-align: baseline;
	}

	:global(body, html) {
		background: fixed repeat 1% url('/img-noise-361x370.png');
		width: 100%;
		height: 100%;
	}
	:global(h1) {
		font-family: 'Nabla', cursive;
	}
	:global(h2) {
		font-family: 'Baloo 2', cursive;
	}
	:global(p) {
		font-family: 'Zen Maru Gothic', sans-serif;
	}

	:global(.card) {
		max-width: 1000px;
		background-color: rgba(135, 135, 135, 0.803);
		padding: 10px;
		display: flex;
		width: 90vw;
		margin: 10px;
		flex-direction: row;
		align-items: center;
		border-radius: 10px;
		outline: 3px solid yellow;
		box-shadow: inset 0 0 10px 5px black, 0px 10px 20px black;
	}
	.card-text {
		max-width: fit-content;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-evenly;
		height: 100%;
	}
	.card h2 {
		font-size: 3rem;
		line-height: 3rem;
		color: rgb(255, 225, 33);
		text-shadow: -2px 5px 7px black;
	}
	img {
		border-radius: 10px;
		margin: 10px;
		object-fit: cover;
		width: 50%;
		height: 90%;
		box-shadow: 0 0 10px black;
		border: 2px solid rgb(0, 0, 0);
	}

	h2 {
		margin: 10px;
	}
	p {
		color: rgb(255, 233, 33);
		text-shadow: 1px 1px 1px black;
		margin: 5px 10px;
		font-size: larger;
		line-height: 2rem;
	}
	button {
		text-shadow: 1px 1px 1px black;
		font-size: large;
		padding: 10px 20px;
		margin: 10px;
		font-family: 'Baloo 2', cursive;
		color: yellow;
		border-radius: 10px;
		border: none;
		background-color: #4654b2;
		box-shadow: 0px -1px 3px black, inset -2px -2px rgba(255, 255, 255, 0.2);
	}
	@media (max-width: 600px) {
		.card {
			flex-direction: column;
			align-items: center;
			margin-bottom: 75px;
		}
		img {
			width: 90%;
		}
	}
</style>
