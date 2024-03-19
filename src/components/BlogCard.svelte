<script lang="ts">
	import type { Blog } from '$lib/types/Blog.interface';
	export let blog: Blog;

</script>


<div class="w-full col-span-3 my-10 md:px-4 ">
    <a href="/blogs/1">
        <div class="blogCard ">
          <div class="wrapper ">
            <img src={blog.coverImage} class="cover-image" alt="cover-img" />
            <img src={blog.bgImage} class="top" alt="bg-img" />
          </div>
          <div class="title text-center" >
        <h1 class="text-white golden-text text-5xl md:text-6xl">{blog.title}</h1>

        <h1 class="text-white my-3 text-lg md:text-2xl"><span class="text-gray-200 poppins">by ~ </span> {blog.author}</h1>
        
        
        </div>
          <img src={blog.avatar} class="character" alt="character-img" />
        </div>
      </a>

    </div>

    