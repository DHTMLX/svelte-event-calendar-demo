<script>
	import EventCalendar from "./EventCalendar.svelte";
	import { getData } from "./data.js";
</script>

<EventCalendar events={getData()} date={new Date(2024, 5, 10)} />
