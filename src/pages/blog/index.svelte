<script>
    import {url} from '@sveltech/routify'
    import Header from '../../components/UI/Header.svelte'
    // export let slug  
</script>

<Header pagetitle='Blog' subtitle='Voulez-vous en savoir plus?' />
<ul>
  <li><a href={$url("/blog/machin")}>machin</a></li>
  <li><a href={$url("/blog/truc")}>truc</a></li>
  <li><a href={$url("/blog/bidule")}>bidule</a></li>
</ul>