<script lang="ts">
    import schoolImage from '#lib/assets/brocku-logo.png';
    import pfp1 from '#lib/assets/pfp1.png';
    import pfp2 from '#lib/assets/pfp2.png';
    import resume from '#lib/assets/resume.pdf';

    // Project Logos
    import previewBP2E from '#lib/assets/previewBP2E.png';
    import previewAndroidCalc from '#lib/assets/previewAndroidCalc.png';
    import previewDiscord from '#lib/assets/previewDiscord.png';
    import previewBITES from '#lib/assets/previewBITES.png';
    import previewPomodoro from '#lib/assets/previewPomodoro.png';
    import previewGradeCalc from '#lib/assets/previewGradeCalc.png';
    import previewPortfolio from '#lib/assets/previewPortfolio.png';

    let showFirstPortrait = $state(true);

    interface Project {
        title: string;
        image: string;
        description: string;
        tags: string[];
        repo: string;
        demo?: {
            label: string;
            href: string;
        };
    }

    const projects: Project[] = [
        {
            title: 'Pomodoro Timer',
            image: previewPomodoro,
            description:
                'A Pomodoro timer application with a clean and customizable interface and adjustable parameters. Features a set of ambient soundtracks to mix and match for your preferred environment.',
            tags: ['HTML', 'CSS', 'JavaScript'],
            repo: 'https://github.com/Julellisg/Pomodoro-Timer',
            demo: {
                label: 'Try it out!',
                href: 'https://julellisg.github.io/Pomodoro-Timer/'
            }
        },
        {
            title: 'Current & Final Grade Calculator',
            image: previewGradeCalc,
            description:
                'Easy-to-use web application intended for students to calculate their current and/or final grades based on known grading criteria. Calculates targeted grades needed to achieve a desired final grade.',
            tags: ['HTML', 'CSS', 'JavaScript'],
            repo: 'https://github.com/Julellisg/Grade-Calculator',
            demo: {
                label: 'Try it out!',
                href: 'https://julellisg.github.io/Grade-Calculator/'
            }
        },
        {
            title: 'Brock Plan 2 Eat',
            image: previewBP2E,
            description:
                'An Android app for displaying available food and drink establishments across the Brock University campus.',
            tags: ['Java', 'Android Studio', 'BrainShop API', 'Firebase'],
            repo: 'https://github.com/Julellisg/BrockPlan2EatApp',
            demo: {
                label: 'Demonstration',
                href: 'https://github.com/Julellisg/BrockPlan2EatApp/blob/master/src/demonstration.gif'
            }
        },
        {
            title: 'Android Calculator',
            image: previewAndroidCalc,
            description:
                'An Android calculator built in Android Studio. It has a Basic mode that calculates left to right and a Formula mode that follows the standard order of operations, with the result updating as you type.',
            tags: ['Java', 'Android Studio'],
            repo: 'https://github.com/Julellisg/Android-Calculator'
        },
        {
            title: 'Portfolio Website',
            image: previewPortfolio,
            description:
                'The website you are currently viewing! A personal portfolio built with SvelteKit and Tailwind CSS to showcase my projects and skills. Intentionally designed to read similarly to a paper-resume.',
            tags: ['SvelteKit', 'Tailwind CSS', 'HTML', 'CSS', 'TypeScript'],
            repo: 'https://github.com/Julellisg/Portfolio',
            demo: {
                label: 'Back to Top',
                href: '#top'
            }
        },
        {
            title: 'Discord Bot',
            image: previewDiscord,
            description:
                'A private Discord bot featuring 10+ quality-of-life functions used across multiple servers.',
            tags: ['Python', 'discord.py', 'YouTube Data API v3'],
            repo: 'https://github.com/Julellisg/Gamious-Bot'
        },
        {
            title: 'Brock Interactive Training Engineering System',
            image: previewBITES,
            description:
                'BITES is an interactive learning platform focused on software engineering, designed to keep users engaged and make learning faster and more efficient.',
            tags: ['SvelteKit', 'Tailwind CSS', 'HTML', 'CSS', 'TypeScript'],
            repo: 'https://github.com/SWE-2024/COSC-4P02'
        }
    ];
</script>

