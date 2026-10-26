<script lang="ts">
    // Define any URLs
    import schoolImage from '#lib/assets/brocku-logo.png';
    import pfp1 from '#lib/assets/pfp1.png';
    import pfp2 from '#lib/assets/pfp2.png';

    let showFirstPortrait = $state(true);
</script>

<div class="portfolio-container">
    <div class="grid grid-cols-1 md:grid-cols-[minmax(0,1fr)_14rem] gap-6">
        <!-- Left Half  -->
        <div class="flex-1">
            <h1 class="text-[38px] font-extrabold">JULIAN ELLIS GERONIMO</h1>
            <h2>ABOUT</h2>
            <hr>
            <p class="text-base text-[var(--text-sub-color)]">I’m a web developer and a generalist at heart, and I learn by building, from remakes of things that exist to ideas that don’t yet. I enjoy trying different mediums, but the web is where I am most passionate and do my best work. I use AI as an assistant to work faster and test ideas.</p>
        </div>
        <!-- Right Half -->
        <div>
            <button
                type="button"
                aria-label={showFirstPortrait ? 'Show second portrait' : 'Show first portrait'}
                onclick={() => (showFirstPortrait = !showFirstPortrait)}
                class="relative aspect-square w-full self-start overflow-hidden rounded-2xl focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-current"
            >
                <img
                    src={pfp1}
                    alt=""
                    aria-hidden="true"
                    class="portrait-image absolute inset-0 h-full w-full object-cover drop-shadow-2xl"
                    style:opacity={showFirstPortrait ? 1 : 0}
                    style:z-index={showFirstPortrait ? 1 : 0}
                />
                <img
                    src={pfp2}
                    alt=""
                    aria-hidden="true"
                    class="portrait-image absolute inset-0 h-full w-full object-cover drop-shadow-2xl"
                    style:opacity={showFirstPortrait ? 0 : 1}
                    style:z-index={showFirstPortrait ? 0 : 1}
                />
            </button>
        <p class="text-center text-lg italic text-[var(--text-sub-color)]">⇄</p>
        </div>
    </div>
    <br>
    

    <h2>EDUCATION</h2>
    <hr>
    <div class="grid grid-cols-[60px_minmax(0,1fr)] gap-4 pb-4">
        <a
            href="https://brocku.ca/"
            target="_blank"
            rel="noopener noreferrer"
            class="h-[60px] w-[60px] "
        >
            <img
                src={schoolImage}
                alt="Brock University icon"
                class="rounded-lg drop-shadow-lg"
            />
        </a>
        <div class="min-w-0">
            <div class="flex flex-wrap items-baseline justify-between gap-x-4">
                <h3 class="font-semibold">Brock University</h3>
                <span class="ml-auto text-right ">St. Catharines, Ontario</span>
            </div>
            <div class="mt-1 flex flex-wrap items-baseline justify-between gap-x-4">
                <p class="text-[var(--text-sub-color)]">Bachelor of Science (Honours) - BS, Computer Science</p>
                <span class="ml-auto text-right text-[var(--text-sub-color)]">Sep 2019 - April 2024</span>
            </div>
        </div>
    </div>
    <br>

    <h2>PROJECTS</h2>
    <hr>
    <br>

    <h2>TECHNICAL SKILLS</h2>
    <hr>
    <div>Languages / Frameworks: Java, HTML, CSS, JavaScript/TypeScript, Python, C++, SQL, SvelteKit, TailwindCSS, Bootstrap</div>
    <div>Tools: Android Studio, Figma, Firebase, Photoshop, Git, GitHub Desktop, Notion, PostgreSQL, Ubuntu</div>
    <br><br>

    <h2 class="text-center">CONTACT</h2>


    <footer class="text-center py-4 mt-4 ">© 2026 Julian Ellis Geronimo</footer>
</div>

<style>
    .portrait-image {
        transition: opacity 500ms ease-in-out;
    }

    @media (prefers-reduced-motion: reduce) {
        .portrait-image {
            transition: none;
        }
    }
</style>
