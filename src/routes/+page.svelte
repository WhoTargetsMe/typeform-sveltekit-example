<script lang="ts">
  import "@typeform/embed/build/css/widget.css";
  import { createWidget } from "@typeform/embed";
  import { onMount } from "svelte";

  const formId = "y1uAAugn";

  let elem: HTMLElement;

  onMount(() => {
    elem = document.createElement("div");

    try {
      createWidget(formId, {
        container: elem,
      });
    } catch (error) {
      console.error("Error creating Typeform widget", error);
    }
  });
</script>

<div bind:this={elem} />
