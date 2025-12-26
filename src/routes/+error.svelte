<script lang="ts">
	import { page } from '$app/state';
	import { goto } from '$app/navigation';
</script>

{#if page.error}
	<!-- display the status code -->
	<div class="flex items-center justify-center">
		<p class="text-center text-8xl font-semibold text-neutral-950">{page.status}</p>
	</div>

	<div class="flex flex-col">
		<!-- display different messages depending on the status code -->
		{#if page.status === 404}
			<p class="text-center text-lg font-medium text-neutral-950">This page does not exist</p>
		{:else}
			<!-- Will put other status code -->
		{/if}

		<!-- return user into the home page -->
		<button
			class="text-semibold mx-auto mt-2 rounded-xl bg-blue-500 px-4 py-2 text-lg text-neutral-100 hover:bg-blue-600"
			onclick={goto('/')}
			>Return to Home
		</button>
	</div>
{/if}
