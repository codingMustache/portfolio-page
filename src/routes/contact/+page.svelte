<script>
	import { fade } from 'svelte/transition';
</script>

<div class="card">
	<a href="https://github.com/codingMustache">
		<img src="github.png" alt="github" />
		<h2>GitHub</h2>
	</a>

	<a href="tel:6031112298">
		<img src="phone.png" alt="github" />
		<h2>Phone</h2>
	</a>

	<a href="mailto:codingMustache@icloud.com">
		<img src="email.png" alt="github" />
		<h2>Email</h2>
	</a>

	<a href="https://www.linkedin.com/in/codingmustache/">
		<img src="linkedin.png" alt="github" />
		<h2>LinkedIn</h2>
	</a>
</div>

<style>
	.card {
		flex-wrap: wrap;
		justify-content: center;
		max-width: 400px;
	}
	a {
		padding: 10px;
		display: flex;
		flex-direction: column;
		align-items: center;
		min-width: 100px;
		margin: 20px 10px;
		text-decoration: none;
		color: yellow;
		text-shadow: 2px 1px black;
		font-family: 'Baloo 2', cursive;
		font-size: x-large;
		border-radius: 10px;
		background-color: #4654b2;
		box-shadow: -1px -1px 3px black, inset -5px -5px rgba(255, 255, 255, 0.2);
	}
	img {
		border-radius: 10%;
		padding: 5px;
		background-color: rgb(145, 145, 215);
		border: 3px solid black;
		box-shadow: -2px -2px 5px black;
		width: 70px;
	}
</style>
