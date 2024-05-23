<script>
    import { tweened } from 'svelte/motion';
    import { cubicInOut } from 'svelte/easing';
    import { onMount } from 'svelte';

    let isOpen = false;

    // Store para controlar a abertura das cortinas
    const curtainWidth = tweened(50, { duration: 1000, easing: cubicInOut });

    function toggleCurtains() {
        isOpen = !isOpen;
        curtainWidth.set(isOpen ? 0 : 50);
    }

    onMount(() => {
        // Initialize the curtain as closed
        curtainWidth.set(50);
    });
</script>

<style>
    .curtain {
        transition: width 1s cubic-bezier(0.4, 0, 0.2, 1);
    }
</style>

<div class="relative w-full h-screen bg-gray-100 overflow-hidden">
    <!-- Cortinas -->
    <div class="absolute top-0 left-0 h-full bg-purple-700 curtain" style="width: { $curtainWidth }%;"></div>
    <div class="absolute top-0 right-0 h-full bg-purple-700 curtain" style="width: { $curtainWidth }%;"></div>

    <!-- Conteúdo Central -->
    <div class="relative z-10 flex items-center justify-center h-full">
        <button
                class="px-4 py-2 text-xl font-bold text-white bg-purple-500 rounded-lg hover:bg-purple-600"
                on:click={toggleCurtains}>
            {isOpen ? 'Close' : 'Open'} Curtains
        </button>
    </div>

    <!-- Conteúdo a ser exibido quando as cortinas estiverem abertas -->
    {#if isOpen}
        <div class="relative z-10 pt-16 text-center bg-gray-100">
            <div class="pb-8 pt-16 text-center">
                <p class="pb-4 text-base sm:text-lg md:text-xl lg:text-2xl xl:text-4xl font-bold text-purple-400">Round {round}/8</p>
                <span class="inline-block bg-purple-300 p-4 rounded-lg">
                    <p class="text-base sm:text-lg md:text-xl lg:text-3xl xl:text-6xl font-bold text-purple-950">
                        {CopiedArray[ChossenImage].pictureName}
                    </p>
                </span>
            </div>
            <div class="flex items-center justify-center flex-wrap">
                <img
                        src="{CopiedArray[ChossenImage].imageSource}"
                        alt="pintura bonita"
                        class="container object-contain border-double border-purple-900 border-8"
                >
            </div>
            <p class="text-base sm:text-sm md:text-base lg:text-xl xl:text-2xl text-center font-semibold pb-8 pt-16 text-purple-600">{CopiedArray[ChossenImage].autorName}</p>

            <form id="numberForm" on:submit|preventDefault={BidClick}>
                <div class="flex items-center justify-center flex-wrap">
                    {#if inputValue === null || !binded}
                        <input
                                placeholder="$0"
                                type="number"
                                id="number"
                                name="number"
                                oninput="this.value = this.value.replace(/[^0-9]/g, '')"
                                bind:value={inputValue}
                                class="border-8 border-purple-700 bg-purple-300 text-purple-950 placeholder:text-purple-950 text-2xl number-input h-24 text-center appearance-none px-4 py-2 focus:outline-none focus:border-blue-500 placeholder-gray-400 no-spin"
                                required
                        >
                    {:else}
                        <input
                                placeholder="$0"
                                type="text"
                                id="number"
                                name="number"
                                value={formatNumberWithSpaces($roundedCount)}
                                class="border-8 border-purple-700 bg-purple-300 text-purple-950 placeholder:text-purple-950 text-2xl number-input h-24 text-center appearance-none px-4 py-2 focus:outline-none focus:border-blue-500 placeholder-gray-400 no-spin"
                                required
                        >
                    {/if}
                    <img
                            src="{bidSource}"
                            alt="Bid"
                            on:mouseover={ChangeBidSprite}
                            on:mouseout={ChangeDefaultBidSprite}
                            on:click={BidClick}
                            width="96"
                            class="border-8 border-purple-700 cursor-pointer"
                    >
                </div>
            </form>

            <div class="flex items-center justify-center flex-wrap pt-16 text-center">
                {#if showPoints}
                    <div class="inline-flex bg-fuchsia-200 p-4 rounded-lg ">
                        <p class="text-2xl text-purple-950 mx-auto pr-20 my-auto">{points} points</p>
                        <button class="rounded-lg bg-purple-300 h-24 w-44 text-2xl font-extrabold text-purple-950 border-dashed" on:click={NextPicture}>Next</button>
                    </div>
                {/if}
            </div>
        </div>
    {/if}
</div>
