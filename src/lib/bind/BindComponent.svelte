<script lang="ts">
  export let input: string;

  function clearInput() {
    input = "";
  }
</script>

<h1>Bind Component</h1>

<p>The current input is: {input}</p>

<div>
  <label for="bind-input">Bind Input</label>

  <input id="bind-input" bind:value={input} />

  <button on:click={clearInput}>Clear input</button>
</div>
