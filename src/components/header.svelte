<script>
    export let y;

    export let tabs = [
        { name: "Events ", link: "/events" },
        { name: "Statistics", link: "/statistics" },
        { name: "About us", link: "/about" },
        
    ];
</script>

<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-slate-950 border-orange-950"
            : " py-6 bg-transparent border-transparent")}
>
    <h1 class="font-medium flex items-center space-x-2">
        <!-- svelte-ignore a11y_consider_explicit_label -->
        <a href="/"><img src= "images/logo.png" class="w-10"alt = "logo"></a> <span class="text-orange-400">Roofoverhead Initiative</span>
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 hover:text-orange-400"
                target={index === 2 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
       
        <a href="/about"
            
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
        >
            <!-- svelte-ignore element_invalid_self_closing_tag -->
            <div
                class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
            />
            <h4 class="relative z-9">Get in touch</h4>
        </a>
    </div>
</header>