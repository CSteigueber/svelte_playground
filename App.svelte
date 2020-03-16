<script>
	let name = 'evil overlord';
	let count=0;
	$: if (count>10) {
		alert(`Mr ${name.toUpperCase()}, you already clicked 10 times. Let us reset the counter!`);
		count=0;
	}
	function handleClick(){
		count++;
	}
</script>

<h1>Hello {name.toUpperCase()}!</h1>
<button on:click={handleClick}>
You, {name.toUpperCase()} clicked {count} {count===1? 'time':'times'}
</button>