<script>
  import FeedbackItem from './FeedbackItem.svelte';
  export let feedback = [];
</script>

{#each feedback as feedback (feedback.id)}
  <FeedbackItem item={feedback} on:delete-feedback />
{/each}
