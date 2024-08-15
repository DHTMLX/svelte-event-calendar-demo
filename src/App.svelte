<script>
	import EventCalendar from "./EventCalendar.svelte";
	import { getData } from "./data.js";

	const events = getData();
</script>

<EventCalendar events={events} date={new Date(2024, 5, 10)} />
