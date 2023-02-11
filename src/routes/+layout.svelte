<script>
	import { onMount } from 'svelte';
	export let segment;
	export let test = '';
	const handleNav = (loc) => {
		segment = loc;

		test = ' ani';
		setTimeout(() => {
			test = '';
		}, 500);
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
	.ani {
		animation: fade 0.5s ease-in-out 0s 1;
	}
	ul {
		display: flex;
		list-style-type: none;
		justify-content: space-evenly;
		width: 100%;
	}
	li:hover,
	.on:hover {
		box-shadow: inset 0px 0px 5px black;
	}
	li,
	img {
		border-radius: 100px;
		background-color: #494949;
		box-shadow: 0px -1px 3px black, inset -0px -3px 5px rgba(255, 255, 255, 0.44);
	}
	.on a {
		color: yellow;
	}

	img {
		display: flex;
		position: fixed;
		width: 60px;
		left: 10px;
		top: 10px;
		padding: 5px;
		background-color: #494949;
	}

	.header {
		position: relative;
	}
	.navbar {
		width: 100%;
		display: flex;
		justify-content: flex-end;
	}
	nav {
		position: fixed;
		display: flex;
		width: 70%;
		align-items: center;
		height: 75px;
		background: #6767676f;
		border-top: none;
		backdrop-filter: blur(5px);
		border-radius: 0 0 0px 60px;
		box-shadow: inset 0px -3px 5px rgba(255, 255, 255, 0.642), 0px -3px 10px 5px black;
	}
	a {
		text-shadow: 1px 1px 3px black;
		text-decoration: none;
		color: #ffffff;
		font-family: Julius, cursive;
		font-size: calc(15px + 0.390625vw);
	}

	.name {
		display: none;
	}

	li {
		padding: 8px;
	}

	img:hover {
		animation: wiggle 0.4s 1;
	}

	@media (max-width: 600px) {
		li,
		.on,
		img {
			border-radius: 100px;
			background-color: #494949;
			box-shadow: 0px 1px 3px black, inset 0px 3px 5px rgba(255, 255, 255, 0.44);
		}
		.page {
			padding-top: 70px;
		}
		img {
			top: 10px;
			width: 50px;
		}
		.name {
			display: flex;
			position: fixed;
			top: 15px;
			width: fit-content;
			margin: 0px 0px 0px 75px;
			font-size: calc(15px + 0.390625vw);
			padding: 7px 10px;
			border-radius: 100px;
			color: white;
			background-color: #4b4b4c;
			box-shadow: 0px 1px 3px black, inset 0px 3px 5px rgba(255, 255, 255, 0.44);
		}
		.top-left {
			display: flex;
			position: relative;
			border-radius: 10px;
		}
		.navbar {
			justify-content: center;
		}
		nav {
			box-shadow: inset 0px 3px 5px rgba(255, 255, 255, 0.64), 0px 3px 10px black;
			bottom: 0px;
			width: 100%;
			border-radius: 0px;
			padding: 15px;
			height: 20px;
			border-bottom: none;
		}
		li {
			padding: 3px 5px;
		}
	}
</style>
