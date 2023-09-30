<script>
  import BasicComponent from "$lib/basic/BasicComponent.svelte";
  import InputComponent from "$lib/input/InputComponent.svelte";
  import BindComponent from "$lib/bind/BindComponent.svelte";
  import EventComponent from "$lib/event/EventComponent.svelte";
  // EventComponent
  import { fade } from "svelte/transition";
  import StyleComponent from "$lib/style/StyleComponent.svelte";

  let input = "";

  // EventComponent
  let showResetMessage = false;
</script>

<!-- <BasicComponent /> -->

<!-- <InputComponent {input} />

<input bind:value={input} /> -->

<!-- <BindComponent bind:input />

<div>
  <label for="root-input">Root Input</label>

  <input type="text" id="root-input" bind:value={input} />
</div> -->

<!-- <EventComponent
  on:textInput={(event) => {
    input = event.detail;
  }}
  on:reset={() => {
    input = "";

    showResetMessage = true;

    setTimeout(() => {
      showResetMessage = false;
    }, 1000);
  }}
/>

<div>{input}</div>

{#if showResetMessage}
  <div transition:fade class="reset-message">You reset the input!</div>
{/if} -->

<!-- <StyleComponent />

<p class="conflicting-style">Conflicting style with child</p> -->

<style>
  /* EventComponent */
  /* .reset-message {
    padding: 1rem;
    width: fit-content;
    background: orange;
  } */

  /* StyleComponent */
  /* .conflicting-style {
    padding: 1rem;
    background: red;
    font-size: 2rem;
    color: white;
  } */
</style>
