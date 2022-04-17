<script>
	let count = 0;
	$: doubled = count * 2;
	function handleClick() {
		count += 1;
	}
</script>

<button on:click={handleClick}>
	{count} click {count === 1 ? 'time' : 'times'} , but doubled is {doubled}
</button>