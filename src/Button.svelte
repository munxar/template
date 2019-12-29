<script>
    import { appendClass } from './utils'
</script>
<button on:click class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded{appendClass($$props)}">
  <slot />
</button>
