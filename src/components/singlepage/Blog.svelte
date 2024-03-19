
<script lang="ts">
    import {gsap}  from "gsap/dist/gsap";        
    import {ScrollTrigger} from "gsap/dist/ScrollTrigger";
    import { onMount, onDestroy }   from 'svelte';
	import IllustrationCards from './IllustrationCards.svelte';
	import type { Illustration } from '$lib/types/Illustration.interface';
	import BlogSidebar from "../blogspage/BlogSidebar.svelte";
	import ResponsiveCard from "./ResponsiveCard.svelte";
    
    let illustrations: Array<Illustration> = [];
    
        illustrations = [
    
     {
    id: 1,
    cardType:"card-one",
    bgImage: "/single/intro.png",
        },
        {
            id: 2,
            cardType:"card-two",
    bgImage: "/single/c1.png",
        },
    
        {
            id: 3,
            cardType:"card-three",
    bgImage: "/single/c2.png",
        },
        {
            id: 4,
            cardType:"card-four",
    bgImage: "/single/c3.png",
        },
        {
            id: 5,
            cardType:"card-five",
    bgImage: "/single/c4.png",
        },

        {
            id: 6,
            cardType:"card-six",
    bgImage: "/single/c5.png",
        },

        {
            id: 7,
            cardType:"card-seven",
    bgImage: "/single/c6.png",
        }


    ];
    
    
    
    const init = () => {
        const tl = gsap.timeline({scrollTrigger:{
        trigger:"#main",
        // markers:true,
        start:"0% 10%",
        end:"+=300%",
        scrub:2,
        pin:true
    }});
            
            
            tl
    .to("#card-one",{top: "35%",},'a')
    .to("#card-two",{top: "130%"},'a')
    .to("#card-two",{top: "38%"},'b')
    .to("#card-one",{width: "65%", height: "65vh"},'b')
    .to("#card-three",{top: "130%"}, 'b')
    .to("#card-three",{top: "40%"}, 'c')
    .to("#card-two",{width: "70%",height: "70vh"},'c')
    .to("#card-four", { top: "130%" }, 'c')
    .to("#card-four", { top: "42%" }, 'd')
    .to("#card-three", { width: "75%", height: "75vh" }, 'd')
    .to("#card-five", { top: "130%" }, 'd')
    .to("#card-five", { top: "44%" }, 'e')
    .to("#card-four", { width: "80%", height: "80vh" }, 'e')
    .to("#card-six", { top: "130%" }, 'e')
    .to("#card-six", { top: "46%" }, 'f')
    .to("#card-five", { width: "85%", height: "85vh" }, 'f')
    .to("#card-seven", { top: "130%" }, 'f')
    .to("#card-seven", { top: "48%" }, 'g')
    .to("#card-six", { width: "90%", height: "90vh" }, 'g');
    
    
    };



    

    
    onMount(() => {
        
    gsap.registerPlugin(ScrollTrigger);
    init();
    });
    
    onDestroy(() => {
    ScrollTrigger.getAll().forEach(trigger => trigger.kill());
    });
    
    </script>
    
    
    <section class=" md:pt-20 pt-10 overflow-hidden ">
        <div class="container px-3 mx-auto lg:px-4">

            <h2 
            class="font-heading poppins text-3xl sm:text-4xl md:text-6xl lg:text-9xl golden-text font-semibold tracking-tight"
        >
        Yosef and the Tax Tango :<br />
       
        </h2>
        
               <div class=" w-full mx-auto hidden xl:block" id="main">
  
     
        {#each illustrations as illustration (illustration.id)}
                                <IllustrationCards {illustration} />
                            {/each}
            
                        
    
    
    
    
                    </div>


                    <div class=" block xl:hidden md:grid md:grid-cols-6  gap-6 blog mb-6 md:mt-24 mt-12" >
  
     
                        {#each illustrations as illustration (illustration.id)}
                                                <ResponsiveCard {illustration} />
                                            {/each}
                            
                                        
                    
                    
                    
                    
                                    </div>

                  </div>

                  <div class="sm:px-3 px-2 mx-auto lg:px-6 xl:container">
                   
                  <div class="md:grid md:grid-cols-7    xl:grid-cols-6   mt-24  mx-auto">
                    <div class=" xl:col-span-4  md:col-span-4 w-full">
                        <div class=" bg-white group rounded-3xl p-2 mb-24">
       
            
                            <div class="py-4 md:px-4">
                                <div class="md:flex justify-between items-center mt-5 poppins">
                                    <div class="flex items-center">

                                        <a
                    href="/"
                    class="bg-gray-100 mx-2 text-gray-800 hover:bg-gray-200 text-xs font-medium me-2 px-2.5 py-0.5 rounded"
                    >Individual Taxes</a
                >
                                       
                                        <div class="flex items-center ml-10">
                                            <i class="fas fa-user mr-2 text-indigo-500" />
                                            <div class="font-poppins text-sm text-neutral-500 text-opacity-100 font-semibold">
                                                Japheth 
                                            </div>
                                        </div>
                                    </div>
                                    <div class="flex items-center mt-5">
                                        <i class="fas fa-calendar mr-2 text-indigo-500" />
                                        <div class="font-poppins  text-sm text-neutral-500 text-opacity-100 font-semibold">
                                            18/03/2024
                                        </div>
                                    </div>
                                </div>
                    
                                <h3
                                    class="poppins md:mt-0 mt-3 transition ease-in-out duration-150   text-xl lg:text-2xl text-zinc-800 text-opacity-100 font-semibold"
                                >
                                Yosef and the Tax Tango
                                </h3>
                    
                       
                                <div>
                                 
                    
                                        <h1 class="text-gray-600 my-5">Scenario:</h1>
    
                                 
    
                                        <div class="poppins my-3 text-sm md:text-base text-gray-700">
                    
                                        <p class="my-5">Once upon a time, in a land not too different from our own, lived a man named Yosef. Yosef was known far and wide, not for his dance moves (which were admittedly lacking), nor for his culinary skills (unless you count burning water as a skill), but for his unparalleled ability to wiggle his way out of paying taxes. In a community where taxes were as certain as the daily sunrise, Yosef's escapades became the stuff of legend.
                                        </p>
    
                                        <p class="my-5">
                                            Yosef, a man with a smile as charming as his wits were sharp, had a knack for finding the most creative loopholes in the tax code. If there was a way to pay less, Yosef knew it. From claiming his pet goat as a dependent to registering his tiny balcony as agricultural land because of the one struggling tomato plant, Yosef did it all. He was not just dodging taxes; he was doing the tango around them.
                                        </p>
                                        <p class="my-5">
                                            The local tax office, exasperated by Yosef's antics, could only shake their heads in disbelief. "Yosef," they'd sigh, "why must you make our jobs so difficult?" But deep down, they couldn't help but admire his ingenuity (and secretly wished they knew his tricks for their own tax returns).

                                        </p>

<div class="lg:flex mx-auto">
<div class="lg:w-2/6 w-full">
    <img src="/blogs/puzzle-avatar.png" alt="" />
    
                                                    </div>
                                               
                                        <div class="lg:w-4/6 w-full">
                                            <p class="my-5">
                                                One sunny afternoon, as Yosef was sipping on his chai, boasting to his neighbor about his latest exploit of importing "invisible" goods to avoid import taxes, his luck finally ran out. A new tax officer, Ms. Njeri, had been assigned to his case. Ms. Njeri, armed with a sharp mind and zero tolerance for tax evasion, was about to give Yosef a run for his money.
                                               </p>

                                               <p class="my-5">
                                                Unbeknownst to Yosef, Ms. Njeri had been studying his case for months. With a knock on his door, Yosef's world of tax evasion came crashing down. Ms. Njeri, with a smile that mirrored Yosef's own cunning grin, presented him with a bill—a compilation of all the taxes he had dodged, plus fines. The amount made Yosef's head spin, and for the first time, his witty retorts failed him.
                                            </p>

                                            <div class="p-10 text-black italic bg-[#F8F7F7]">
                                                <span><i class="fa fa-quote-left text-6xl text-gray-700"></i></span>
                                                <p class="my-5 serif-4">
                                                    Yosef, realizing the jig was up, had no choice but to pay up. But Ms. Njeri, in a surprising turn of events, offered him an alternative. Yosef could reduce his fines by becoming an advocate for tax education, using his cunning and creativity for good. Reluctantly, Yosef agreed, finding himself on the other side of the tax tango.
                                                    </p>
<p class="text-end"> <span><i class="fa fa-quote-right  text-6xl text-gray-700"></i></span></p>
                                                   
    
                                            </div>
            
                                            </div>

                 </div>

                 <p class="my-5">
                    Yosef, realizing the jig was up, had no choice but to pay up. But Ms. Njeri, in a surprising turn of events, offered him an alternative. Yosef could reduce his fines by becoming an advocate for tax education, using his cunning and creativity for good. Reluctantly, Yosef agreed, finding himself on the other side of the tax tango.
                    </p>
                                       
                                      
                                        <p class="my-5">
                                            As Yosef began to educate his fellow citizens on the importance of taxes—how they paved the roads, kept the lights on, and made the community a better place—he found a new sense of purpose. His narrations, filled with humor and tales of his own misadventures, made taxes seem less like a burden and more like a responsibility that, if shared fairly, could lead to prosperity for all.
                                        </p>
                                        <p class="my-5">
                                            In the end, Yosef learned that while dodging taxes might save you money in the short term, it's the community that pays the price. And so, with a new lease on life and a slightly lighter wallet, Yosef became an unlikely hero in the world of taxes. His story, "Yosef and the Tax Tango," became a beloved tale, reminding everyone that while no one loves to pay taxes, avoiding them is a dance that's better left unperformed.
                                        </p>
                                   

                                   
                                </div>
                                </div>
                            </div>
                     
    
    
    
                        </div>



                        <div class=" p-4 bg-white   rounded-3xl relative   mt-12   shadow-lg   mx-auto">
                            <div class="flex items-center justify-between m  w-full md:p-3">
                                <div class="flex  ">
                                   <div class="">
                                        <h1 class="font-bold   md:text-3xl text-sm">Comments</h1>
    
                                    </div>
                                </div>
    
    
                             
                            </div>
    
                            <div class="flex flex-row items-center  rounded-xl  w-full  my-3">
                                <div>
                                    <img class="w-12 h-12  border-2 border-gray-300 rounded-full" alt="avatar" src="https://images.unsplash.com/photo-1519699047748-de8e457a634e?q=80&w=2080&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
                                </div>
                                <div class="flex-grow ml-4">
                                    <div class="relative w-full">
                                        <input type="text" class="flex w-full border rounded-xl focus:outline-none focus:border-indigo-300 pl-4 h-10" />
                                        <button class="absolute flex items-center justify-center h-full w-12 right-0 top-0 text-gray-400 hover:text-gray-600">
                                            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                                            </svg>
                                        </button>
                                    </div>
                                </div>
                                <div class="ml-4">
                                    <button class="flex items-center justify-center bg-indigo-500 hover:bg-indigo-600 rounded-xl text-white px-4 py-1 flex-shrink-0">
    
                                        <span class="ml-2">
                                            <svg class="w-4 h-4 transform rotate-45 -mt-px" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"></path>
                                            </svg>
                                        </span>
                                    </button>
                                </div>
                            </div>
    
                            <div class=" mx-auto mt-3">
    
                                <div class="flex-col w-full py-4 mx-auto  border-b-2 border-r-2 border-gray-200 sm:px-4 sm:py-4 md:px-4 sm:rounded-lg sm:shadow-sm ">
                                    <div class="flex flex-row">
                                        <img class="object-cover w-12 h-12 border-2 border-gray-300 rounded-full" alt="avatar" src="https://images.unsplash.com/photo-1522529599102-193c0d76b5b6?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
                                        <div class="flex-col mt-1">
                                            <div class="flex items-center flex-1 px-4 font-bold leading-tight">Adrian Kimani
                                                <span class="ml-2 text-xs font-normal text-gray-500 ">2 weeks ago</span>
                                            </div>
                                            <div class="flex-1 px-2 ml-2 text-sm font-medium leading-loose text-gray-600 ">Wow!!! this is amazing
                                            </div>
                                            <button class="inline-flex items-center px-1 pt-2 ml-1 flex-column">
                                                <svg class="w-5 h-5 ml-2 text-gray-600 cursor-pointer fill-current hover:text-gray-900 " viewBox="0 0 95 78" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M29.58 0c1.53.064 2.88 1.47 2.879 3v11.31c19.841.769 34.384 8.902 41.247 20.464 7.212 12.15 5.505 27.83-6.384 40.273-.987 1.088-2.82 1.274-4.005.405-1.186-.868-1.559-2.67-.814-3.936 4.986-9.075 2.985-18.092-3.13-24.214-5.775-5.78-15.377-8.782-26.914-5.53V53.99c-.01 1.167-.769 2.294-1.848 2.744-1.08.45-2.416.195-3.253-.62L.85 30.119c-1.146-1.124-1.131-3.205.032-4.312L27.389.812c.703-.579 1.49-.703 2.19-.812zm-3.13 9.935L7.297 27.994l19.153 18.84v-7.342c-.002-1.244.856-2.442 2.034-2.844 14.307-4.882 27.323-1.394 35.145 6.437 3.985 3.989 6.581 9.143 7.355 14.715 2.14-6.959 1.157-13.902-2.441-19.964-5.89-9.92-19.251-17.684-39.089-17.684-1.573 0-3.004-1.429-3.004-3V9.936z" fill-rule="nonzero" />
                                                </svg>
                                            </button>
                                            <button class="inline-flex items-center px-1 -ml-1 flex-column">
                                                <svg class="w-5 h-5 text-gray-600  cursor-pointer hover:text-gray-700" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 10h4.764a2 2 0 011.789 2.894l-3.5 7A2 2 0 0115.263 21h-4.017c-.163 0-.326-.02-.485-.06L7 20m7-10V5a2 2 0 00-2-2h-.095c-.5 0-.905.405-.905.905 0 .714-.211 1.412-.608 2.006L7 11v9m7-10h-2M7 20H5a2 2 0 01-2-2v-6a2 2 0 012-2h2.5">
                                                    </path>
                                                </svg>
                                            </button>
                                        </div>
                                    </div>
                                    <hr class="my-2 ml-16 border-gray-200">
                                    <div class="flex flex-row pt-1 md-10 md:ml-16">
                                        <img class="w-12 h-12 border-2 border-gray-300 rounded-full" alt="avatar" src="https://images.unsplash.com/photo-1519699047748-de8e457a634e?q=80&w=2080&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
                                        <div class="flex-col mt-1">
                                            <div class="flex items-center flex-1 px-4 font-bold leading-tight">Emily
                                                <span class="ml-2 text-xs font-normal text-gray-500 ">5 days ago</span>
                                            </div>
                                            <div class="flex-1 px-2 ml-2 text-sm font-medium leading-loose text-gray-600 ">Exactly this is amazing
                                            </div>
                                            <button class="inline-flex items-center px-1 pt-2 ml-1 flex-column">
                                                <svg class="w-5 h-5 ml-2 text-gray-600 cursor-pointer fill-current hover:text-gray-900 " viewBox="0 0 95 78" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M29.58 0c1.53.064 2.88 1.47 2.879 3v11.31c19.841.769 34.384 8.902 41.247 20.464 7.212 12.15 5.505 27.83-6.384 40.273-.987 1.088-2.82 1.274-4.005.405-1.186-.868-1.559-2.67-.814-3.936 4.986-9.075 2.985-18.092-3.13-24.214-5.775-5.78-15.377-8.782-26.914-5.53V53.99c-.01 1.167-.769 2.294-1.848 2.744-1.08.45-2.416.195-3.253-.62L.85 30.119c-1.146-1.124-1.131-3.205.032-4.312L27.389.812c.703-.579 1.49-.703 2.19-.812zm-3.13 9.935L7.297 27.994l19.153 18.84v-7.342c-.002-1.244.856-2.442 2.034-2.844 14.307-4.882 27.323-1.394 35.145 6.437 3.985 3.989 6.581 9.143 7.355 14.715 2.14-6.959 1.157-13.902-2.441-19.964-5.89-9.92-19.251-17.684-39.089-17.684-1.573 0-3.004-1.429-3.004-3V9.936z" fill-rule="nonzero" />
                                                </svg>
                                            </button>
                                            <button class="inline-flex items-center px-1 -ml-1 flex-column">
                                                <svg class="w-5 h-5 text-gray-600 cursor-pointer hover:text-gray-700 " xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor">
                                                    <path d="M2 10.5a1.5 1.5 0 113 0v6a1.5 1.5 0 01-3 0v-6zM6 10.333v5.43a2 2 0 001.106 1.79l.05.025A4 4 0 008.943 18h5.416a2 2 0 001.962-1.608l1.2-6A2 2 0 0015.56 8H12V4a2 2 0 00-2-2 1 1 0 00-1 1v.667a4 4 0 01-.8 2.4L6.8 7.933a4 4 0 00-.8 2.4z" />
                                                </svg>
                                            </button>
                                        </div>
                                    </div>
                                </div>
    
                                <div class="flex-col w-full py-4 mx-auto mt-3  border-b-2 border-r-2 border-gray-200 sm:px-4 sm:py-4 md:px-4 sm:rounded-lg sm:shadow-sm ">
                                    <div class="flex flex-row md-10">
                                        <img class="w-12 h-12 border-2 border-gray-300 rounded-full" alt="avatar" src="https://plus.unsplash.com/premium_photo-1661255367848-a4a29983bc2e?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D">
                                        <div class="flex-col mt-1">
                                            <div class="flex items-center flex-1 px-4 font-bold leading-tight">Mark Kuria
                                                <span class="ml-2 text-xs font-normal text-gray-500  ">3 days ago</span>
                                            </div>
                                            <div class="flex-1 px-2 ml-2 text-sm font-medium leading-loose text-gray-600 ">Amazing story indeed
                                            </div>
                                            <button class="inline-flex items-center px-1 pt-2 ml-1 flex-column">
                                                <svg class="w-5 h-5 ml-2 text-gray-600 cursor-pointer fill-current hover:text-gray-900 " viewBox="0 0 95 78" xmlns="http://www.w3.org/2000/svg">
                                                    <path d="M29.58 0c1.53.064 2.88 1.47 2.879 3v11.31c19.841.769 34.384 8.902 41.247 20.464 7.212 12.15 5.505 27.83-6.384 40.273-.987 1.088-2.82 1.274-4.005.405-1.186-.868-1.559-2.67-.814-3.936 4.986-9.075 2.985-18.092-3.13-24.214-5.775-5.78-15.377-8.782-26.914-5.53V53.99c-.01 1.167-.769 2.294-1.848 2.744-1.08.45-2.416.195-3.253-.62L.85 30.119c-1.146-1.124-1.131-3.205.032-4.312L27.389.812c.703-.579 1.49-.703 2.19-.812zm-3.13 9.935L7.297 27.994l19.153 18.84v-7.342c-.002-1.244.856-2.442 2.034-2.844 14.307-4.882 27.323-1.394 35.145 6.437 3.985 3.989 6.581 9.143 7.355 14.715 2.14-6.959 1.157-13.902-2.441-19.964-5.89-9.92-19.251-17.684-39.089-17.684-1.573 0-3.004-1.429-3.004-3V9.936z" fill-rule="nonzero" />
                                                </svg>
                                            </button>
                                            <button class="inline-flex items-center px-1 -ml-1 flex-column">
                                                <svg class="w-5 h-5 text-gray-600 cursor-pointer hover:text-gray-700 " fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                                                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 10h4.764a2 2 0 011.789 2.894l-3.5 7A2 2 0 0115.263 21h-4.017c-.163 0-.326-.02-.485-.06L7 20m7-10V5a2 2 0 00-2-2h-.095c-.5 0-.905.405-.905.905 0 .714-.211 1.412-.608 2.006L7 11v9m7-10h-2M7 20H5a2 2 0 01-2-2v-6a2 2 0 012-2h2.5">
                                                    </path>
                                                </svg>
                                            </button>
                                        </div>
                                    </div>
                                </div>
    
                            </div>
    
                        </div>
    
    
                    </div>
                
                    <div class="xl:col-span-2   md:col-span-3 w-full">
                        <BlogSidebar  />
                    </div>
                </div>
            </div>

                    </section>
    
    
    
    