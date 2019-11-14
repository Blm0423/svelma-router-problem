<!-- App.svelte -->
<script>
	import { Router, Link, Route } from "svelte-routing";
// import NavLink from "./components/NavLink.svelte";
// import { Home, About, Blog, BlogPost } from "./routes";

import 'bulma/css/bulma.css';
import '@fortawesome/fontawesome-free/css/all.css';

import Home from "./routes/home.svelte";
import About from "./routes/about.svelte";
import Blog from "./routes/blog.svelte";	
// import BlogPost from "./routes/blogbost.svelte";	

  export let url = "";
</script>

<Router url="{url}">
  <nav>
    <Link to="/">Home</Link>
    <Link to="about">About</Link>
    <Link to="blog">Blog</Link>
  </nav>
	<hr>
  <div>
    <!-- <Route path="blog/:id" component="{BlogPost}" /> -->
    <Route path="blog" component="{Blog}" />
    <Route path="about" component="{About}" />
    <Route path="/"><Home /></Route>
  </div>
</Router>

<hr>

<ol>
  <li>Växla mellan <strong>Home</strong> och <strong>About</strong> - det funkar perfekt</li>
  <li>Välj <strong>Blog</strong>, så kommer den sidan ligga kvar även om URL i browser ändras.</li>
	<li>Det går  att göra refresh i browsern, så kommer rätt sida fram.</li>
</ol>

<hr>

<p>https://github.com/c0bra/svelma</p>
<p>https://c0bra.github.io/svelma/components/field</p>