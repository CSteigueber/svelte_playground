<script>
	import Nested from './Nested.svelte';
	let name = 'evil overlord';
	let count=0;
	let numbers=[1,2];
	$: if (count>10) {
		alert(`Mr ${name.toUpperCase()}, you already clicked 10 times. Let us reset the counter!`);
		count=0;
	}
	function handleClick(){
		numbers[numbers.length] =numbers.length + 1;
		count++;
	}
	$: sum=numbers.reduce((t,n)=> t+n,0);
</script>

<p>{numbers.join(' + ')} = {sum} </p>

<h1>Hello {name.toUpperCase()}!</h1>
<button on:click={handleClick}>
You, {name.toUpperCase()} clicked {count} {count===1? 'time':'times'}
</button>
<Nested lord={name}/>