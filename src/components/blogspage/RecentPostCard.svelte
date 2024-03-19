<script lang="ts">
	import type { Blog } from '$lib/types/Blog.interface';
	export let recentBlog: Blog;

</script>


<div class="w-full col-span-3 my-20  ">
    <a href="/blogs/1">
        <div class="blogCard ">
          <div class="wrapper ">
            <img src={recentBlog.coverImage} class="cover-image" alt="cover-img" />
            <img src={recentBlog.bgImage} class="top" alt="bg-img" />
          </div>
          <div class="title text-center" >
        <h1 class="text-white golden-text text-5xl lg:text-6xl">{recentBlog.title}</h1>

        <h1 class="text-white my-3 text-lg lg:text-2xl"><span class="text-gray-200 poppins">by ~ </span> {recentBlog.author}</h1>
        
        
        </div>
          <img src={recentBlog.avatar} class="recent-character" alt="character-img" />
        </div>
      </a>

    </div>
