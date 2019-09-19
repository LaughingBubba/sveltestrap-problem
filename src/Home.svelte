<h2>Home!</h2>

<p>Welcome to this sample code!</p>
<p>Things to try:</p>
<ul>
    <li>Open the console before clicking on the button below ...</li>
</ul>
<button type="button" class="btn btn-success" on:click={()=>navigate('/hello')} >Say Hello</button>

<script>

  import { navigate } from 'svelte-routing'
  import { Button } from 'sveltestrap'

</script>