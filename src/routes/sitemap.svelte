<script>
var sitemap = {
  "Main": [
    {path: ".", title: "Home"},
    {path: "about", title: "About"},
    {path: "policies", title: "Policies"},
    {path: "sitemap", title: "Sitemap"}
  ],
  "WhiteHorse": [
    {path: "https://whitehorse.swavesey.app", title: "Home"},
    {path: "https://whitehorse.swavesey.app/menu", title: "Menu"}
  ]
}

</script>

<style>
.row {
  display: flex;
  flex-wrap: wrap;
}

.column {
  flex: 1;
  min-width: 15rem;
}
.column ul li a {
  text-decoration: none!important;
}
.column ul li a:hover {
  background-color: #FFFF00;
}
</style>

<svelte:head>
	<title>Swavesey - Sitemap</title>
</svelte:head>

<h1>Sitemap</h1>

<div class="row">
  {#each Object.entries(sitemap) as [category, links]}
  <div class="column">
    <h2>{category}</h2>
    <ul>
      {#each links as link}
      <li><a href="{link.path}">{link.title}</a></li>
      {/each}
    </ul>
  </div>
  {/each}
</div>
