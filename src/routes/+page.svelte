<script>
	import Calendar from '@event-calendar/core';
	import DayGrid from '@event-calendar/day-grid';

	let plugins = [DayGrid];
	let options = {
		view: 'dayGridMonth',
		events: [
			{ title: 'test', start: new Date('2023-07-30T00:00:00'), end: new Date('2023-07-30T09:00:00'), backgroundColor: 'red' },
			{ title: 'test', start: new Date('2023-07-31T00:00:00'), end: new Date('2023-07-31T09:00:00'), backgroundColor: 'blue' },
		]
	};
	console.log(options.events); 
	// the events are avaliable server-side even when javascript is disabled client side,
	// the calendar just doesn't render them for some reason
</script>


<section>
	<Calendar {plugins} {options} />
</section>