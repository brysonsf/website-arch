<script>
	let page;
	//let current = 'home';
  import svelteLogo from './assets/svelte.svg';
  import Counter from './lib/Counter.svelte';
  import About from './routes/about/+page.svelte';
  import Demos from './routes/demos/+page.svelte';
  import contact from './routes/contact/+page.svelte';
</script>

<main>
  
<layout/>
  <div>
    <a href="/about">About</a>
    <a href="/demos">Demos</a>
    <a href="/contact">Contact</a>
  </div>

  <div class="card">
    <Counter />
  </div>

  <p>
    Check out <a href="https://github.com/sveltejs/kit#readme" target="_blank" rel="noreferrer">SvelteKit</a>, the official Svelte app framework powered by Vite!
  </p>

  <p class="read-the-docs">
    Click on the Vite and Svelte logos to learn more
  </p>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
