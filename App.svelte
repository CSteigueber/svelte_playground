<script>
	import Nested from './Nested.svelte';
	let name = 'evil overlord';
	let value=name
	$:name=value

</script>
<Nested lord={name}/>
Do you wish to change your name dear Mr {name.toUpperCase()}?
<textarea bind:value></textarea>

