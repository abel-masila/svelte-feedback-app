<script>
  import { fade, scale } from 'svelte/transition';
  import FeedbackItem from './FeedbackItem.svelte';
  export let feedback = [];
</script>

{#each feedback as feedback (feedback.id)}
  <div in:scale out:fade={{ duration: 500 }}>
    <FeedbackItem item={feedback} on:delete-feedback />
  </div>
{/each}
