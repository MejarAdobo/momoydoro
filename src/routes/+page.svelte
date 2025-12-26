<script lang="ts">
	import Timer from '../lib/components/timer/Timer.svelte';
	import { Settings } from '@lucide/svelte';
</script>

<div class="p-4">
	<!-- title and the setting icon -->
	<div class="flex justify-between py-2">
		<p class="text-2xl font-semibold text-neutral-950">Momoydoro</p>
		<Settings class="hover:text-neutral-500" />
	</div>

	<!-- timer -->
	<Timer />
</div>
