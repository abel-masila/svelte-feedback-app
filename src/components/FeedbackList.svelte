<script>
  import { FeedbackStore } from './../stores';
  import { fade, scale } from 'svelte/transition';
  import FeedbackItem from './FeedbackItem.svelte';
</script>

{#each $FeedbackStore as feedback (feedback.id)}
  <div in:scale out:fade={{ duration: 500 }}>
    <FeedbackItem item={feedback} />
  </div>
{/each}
