<!--
 /src/lib/components/DialogControl.svelte
 DialogControl.svelte
 cml-narrative
 
 Created by Ian Thompson on September 7th 2022
 icthomp@g.clemson.edu
 
 https://idealab.sites.clemson.edu
 
--->
<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	/** Dispatch the back dialogEvent */
	const back = () => {
		dispatch('dialogEvent', {
			state: 'back'
		});
	};

	/** Dispatch the forward dialogEvent */
	const forward = () => {
		dispatch('dialogEvent', {
			state: 'forward'
		});
	};
</script>

<div class="flex space-x-2 rounded-md border-2 border-black bg-gray-500 p-2 text-4xl text-white">
	<button on:click={back}> &larr; </button>
	<button>R</button>
	<button on:click={forward}>&rarr;</button>
</div>
