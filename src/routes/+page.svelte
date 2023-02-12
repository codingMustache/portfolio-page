<div class="card">
	<img src="pfp-transp.webp" alt="profile-pic" />
	<div class="card-text">
		<h2>Jorge Carvajal</h2>
		<p>
			I was born and raised in Miami, FL. As a web developer, I have a passion for technology and a
			love for all things web. My goal is to create websites that are not only functional but also
			visually appealing. In my free time, I enjoy indulging in a good book, drawing and sketching,
			working on civic hacking projects and staying up-to-date on the latest developments in the
			world of web technology.
		</p>
		<a href="/portfolio/resume.pdf" target="_blank" rel="noopener noreferrer">
			<button>View Resume</button>
		</a>
	</div>
</div>

<style>
	.card {
		display: flex;
		align-items: center;
		max-width: 1000px;
		margin: 0 auto;
		width: 90vw;
		height: 70%;
		padding: 20px;
		padding-bottom: 100px;
		background-color: #676767;
		border-radius: 5px;
		box-shadow: inset 0 0 10px rgb(255, 255, 255), 0px 10px 20px black;
	}
	.card-text {
		width: 50%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-evenly;
		height: 100%;
	}
	.card h2 {
		font-size: 40px;
		color: rgb(255, 255, 255);
		text-shadow: -2px 5px 7px black;
	}

	img {
		/* object-fit: cover;
		width: 50%;
		height: 100%;
		border-radius: 0 0 150px 150px; */
		--s: 500px; /* image size */
		--b: 0px; /* border thickness */
		--c: #3f3f3f; /* border color */
		--f: 1; /* initial scale */

		width: var(--s);
		aspect-ratio: 1;
		padding-top: calc(var(--s) / 5);
		cursor: pointer;
		border-radius: 0 0 999px 999px;
		--_g: 50% / calc(100% / var(--f)) 100% no-repeat content-box;
		--_o: calc((1 / var(--f) - 1) * var(--s) / 2 - var(--b));
		outline: var(--b) solid var(--c);
		outline-offset: var(--_o);
		background: radial-gradient(
				circle closest-side,
				#3f3f3f calc(99% - var(--b)),
				var(--c) calc(100% - var(--b)) 99%,
				#00000000
			)
			var(--_g);
		-webkit-mask: linear-gradient(#000 0 0) no-repeat 50% calc(1px - var(--_o)) /
				calc(100% / var(--f) - 2 * var(--b) - 2px) 50%,
			radial-gradient(circle closest-side, #000 99%, #00000000) var(--_g);
		transform: scale(var(--f));
		transition: 0.5s;
	}
	img:hover {
		--f: 1.35; /* hover scale */
	}

	p {
		color: rgb(255, 255, 255);
		text-shadow: 1px 1px 1px black;
		margin: 5px 10px;
		font-size: medium;
		line-height: 2rem;
	}
	button {
		text-shadow: 1px 1px 1px black;
		font-size: large;
		padding: 10px 20px;
		margin: 10px;
		font-family: Pont, cursive;
		color: rgb(255, 255, 255);
		border-radius: 10px;
		border: none;
		background-color: #494949;
		box-shadow: 0px -1px 3px black, inset -2px -2px rgba(255, 255, 255, 0.2);
	}
	@media (max-width: 800px) {
		.card {
			flex-direction: column;
			align-items: center;
			margin-bottom: 70px;
		}
		img {
			width: 90%;
			z-index: 0;
		}
		.card-text {
			margin-top: 20px;
		}

		.card {
			margin-top: 0;
		}
		.card-text {
			width: 100%;
		}
	}
</style>
