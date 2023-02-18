<script>
	let count = 0;

	function incrementCount() {
		// event handler code goes here
		count += 1;
	}

    // reactive value 
	$: doubled = count * 2;

    $: if (count >= 10) {
		alert('count is dangerously high!');
		count = 9;
	}
</script>

<button on:click={incrementCount}>
	Clicked {count} {count === 1 ? 'time' : 'times'}
</button>

<p>{count} doubled is {doubled}</p>