<div id="top" class="portfolio-container">
    <!-- About Me -->
    <div class="grid grid-cols-1 md:grid-cols-[1fr_auto] gap-6 md:items-stretch">
        <!-- Left Half  -->
        <div class="flex-1">
            <h1 class="font-extrabold leading-tight">JULIAN ELLIS GERONIMO</h1>
            <h2>ABOUT</h2>
            <hr />
            <p class="text-base text-(--text-sub-color)">
                I’m a web developer and a generalist at heart, and I learn by
                building, from remakes of things that exist to ideas that don’t
                yet. I enjoy trying different mediums, but the web is where I
                am most passionate and do my best work. I use AI as an assistant
                to work faster and test ideas.
            </p>
        </div>
        <!-- Right Half -->
        <div class="mx-auto md:mx-0 w-40 sm:w-48 md:w-auto md:h-full flex flex-col items-center justify-center">
            <button
                type="button"
                aria-label={showFirstPortrait
                    ? 'Show second portrait'
                    : 'Show first portrait'}
                onclick={() => (showFirstPortrait = !showFirstPortrait)}
                class="group relative aspect-square w-full md:w-auto md:h-full overflow-hidden rounded-2xl focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-current"
            >
                <img
                    src={pfp1}
                    alt=""
                    aria-hidden="true"
                    class="portrait-image absolute inset-0 h-full w-full object-cover drop-shadow-2xl transition-opacity duration-300 ease-in-out"
                    style:opacity={showFirstPortrait ? 1 : 0}
                />
                <img
                    src={pfp2}
                    alt=""
                    aria-hidden="true"
                    class="portrait-image absolute inset-0 h-full w-full object-cover drop-shadow-2xl transition-opacity duration-300 ease-in-out"
                    style:opacity={showFirstPortrait ? 0 : 1}
                />
                <span
                    class="absolute bottom-2 right-2 rounded-md bg-black/50 px-1.5 py-0.5 text-xs text-white/90 backdrop-blur-sm transition-opacity group-hover:bg-black/70"
                >
                    ⇄
                </span>
            </button>
        </div>
    </div>

    <!-- Social & Quick Links -->
    <div class="my-6 flex items-center justify-center gap-6 text-(--text-color)">
        <a
            href={resume}
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Resume"
            class="group relative transition-colors duration-200 hover:text-white"
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-7 w-7"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
            >
                <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z" />
                <polyline points="14 2 14 8 20 8" />
                <line x1="16" y1="13" x2="8" y2="13" />
                <line x1="16" y1="17" x2="8" y2="17" />
                <polyline points="10 9 9 9 8 9" />
            </svg>
            <span
                class="pointer-events-none absolute -top-8 left-1/2 -translate-x-1/2 whitespace-nowrap rounded-md border border-(--accent-color) bg-(--primary-color) px-2 py-0.5 text-xs text-(--text-color) opacity-0 drop-shadow-md transition-opacity duration-200 group-hover:opacity-100"
            >
                Resume
            </span>
        </a>
        <a
            href="https://github.com/Julellisg"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="GitHub Profile"
            title="GitHub"
            class="transition-colors duration-200 hover:text-white"
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-7 w-7"
                fill="currentColor"
                viewBox="0 0 24 24"
            >
                <path
                    d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"
                />
            </svg>
        </a>
        <a
            href="https://www.linkedin.com/in/"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="LinkedIn Profile"
            title="LinkedIn"
            class="transition-colors duration-200 hover:text-white"
        >
            <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-7 w-7"
                fill="currentColor"
                viewBox="0 0 24 24"
            >
                <path
                    d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                />
            </svg>
        </a>
    </div>

    <!-- Education -->
    <h2>EDUCATION</h2>
    <hr />
    <div class="mb-6 grid grid-cols-[48px_minmax(0,1fr)] sm:grid-cols-[60px_minmax(0,1fr)] gap-3 sm:gap-4 pb-4">
        <a
            href="https://brocku.ca/"
            target="_blank"
            rel="noopener noreferrer"
            class="h-12 w-12 sm:h-[60px] sm:w-[60px] shrink-0"
        >
            <img
                src={schoolImage}
                alt="Brock University icon"
                class="rounded-lg drop-shadow-lg"
            />
        </a>
        <div class="min-w-0">
            <div class="flex flex-col sm:flex-row sm:items-baseline sm:justify-between gap-x-4">
                <h3 class="font-semibold text-base sm:text-lg">Brock University</h3>
                <span class="text-xs sm:text-sm text-(--text-sub-color) sm:text-right">St. Catharines, Ontario</span>
            </div>
            <div class="mt-1 flex flex-col sm:flex-row sm:items-baseline sm:justify-between gap-x-4">
                <p class="text-xs sm:text-sm md:text-base text-(--text-sub-color)">
                    Bachelor of Science (Honours) - BS, Computer Science
                </p>
                <span class="text-xs sm:text-sm text-(--text-sub-color) sm:text-right">
                    Sep 2019 - April 2024
                </span>
            </div>
        </div>
    </div>

    <!-- Technical Skills -->
    <h2>TECHNICAL SKILLS</h2>
    <hr />
    <div class="mb-6 grid grid-cols-1 sm:grid-cols-[max-content_1fr] items-start gap-x-6 gap-y-3">
        <span class="flex h-[26px] items-center font-bold">Languages:</span>
        <div class="tags">
            <span>Java</span>
            <span>Python</span>
            <span>C++</span>
            <span>JavaScript</span>
            <span>TypeScript</span>
            <span>HTML</span>
            <span>CSS</span>
            <span>SQL</span>
        </div>

        <span class="flex h-[26px] items-center font-bold">Frameworks &amp; Libraries:</span>
        <div class="tags">
            <span>SvelteKit</span>
            <span>Tailwind CSS</span>
            <span>Bootstrap</span>
        </div>

        <span class="flex h-[26px] items-center font-bold">Tools:</span>
        <div class="tags">
            <span>VSCode</span>
            <span>Git</span>
            <span>GitHub</span>
            <span>Figma</span>
            <span>Firebase</span>
            <span>PostgreSQL</span>
            <span>Android Studio</span>
            <span>Photoshop</span>
            <span>Notion</span>
            <span>Ubuntu</span>
        </div>
    </div>

    <!-- Projects -->
    <h2>PROJECTS</h2>
    <hr />
    <p class="mb-4">
        Here are a list of my featured projects. To see <em>all</em> my projects,
        visit my
        <a
            href="https://github.com/Julellisg?tab=repositories"
            target="_blank"
            rel="noopener noreferrer"
            class="font-bold underline"
        >
            GitHub Repositories.
        </a>
    </p>

    <div class="project-container mb-8">
        {#each projects as project}
            <div class="project-card">
                <img src={project.image} alt="" aria-hidden="true" />
                <div class="card-text">
                    <h3>{project.title}</h3>
                    <hr />
                    <p>{project.description}</p>
                </div>

                <!-- Tags -->
                <div class="tags px-4">
                    {#each project.tags as tag}
                        <span>{tag}</span>
                    {/each}
                </div>

                <!-- Buttons -->
                <div class="my-4 flex w-full gap-2 px-4">
                    <a
                        href={project.repo}
                        target="_blank"
                        rel="noopener noreferrer"
                        class="btn-primary"
                    >
                        GitHub Repo
                    </a>
                    {#if project.demo}
                        <a
                            href={project.demo.href}
                            target={project.demo.href.startsWith('http') ? '_blank' : undefined}
                            rel={project.demo.href.startsWith('http') ? 'noopener noreferrer' : undefined}
                            class="btn-secondary"
                        >
                            {project.demo.label}
                        </a>
                    {/if}
                </div>
            </div>
        {/each}
    </div>

    <!-- Contact -->
    <h2>CONTACT</h2>
    <hr />
    <p class="text-base text-(--text-sub-color)">
        For all inquiries, please contact me via my
        <a href="mailto:julianellisg@gmail.com"
            class="underline font-bold text-(--text-color)">
            julianellisg@gmail.com
        </a>
        and I will respond as soon as possible.
    </p>

    <footer>© 2026 Julian Ellis Geronimo • 
        <a href="https://github.com/Julellisg/Portfolio"
        target="_blank"
        class="hover:underline">
            View Source
        </a></footer>
</div>
