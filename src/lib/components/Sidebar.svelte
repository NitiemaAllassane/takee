<script>
    import { House, Wallet, Tag, Bookmark, Store, Smartphone, LogOut } from "lucide-svelte";
	import Logo from "./Logo.svelte";
	import Badge from "./Badge.svelte";

</script>

<section class=" sticky top-0 h-fit p-12 bg-primary">
    <!-- content -->
    <nav>
        <!-- top part -->
        <div class=" mb-20">
            <Logo  />
            <ul class=" mt-20 flex flex-col justify-start gap-2">

                <li class="flex items-center gap-3 hover:bg-second py-2 rounded-[4px]">
                    <House class=" text-gray-500" />
                    <a href="/test" class="w-full">
                       Home
                    </a>
                </li>

                <li class="flex items-center gap-3 hover:bg-second py-2 rounded-[4px]">
                    <Wallet class=" text-gray-500" />
                    <a href="/" class=" flex w-full items-center justify-between">
                        <span>Wallet</span>
                        <Badge content="4" />
                    </a>
                </li>

                <li class="flex items-center gap-3 hover:bg-second py-2 rounded-[4px]">
                    <Tag class=" text-gray-500" />
                    <a href="/" class="flex w-full items-center justify-between">
                        <span>Offers</span>
                        <Badge content="17" />
                    </a>
                </li>

                <li class="flex items-center gap-3 hover:bg-second py-2 rounded-[4px]">
                    <Bookmark class=" text-gray-500" />
                    <a href="/" class="w-full">
                        Saves
                    </a>
                </li>

                <li class="flex items-center gap-3 hover:bg-second py-2 rounded-[4px]">
                    <Store class=" text-gray-500" />
                    <a href="/" class="w-full">
                        Shoping
                    </a>
                </li>

                <li class="flex items-center gap-3 hover:bg-second py-2 rounded-[4px]">
                    <Smartphone class=" text-gray-500" />
                    <a href="/" class="w-full">
                        Applications
                    </a>
                </li>
            </ul>
        </div>

        <div>
            <article class=" p-8 rounded-2xl shadow-[8px_8px_14px_rgba(255,255,255,1)] shadow-white">
                <div class="flex items-center gap-2 mb-5">
                    <figure class="bg-red rounded-full">
                        <img src="/images/obito.svg" alt="Kruis avatar">
                    </figure>
                    <div>
                        <h4 class=" text-[18px] font-bold ">Kruis 337</h4>
                        <p class=" text-sm text-gray-500">Programmer</p>
                    </div>
                </div>
                <button class="bg-red flex justify-center items-center gap-2 w-full py-2 rounded-lg cursor-pointer ">
                    <LogOut />
                    Logout
                </button>
            </article>
        </div>

    </nav>
</section>