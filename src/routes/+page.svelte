<script>
	import Badge from "$lib/components/Badge.svelte";
	import Header from "$lib/components/Header.svelte";
    import { ArrowDown, ArrowUp } from "lucide-svelte";

    const discovers = [
        {
            img: "/images/image1.svg",
            title: "Masked Girl",
            userImg: "/images/james.svg",
            userName: "James Irk3"
        },

        {
            img: "/images/image2.svg",
            title: "Oni Cyborg",
            userImg: "/images/obito.svg",
            userName: "Kruis 337"
        },

        {
            img: "/images/image3.svg",
            title: "Vanda",
            userImg: "/images/goku.svg",
            userName: "Alon Rig"
        },

        {
            img: "/images/image4.svg",
            title: "Humai Khraken",
            userImg: "/images/stromphe.svg",
            userName: "Smurf D"
        },
    ];


    const walletsNews = [
        { count: "7,349", received: true },
        { count: "25,784", received: false }
    ];


    const bestSellers = [
        {
            name: "James Irk3",
            work: "Programmer",
            img: "/images/obito.svg",
            sellNum: "+12k"
        },

        {
            name: "Smurf D",
            work: "Designer",
            img: "/images/stromphe.svg",
            sellNum: "+8k"
        },

        {
            name: "Alon Rig",
            work: "Freelancer",
            img: "/images/goku.svg",
            sellNum: "+6k"
        }
    ];

</script>

<Header />

<main class="grid grid-cols-1 md:grid-cols-[2fr_1fr] gap-6 mb-4">
    <section>
        <header class=" mb-10">
            <article class="bg-red flex items-center px-10 rounded-4xl">
                <div>
                    <h2 class="font-thin mb-1">Announcement</h2>
                    <h1 class="font-bold mb-1">Get NFT on your email</h1>
                    <p class="font-bold text-sm mb-6">Notifications of new collections</p>
                    <a href="/" class=" bg-white font-bold text-black py-3 px-6 rounded-2xl">
                        Subscribe
                    </a>
                </div>
                <figure>
                    <img src="/images/anounce.svg" alt="Anouncement">
                </figure>
            </article>
        </header>

        <section>
            <h2 class=" mb-6">Discover</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                {#each discovers as discover, index}
                    <a href="/" class=" block bg-primary rounded-4xl hover:-translate-y-2 transition-transform duration-200">
                        <figure>
                            <img src={discover.img} alt={discover.title}>
                        </figure>
                        <div class=" pt-5 pb-3 px-6">
                            <h3 class="text-2xl font-bold mb-3">{ discover.title }</h3>
                            <div class="flex justify-between items-center">
                                <div class="flex items-center gap-3">
                                    <figure class="{ index === 1 ? " bg-red rounded-full ": ""} ">
                                        <img src={ discover.userImg } alt={discover.userName}>
                                    </figure>
                                    <h4>{ discover.userName }</h4>
                                </div>
                                <!-- <Badge content="Current bid 2.00 ETH"  /> -->
                                 <button class="text-black font-bold bg-white rounded-2xl px-3 py-2.5 text-center leading-tight w-32">
                                    Current bid 2.00 ETH
                                </button>
                            </div>
                        </div>
                    </a>
                {/each}
            </div>
        </section>

    </section>

    <section>
        <article class=" bg-primary rounded-4xl mb-6">
            <header class=" p-5 flex items-center gap-6">
                <figure>
                    <img src="/images/eth.svg" alt="eth icon">
                </figure>
                <div>
                    <h4 class="flex items-center justify-between">
                        <span class=" text-xl font-bold ">Wallet new</span>
                        <small class=" text-white bg-green-500 rounded-md font-medium p-1">3 New</small>
                    </h4>
                    <p class=" text-sm text-gray-500">Brief information about the course</p>
                </div>
            </header>

            <!-- * graph -->
            <figure>
                <img src="/images/data.svg" alt="NFT GRAPH">
            </figure>

            <div class="flex items-center gap-10 p-5">
                {#each walletsNews as wallet }
                    <p class=" text-sm flex items-center gap-1">
                        {#if wallet.received}
                            <ArrowDown class=" text-red text-xs" />
                        {:else}
                            <ArrowUp class=" text-green-500 text-xs" />
                        {/if}

                        <span>
                            { wallet.count }
                            <span class=" text-gray-500">USD</span>
                        </span>
                    </p>
                {/each}
            </div>
        </article>

        <article class=" bg-primary p-8 rounded-4xl mb-6">
            <div>
                <h3 class=" text-xl font-bold mb-8">Top sellers</h3>
                <ul>
                    {#each bestSellers as seller, index}
                        <li class="flex items-center justify-between {index === 2 ? "mb-0" : "mb-6"} ">
                            <div class="flex items-center gap-2">
                                <figure class="{ index === 0 ? "bg-red rounded-full" : ""} ">
                                    <img src={seller.img} alt={seller.name}>
                                </figure>
                                <div>
                                    <h4 class="text-[18px] font-bold ">{ seller.name }</h4>
                                    <p class=" text-xs text-gray-500">{ seller.work }</p>
                                </div>
                            </div>
                            <Badge content={seller.sellNum} border="8px"  />
                        </li>
                    {/each}
                </ul>
            </div>
        </article>

        <article class="flex items-center gap-6">
            <a href="/" class=" block bg-primary rounded-4xl p-10">
                <h3 class="text-xl mb-3">News</h3>
                <h1 class=" text-4xl font-bold">Get more specials on your email</h1>
            </a>
            <div class=" flex flex-col gap-6">
                <a href="/" class="block bg-primary p-4 rounded-xl">
                    <img src="/images/earth.svg" alt="Earth illustration">
                    <span>News</span>
                </a>
                <a href="/" class="block bg-primary p-4 rounded-xl">
                    <img src="/images/fuse.svg" alt="Rocket illustration">
                    <span>More</span>
                </a>
            </div>
        </article>
    </section>
</main>