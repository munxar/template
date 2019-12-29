<script>
	import Tailwind from './Tailwind.svelte'
	import Button from './Button.svelte'
	import Emoticon from './Emoticon.svelte'
	let counter = 0
</script>

<Tailwind />

<main class="p-4">	
	<h1 class="text-4xl mb-2">Svelte & Tailwind</h1>
	<Button class="mb-3" on:click={() => counter++}>Button</Button>
	<div>
		<Emoticon code={counter} />
	</div>
</main>
