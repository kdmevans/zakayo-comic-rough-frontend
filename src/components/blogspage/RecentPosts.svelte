<script lang="ts">



	import type { Blog } from '$lib/types/Blog.interface';
	import RecentPostCard from "./RecentPostCard.svelte";
	import SearchBar from './SearchBar.svelte';

	let recentBlogs: Array<Blog> = [];

		recentBlogs = [

{
id: 1,
title: "Navigating the Tax Maze",
author: "Evans Maina",
coverImage: "/blogs/maze-cover-img.webp",
bgImage: "/blogs/maze-bg.webp",
avatar: "/blogs/maze-avatar.png"
   },
   {
	   id: 2,
title: "What is Tax?",
author: "Japheth Kosgei",
coverImage: "/blogs/tax-cover-img.png",
bgImage: "/blogs/tax-bg.webp",
avatar: "/blogs/tax-avatar.png"
   },

   {
	   id: 3,
title: "The Taxpayer's Dilemma?",
author: "Jonas Ojwang",
coverImage: "/blogs/dilema-cover-img.png",
bgImage: "/blogs/dilema-bg.png",
avatar: "/blogs/dilema-avatar.png"
   }
];

</script>


<div class="mb-6 py-4 md:px-6 px-2 rounded-xl ">
	<div class="lg:text-6xl text-4xl text-center">
		<h1
			class="poppins mb-8 mt-3 whitespace-nowrap golden-text  text-opacity-100 leading-none font-semibold"
		>
			Recent Posts
		</h1>
	</div>

	<div class="md:mb-16 mb-8">
		<SearchBar />
	</div>

	
		<div class="blog">
			{#each recentBlogs as recentBlog (recentBlog.id)}
				<RecentPostCard {recentBlog} />
			{/each}
		</div>
	
</div>





