<script>
    export let step;

</script>
    <a href={step.href} class="p-4 sm:p-6 flex flex-col gap-4 rounded-lg border border-solid border-sky-700 text-center group cursor-pointer
    hover:border-sky-400 duration-200">
    <div class="bg-slate-950 grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200">
    <i class={step.icon}></i>
    </div>
    <h3 class="font-md text-xl sm:text-2xl md:text-3xl">{step.name}</h3>
    <slot/>
    <div class="flex-1 flex justify-between gap-4 items-center">
        <div class="ml-auto cursor-pointer hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full
        after:w-full hover:bg-white after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden rounded-sm p-1">
        <p class="relative z-4">Go to &rarr;</p>
        </div>
    </div>
    </a>
