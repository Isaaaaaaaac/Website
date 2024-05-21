<script>
	let left = false;
	let right = false;
	let enterHouse = false;
	let walkPastHouse = false;
</script>

<div class="bg-slate-700 w-1/3 h-60 overflow-y-scroll">
	<p class="text-gray-50 p-3">
		You find yourself standing at the edge of a dense forest. The sun is setting, casting long
		shadows on the ground. In front of you, there are two paths.
	</p>
	<b class="text-gray-50 p-3">Which one do you choose?</b>
	<div class="p-3 px-8">
		<button on:click={() => (left = true)} class="text-gray-50 bg-slate-900 p-2 rounded-md"
			>Left path</button
		>
		<span class="p-5"></span>
		<button on:click={() => (right = true)} class="text-gray-50 bg-slate-900 p-2 rounded-md"
			>Right path</button
		>
	</div>

	{#if left == true}
		<p class="text-gray-50 p-3">
			You walk down the left path and soon come across an old, abandoned house. The door is slightly
			ajar.
		</p>
		<b class="text-gray-50 p-3">What do you do?</b>
		<div class="p-3 px-8">
			<button on:click={() => (enterHouse = true)} class="text-gray-50 bg-slate-900 p-2 rounded-md"
				>Enter the house</button
			>
			<span class="p-5"></span>
			<button
				on:click={() => (walkPastHouse = true)}
				class="text-gray-50 bg-slate-900 p-2 rounded-md">Continue walking past the house</button
			>
		</div>
	{:else if right == true}
		<p class="text-gray-50 p-3">A bear finds u and eats u.</p>
	{/if}
</div>
