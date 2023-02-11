<div class="card">
	<div class="circle-top" />
	<img src="pfp-transp.webp" alt="profile-pic" />
	<div class="circle-bottom" />
	<div class="card-text">
		<h2>Jorge Carvajal</h2>
		<p>
			I was born and raised in Miami, FL. As a web developer, I have a passion for technology and a
			love for all things web. My goal is to create websites that are not only functional but also
			visually appealing. In my free time, I enjoy indulging in a good book, drawing and sketching,
			working on civic hacking projects and staying up-to-date on the latest developments in the
			world of web technology.
		</p>
		<button href="">View Resume</button>
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
		object-fit: cover;
		width: 50%;
		height: 100%;
		border-radius: 10px;
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
	@media (max-width: 600px) {
		.card {
			flex-direction: column;
			align-items: center;
			margin-bottom: 70px;
		}
		img {
			width: 90%;
		}
		.card {
			margin-top: 0;
		}
		.card-text {
			width: 100%;
		}
	}
</style>
