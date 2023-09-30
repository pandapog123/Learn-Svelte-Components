<script context="module" lang="ts">
  export interface ComponentEvents {
    textInput: string;
    reset: undefined;
  }
</script>

<script lang="ts">
  import { createEventDispatcher } from "svelte";

  let dispatchEvent = createEventDispatcher<ComponentEvents>();

  let inputValue = "";

  $: if (inputValue) {
    dispatchEvent("textInput", inputValue);
  }

  function handleReset() {
    dispatchEvent("reset");

    inputValue = "";
  }
</script>

<h1>Event Component</h1>

<input type="text" bind:value={inputValue} />

<button on:click={handleReset}>Reset!</button>
