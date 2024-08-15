<script>
    import { onMount, onDestroy } from "svelte";
    import { EventCalendar } from "@dhx/trial-eventcalendar";
    import "@dhx/trial-eventcalendar/dist/event-calendar.css";
    
    export let events;
    export let date;

    let container;
    let calendar;

    onMount(() => {
        calendar = new EventCalendar(container, {
            //events, 
            //date
        })

        calendar.api.on("add-event", (obj) => {
            console.log(obj);
        });
    });
    onDestroy(() => {
        calendar.destructor();
    });
</script>

<div bind:this={container} style="width: 100%; height: 100%;"></div>
