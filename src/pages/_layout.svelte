<script>
	// import Navbar from './../components/UI/Navbar.svelte';
    import {url, isActive} from '@sveltech/routify'
    import Navbar from '../components/UI/Navbar.svelte'
import { pathToParams } from '@sveltech/routify/lib/utils'
const links = [
  ['.', 'accueil'],
  ['./about', 'a propos'],
  ['./blog', 'blog']
]
    // let navbarCollapse = false
    // let showDropdown = false
</script>
<div>
    <Navbar >
        <ul class="navbar-nav mr-auto">
          {#each links as [path, name]}
            
            <li class="nav-item" on:select={$isActive(path)} >
              <!-- svelte-ignore a11y-invalid-attribute -->
              <a class="nav-link" href={$url(path)}>{name}<span class="sr-only">(current)</span></a>
            </li>
            {/each}
<!--

           <li class="nav-item active">
              
              <a class="nav-link" href={url}>Accueil <span class="sr-only">(current)</span></a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Produits</a>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                Liste
              </a>
              <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                <a class="dropdown-item" href="#">Action</a>
                <a class="dropdown-item" href="#">Another action</a>
                <div class="dropdown-divider"></div>
                <a class="dropdown-item" href="#">Something else here</a>
              </div>
            </li>
            <li class="nav-item">
              <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
            </li>
--> 
          </ul>
    </Navbar>
    <slot />
    
    
</div>