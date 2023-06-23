<script>
	import { onMount } from 'svelte';
    import Noticia from "$lib/components/noticia.svelte";
    import { fade, blur, fly, slide, scale } from "svelte/transition";

    let items = null;

	onMount(async () => {
		const res = await fetch("https://api.fureweb.com/spreadsheets/1g6oQpD1zCkJiusttXB-lcX_YZAu3oKdBxG5XRIgJV48");
        //Declaro una variable, res. Se le dice que espere hasta que fetch de un resultado.
		items = await res.json();
        console.log(items);
        //EventListener, llama a una funcion (Callback)

	});
    //On mount se ejecuta despues de que todo esta cargado

    //https://docs.google.com/spreadsheets/d/1g6oQpD1zCkJiusttXB-lcX_YZAu3oKdBxG5XRIgJV48/edit?usp=sharing

</script>


{#if items}
<ul transition:fade>
    {#each items.data as item}
         <!--<li>{item.nombre} // <span>{item.apellido}</span></li>-->
         <!--<img src={item.poster} alt={item.nombre}>-->
         <Noticia
            titulo={item.nombre}
            poster={item.posicion}
        />
    {/each}
</ul>
{/if}

<style>
    li{
        color:blue;
        margin-left:20px;
    }
</style>
