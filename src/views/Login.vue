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
                                            class="block w-full rounded-md border-0 py-3 px-11 text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400 focus:ring-2 focus:ring-inset focus:ring-indigo-600 sm:text-sm sm:leading-6"
                                            placeholder="Password">
                                    </div>
                                </div>


                                <div>
                                    <button class="continue-application w-full bg-primary-color  text-white py-3" type="submit">
                                        <div>
                                            <div class="pencil"></div>
                                            <div class="folder mt-[-3px]">
                                                <div class="top mt-[-3px]">
                                                    <svg viewBox="0 0 24 27">
                                                        <path d="M1,0 L23,0 C23.5522847,-1.01453063e-16 24,0.44771525 24,1 L24,8.17157288 C24,8.70200585 23.7892863,9.21071368 23.4142136,9.58578644 L20.5857864,12.4142136 C20.2107137,12.7892863 20,13.2979941 20,13.8284271 L20,26 C20,26.5522847 19.5522847,27 19,27 L1,27 C0.44771525,27 6.76353751e-17,26.5522847 0,26 L0,1 C-6.76353751e-17,0.44771525 0.44771525,1.01453063e-16 1,0 Z"></path>
                                                    </svg>
                                                </div>
                                                <div class="paper"></div>
                                            </div>
                                        </div>
                                        <p class="mx-auto w-full text-center ml-[-15px]">Login</p>
                                    </button>
                                </div>
                            </form>
                            <div
                                class="grid grid-cols-2 justify-between sm:flex sm:flex-wrap gap-y-6  mt-6 text-gray-500 text-sm">

                                <div class="flex-row float-left">
                                    <!-- <input type="checkbox" name="" id=""> -->
                                    <router-link to="/register" class="mt-px font-light text-gray-700 cursor-pointer select-none"
                                        htmlFor="check">
                                        Create an account
                                    </router-link>
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

<style>
.continue-application {
  
  --background: #404660;
  --background-hover: #3A4059;
  --background-left: #2B3044;
  --folder: #F3E9CB;
  --folder-inner: #BEB393;
  --paper: #FFFFFF;
  --paper-lines: #BBC1E1;
  --paper-behind: #E1E6F9;
  --pencil-cap: #fff;
  --pencil-top: #275EFE;
  --pencil-middle: #fff;
  --pencil-bottom: #5C86FF;
  --shadow: rgba(13, 15, 25, .2);
  border: none;
  outline: none;
  cursor: pointer;
  position: relative;
  border-radius: 5px;
  font-size: 14px;
  font-weight: 500;
  line-height: 19px;
  -webkit-appearance: none;
  -webkit-tap-highlight-color: transparent;
  padding: 17px 29px 17px 69px;
  transition: background 0.3s;
  color: var(--color);
  background: var(--bg, var(--background));
}

.continue-application > div {
  top: 0;
  left: 0;
  bottom: 0;
  width: 53px;
  position: absolute;
  overflow: hidden;
  border-radius: 5px 0 0 5px;
  background: var(--background-left);
}

.continue-application > div .folder {
  width: 23px;
  height: 27px;
  position: absolute;
  left: 15px;
  top: 13px;
}

.continue-application > div .folder .top {
  left: 0;
  top: 0;
  z-index: 2;
  position: absolute;
  transform: translateX(var(--fx, 0));
  transition: transform 0.4s ease var(--fd, 0.3s);
}

.continue-application > div .folder .top svg {
  width: 24px;
  height: 27px;
  display: block;
  fill: var(--folder);
  transform-origin: 0 50%;
  transition: transform 0.3s ease var(--fds, 0.45s);
  transform: perspective(120px) rotateY(var(--fr, 0deg));
}

.continue-application > div .folder:before, .continue-application > div .folder:after,
.continue-application > div .folder .paper {
  content: "";
  position: absolute;
  left: var(--l, 0);
  top: var(--t, 0);
  width: var(--w, 100%);
  height: var(--h, 100%);
  border-radius: 1px;
  background: var(--b, var(--folder-inner));
}

.continue-application > div .folder:before {
  box-shadow: 0 1.5px 3px var(--shadow), 0 2.5px 5px var(--shadow), 0 3.5px 7px var(--shadow);
  transform: translateX(var(--fx, 0));
  transition: transform 0.4s ease var(--fd, 0.3s);
}

.continue-application > div .folder:after,
.continue-application > div .folder .paper {
  --l: 1px;
  --t: 1px;
  --w: 21px;
  --h: 25px;
  --b: var(--paper-behind);
}

.continue-application > div .folder:after {
  transform: translate(var(--pbx, 0), var(--pby, 0));
  transition: transform 0.4s ease var(--pbd, 0s);
}

.continue-application > div .folder .paper {
  z-index: 1;
  --b: var(--paper);
}

.continue-application > div .folder .paper:before, .continue-application > div .folder .paper:after {
  content: "";
  width: var(--wp, 14px);
  height: 2px;
  border-radius: 1px;
  transform: scaleY(0.5);
  left: 3px;
  top: var(--tp, 3px);
  position: absolute;
  background: var(--paper-lines);
  box-shadow: 0 12px 0 0 var(--paper-lines), 0 24px 0 0 var(--paper-lines);
}

.continue-application > div .folder .paper:after {
  --tp: 6px;
  --wp: 10px;
}

.continue-application > div .pencil {
  height: 2px;
  width: 3px;
  border-radius: 1px 1px 0 0;
  top: 3px;
  left: 105%;
  position: absolute;
  z-index: 3;
  transform-origin: 50% 19px;
  background: var(--pencil-cap);
  transform: translateX(var(--pex, 0)) rotate(35deg);
  transition: transform 0.4s ease var(--pbd, 0s);
}

.continue-application > div .pencil:before, .continue-application > div .pencil:after {
  content: "";
  position: absolute;
  display: block;
  background: var(--b, linear-gradient(var(--pencil-top) 55%, var(--pencil-middle) 55.1%, var(--pencil-middle) 60%, var(--pencil-bottom) 60.1%));
  width: var(--w, 5px);
  height: var(--h, 20px);
  border-radius: var(--br, 2px 2px 0 0);
  top: var(--t, 2px);
  left: var(--l, -1px);
}

.continue-application > div .pencil:before {
  -webkit-clip-path: polygon(0 5%, 5px 5%, 5px 17px, 50% 20px, 0 17px);
  clip-path: polygon(0 5%, 5px 5%, 5px 17px, 50% 20px, 0 17px);
}

.continue-application > div .pencil:after {
  --b: none;
  --w: 3px;
  --h: 6px;
  --br: 0 2px 1px 0;
  --t: 3px;
  --l: 3px;
  border-top: 1px solid var(--pencil-top);
  border-right: 1px solid var(--pencil-top);
}

.continue-application:before, .continue-application:after {
  content: "";
  position: absolute;
  width: 10px;
  height: 2px;
  border-radius: 1px;
  background: var(--color);
  transform-origin: 9px 1px;
  transform: translateX(var(--cx, 0)) scale(0.5) rotate(var(--r, -45deg));
  top: 26px;
  right: 16px;
  transition: transform 0.3s;
}

.continue-application:after {
  --r: 45deg;
}

.continue-application:hover {
  --cx: 2px;
  --bg: var(--background-hover);
  --fx: -40px;
  --fr: -60deg;
  --fd: .15s;
  --fds: 0s;
  --pbx: 3px;
  --pby: -3px;
  --pbd: .15s;
  --pex: -24px;
}

</style>