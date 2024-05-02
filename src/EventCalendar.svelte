<script>
    import { onMount, onDestroy } from "svelte";
    
    import { EventCalendar } from "@dhx/trial-eventcalendar";
    import "@dhx/trial-eventcalendar/dist/event-calendar.css";
    
    export let events;
    export let date;

    let container;
    onMount(() => {
        const eventCalendarInstance = new EventCalendar(container, {
            events, date
        })
    });
    onDestroy(async () => {
        eventCalendarInstance.destructor();
    });
</script>

<div bind:this={container} style="width: 100%; height: 100%;"></div>
