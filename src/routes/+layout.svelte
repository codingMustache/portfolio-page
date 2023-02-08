<script>
	import { onMount } from 'svelte';
	import { fade } from 'svelte/transition';
	export let segment;
	export let test = '';
	const handleNav = (loc) => {
		segment = loc;

		test = ' ani';
		setTimeout(() => {
			test = '';
		}, 1000);
	};

	onMount(() => (segment = window.location.pathname));
</script>

<div class="header">
	<div class="top-left">
		<img src="logo.svg" width="30px" alt="logo" />
		<h1 class="name">Coding Mustache</h1>
	</div>
	<div class="navbar">
		<nav>
			<ul>
				<li class={segment === '/' ? 'on' : ''}>
					<a on:click={() => handleNav('/')} href={`/`}>About</a>
				</li>
				<li class={segment === '/projects' ? 'on' : ''}>
					<a on:click={() => handleNav('/projects')} href="/projects">Projects</a>
				</li>
				<li class={segment === '/skills' ? 'on' : ''}>
					<a on:click={() => handleNav('/skills')} href="/skills">Skills</a>
				</li>
				<li class={segment === '/contacts' ? 'on' : ''}>
					<a on:click={() => handleNav('/contacts')} href="/contact">Contact</a>
				</li>
			</ul>
		</nav>
	</div>
</div>
<div class="page{test}">
	<slot />
</div>

<style>
	ul {
		display: flex;
		list-style-type: none;
		margin: 5px;
	}
	.on:hover {
		box-shadow: 0px 0px 3px black, inset -2px -2px rgba(255, 255, 255, 0.2);
	}
	.on {
		border-radius: 10px;
		background-color: #4654b2;
		box-shadow: 0px -1px 3px black, inset -2px -2px rgba(255, 255, 255, 0.2);
	}
	.on a {
		text-shadow: none;
		color: yellow;
	}
	.page {
		display: flex;
		margin: auto;
		flex-wrap: wrap;
		justify-content: center;
		padding-top: 80px;
		padding-bottom: 100px;
	}
	img {
		display: flex;
		position: fixed;
		width: 50px;
		left: 10px;
		top: 10px;
		padding: 3px;
		border-radius: 10px;
		background-color: #4654b2;
		box-shadow: 0px -1px 3px black, inset -2px -2px rgba(255, 255, 255, 0.2);
	}

	.header {
		position: relative;
	}
	.navbar {
		width: 100%;
		display: flex;
		justify-content: center;
	}
	nav {
		position: fixed;
		gap: 1rem;
		padding: 5px 50px;
		justify-content: space-evenly;
		align-items: center;
		height: 50px;
		display: flex;
		background: #4e5ec9dd;
		border: 4px solid yellow;
		outline: 4px solid rgb(144, 144, 2);
		border-top: none;
		border-radius: 0 0 100px 100px;
		box-shadow: inset 0px -3px 5px rgba(255, 255, 255, 0.2), 0px -3px 10px 5px black;
	}
	a {
		text-shadow: 1px 1px 3px black;
		margin: 5px;
		text-decoration: none;
		color: #ffffff;
		font-weight: bold;
		font-family: 'Baloo 2', cursive;
		font-size: large;
	}
	.name {
		display: none;
	}

	@keyframes wiggle {
		0% {
			transform: rotate(10deg);
		}
		25% {
			transform: rotate(-13deg);
		}
		50% {
			transform: rotate(15deg);
		}
		75% {
			transform: rotate(-11deg);
		}
		100% {
			transform: rotate(12deg);
		}
	}
	@-o-keyframes wiggle {
		0% {
			transform: rotate(0deg);
		}
		25% {
			transform: rotate(-3deg);
		}
		50% {
			transform: rotate(5deg);
		}
		75% {
			transform: rotate(-1deg);
		}
		100% {
			transform: rotate(2deg);
		}
	}
	@-moz-keyframes wiggle {
		0% {
			transform: rotate(0deg);
		}
		25% {
			transform: rotate(-3deg);
		}
		50% {
			transform: rotate(5deg);
		}
		75% {
			transform: rotate(-1deg);
		}
		100% {
			transform: rotate(2deg);
		}
	}
	@-webkit-keyframes wiggle {
		0% {
			transform: rotate(0deg);
		}
		25% {
			transform: rotate(-3deg);
		}
		50% {
			transform: rotate(5deg);
		}
		75% {
			transform: rotate(-1deg);
		}
		100% {
			transform: rotate(2deg);
		}
	}
	@keyframes fade {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	@-o-keyframes fade {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	@-moz-keyframes fade {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	@-webkit-keyframes fade {
		0% {
			opacity: 0;
		}
		100% {
			opacity: 1;
		}
	}
	.ani {
		-webkit-animation: fade 1s 1;
		-moz-animation: fade 1s 1;
		-o-animation: fade 1s 1;
		animation: fade 0.7s 1;
	}

	img:hover {
		animation: wiggle 0.5s infinite;
	}

	@media (max-width: 600px) {
		.page {
			padding-top: 70px;
		}
		.name {
			display: flex;
			position: fixed;
			top: 12px;
			margin: 0 0px 0px 75px;
			font-size: large;
			padding: 3px 10px;
			border-radius: 10px;
			background-color: #4654b2;
			box-shadow: 0px -1px 3px black, inset -2px -2px rgba(255, 255, 255, 0.2);
			line-break: strict;
		}
		.top-left {
			display: flex;
			position: relative;
			border-radius: 10px;
		}
		nav {
			box-shadow: inset 0px 3px 5px rgba(255, 255, 255, 0.2), 0px 3px 10px black;
			bottom: 0px;
			width: 90%;
			border-radius: 100px 100px 0px 0px;
			padding: 10px;
			height: 20px;
			border: 4px solid yellow;
			outline: 4px solid rgb(144, 144, 2);
			border-bottom: none;
		}
		a {
			font-size: medium;
		}
	}
</style>
