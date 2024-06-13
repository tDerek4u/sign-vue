<template>
    <div class="w-full " style="height: 100vh;">
        <div class="flex sm:w-full md:h-full h-full">
            <div class="w-1/2 xl:block lg:block md:hidden hidden">
                <img src="../assets/images/login_picture-03.png" class="" style="height: 100vh;" alt="login">
            </div>
            <div class="xl:w-1/2 lg:w-1/2 w-full h-full">
                <div class="flex justify-center items-center h-full">

                    <div
                        class="flex min-h-full w-full flex-col justify-center py-auto px-10 md:px-20 lg:px-20 xl:px-30">
                        <div class="sm:mx-auto sm:w-full sm:max-w-sm">
                            <img class="mx-auto h-10 w-auto" src="../assets/images/ESingNewLogo 1.png"
                                alt="Your Company">
                            <h2
                                class="mt-10 text-center text-2xl font-medium primary-color leading-9 tracking-tight text-gray-900">
                                Login Account</h2>
                        </div>

                        <div class="mt-10 sm:mx-auto sm:w-full sm:max-w-sm">
                            <form class="space-y-6 h-auto" action="#" method="POST">

                                <div>
                                    <div class="relative flex items-center mt-2">
                                        <span class="absolute icon-[circum--user]">
                                            <svg class="w-5 h-5 mx-3" xmlns="http://www.w3.org/2000/svg" width="1em"
                                                height="1em" viewBox="0 0 48 48">
                                                <g fill="none" stroke="grey" stroke-linecap="round"
                                                    stroke-linejoin="round" stroke-width="2">
                                                    <path fill="none" stroke="grey" stroke-linecap="round"
                                                        stroke-linejoin="round"
                                                        d="M9.5 13c13.687 13.574 14.825 13.09 29 0" />
                                                    <rect width="37" height="31" x="5.5" y="8.5" fill="none"
                                                        stroke="grey" stroke-linecap="round"
                                                        stroke-linejoin="round" rx="4" ry="4" />
                                                </g>

                                            </svg>
                                        </span>
                                        <input id="email" name="email" type="email" autocomplete="email" required
                                            class="block w-full rounded-md border-0 py-3 px-11 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                                            placeholder="Email">
                                    </div>
                                </div>

                                <div>

                                    <div class="relative flex items-center mt-2">
                                        <span class="absolute icon-[circum--user]">
                                            <svg class="w-5 h-5 mx-3" xmlns="http://www.w3.org/2000/svg" width="1em"
                                                height="1em" viewBox="0 0 24 24">
                                                <g fill="none" stroke="grey" stroke-linecap="round"
                                                    stroke-linejoin="round" stroke-width="1">
                                                    <path
                                                        d="M12 11.543A2.17 2.17 0 1 0 12 7.2a2.17 2.17 0 0 0 0 4.342m0 .001v3.256" />
                                                    <path
                                                        d="M20.672 11.89V6.61a1.928 1.928 0 0 0-1.32-1.831L14.438 3.14a7.805 7.805 0 0 0-4.876 0L4.648 4.778a1.927 1.927 0 0 0-1.32 1.83v5.28a7.709 7.709 0 0 0 3.603 6.524l4.048 2.544a1.927 1.927 0 0 0 2.042 0l4.047-2.544a7.708 7.708 0 0 0 3.604-6.523" />
                                                </g>
                                            </svg>
                                        </span>
                                        <input id="password" name="password" type="password"
                                            autocomplete="current-password" required
                                            class="block w-full rounded-md border-0 py-1.5 px-11 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                                            placeholder="Password">
                                    </div>
                                </div>


                                <div>
                                    <button type="submit"
                                        class="flex w-full justify-center rounded-md bg-indigo-600 px-3 py-3 text-sm font-semibold leading-6 text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">
                                        Sign in
                                    </button>
                                </div>
                            </form>
                            <div
                                class="grid grid-cols-2 justify-between sm:flex sm:flex-wrap gap-y-6  mt-6 text-gray-500 text-sm">

                                <div class="flex-row float-left">
                                    <input type="checkbox" name="" id="">
                                    <label class="mt-px font-light text-gray-700 cursor-pointer select-none"
                                        htmlFor="check">
                                        Remember Me
                                    </label>
                                </div>

                                <div class="flex-row-reverse float-right">
                                    <a href="#"
                                        class="font-regular primary-color flex-row-reverse hover:text-blue-70">Forgot
                                        password?</a>
                                </div>
                            </div>


                        </div>
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>