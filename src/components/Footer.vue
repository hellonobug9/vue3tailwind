<template>
  <footer class="mx-auto max-w-[1040px] bg-red-200">
    <div>
      <div class="grid grid-cols-1 lg:grid-cols-2">
        <div class="col-span-1">
          <img :src="'/common/logo-maci.png'" alt="MaCi" class="w-24" />

          <p class="mt-6 text-center text-sm sm:mx-0 sm:text-left">
            MaCi is one of your best friends. Discover and treat your mental
            health problems to make your mental life happier than ever.
          </p>

          <ul
            class="mt-[3.375rem] flex justify-center gap-6 sm:justify-start md:gap-8"
          >
            <li>
              <span class="sr-only">Facebook</span>
              <svg
                aria-hidden="true"
                class="h-6 w-6"
                fill="currentColor"
                viewBox="0 0 24 24"
              >
                <path
                  clip-rule="evenodd"
                  d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z"
                  fill-rule="evenodd"
                />
              </svg>
            </li>

            <li>
              <a
                class="text-black transition hover:text-black/75"
                href="/"
                rel="noopener noreferrer"
                target="_blank"
              >
                <span class="sr-only">Instagram</span>
                <svg
                  aria-hidden="true"
                  class="h-6 w-6"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    clip-rule="evenodd"
                    d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z"
                    fill-rule="evenodd"
                  />
                </svg>
              </a>
            </li>

            <li>
              <a
                class="text-black transition hover:text-black/75"
                href="/"
                rel="noopener noreferrer"
                target="_blank"
              >
                <span class="sr-only">Twitter</span>
                <svg
                  aria-hidden="true"
                  class="h-6 w-6"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84"
                  />
                </svg>
              </a>
            </li>
          </ul>
        </div>

        <div
          class="text-gray-70 col-span-1 hidden grid-cols-1 sm:grid sm:grid-cols-2 sm:gap-12 sm:pl-[97px]"
        >
          <div
            v-for="nav in navigation"
            :key="nav.id"
            class="text-center sm:text-left"
          >
            <p class="text-mobileBody-1 sm:text-desktopBody-1 font-semibold">
              {{ nav.label }}
            </p>

            <nav class="mt-8">
              <ul class="space-y-4 text-sm">
                <li v-for="item in nav.items" :key="item.id">
                  <a class="hover:text-darkGay-70/75 transition" href="/">
                    {{ item.label }}
                  </a>
                </li>
              </ul>
            </nav>
          </div>
        </div>
        <div class="sm:hidden space-y-8">
          <div v-for="nav in navigation" :key="nav.id" class="border-b-[0.4px] border-gray-50 pb-3">
            <FooterItem :item="nav" />
          </div>
        </div>
      </div>

      <div class="border-gray-20 text-gray-70 mt-6 border-t pt-6">
        <div class="flex justify-between text-center sm:text-left">
          <div class="flex items-center space-x-3">
            <p>Terms of us</p>
            <p>&#183;</p>
            <p>Privacy Policy</p>
          </div>
          <p>
            <span
              >Copyright ?? {{ copyrightYear }} MaCi. All rights reserved.</span
            >
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>
import { withDefaults } from "vue";
import FooterItem from "./FooterItem.vue";
const navigation = [
  {
    id: 1,
    label: "Explore MaCi",
    items: [
      { id: 1, href: "app.live-class.overview", label: "Live Class" },
      { id: 2, href: "app.therapy.info", label: "Online Therapy" },
      { id: 3, href: "app.warmline", label: "Warmline" },
      { id: 4, href: "app.blog.index", label: "Blog" },
      {
        id: 5,
        href: "app.mental-health-test.index",
        label: "Mental Health Test",
      },
    ],
  },
  {
    id: 2,
    label: "About us",
    items: [
      { id: 1, href: "app.about-us.our-mission", label: "Our Mission" },
      { id: 2, href: "app.about-us.careers", label: "Careers" },
      { id: 3, href: "app.about-us.our-experts", label: "Our Experts" },
      { id: 4, href: "app.about-us.contact-us", label: "Contact us" },
    ],
  },
];
</script>
