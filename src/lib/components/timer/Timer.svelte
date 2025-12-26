<script lang="ts">
	import { Coffee, Utensils, Target, RotateCcw, Play, Pause, SkipForward } from '@lucide/svelte';

	let timerRunning = $state(false);
</script>

<div class="px-4 py-2">
	<div class=" flex flex-col items-center justify-center rounded-xl bg-neutral-500 p-2">
		<!-- navigation between each timer -->
		<div class="my-5 flex max-w-lg justify-center gap-2 rounded-xl bg-neutral-200 px-2 py-1">
			<button
				class="w-64 flex-1 rounded-xl py-1 transition duration-250 ease-in hover:bg-neutral-300 focus:bg-neutral-400"
			>
				<span class="flex items-center justify-center gap-2">
					<span class="text-lg font-medium">Focus</span>
					<Target />
				</span>
			</button>
			<button
				class="w-64 flex-1 rounded-xl py-1 transition duration-250 ease-in hover:bg-neutral-300 focus:bg-neutral-400"
			>
				<span class="flex items-center justify-center gap-2">
					<span class="text-lg font-medium">Short Break</span>
					<Coffee />
				</span>
			</button>
			<button
				class="w-64 flex-1 rounded-xl py-1 transition duration-250 ease-in hover:bg-neutral-300 focus:bg-neutral-400"
			>
				<span class="flex items-center justify-center gap-2">
					<span class="text-lg font-medium">Long Break</span>
					<Utensils />
				</span>
			</button>
		</div>

		<!-- timer -->
		<p class="my-25 text-9xl font-semibold">25:00</p>

		<!-- timer player -->
		<div class="my-5 flex gap-8">
			<button class="rounded-xl bg-neutral-300 p-4 hover:bg-neutral-200"
				><RotateCcw size={32} /></button
			>
			<button
				class="rounded-xl bg-neutral-200 p-4 hover:bg-green-200"
				onclick={() => (timerRunning = !timerRunning)}
			>
				{#if timerRunning}
					<Play size={32} />
				{:else}
					<Pause size={32} />
				{/if}
			</button>
			<button class="rounded-xl bg-neutral-300 p-4 hover:bg-neutral-200">
				<SkipForward size={32} />
			</button>
		</div>
	</div>
</div>
