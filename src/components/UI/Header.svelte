<script>
  export let pagetitle = 'title'
  export let subtitle = 'subtitle'
</script>

<svelte:head>
  <title>{pagetitle}</title>
</svelte:head>
<div class="text-center container my-4">
<h1 class="text-uppercase mb-4">{pagetitle}</h1>
<h2 class="text-capitalize ">{subtitle}</h2>
</div>