<script>
    import Card from '../components/Card.svelte'
    export let posts=[];

</script>
<style>
    .TimeLine {
      padding: 4em 0 0 0;
    }
  </style>
<div class="TimeLine">
   <div class="Timeline-container">
     {#each posts as post}
     <Card {...post}/>
     {/each}
   </div>
</div>