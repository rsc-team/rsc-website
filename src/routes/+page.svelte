<script>
   let sponsors = [
      {url:"/sponsors/rusoe.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/airtech.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/badger.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/bayarea.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/climate.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/endurans.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/gobain.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/gs.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/komo.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/lockheed.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/maxeon.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/mrg.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/pcbway.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/pmc.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/tripower.png",alt:"Rutgers School of Eningeering"},
      {url:"/sponsors/viking.png",alt:"Rutgers School of Eningeering"}
      
   ]

   // Work in progress!
   let canvas;
   let ctx;
   const clipPath = [10, 0, 90, 0, 100, 10, 100, 90, 90, 100, 10, 100, 0, 90, 0, 10]

   function draw(delta) {
      ctx.globalCompositeOperation = "destination-over";
      ctx.clearRect(0, 0, 300, 300); // clear canvas

      /*ctx.fillStyle = 'white';
      
      ctx.fillRect(0,25,25,25);*/

      window.requestAnimationFrame(draw);
   }

   $effect(()=>{
      ctx = canvas.getContext("2d");

      window.requestAnimationFrame(draw);
   })

</script>

<div class="h-full w-full align-middle bg-navy">

   <!-- Logo/Welcome Screen -->
   <div class="relative w-full h-150 lg:h-200 drop-shadow-lg">
      <div class="absolute z-2 user-none w-full h-full max-w-content"> </div>
      <video class="absolute user-none w-full h-full object-cover brightness-50 overflow-hidden" autoplay muted loop>
         <source src="assets/tempbg.mp4" type="video/mp4">
      </video>
      <div class="relative max-w-content justify-center z-2 w-auto top-[50%] translate-y-[-50%] lg:translate-y-[-50%] mx-auto">
         <img class="hidden" src="assets/rscsplash.png" alt="Rutgers Solar Car Logo">
         <p class="text-center  text-red font-sweetsquare font-black drop-shadow-logo text-4xl lg:text-5xl sm:text-5xl ">
            Making fast, sustainable, solar-powered cars
         </p>
      </div>
   </div>


   <!-- About the team -->
   <div class="drop-shadow-lg items-center  overflow-hidden w-full h-250 xl:h-200  bg-gray-600 bg-[url(/assets/sidgrind.webp)]  bg-blend-multiply  bg-position-[13%_70%] bg-no-repeat lg:bg-position-[20%_75%] xl:bg-cover xl:bg-position-[20%_95%] 2xl:bg-position[20%_10%]  flex flex-col justify-center">
      <div class="flex items-center align-middle mt-50 lg:-mt-20 flex-nowrap  flex-col-reverse lg:flex-row xl:pr-25 h-full w-full xl:max-w-content justify-center">
         <img src="assets/sun.webp" alt="Rutgers Solar Car Sun" class="relative top-20 sm:static  xl:static self-center  w-100 h-100">
         <div class="w-full text-xl xl:text-4xl sm:text-3xl flex flex-col self-center mt-20 justify-center text-left p-10 xl:w-200 sm:w-150  drop-shadow-small lg:drop-shadow-med  text-white font-sweetsquare font-black ">
            <p class="pb-15">
               <span class="text-red">Rutgers Solar Car</span> is a nonprofit, passionate, student-led organization committed to advancing innovation, sustainability, and collaboration in solar-powered vehicle development
            </p>
            <p>
               Through the design, manufacturing, and testing of solar vehicles, we work on developing competitive, road-legal, fully solar-powered race cars.
            </p>
            <a href="/team" class="mt-10 h-10 transition-all not-hover:drop-shadow-logo xl:order-3 self-center w-65">
               <button class="transition-all hover:text-navy text-white  hover:bg-white cursor-pointer p-3 w-full font-black  bg-red text-4xl solar-clip-rectangle">
                  <p class="w-full h-full transition-all  group-hover:drop-shadow-med">Learn More</p>
               </button>
            </a> 
         </div>
      </div>
   </div>

   <!-- Sponsors Preview -->
   <div class="flex flex-col overflow-hidden h-50 bg-navy place-content-center">
      <p class="font-black text-gold text-center pb-5 text-2xl drop-shadow-med">Backed by trusted sponsors</p>
      <div class="self-center relative overflow-hidden whitespace-nowrap  max-w-content [mask-image:_linear-gradient(to_right,_transparent_0,_white_128px,white_calc(100%-128px),_transparent_100%)]">
         {#each {length:2} as _, i}
            <div class="inline-block animate-scrolling w-max">
               {#each sponsors as sponsor}
                  <img class="mx-4 inline h-25" src={sponsor.url} alt={sponsor.alt}>
               {/each}
            </div>
         {/each}
      </div>
   </div>

   <!-- Sponsor Blurb -->
    <div class="border-none drop-shadow-lg items-center overflow-hidden w-full h-250 xl:h-200  bg-gray-600 bg-[url(/assets/spacemain.webp)]  bg-blend-multiply bg-auto  bg-position-[50%_50%] bg-no-repeat lg:bg-position-[20%_75%] xl:bg-cover xl:bg-position-[20%_95%] 2xl:bg-position[20%_10%]  flex flex-col justify-center">
      <div class="flex items-center align-middle mt-50 lg:-mt-20 flex-nowrap  flex-col lg:flex-row xl:pr-25 h-full w-full xl:max-w-content justify-center">
         <div class="w-full text-xl xl:text-4xl sm:text-3xl flex flex-col self-center mt-20 justify-center text-left p-10 xl:w-200 sm:w-150  drop-shadow-small lg:drop-shadow-med  text-white font-sweetsquare font-black ">
            <p class="pb-15">
               Our team provides students with a hands-on, inclusive learning environment where they can exercise creative freedom while pushing the boundaries of automotive design and technology.
            </p>
            <p>
               We equip students with real-world engineering, teamwork, and leadership experience, fostering growth in innovation, supply chain, finance, and marketing, ensuring all disciplines contribute meaningfully.
            </p>
            <a 
            target="_blank"
            rel="noopener noreferrer"
            href="https://give.rutgersfoundation.org/rutgers-solar-car-team/20133.html" class="mt-10 h-10 transition-all not-hover:drop-shadow-logo xl:order-3 self-center w-65">
               <button class="transition-all hover:text-navy text-white  hover:bg-white cursor-pointer p-3 w-full font-black  bg-red text-4xl solar-clip-rectangle">
                  <p class="w-full h-full transition-all  group-hover:drop-shadow-med">Donate Now</p>
               </button>
            </a> 
         </div>
         <img src="assets/solarlogo.svg" alt="Rutgers Solar Car Sun" class="relative  sm:static  xl:static self-center  w-100 h-100">
      </div>
   </div>

   <!-- What is Solar Racing? -->
   <div class="flex flex-col sm:flex-row justify-center border-none drop-shadow-lg items-center overflow-hidden w-full h-300 sm:h-300 lg:h-400  bg-gray-600 bg-[url(/assets/solarsunset.webp)]  bg-blend-multiply bg-auto  bg-position-[60%_50%] bg-no-repeat lg:bg-position-[20%_75%] xl:bg-cover xl:bg-position-[20%_95%] 2xl:bg-position[20%_10%]">
         <!-- Frames left -->
            <div class="relative drop-shadow-2xl lg:-mt-100">
               {#each {length:3} as _,i}
                  <div class="transition-all ease-frame {i%2==0 ? "hover:-rotate-6" : "hover:rotate-6"}  {i%2==0 ? "-rotate-3" : "rotate-3"} drop-shadow-2xl w-75 h-75 mb-5 ml-{i%2==0 ? 10 : 0} bg-white flex p-3">
                     <img class="w-full h-60"
                     src="assets/solarsunset.webp" alt="lol">
                  </div>
               {/each}
            </div>
         <!----------------->
      <div class="drop-shadow-small lg:drop-shadow-med max-w-content flex flex-col h-full  text-lg xl:text-3xl sm:text-2xl justify-center text-center  text-white font-sweetsquare font-black">
         <p class="w-full lg:mb-20 text-3xl lg:text-6xl justify-center text-center p-10  drop-shadow-small lg:drop-shadow-med  text-white font-sweetsquare font-black ">
            What is <span class="text-red">Solar Racing?</span>
         </p>
         <div class="lg:text-3xl ml-10 mr-10 w-80 sm:w-100 lg:w-200 self-center">
            <p class="">
               Since 1987, the American Solar Challenge has brought together college teams for a race that tests strategy, endurance, and cutting-edge engineering. Teams must design and build solar-powered vehicles, relying solely on solar cells embedded in the car. This multi-stage endurance race spans over 1,700 miles, covering several days in a Tour de France-style format.
            </p>
            <div class="scale-60 -m-10 sm:m-0 sm:scale-80 lg:scale-100 flex flex-row justify-center drop-shadow-none ">
               <div class="flex flex-col w-50 h-10 self-center mt-3.5">
                  <div class="w-full h-5 mb-2 bg-red drop-shadow-logo"></div>
                  <div class="w-full h-5 bg-red drop-shadow-logo"></div>
               </div>
               <p class="text-red text-9xl mt-6  mb-10 select-none drop-shadow-logo">
                  66
               </p>
               <div class="flex flex-col w-50 h-10 self-center mt-3.5">
                  <div class="w-full h-5 mb-2 bg-red drop-shadow-logo"></div>
                  <div class="w-full h-5 bg-red drop-shadow-logo"></div>
               </div>
            </div>
            <p class="">
               However, the competition embodies a greater objective than engineering prowess; it represents the awesome power and applicability of solar energy. Educating people about sustainable energy is revolutionizing our daily lives, and how it will be integrated in the years to come with cars and other modes of transport is the cornerstone of our team's mission.
            </p>
         </div>

         
      </div>

      <!-- Frames right -->
            <div class="mt-10 lg:mt-100 relative drop-shadow-2xl">
               {#each {length:3} as _,i}
                  <div class="transition-all ease-frame  {i%2==0 ? "hover:rotate-6" : "hover:-rotate-6"} {i%2==0 ? "rotate-3" : "-rotate-3"} drop-shadow-2xl w-75 h-75 mb-5  ml-{i==1 ? 10 : 0}  bg-white flex p-3">
                     <img class="w-full h-60"
                     src="assets/solarsunset.webp" alt="lol">
                  </div>
               {/each}
            </div>
         <!------------------>
   </div>

   <!-- Small Quote -->
    <div class="overflow-hidden h-50  bg-navy place-content-center flex drop-shadow-lg justify-center">
      <div class="text-2sm sm:text-2xl lg:text-3xl flex flex-col max-w-content self-center font-black p-5 lg:p-20  text-white text-left drop-shadow-med">
         <p class="">"Solar car teams' technologies are often ahead of their time in terms of looking at [the] next best generation of batteries, best solar panels, best motors and converters, things like that."</p>
         <p class="text-right text-red mt-5">— J.B. Straubel, Co-Founder of Tesla Motors</p>
      </div>
   </div>

   <!-- Where do we compete? -->
   <div class="absolute w-full overflow-hidden h-250 bg-beige flex-col flex">
      <div class="absolute w-full h-full bg-no-repeat bg-position-[50%_50%]  scale-150 bg-beige bg-blend-overlay  bg-[url(/assets/brainerd.svg)]"></div>
      <p class="w-full lg:mb-20 text-4xl lg:text-6xl justify-center text-center p-10  drop-shadow-small lg:drop-shadow-med text-white font-sweetsquare font-black ">
         <span class="text-red">Where do we compete?</span>
      </p>
      <div class="" style="bottom:30%;width:120%">
        <div class="bg-gray-900 overflow-hidden relative" style="height:18px">
            <div class="relative z-1 top-1/2 left-0 right-0 h-0.5 transform -translate-y-1/2 " style="background:repeating-linear-gradient(to right, #facc15 0px, #facc15 12px, transparent 12px, transparent 20px)"></div>
            <div class="h-full bg-black relative" style="width: 100%;"></div>
        </div>
        <div class="animate-driving-faster sm:animate-driving-normal relative bottom-11 z-2"><img src="assets/arctanarttransflip.webp" alt="Solar Car" style="width:80px;height:auto"></div>
      </div>
      <div class="p-10 self-center w-full flex flex-col sm:flex-row justify-center max-w-content">
         <div class="w-full flex flex-col">
            <p class="self-center text-2xl sm:text-4xl font-black text-red drop-shadow-small">
               Rutgers Solar Car competes at Formula Sun Gran Prix (FSGP), an annual event to compete for the most amount of laps in a solar-powered vehicle.
            </p>
            <a target="_blank"
            rel="noopener noreferrer"
            href="https://www.americansolarchallenge.org/formula-sun-grand-prix/" class="mt-10 h-10 transition-all not-hover:drop-shadow-logo xl:order-3 self-center w-65">
               <button class="transition-all hover:text-navy text-white  hover:bg-white cursor-pointer p-3 w-full font-black  bg-red text-4xl solar-clip-rectangle">
                  <p class="w-full h-full transition-all  group-hover:drop-shadow-med">FSGP Info</p>
               </button>
            </a> 
         </div>
         <div class="relative z-1 self-center min-w-75 transition-all ease-frame hover:rotate-6  rotate-3 drop-shadow-1xl w-75 h-75 mb-5 bg-white flex p-3">
            <img class="min-w-full w-full h-60" src="assets/solarsunset.webp" alt="lol">
         </div>
      </div>
   </div>

   <!-- Contact -->
   <div class=" overflow-hidden drop-shadow-2xl mt-140 solar-gradient sphere-mask  h-200">
      <!-- Solar panels -->
      <canvas bind:this={canvas} class="absolute h-full w-full"></canvas>
      <!-- Content -->
      <div class="z-2 pt-70 p-5 max-w-content m-auto drop-shadow-small lg:drop-shadow-med text-white font-sweetsquare font-black">
         <p class="w-full mb-5 text-7xl lg:text-7xl justify-center text-center p-10">
            <span class="text-white">Contact Us</span>
         </p>
         <p class="text-center text-2xl sm:text-4xl max-w-200 m-auto">
            We're happy to answer any questions you may have about the team.
         </p>
      </div>
   </div>

   <!-- Join Team -->
    <div class="overflow-hidden h-50  bg-navy place-content-center flex drop-shadow-lg justify-center">
      <div class="text-2sm sm:text-2xl lg:text-4xl flex max-w-content self-center font-black p-5 lg:p-20  text-white text-left drop-shadow-med">
         <p class="text-gold">Are you a student at Rutgers University? Help us design, build, and race the next generation of solar-powered vehicles!</p>
         <a href="/join" class="h-10 transition-all not-hover:drop-shadow-logo xl:order-3 self-center ml-3  min-w-65">
               <button class="transition-all hover:text-navy text-white  hover:bg-white cursor-pointer p-3 w-full font-black  bg-red text-4xl solar-clip-rectangle">
                  <p class="w-full h-full transition-all  group-hover:drop-shadow-med">Next Steps</p>
               </button>
            </a> 
      </div>
   </div>

 </div>
