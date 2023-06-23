<script>
    export let titulo;
    export let poster;
    import { fade, blur, fly, slide, scale } from "svelte/transition";
</script>

<h3 transition:scale>{titulo}</h3>
<h3 transition:slide>{poster}</h3>