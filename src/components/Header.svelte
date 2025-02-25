<script>
    export let y;
    console.log(y);

    let tabs = [
        {name: 'Projects', link: '#projects'},
        {name: 'About Me', link: '#about'},
    ];
</script>

<header class="sticky z-[10] top-0 duration-200 px-4 flex items-center justify-between border border-solid"
    class:py-4={y > 0}
    class:bg-slate-950={y > 0}
    class:border-violet-950={y > 0}
    class:py-6={y <= 0}
    class:bg-transparent={y <= 0}
    class:border-transparent={y <= 0}>
    <h1 class="font-medium">
        <b class="font-bold poppins">Ryan </b> Brockley
    </h1>
    <div class="sm:flex ml-auto pr-4 items-center gap-4 hidden">
        {#each tabs as tab, index}
        <a href={tab.link} class="duration-200 hover:text-violet-400">
            <p>{tab.name}</p>
        </a>
        {/each}
    <!-- <a href="https://www.linkedin.com/in/ryan-brockley-35213513b/" target="_blank" class="blueShadow relative overflow-hidden px-5 py-1 group rounded-full bg-white text-slate-950 mt-1">
        <div class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"/>
        <h4 class="relative z-9 font-bold">Get in touch</h4>
    </a> -->
</div>

</header>