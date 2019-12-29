<script>
	import { onMount } from 'svelte'
	let canvas
	let ctx
	const update = tick => {
		requestAnimationFrame(update)
		const width = canvas.width = window.innerWidth
		const height = canvas.height = window.innerHeight
		const shade = 127 + Math.sin(tick / 120) * 127
		ctx.fillStyle = `rgb(${shade}, ${shade}, ${shade})`
		ctx.fillRect(0, 0, width, height)			
	}
	onMount(() => {
		ctx = canvas.getContext('2d')
		requestAnimationFrame(update)
	})
</script>

<canvas bind:this={canvas}>
</canvas>

<style>
	:global(html, body) {
		width: 100%;
		height: 100%;
		margin: 0;
		padding: 0;
	}
</style>
