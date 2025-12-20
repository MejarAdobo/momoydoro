<script lang="ts">
    import Timer from "$lib/components/Timer.svelte";
    let timerLength = 25;
    let timerName = "Pomodoro";
</script>

<Timer {timerLength} {timerName} />
