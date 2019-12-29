<script>
    export let code = 0
</script>

<style>
    .emoticon {
        @apply text-6xl;
    }
</style>

<span class="emoticon">
    {@html `&#1285${ 12 + (code % 56)};`}
</span>
