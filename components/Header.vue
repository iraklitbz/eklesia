<script setup>
    const mobileMenuOpen = ref(false)
    const open = ref(false)
</script>
<template>
    <div>
        <header class="h-24 bg-white border-b border-slate-200/80">
            <div
                class="flex items-center w-full h-full max-w-screen-xl px-5 mx-auto sm:px-6 lg:px-8"
            >
                <nav class="relative z-50 flex items-center justify-between w-full">
                <!-- Logo -->
                <div class="flex items-center shrink-0">
                    <nuxt-link
                    to="/"
                    aria-label="Home"
                    class="flex items-center flex-shrink-0"
                    >

                    <img
                        src="~/assets/images/logo-icon.png"
                        alt=""
                        class="w-auto h-10 md:block"
                    />
                    </nuxt-link>
                </div>

                <!-- Desktop navigation links -->
                <div class="items-center hidden md:flex md:space-x-6 lg:space-x-8">
                    <nuxt-link
                    to="/"
                    class="relative duration-200 after:absolute after:left-1/2 after:-bottom-2.5 after:h-0.5 after:w-4 after:-translate-x-1/2 after:rounded-full after:bg-slate-900 after:opacity-0 after:content-[&quot;&quot;] font-medium text-slate-700 hover:text-slate-900 hover:after:opacity-25"
                    >
                    Home
                    </nuxt-link>
                    <nuxt-link
                    to="/about"
                    class="relative duration-200 after:absolute after:left-1/2 after:-bottom-2.5 after:h-0.5 after:w-4 after:-translate-x-1/2 after:rounded-full after:bg-slate-900 after:opacity-0 after:content-[&quot;&quot;] font-medium text-slate-700 hover:text-slate-900 hover:after:opacity-25"
                    >
                    About
                    </nuxt-link>
                    <nuxt-link
                    to="/blog"
                    class="relative duration-200 after:absolute after:left-1/2 after:-bottom-2.5 after:h-0.5 after:w-4 after:-translate-x-1/2 after:rounded-full after:bg-slate-900 after:opacity-0 after:content-[&quot;&quot;] font-medium text-slate-700 hover:text-slate-900 hover:after:opacity-25"
                    >
                    Blog
                    </nuxt-link>
                    <nuxt-link
                    to="/contact"
                    class="relative duration-200 after:absolute after:left-1/2 after:-bottom-2.5 after:h-0.5 after:w-4 after:-translate-x-1/2 after:rounded-full after:bg-slate-900 after:opacity-0 after:content-[&quot;&quot;] font-medium text-slate-700 hover:text-slate-900 hover:after:opacity-25"
                    >
                    Contact
                    </nuxt-link>

                    <!-- Template pages dropdown container -->
                </div>

                <div class="flex items-center">
                    <!-- Call to action -->
                    <a
                    class="text-slate-900 shadow-sm shadow-sky-100/50 ring-1 ring-slate-100 hover:bg-slate-200/60 hover:shadow-sky-100/50 bg-slate-100/80 inline-flex items-center rounded-full gap-2.5 justify-center px-7 py-3 text-md font-semibold leading-none outline-offset-2 transition-all duration-200 ease-in-out active:transition-none"
                    href="#0"
                    >
                    Lorem ipsum
                    </a>

                    <!-- Mobile menu button -->
                    <div class="ml-4 md:hidden" x-data="{ mobileMenuOpen: false }">
                    <button
                        class="relative z-50 flex items-center justify-center p-3 transition duration-300 ease-in-out rounded-full shadow-sm cursor-pointer group bg-slate-100/80 shadow-sky-100/50 ring-1 ring-slate-900/5 hover:bg-slate-200/60 focus:outline-none md:hidden"
                        aria-label="Toggle Navigation"
                        @click="mobileMenuOpen=!mobileMenuOpen"
                    >
                        <span
                        class="relative h-3.5 w-4 transform transition duration-500 ease-in-out"
                        >
                        <span
                            class="absolute block h-0.5 rotate-0 transform rounded-full bg-slate-700 opacity-100 transition-all duration-300 ease-in-out group-hover:bg-slate-900"
                            :class="mobileMenuOpen ? 'top-1.5 left-1/2 w-0': 'top-0 left-0 w-full'"
                        ></span>
                        <span
                            class="absolute left-0 top-1.5 block h-0.5 w-full transform rounded-full bg-slate-700 opacity-100 transition-all duration-300 ease-in-out group-hover:bg-slate-900"
                            :class="mobileMenuOpen ? 'rotate-45': 'rotate-0'"
                        ></span>
                        <span
                            class="absolute left-0 top-1.5 block h-0.5 w-full transform rounded-full bg-slate-700 opacity-100 transition-all duration-300 ease-in-out group-hover:bg-slate-900"
                            :class="mobileMenuOpen ? '-rotate-45': 'rotate-0'"
                        ></span>
                        <span
                            class="absolute block h-0.5 rotate-0 transform rounded-full bg-slate-700 opacity-100 transition-all duration-300 ease-in-out group-hover:bg-slate-900"
                            :class="mobileMenuOpen ? 'top-1.5 left-1/2 w-0': 'left-0 top-3 w-full'"
                        ></span>
                        </span>
                    </button>

                    <!-- Mobile menu container -->
                    <div class="md:hidden">
                        <!-- Background dark overlay when mobile menu is open -->
                        <div
                        x-show="mobileMenuOpen"
                        x-transition:enter="duration-200 ease-out"
                        x-transition:enter-start="opacity-0"
                        x-transition:enter-end="opacity-100"
                        x-transition:leave="duration-150 ease-in"
                        x-transition:leave-start="opacity-100"
                        x-transition:leave-end="opacity-0"
                        class="fixed inset-0 z-20 bg-opacity-50 bg-slate-900"
                        style="display: none"
                        ></div>

                        <!-- Mobile menu popover -->
                        <div
                        x-show="mobileMenuOpen"
                        x-transition:enter="duration-300 ease-out"
                        x-transition:enter-start="opacity-0 scale-90"
                        x-transition:enter-end="opacity-100 scale-100"
                        x-transition:leave="duration-200 ease-in"
                        x-transition:leave-start="opacity-100 scale-100"
                        x-transition:leave-end="opacity-0 scale-90"
                        class="absolute inset-x-0 z-30 px-6 mt-4 overflow-hidden origin-top shadow-xl top-full rounded-2xl bg-slate-50 py-7 shadow-sky-100/40 ring-1 ring-slate-900/5"
                        style="display: none"
                        @click.away="mobileMenuOpen = false"
                        >
                        <div>
                            <!-- Mobile menu links -->
                            <div class="flex flex-col space-y-4">
                            <a
                                href="index.html"
                                class="block text-base font-semibold duration-200 text-slate-700 hover:text-slate-900"
                            >
                                Home
                            </a>
                            <a
                                href="about.html"
                                class="block text-base font-semibold duration-200 text-slate-700 hover:text-slate-900"
                            >
                                About
                            </a>
                            <a
                                href="work.html"
                                class="block text-base font-semibold duration-200 text-slate-700 hover:text-slate-900"
                            >
                                Work
                            </a>
                            <a
                                href="blog.html"
                                class="block text-base font-semibold duration-200 text-slate-700 hover:text-slate-900"
                            >
                                Blog
                            </a>
                            <a
                                href="contact.html"
                                class="block text-base font-semibold duration-200 text-slate-700 hover:text-slate-900"
                            >
                                Contact
                            </a>

                            <!-- Pages dropdown -->
                            <div class="relative" x-data="{ open: false }">
                                <button
                                class="flex items-center w-full gap-2 text-base font-semibold duration-200 ease-in-out group"
                                :class="open ? 'text-slate-900' : 'text-slate-700 hover:text-slate-900'"
                                @click="open = !open"
                                >
                                <span>Pages</span>
                                <svg
                                    xmlns="http://www.w3.org/2000/svg"
                                    viewBox="0 0 20 20"
                                    fill="currentColor"
                                    class="w-5 h-5 duration-300"
                                    :class="open ? 'rotate-90 text-slate-900' : 'text-slate-700 group-hover:text-slate-900'"
                                >
                                    <path
                                    fill-rule="evenodd"
                                    d="M7.21 14.77a.75.75 0 01.02-1.06L11.168 10 7.23 6.29a.75.75 0 111.04-1.08l4.5 4.25a.75.75 0 010 1.08l-4.5 4.25a.75.75 0 01-1.06-.02z"
                                    clip-rule="evenodd"
                                    />
                                </svg>
                                </button>

                                <!-- Dropdown links list -->
                                <ul
                                style="display: none"
                                class="z-20 px-3 space-y-4"
                                x-show.transition="open"
                                >
                                <li class="mt-4">
                                    <a
                                    href="index.html"
                                    class="block font-medium transition duration-200 ease-in-out text-md text-slate-700 hover:text-slate-900"
                                    >
                                    Home
                                    </a>
                                </li>
                                <li class="mt-4">
                                    <a
                                    href="about.html"
                                    class="block font-medium transition duration-200 ease-in-out text-md text-slate-700 hover:text-slate-900"
                                    >
                                    About
                                    </a>
                                </li>
                                <li class="mt-4">
                                    <a
                                    href="work.html"
                                    class="block font-medium transition duration-200 ease-in-out text-md text-slate-700 hover:text-slate-900"
                                    >
                                    Work
                                    </a>
                                </li>
                                <li class="mt-4">
                                    <a
                                    href="case-study.html"
                                    class="block font-medium transition duration-200 ease-in-out text-md text-slate-700 hover:text-slate-900"
                                    >
                                    Case study
                                    </a>
                                </li>
                                <li class="mt-4">
                                    <a
                                    href="blog.html"
                                    class="block font-medium transition duration-200 ease-in-out text-md text-slate-700 hover:text-slate-900"
                                    >
                                    Blog
                                    </a>
                                </li>
                                <li class="mt-4">
                                    <a
                                    href="article.html"
                                    class="block font-medium transition duration-200 ease-in-out text-md text-slate-700 hover:text-slate-900"
                                    >
                                    Blog post
                                    </a>
                                </li>
                                <li class="mt-4">
                                    <a
                                    href="contact.html"
                                    class="block font-medium transition duration-200 ease-in-out text-md text-slate-700 hover:text-slate-900"
                                    >
                                    Contact
                                    </a>
                                </li>
                                </ul>
                            </div>
                            </div>
                        </div>
                        </div>
                    </div>
                    </div>
                </div>
                </nav>
            </div>
            </header>
    </div>
</template>