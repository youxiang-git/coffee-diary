<script lang="ts">
  import Counter from './lib/Counter.svelte'

  const id = "What's your name: "
  const defaultUser = "Current User"
  let username = $state("");
</script>

<main>
  <h1>Welcome to {username || defaultUser}'s Coffee Diary</h1>

  <div class="card">
    <Counter />
  </div>

  <label for={id}>{id}</label>
  <input {id} bind:value={username}/>

</main>

<style>
</style>
