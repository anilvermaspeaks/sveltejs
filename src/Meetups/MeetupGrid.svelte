<script>
    import MeetupItem from "./MeetupItem.svelte";  
    export let meetups;
</script>
    
<style>
.meetups {
  display: flex;
  flex-wrap: wrap;
  margin-left: -15px;
}
</style>
 

<section class="meetups">
    {#each meetups as meet (meet.id) }
<MeetupItem meet ={meet} />
{/each}
</section>