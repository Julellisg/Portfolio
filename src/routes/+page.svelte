<script lang="ts">
    // Define any URLs
    import schoolImage from '#lib/assets/brocku-logo.png';
    import pfp1 from '#lib/assets/pfp1.png';
    import pfp2 from '#lib/assets/pfp2.png';
    import projectPlaceholder from '#lib/assets/project-placeholder.svg';

    // Project Logos
    import previewBP2E from '#lib/assets/previewBP2E.png';
    import previewAndroidCalc from '#lib/assets/previewAndroidCalc.png';
    import previewDiscord from '#lib/assets/previewDiscord.png';
    import previewBITES from '#lib/assets/previewBITES.png';
    import previewPomodoro from '#lib/assets/previewPomodoro.png';
    import previewGradeCalc from '#lib/assets/previewGradeCalc.png';
    import previewPortfolio from '#lib/assets/previewPortfolio.png';

    let showFirstPortrait = $state(true);
</script>

<div class="portfolio-container">
    <!-- About Me -->
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
        <p class="text-center text-lg italic text-(--text-sub-color)">⇄</p>
        </div>
    </div>
    <!-- <br> -->

    <!-- Education -->
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

    <!-- Technical Skills -->
    <h2>TECHNICAL SKILLS</h2>
    <hr>
    <div>Languages / Frameworks: Java, HTML, CSS, JavaScript/TypeScript, Python, C++, SQL, SvelteKit, TailwindCSS, Bootstrap</div>
    <div>Tools: Android Studio, Figma, Firebase, Photoshop, Git, GitHub Desktop, Notion, PostgreSQL, Ubuntu</div>
    <br>

    <!-- Projects -->
    <h2>PROJECTS</h2>
    <hr>
    <p class="mb-4">Here are a list of my featured projects. To see <em>all</em> my projects, visit my <a href="https://github.com/Julellisg?tab=repositories" target="_blank" rel="noopener noreferrer" class="font-bold underline">GitHub Repositories.</a>.</p>
    <div class="project-container ">
        <!-- Pomodoro Timer -->
        <div id="project-card">
            <img src={previewPomodoro} alt="" aria-hidden="true">
            <div id="card-text">
                <h3>Pomodoro Timer</h3>
                <hr>
                <p>A Pomodoro timer application with a clean and customizable interface and adjustable parameters. Features a set of ambient soundtracks to mix and match for your preferred environment.</p>
            </div>
        </div>
        <!-- Grade Calculator -->
        <div id="project-card">
            <img src={previewGradeCalc} alt="" aria-hidden="true">
            <div id="card-text">
                <h3>Current & Final Grade Calculator</h3>
                <hr>
                <p>Easy-to-use web application intended for students to calculate their current and/or final grades based on known grading criteria. Calculates targeted grades needed to achieve a desired final grade.</p>
            </div>
        </div>
        <!-- Brock Plan 2 Eat -->
        <div id="project-card">
            <img src={previewBP2E} alt="" aria-hidden="true">
            <div id="card-text">
                <h3>Brock Plan 2 Eat</h3>
                <hr>
                <p>An Android app for displaying available food and drink establishments across the Brock University campus. </p>
            </div>
        </div>
        <!-- Android Calculator -->
        <div id="project-card">
            <img src={previewAndroidCalc} alt="" aria-hidden="true">
            <div id="card-text">
                <h3>Android Calculator</h3>
                <hr>
                <p>An Android calculator built in Android Studio. It has a Basic mode that calculates left to right and a Formula mode that follows the standard order of operations, with the result updating as you type.</p>
            </div>
        </div>
        <!-- Portfolio -->
        <div id="project-card">
            <img src={previewPortfolio} alt="" aria-hidden="true">
            <div id="card-text">
                <h3>Portfolio Website</h3>
                <hr>
                <p>The website you are currently viewing! A personal portfolio built with SvelteKit and TailwindCSS to showcase my projects and skills. Intentionally designed to read similarly to a paper-resume.<p>
            </div>
        </div>        
        <!-- Discord Bot -->
        <div id="project-card">
            <img src={previewDiscord} alt="" aria-hidden="true">
            <div id="card-text">
                <h3>Discord Bot</h3>
                <hr>
                <p>A private Discord bot featuring 10+ quality-of-life functions used across multiple servers.</p><br>
                <p>Built using the 'discord.py' library.</p>
            </div>
        </div>
        <!-- Brock Interactive Training Engineering System -->
        <div id="project-card">
            <img src={previewBITES} alt="" aria-hidden="true">
            <div id="card-text">
                <h3>Brock Interactive Training Engineering System</h3>
                <hr>
                <p>BITES is an interactive learning platform focused on software engineering, designed to keep users engaged and make learning faster and more efficient.</p>
            </div>
        </div>
    </div>
    <br><br>

    <!-- Contact -->
    <h2 class="text-center">CONTACT</h2>


    <footer class="text-center py-4 mt-4 ">© 2026 Julian Ellis Geronimo</footer>
</div>
