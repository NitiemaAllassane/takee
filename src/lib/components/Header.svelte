<script>
    import { Search, Globe, Bell } from "lucide-svelte";
</script>


<header class=" flex items-center justify-between py-3 mb-6">
    <form class=" bg-primary flex items-center gap-5 py-3 px-6 rounded-2xl focus-within:ring-2">
        <label for="search">
            <Search />
        </label>
        <input 
            type="search" 
            name="search" 
            id="search" 
            placeholder="Search for NFT"
            class=" outline-none ps-3 py-1"
        >
    </form>

    <div class="flex items-center justify-between w-1/2">
        <div class=" flex items-center gap-16">
            <p class=" text-gray-500 ">Trades</p>
            <a href="/" class="flex items-center gap-3 text-gray-500">
                <Globe />
                Language
            </a>
        </div>
        <button 
            aria-label="Notifications"
            class=" text-gray-500 cursor-pointer"
        >
            <Bell />
        </button>
    </div>
</header>