<script>
    
    let ImagesNames = [
        {
            price: 4727500,
            pictureName: "Garden Elements",
            autorName: "Isamu Noguchi, 1958",
            imageSource: "/src/lib/images/ImgGame/Garden Elements.jpg"
        },
        {
            price: 11000,
            pictureName: "Maximilian Schmidt Brass-Mounted Mahogany Octagonal Center Table",
            autorName: "Maximilian Schmidt",
            imageSource: "/src/lib/images/ImgGame/Maximilian Schmidt Brass-Mounted Mahogany Octagonal Center Table.jpg"
        },
        {
            price: 568100,
            pictureName: "Tête de femme’ table lamp",
            autorName: "Designed by Alberto Giacometti, 1937",
            imageSource: "/src/lib/images/ImgGame/Tête de femme’ table lamp.jpg"
        },
        {
            price: 306288,
            pictureName: "Concetto Spaziale",
            autorName: "Lucio Fontana, 1962/1965",
            imageSource: "/src/lib/images/ImgGame/Concetto Spaziale.jpg"
        },
        {
            price: 13000,
            pictureName: "\"LANDSCAPE\" GLASS INSTALLATION, 20 PIECES",
            autorName: "Martin Blank, 2011",
            imageSource: "/src/lib/images/ImgGame/LANDSCAPE GLASS INSTALLATION, 20 PIECES.jpg"
        },
        {
            price: 56875,
            pictureName: "TÊTE DE FEMME",
            autorName: "Pablo Picasso, Executed  circa  1940-1944",
            imageSource: "/src/lib/images/ImgGame/TÊTE DE FEMME.jpg"
        },
        {
            price: 39505700,
            pictureName: "ABSTRAKTES BILD",
            autorName: "Gerhard Richter, 1986",
            imageSource: "/src/lib/images/ImgGame/ABSTRAKTES BILD.jpg"
        },
        {
            price: 1463500,
            pictureName: "Il Parle",
            autorName: "Jean Dubuffet, 1961",
            imageSource: "/src/lib/images/ImgGame/Il Parle.jpg"
        },
        {
            price: 375000,
            pictureName: "LES OIES'",
            autorName: "François-Xavier Lalanne, designed circa 1992",
            imageSource: "/src/lib/images/ImgGame/LES OIES'.jpg"
        },
        {
            price: 26250,
            pictureName: "Defense Against Banality",
            autorName: "Rafal Olbinski",
            imageSource: "/src/lib/images/ImgGame/Defense Against Banality.jpg"
        },
        {
            price: 276250,
            pictureName: "Spare Moment",
            autorName: "Tschabalala Self, Executed in 2015",
            imageSource: "/src/lib/images/ImgGame/Spare Moment.jpg"
        },
        {
            price: 260000,
            pictureName: "STRINGED OBJECT",
            autorName: "Henry Moore, 1938",
            imageSource: "/src/lib/images/ImgGame/STRINGED OBJECT.jpg"
        },
        {
            price: 159408,
            pictureName: "Lauriers blancs dans un vase Galle I",
            autorName: "Bernard Buffet, 1990",
            imageSource: "/src/lib/images/ImgGame/Lauriers blancs dans un vase Galle I.jpg"
        },
        {
            price: 410400,
            pictureName: "Crocefisso",
            autorName: "Designed by Lucio Fontana, 1950 - 1955",
            imageSource: "/src/lib/images/ImgGame/Crocefisso.jpg"
        },
        {
            price: 79380,
            pictureName: "Des Mandarins",
            autorName: "Qing Dynasty 19th Century",
            imageSource: "/src/lib/images/ImgGame/Des Mandarins.jpg"
        },
        {
            price: 2346500,
            pictureName: "Figura de perfil",
            autorName: "Salvador Dalí, 1925",
            imageSource: "/src/lib/images/ImgGame/Figura de perfil.jpg"
        },
        {
            price: 1870000,
            pictureName: "Keep it Spotless",
            autorName: "Banksy",
            imageSource: "/src/lib/images/ImgGame/Keep it Spotless.jpg"
        },
        {
            price: 56875,
            pictureName: "Moreton Bay Fig, Botanic Gardens",
            autorName: "Brett Whiteley, 1984",
            imageSource: "/src/lib/images/ImgGame/Moreton Bay Fig, Botanic Gardens.jpg"
        },
        {
            price: 2364050,
            pictureName: "Reclining Figure",
            autorName: "Henry Moore, 1945",
            imageSource: "/src/lib/images/ImgGame/Reclining Figure.jpg"
        },
        {
            price: 56875,
            pictureName: "THE NUBIAN GUARD",
            autorName: "Pablo Picasso, Executed  circa  1940-1944",
            imageSource: "/src/lib/images/ImgGame/THE NUBIAN GUARD.jpg"
        },
        {
            price: 346680,
            pictureName: "Tête de femme penchée",
            autorName: "Charles Knighton Warren",
            imageSource: "/src/lib/images/ImgGame/Tête de femme penchée.jpg"
        },
        {
            price: 372000,
            pictureName: "PETUNIAS IN OVAL, NO. 2",
            autorName: "Georgia O'Keeffe",
            imageSource: "/src/lib/images/ImgGame/PETUNIAS IN OVAL, NO. 2.jpg"
        },
        {
            price: 16165000,
            pictureName: "Forme uniche della continuità nello spazio (Unique Forms of Continuity in Space)",
            autorName: "Umberto Boccioni, 1972, Conceived in 1913 and cast in 1972",
            imageSource: "/src/lib/images/ImgGame/Forme uniche della continuità nello spazio (Unique Forms of Continuity in Space).jpg"
        },
        {
            price: 519000,
            pictureName: "Year After Year",
            autorName: "Ed Ruscha, 1973",
            imageSource: "/src/lib/images/ImgGame/Year After Year.jpg"
        },
        {
            price: 432500,
            pictureName: "Roses dans un vase de fleurs",
            autorName: "Pierre-Auguste Renoir",
            imageSource: "/src/lib/images/ImgGame/Roses dans un vase de fleurs.jpg"
        },
        {
            price: 2081700,
            pictureName: "Manteau de Cheminée",
            autorName: "Designed by Jean Dunand, 1926",
            imageSource: "/src/lib/images/ImgGame/Manteau de Cheminée.jpg"
        },
        {
            price: 30875,
            pictureName: "Roses",
            autorName: "Yao Hua, 1924",
            imageSource: "/src/lib/images/ImgGame/Roses.jpg"
        },
        {
            price: 56875,
            pictureName: "GENERAL",
            autorName: "Boris Orlov, dated 2004",
            imageSource: "/src/lib/images/ImgGame/GENERAL.jpg"
        },
        {
            price: 1805000,
            pictureName: "PETIT SERGENT MAJOR",
            autorName: "Jean Dubuffet, 1943",
            imageSource: "/src/lib/images/ImgGame/PETIT SERGENT MAJOR.jpg"
        },
        {
            price: 872625,
            pictureName: "Segelschiff I",
            autorName: "Walter Dexel, 1922, Painted in 1922",
            imageSource: "/src/lib/images/ImgGame/Segelschiff I.jpg"
        },
        {
            price: 3419500,
            pictureName: "Ram's Head, Blue Morning Glory",
            autorName: "Georgia O'Keeffe, 1938",
            imageSource: "/src/lib/images/ImgGame/Ram's Head, Blue Morning Glory.jpg"
        },
        {
            price: 2081700,
            pictureName: "J'accours",
            autorName: "Jean Dubuffet, 1964",
            imageSource: "/src/lib/images/ImgGame/J'accours.jpg"
        },
        {
            price: 52000,
            pictureName: "Magnolia Door One",
            autorName: "Gary Hume, Painted in 1988",
            imageSource: "/src/lib/images/ImgGame/Magnolia Door One.jpg"
        },
        {
            price: 22587500,
            pictureName: "Ocean Park #137",
            autorName: "Richard Diebenkorn, 1985",
            imageSource: "/src/lib/images/ImgGame/Ocean Park 137.jpg"
        }
    
    ]

    let CopiedArray = ImagesNames;
    let inputValue = null;
    let bidSource = "/src/lib/images/BidUnColor.png";
    let binded = false
    let points = 0;
    let showPoints = false;
    let ChossenImage = getRandomInt(0, CopiedArray.length)
    let TotalPoints = 0;
    let round = 1;
    
    function getRandomInt(min, max) {
        const minCeiled = Math.ceil(min);
        const maxFloored = Math.floor(max);
        return Math.floor(Math.random() * (maxFloored - minCeiled) + minCeiled); // The maximum is exclusive and the minimum is inclusive
    }
    
    
    function ChangeBidSprite()
    {
        bidSource = "/src/lib/images/bidColor.png";
    }
    function ChangeDefaultBidSprite()
    {
        bidSource = "/src/lib/images/BidUnColor.png";
    }
    
    
    function BidClick() {
        
        if (inputValue != null) {
            
            animateTo(CopiedArray[ChossenImage].price);
            binded = true; // Define como true quando o usuário clica na imagem Bid
            points = calcPoints(inputValue, CopiedArray[ChossenImage].price);
            showPoints = true;
            
        }
    }

    import { tweened } from 'svelte/motion';
    import { cubicOut } from 'svelte/easing';
    import { derived } from 'svelte/store';
    
    let isOpen = false;

    // Store para controlar a abertura das cortinas
    const curtainWidth = tweened(50, { duration: 1000, easing: cubicOut });

    function toggleCurtains() {
        isOpen = !isOpen;
        curtainWidth.set(isOpen ? 0 : 50);
    }
 //-------------------------------------------------------
    // Cria uma store tweened com valor inicial 0
    const count = tweened(0, {
        duration: 2000, // duração da animação em milissegundos
        easing: cubicOut // função de easing para suavizar a animação
    });
    
    // Cria uma store derivada que arredonda o valor da store tweened
    const roundedCount = derived(count, $count => Math.round($count));

    // Função para iniciar a animação
    function animateTo(target) {
        count.set(target);
    }
    function formatNumberWithSpaces(number) {
        const numberString = String(number).replace(/,/g, '');
        // Insere espaços a cada três dígitos
        const formattedNumber = numberString.replace(/\B(?=(\d{3})+(?!\d))/g, ' ');
        // Retorna o número formatado com o símbolo "$" no início
        return '$' + formattedNumber;
    }

    function calcPoints(userValue, originalPrice) {
        const difference = Math.abs(originalPrice - userValue);
        const score = Math.max(0, 100 - (difference / originalPrice) * 100);
        return Math.round(score);
    }

    function NextPicture(){
        showPoints = false;
        binded = false;
        bidSource = "/src/lib/images/BidUnColor.png";
        inputValue = null;
        TotalPoints += points;
        points = 0;
        round++;
        if(round >= 8)
        {
            round = 0;
        }
        CopiedArray.splice(ChossenImage, 1)
        ChossenImage = getRandomInt(0, CopiedArray.length)
        
    }
    /*
    function animateOpen() {
        const box = document.querySelector('.overlay-image');
        const box1 = document.querySelector('.overlay-image-left');
        box.classList.add('slideIn1');
        box1.classList.add('slideIn');
    }
    */
    let isEaseInAnimation = true;

    function toggleAnimation() {
        isEaseInAnimation = !isEaseInAnimation;
        const animatingDiv = document.getElementById('elementToSlide1');
        console.log(animatingDiv.style.animation);
        if (isEaseInAnimation) {
            
            //animatingDiv.style.animation = 'slideIn1 4s forwards';
        } else {
            animatingDiv.style.animation = 'slideOut1 4f forwards';
        }
    }
    
    
