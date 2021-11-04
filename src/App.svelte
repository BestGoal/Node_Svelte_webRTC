<script>
	import { Router, Link, Route } from "svelte-routing";
	import Home from "./Home.svelte";
	import Video from "./Video.svelte";
	export let url = "http://localhost:5000";
</script>

<Router url="{url}">
	<header>
		<h1>History</h1>

		<nav>
			<Link to="/">Home</Link>
			<Link to="video">Video</Link>
		</nav>
	</header>

	<main>
		<Route path="/" component={Home} />
		<Route path="/video" component={Video} />
	</main>
</Router>
