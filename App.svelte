<script>
	import {count} from './store.js';
	import {time, elapsed} from './readableStore.js';
	import Incrementer from './Incrementer.svelte';
	import Decrementer from './Decrementer.svelte';
	import Resetter from './Resetter.svelte';

	const formatter = new Intl.DateTimeFormat('en',{
		hour12: true,
		hour: 'numeric',
		minute:'2-digit',
		second: '2-digit'
	});


</script>

<h1>The count is {$count}</h1>
<Incrementer/> 
<Decrementer/>
<Resetter/>
<h2>The time is {formatter.format($time)}</h2>
<h3>This page has been open for {$elapsed} {$elapsed===1?'second':'seconds'} </h3>