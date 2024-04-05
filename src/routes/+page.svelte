<script lang="ts">

  import { Avatar } from "@skeletonlabs/skeleton";
  import avatar from "../assets/avatar.png";
  import Request from "$lib/Request.svelte";
  import Thanks from "$lib/Thanks.svelte";

  const requestDate = new Date('2024/04/05');
  const today = new Date();

  const done = false

  function calculateDaysBetween(date1: Date, date2: Date) {
    const oneDay = 1000 * 60 * 60 * 24;
	const diffInTime = Math.abs(date2.getTime() - date1.getTime());
    return Math.ceil(diffInTime / oneDay);
  }

</script>

{#if done}
	<Thanks/>
{:else}
	<Request/>
{/if}