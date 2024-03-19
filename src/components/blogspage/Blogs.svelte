<script lang="ts">

import type { Blog } from '$lib/types/Blog.interface';
import BlogsCard from "./BlogsCard.svelte";


let blogs: Array<Blog> = [];

    blogs = [

{
id: 1,
title: "Navigating the Tax Maze",
author: "Evans Maina",
coverImage: "blogs/maze-cover-img.webp",
bgImage: "blogs/maze-bg.webp",
avatar: "blogs/maze-avatar.png"
   },
   {
	   id: 2,
title: "What is Tax?",
author: "Japheth Kosgei",
coverImage: "blogs/tax-cover-img.png",
bgImage: "blogs/tax-bg.webp",
avatar: "blogs/tax-avatar.png"
   },

   {
	   id: 3,
title: "The Taxpayer's Dilemma?",
author: "Jonas Ojwang",
coverImage: "blogs/dilema-cover-img.png",
bgImage: "blogs/dilema-bg.png",
avatar: "blogs/dilema-avatar.png"
   },
   {
id: 4,
title: "Decode the Tax Puzzle",
author: "Evans Maina",
coverImage: "blogs/puzzle-cover-img.webp",
bgImage: "blogs/puzzle-bg.webp",
avatar: "blogs/puzzle-avatar.png"
   }
];


</script>


<section class=" md:pt-20 pt-10 overflow-hidden ">
	<div class="container px-3 mx-auto lg:px-4">
	
			<div class=" w-full mx-auto" >


    <div class="lg:flex justify-center">
        <div>
          
                <img  class="mx-auto rellax sm:block hidden" src="smile.gif" alt="Smiley">
           
        </div>
        <div  class="lg:text-7xl md:text-5xl sm:text-4xl text-2xl  text-center">
        
            <span 
            class="inline-block poppins mb-4 text-sm text-red-500 font-bold uppercase tracking-widest"
            >Blogs</span
        >
        <h2 
            class="font-heading rellax poppins mb-6 text-2xl sm:text-3xl md:text-5xl lg:text-6xl text-zinc-800 font-semibold tracking-tight"
        >
            Here are some<br />
            articles to guide you
        </h2>
            
        </div>
    </div>

    <div class="md:grid md:grid-cols-6  gap-6 blog mb-6 md:mt-24 mt-12">

	{#each blogs as blog (blog.id)}
							<BlogsCard {blog} />
						{/each}
		
					
</div>


<!-- Pagination -->

<div class="md:my-20 my-16">
    <ol class="flex justify-center poppins gap-1 text-xs font-medium">
        <li>
            <a
                href="/"
                class="transition ease-in-out duration-150 inline-flex h-9 w-9 sm:h-12 sm:w-12 items-center justify-center rounded-full border border-gray-100 bg-white text-gray-700 rtl:rotate-180 hover:scale-105 hover:bg-slate-50"
            >
                <span class="sr-only">Prev Page</span>
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:h-7 sm:w-7 h-3 w-3"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                >
                    <path
                        fill-rule="evenodd"
                        d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
                        clip-rule="evenodd"
                    />
                </svg>
            </a>
        </li>

        <li>
            <a
                href="/"
                class="transition ease-in-out duration-150 flex justify-center items-center h-9 w-9 sm:h-12 sm:w-12 sm:text-lg text-sm rounded-full border border-gray-100 bg-white text-center text-gray-700 hover:scale-105 hover:bg-slate-50"
            >
                1
            </a>
        </li>

        <li
            class="transition ease-in-out duration-150 flex justify-center items-center h-9 w-9 sm:h-12 sm:w-12 sm:text-lg text-sm rounded-full border-[#f23f00] bg-[#f23f00] text-white hover:scale-105"
        >
            2
        </li>

        <li>
            <a
                href="/"
                class="transition ease-in-out duration-150 flex justify-center items-center h-9 w-9 sm:h-12 sm:w-12 sm:text-lg text-sm rounded-full border border-gray-100 bg-white text-center text-gray-700 hover:scale-105 hover:bg-slate-50"
            >
                3
            </a>
        </li>

        <li>
            <a
                href="/"
                class="transition ease-in-out duration-150 flex justify-center items-center h-9 w-9 sm:h-12 sm:w-12 sm:text-lg text-sm rounded-full border border-gray-100 bg-white text-center text-gray-700 hover:scale-105 hover:bg-slate-50"
            >
                4
            </a>
        </li>

        <li>
            <a
                href="/"
                class="transition ease-in-out duration-150 inline-flex h-9 w-9 sm:h-12 sm:w-12 items-center justify-center rounded-full border border-gray-100 bg-white text-gray-700 rtl:rotate-180 hover:scale-105 hover:bg-slate-50"
            >
                <span class="sr-only">Next Page</span>
                <svg
                    xmlns="http://www.w3.org/2000/svg"
                    class="sm:h-7 sm:w-7 h-3 w-3"
                    viewBox="0 0 20 20"
                    fill="currentColor"
                >
                    <path
                        fill-rule="evenodd"
                        d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                        clip-rule="evenodd"
                    />
                </svg>
            </a>
        </li>
    </ol>
</div>



                </div>
                </div>
           
                </section>



