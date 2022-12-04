<script>
    import axios from 'axios';

    const token = process.env.STRAPI_TOKEN;

    // Request API.
    axios
    .get('https://strapi.mtc.berlin/api/collections', {
        headers: {
        Authorization: `Bearer ${token}`,
        },
    })
    .then(response => {
        // Handle success.
        console.log('Data: ', response.data);
    })
    .catch(error => {
        // Handle error.
        console.log('An error occurred:', error.response);
    });
    
    
    
    
    
    
    
    
    
    // import { onMount } from 'svelte';
    // import axios from 'axios'
    
    // let collections = [];
    // let error = null
    
    // onMount(async () => {
    //     try {
    //         const col = await axios
    //         .get('https://strapi.mtc.berlin/api/collection');
    //         collections = col.data
            
    //     } catch (e) {
    //         error = e
    //     }
    // });
    
    </script>
    
    <!-- {#if error !== null}
      {error}
    {:else}
      <ul>
      {#each collections as collection}
        <li>
              {collection.attributes.title}
        </li>
      {/each}
      </ul>
    {/if} -->