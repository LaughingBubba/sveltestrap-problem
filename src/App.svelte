<script>
	export let name;
	import Hello from './Hello.svelte'
	import Home from './Home.svelte'
	import {Router, Route, Link, navigate} from 'svelte-routing'
</script>

<Router>
	<Route exact path="/" component={Home} />
	<Route exact path="/hello">
		<Hello name={"Mundo"}/>
	</Route>
</Router>