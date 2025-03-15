<script>
    import Step from "./Step.svelte";
    let steps = [
        {name: 'GameFace', icon: 'fa-solid fa-gamepad', href: 'https://gameface.life'},
        {name: 'React Products', icon: 'fa-brands fa-react', href: 'https://tubular-marzipan-3730e7.netlify.app' },
    ];

    let benefits = [
        {name: 'A self taught developer', description: 'With over 18 years of experience in the engineering industry, I have transitioned into Front-End Development, bringing the same dedication and drive that propelled me to the highest levels in my previous field. My goal is to achieve excellence in software development, leveraging my problem-solving skills and technical expertise to create impactful digital experiences.'},
        {name: 'A front end and UX fanatic', description: 'I have a deep passion for understanding how things work and transforming ideas into tangible, real-world projects. I thrive on building solutions that deliver value and serve a meaningful purpose within their respective industries.'},
        {name: 'An excellent communicator', description: 'I excel both independently and as part of a team. With strong communication skills, I thrive in collaborative environments, articulating ideas clearly and effectively to drive projects forward.'},
    ]
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="intropage"
        class="grid grid-cols lg:grid-cols-2 gap-10 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-sky-400">Ryan</span>
                Brockley <br />Front End
                <span class="poppins text-sky-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="poppins text-sky-400">favorite tech</span> includes
                JavaScript, Vue.js (Nuxt), TailwindCSS, MySQL and Firebase
            </p>
               <a href="https://www.linkedin.com/in/ryan-brockley-35213513b/" target="_blank"
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-sky-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch &rarr;</h4>
        </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/profile-image.jpeg"}
                alt="profile-image"
                class="object-cover rounded-xl"
            />
        </div>
    </section>
    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A few of my creative endevors
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-sky-400"> see</span> my work?
            </h3>
        </div>
        <a
            href="https://github.com/Rybrock?tab=repositories"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white
    flex items-center gap-2 -mb-4 sm:-mn-8 md-mb-10 hover:border-sky-700 duration-200"
        >
            <i
                class="fa-brands fa-github grid place-items-center aspect-square text-5xl"
            />
            view repositories
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>GameFace is a one stop shop for everything gaming. You can search games, add to favorites and even create collections.
                    It was created with <strong class="text-sky-400"> Nuxt.JS and Firebase</strong>
                </p>
            </Step>
                <p class="text-center">More <strong class="text-sky-400 text-2xl"> Coming soon...</strong>
                </p>
        </div>
    </section>
    <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
>
    <!-- <div class="z-[-1] bg-sky-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
    <div
        class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-sky-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-sky-700 py-4"
    >
        <h6 class="text-large sm:text-xl md:text-2xl">
            Want to know more?
        </h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
            A bit <span class="poppins text-sky-400">about</span> me.
        </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
        I am . . .
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
        The <span class="text-sky-400">Complete</span> Package
    </h5>
    <div
        class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
    >
        <table class="bg-white text-slate-700 rounded text-center">
            <thead class={"border-b border-solid border-slate-200  "}>
                <tr class="">
                    <th />
                    <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                    <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                    <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                    <th
                        class="bg-sky-700 text-white whitespace-nowrap p-4 px-8"
                        >Me</th
                    >
                </tr>
            </thead>
            <tbody>
                <tr class="border-b border-solid border-slate-200">
                    <td
                        class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >Dedication</td
                    >
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-green-500" /></td>
                </tr>
                <tr class="border-b border-solid border-slate-200">
                    <td
                        class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >Critical Thought</td
                    >
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-green-500" /></td>
                </tr>
                <tr>
                    <td
                        class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >Interpersonal Skills</td
                    >
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-green-500" /></td>
                </tr>
                <tr class="border-t border-solid border-slate-200">
                    <td
                        class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                        >Progamming Ability</td
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
    <p class="mx-auto">So why not invest?</p>
</section>
</main>