</script>
<div class="pb-8 pt-16 text-center">
    <p class="pb-4 text-base sm:text-lg md:text-xl lg:text-2xl xl:text-4xl font-bold text-purple-400">Round {round}/8</p>
    <span class="inline-block bg-purple-300 p-4 rounded-lg">
        <p class="text-base sm:text-lg md:text-xl lg:text-3xl xl:text-6xl font-bold text-purple-950">
            {CopiedArray[ChossenImage].pictureName}
        </p>
    </span>
</div>
<div class="flex items-center justify-center flex-wrap  ">
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

<div id="elementToSlide" class="overlay-image">
    <img src="/src/lib/images/CortinaRoxa.jpg" alt="Imagem" style="width: 100%; height: 100%;" />
</div>

<div id="elementToSlide1" class="overlay-image-left">
    <img src="/src/lib/images/CortinaRoxa.jpg" alt="Imagem" style="width: 100%; height: 100%;" />
</div>

<button on:click={toggleAnimation} class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
    Alternar Animação
</button>




<style>
    .no-spin::-webkit-outer-spin-button,
    .no-spin::-webkit-inner-spin-button {
        -webkit-appearance: none;
        margin: 0;
    }
    .no-spin {
        -moz-appearance: textfield;
    }
    .container {
        
        width: min-content;
        height: min-content;
        
    }
    
    .overlay-image {
        position: fixed;
        top: 0;
        right: 0;
        width: 50%;
        height: 100%;
        z-index: 9999;
        animation: slideIn1 4s forwards; /* Aplica a animação */
    }
    
    @keyframes slideIn1 {
        from {
            transform: translateX(0%);
        }
        10%{
            transform: translateX(10%);
        }
        50%{
            transform: translateX(150%);
        }
        to {
            transform: translateX(200%);
        }
    }

    @keyframes slideOut1 {
        from {
            transform: translateX(200%);
        }
        10%{
            transform: translateX(150%);
        }
        50%{
            transform: translateX(10%);
        }
        to {
            transform: translateX(0);
        }
    }
    
    .overlay-image-left{
        position: fixed;
        top: 0;
        left: 0%;
        right: 0%;
        width: 50%;
        height: 100%;
        z-index: 9999;
        animation: slideIn 4s forwards;
    }
    
    @keyframes slideIn {
        from {
            transform: translateX(0%);
        }
        10%{
            transform: translateX(-10%);
        }
        50%{
            transform: translateX(-150%);
        }
        to {
            transform: translateX(-200%);
        }
    }
    @keyframes slideOut {
        from {
            transform: translateX(-200%);
        }
        10%{
            transform: translateX(-150%);
        }
        50%{
            transform: translateX(-10%);
        }
        to {
            transform: translateX(0%);
        }
    }

    @keyframes ease-in-animation {
        0% {
            opacity: 0;
            transform: translateX(-100%);
        }
        100% {
            opacity: 1;
            transform: translateX(0);
        }
    }

    @keyframes ease-out-animation {
        0% {
            opacity: 1;
            transform: translateX(0);
        }
        100% {
            opacity: 0;
            transform: translateX(100%);
        }
    }
    
</style>
