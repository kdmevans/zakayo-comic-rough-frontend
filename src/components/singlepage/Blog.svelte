
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
                    </div>
                
                    <div class="xl:col-span-2   md:col-span-3 w-full">
                        <BlogSidebar  />
                    </div>
                </div>
            </div>

                    </section>
    
    
    
    