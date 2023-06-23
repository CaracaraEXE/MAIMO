<script>
    import COMPO from "$lib/components/header.svelte";
    import INTRO from "$lib/components/intro.svelte";
    import LIST from "$lib/components/list.svelte";
    import GALLERY from "$lib/components/gallery.svelte";
    import FOOTER from "$lib/components/footer.svelte";
    import CONTADOR from "$lib/components/contador.svelte";
    import NOTICIAS from "$lib/components/noticias.svelte";
    import NOTICIA from "$lib/components/noticia.svelte";

    let items = [
    {
      titulo:"item 1",
      href:"https://neocities.org",
    },
    {
      titulo:"item 2",
      href:"https://ebird.org/argentina/home",
    },
    {
      titulo:"item 3",
      href:"http://www.eakringbirds.com/eakringbirds6/insectinfocustenebriomolitor.htm",
    },
  ]

  //Nombres de propiedades con variables, sino es confuso

</script>

<COMPO menu={items}/>
<NOTICIAS/>
<NOTICIA/>
<CONTADOR />
<INTRO />
<LIST />
<GALLERY />
<FOOTER />