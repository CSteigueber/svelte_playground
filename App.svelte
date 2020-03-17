<script>
	import {count} from './customStore.js';
	import {time, elapsed} from './readableStore.js';

	const formatter = new Intl.DateTimeFormat('en',{
		hour12: true,
		hour: 'numeric',
		minute:'2-digit',
		second: '2-digit'
	});


</script>

<h1>The count is {$count}</h1>
<button on:click={count.increment}>+</button>
<button on:click={count.decrement}>-</button>
<button on:click={count.reset}>reset</button>
<h2>The time is {formatter.format($time)}</h2>
<h3>This page has been open for {$elapsed} {$elapsed===1?'second':'seconds'} </h3>