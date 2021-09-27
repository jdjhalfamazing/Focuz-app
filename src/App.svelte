<script>
	let todos = [
		{ done: false, text: 'Women' },
		{ done: false, text: 'Pornography' },
		{ done: false, text: 'TV/Movies' },
		{ done: false, text: 'Gossiping' },
		{ done: false, text: 'Online Dating' },
		{ done: false, text: 'Binge Eating' },
		{ done: false, text: 'Binge Youtubing' },
		{ done: false, text: 'Social Media' },
		{ done: false, text: 'Sports' }
	];

	function add() {
		todos = todos.concat({ done: false, text: '' });
	}

	function clear() {
		todos = todos.filter(t => !t.done);
	}
	function unclear() {
		todos = todos.filter(t => t.done);
	}

	$: remaining = todos.filter(t => !t.done).length;




	let todos1 = [
		{ done: false, text: 'Procrastination' },
		{ done: false, text: 'Focus' },
		{ done: false, text: 'Style' },
		{ done: false, text: 'Impressing People' },
		{ done: false, text: 'Overthinking' },
		{ done: false, text: 'Complaining' },
		{ done: false, text: 'Workethic' },
		{ done: false, text: 'Worrying' },
		{ done: false, text: 'Getting In Shape' },
		{ done: false, text: 'Socializing' },

	];

	function add1() {
		todos1 = todos1.concat({ done: false, text: '' });
	}

	function clear1() {
		todos1 = todos1.filter(t => !t.done);
	}
	function unclear1() {
		todos1 = todos1.filter(t => t.done);
	}

	$: remaining = todos1.filter(t => !t.done).length;

	
	let todos2 = [
		{ done: false, text: '"I Am Brave Enough To Chances"'},
		{ done: false, text: '"I Can Handle Anything That Comes My Way"' },
		{ done: false, text: '"I Am Strong And Powerful"' },
		{ done: false, text: '"I Am Capable Of Achieving My Goals"' },
		{ done: false, text: '"My Confidence Continues To Grow"' },
		{ done: false, text: '"I Believe In Myself"' },
		{ done: false, text: '"My Abilities Are Limitless"' },
		{ done: false, text: '"I Am Creating The Life Of My Dreams"' },
	
	];

	function add2() {
		todos2 = todos2.concat({ done: false, text: '' });
	}

	function clear2() {
		todos2 = todos2.filter(t => !t.done);
	}
	function unclear2() {
		todos2 = todos2.filter(t => t.done);
	}

	$: remaining = todos2.filter(t => !t.done).length;

	let todos3 = [
		{ done: false, text: 'Proving People Wrong' },
		{ done: false, text: 'Affording More Steaks' },
		{ done: false, text: 'Owning House' },
		{ done: false, text: 'New Car' },
		{ done: false, text: 'Respect' }
		
	];

	function add3() {
		todos3 = todos3.concat({ done: false, text: '' });
	}

	function clear3() {
		todos3 = todos3.filter(t => !t.done);
	}
	function unclear3() {
		todos3 = todos3.filter(t => t.done);
	}

	$: remaining = todos3.filter(t => !t.done).length;
	
	
	
	</script> 


<div class="box1">
	<h2> FOCUZ </h2>
<h1> What are the distractions you need to avoid? </h1>

{#each todos as todo}
	<div class:done={todo.done}>
		<input
			type=checkbox 
			bind:checked={todo.done}
		>

		<input
			placeholder="Add A Distraction"
			bind:value={todo.text}
		>
	</div>

{/each}

<p>{remaining} remaining</p>

<button on:click={add}>
	Add New Distraction
</button>

<button on:click={clear}>
	Delete Checked Distractions
</button>

<button on:click={unclear}>
	Delete Unchecked Distractions
</button>


<div>

</div>

<h1> What do you need to work on? </h1>

{#each todos1 as todo}
	<div class:done={todo.done}>
		<input
			type=checkbox
			bind:checked={todo.done}
		>

		<input
			placeholder="Add A Distraction"
			bind:value={todo.text}
		>
	</div>
{/each}

<p>{remaining} remaining</p>

<button on:click={add1}>
	Add Improvment
</button>

<button on:click={clear1}>
	Delete Checked Improvements
</button>

<button on:click={unclear1}>
	Delete Unchecked Improvements
</button>


<h1> What are your affirmations? </h1>

{#each todos2 as todo}
	<div class:done={todo.done}>
		<input
			type=checkbox
			bind:checked={todo.done}
		>

		<input
			placeholder="Add A Desire"
			bind:value={todo.text}
		>
	</div>
{/each}

<p>{remaining} remaining</p>

<button on:click={add2}>
	Add An Affirmation
</button>

<button on:click={clear2}>
	Delete Checked Affirmation
</button>

<button on:click={unclear2}>
	Delete Unchecked Affirmation
</button>


<h1> What motivates you? </h1>

{#each todos3 as todo}
	<div class:done={todo.done}>
		<input
			type=checkbox
			bind:checked={todo.done}
		>

		<input
			placeholder="Add A Motivator"
			bind:value={todo.text}
		>
	</div>
{/each}

<p>{remaining} remaining</p>

<button on:click={add3}>
	Add A Motivator
</button>

<button on:click={clear3}>
	Delete Checked Motivators
</button>

<button on:click={unclear3}>
	Delete Unchecked Motivators
</button>
</div>

<style>
	
	.box1{
	 background-image: linear-gradient(to right,lightblue,lightgray);

	margin-left: 0px;
	padding-top: 0px;
	padding-right: -330px;
	margin-right: 750px;
	}  
	input{
		min-width:300px;
		max-width:300px;
		padding-right: 0px;
		margin-right: -141px;
		background-color: royalblue;
		color: white;
	
		

	}
	
h2{
	text-align: center;
	color:white;
}
	
h1{
	text-align: center;
	color: midnightblue;
}
	

</style>