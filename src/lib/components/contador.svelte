<script>
    let contador = 0;

    function ejecutar() {
        contador++;
    }
</script>

<p>Contador: {contador}</p>

<button on:click={ejecutar} class="inline-flex text-white bg-indigo-500 border-0 py-2 px-6 focus:outline-none hover:bg-indigo-600 rounded text-lg">Contar</button>