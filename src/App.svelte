<script>
	import Todo from './Todo.svelte';
</script>

<main>
	<h1>IM 415 Lab 4</h1>
	<h2>Pick your Temple!</h2>
	<Todo />

<div class="container mt-5 temples">
	<div class="row">
	  <div class="col">
	    <img src="./img/angkor.jpg" alt="pic of Angkor Wat, Krong Siem Reap, Cambodia">
	    <p>Angkor Wat, Krong Siem Reap, Cambodia</p>
	  </div>
	  <div class="col">
		<img src="./img/katas.jpg" alt="Picture of Katas Raj Temples, Pakistan">
		<p>Katas Raj Temples, Pakistan</p>
	  </div>
	  <div class="col">
		<img src="./img/bagan.jpg" alt="pic Bagan, Myanmar (Burma)">
		<p>Bagan, Myanmar (Burma)</p>
	  </div>
	</div>
</div>
<div class="container mt-5 temples">
	<div class="row">
	  <div class="col">
	    <img src="./img/byodo.jpg" alt="pic of Byodo-In Temple, Kaneohe, HI, USA">
	    <p>Byodo-In Temple, Kaneohe, HI, USA</p>
	  </div>
	  <div class="col">
		<img src="./img/khajuraho.jpg" alt="pic of Khajuraho, Madhya Pradesh, India">
		<p>Khajuraho, Madhya Pradesh, India</p>
	  </div>
	  <div class="col">
		<img src="./img/kukke.jpg" alt="pic of Kukke, Shivamogga, India">
		<p>Kukke, Shivamogga, India</p>
	  </div>
	</div>
</div>
</main>
<style>

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		width: 75vw;
		background-image: url("/img/sky.jpg");
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 400;
	}

	h2 {
		color: rgb(255, 255, 255);
		font-size: 3em;
		font-weight: 400;
	}

	img {
		width: 20vw;
		box-shadow: 5px 5px 10px rgb(255, 255, 255);
		margin-top: 20px;
	}

	.temples {
		border: 15px solid gray;
		border-bottom: 50px solid rgba(128, 128, 128, 0.5);
	}

	.temples p {
		font-size: 22px;
		font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
		color: rgb(0, 0, 0);
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}

	}

	@media (min-width: 2000px) {
		img {
			width: 15vw;
		}
	}
</style>