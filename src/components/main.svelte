<script>
    import Step from "./Step.svelte";

    let steps = [
        {
            name: "Sleep",
            icon: "fa-solid fa-bed",
            description:
                "Sleepout event",
        },
        {
            name: "Music",
            icon: "fa-solid fa-music",
            description:
                "Music event",
        },
        {
            name: "PJs at Work",
            icon: "fa-solid fa-shirt",
            description:
                "PJs",
        },
    ];

    let benefits = [
        {
            metric: "10x",
            name: "passionate",
            description:
                "a passionate organisation",
        },
        {
            name: "impactful",
            description:
                "We use our money effectively and where it matters.",
        },
        {
            name: "helpful",
            description:
                "We create events that matter and help those in need.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                For those in <span class="poppins text-orange-400">need.</span>
                <br />To
                <span class="poppins text-orange-400">serve</span> those most vulnerable.
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                <span class="text-orange-400"> Roofoverhead Initiative</span> is passionate about creating new <span class="text-orange-400">pathways</span> for those in need.
            </p>
            <a href="/about"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <!-- svelte-ignore element_invalid_self_closing_tag -->
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200" 
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
        </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile.png"}
                alt="Homeless man"
                class="object-cover z-[2] max-h-[90vh]"
            />
        </div>
        <div  class="flex p-0.5 relative max-w-[700px] w-full mx-auto">
            <div
                class="absolute inset-0 overflow-hidden rounded-md flex items-center justify-center"
            >
                <div
                    class="bg-gradient-to-r absolute inset-[-20px]  from-orange-800 to-indigo-800 specialSpin"
                />
            </div>

        
        </div>
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                What's lined up next?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Our <span class="poppins text-orange-400">upcoming</span> events
            </h3>
        </div>
        <a
            href="https://www.youtube.com/watch?v=Xu73iBgHs4I"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-orange-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    Sleepout event is where  <strong
                        class="text-orange-400"
                        >people</strong
                    > sleepout in sleeping bags outdoors.
                    Experience what it feels to be homeless and  <strong
                    class="text-orange-400">understand</strong> the pain that they have to go through everyday. 
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    A free music event that allows you to  <strong
                        class="text-orange-400">raise funds</strong
                    >,
                    <strong class="text-orange-400">for people in need</strong
                    > while enjoying a 
                    & <strong class="text-orange-400">a day </strong> the this year's best hits!
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    PJs at work  <strong class="text-orange-400"
                        >allows your team</strong
                    >
                    to enjoy a 
                    <strong class="text-orange-400">day </strong>, of work in the comfort of your own PJs!
                  
                </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-orange-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-orange-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-orange-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-orange-400">about</span> us.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            We are . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            The <span class="text-orange-400">Complete</span> Package
        </h5>
        <div
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200  "}>
                    <tr class="">
                        <th />
                        <th class="whitespace-nowrap p-2 px-4">Org #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Org #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Org #3</th>
                        <th
                            class="bg-orange-700 text-white whitespace-nowrap p-4 px-8"
                            >Roofoverhead</th
                        >
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Passion</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Impact</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr>
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Fun</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Quality</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-slate-500" /></td>
                        <td><i class="fa-solid fa-check text-green-500" /></td>
                    </tr>
                </tbody>
            </table>
        </div>
        <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div>
        <p class="mx-auto">Help us with our mission by donating or attending our fundraising events.</p>
    </section>
</main>