<script>
  import FeedbackItem from './FeedbackItem.svelte';
  export let feedback = [];
  console.log(feedback);
</script>

{#each feedback as feedback (feedback.id)}
  <FeedbackItem item={feedback} />
{/each}
