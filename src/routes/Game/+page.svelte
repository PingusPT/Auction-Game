<script>
    import { tweened } from 'svelte/motion';
    import { cubicOut } from 'svelte/easing';
    import { derived } from 'svelte/store';
    import { fly } from 'svelte/transition';


    
    let inputValue = 0;
    let bidSource = 'https://cdn-icons-png.flaticon.com/512/2581/2581347.png';///src/lib/images/BidUnColor.png
    let binded = false;
    let points = 0;
    let showPoints = false;
    
    let TotalPoints = 0;
    let round = 1;
    let isOpen = false;
    const curtainWidth = tweened(50, { duration: 1000, easing: cubicOut });
    const count = tweened(0, {
        duration: 2000, // duração da animação em milissegundos
        easing: cubicOut // função de easing para suavizar a animação
    });
    let isEaseInAnimation = false;
    let inAnimation = true;
    let ControllDiv = true;
    let ShowGame = true;//-----------------------------------------------------

    const roundedCount = derived(count, ($count) => Math.round($count));
    
    let ImagesNames = [
        {
            price: 4727500,
            pictureName: 'Garden Elements',
            autorName: 'Isamu Noguchi, 1958',
            imageSource: 'https://www.artnet.com/WebServices/images/ll0073Blld7DRJFgUNECfDrCWvaHBOcBSGF/isamu-noguchi-garden-elements.jpg'///src/lib/images/ImgGame/Garden Elements.jpg
        },
        {
            price: 11000,
            pictureName: 'Maximilian Schmidt Brass-Mounted Mahogany Octagonal Center Table',
            autorName: 'Maximilian Schmidt',
            imageSource: 'https://www.artnet.com/WebServices/images/ll00039lld0emJFgQUmP3CfDrCWvaHBOcpp1F/max-schmidt-maximilian-schmidt-brass-mounted-mahogany-octagonal-center-table.jpg'///src/lib/images/ImgGame/Maximilian Schmidt Brass-Mounted Mahogany Octagonal Center Table.jpg
        },
        {
            price: 568100,
            pictureName: 'Tête de femme’ table lamp',
            autorName: 'Designed by Alberto Giacometti, 1937',
            imageSource: 'https://d7hftxdivxxvm.cloudfront.net/?height=799&quality=85&resize_to=fit&src=https%3A%2F%2Fd32dm0rphc51dk.cloudfront.net%2FLO9zogF6P2aTzalkhL1FDw%2Fnormalized.jpg&width=608'//Tête de femme’ table lamp
        },
        {
            price: 306288,
            pictureName: 'Concetto Spaziale',
            autorName: 'Lucio Fontana, 1962/1965',
            imageSource: 'https://www.dorotheum.com/fileadmin/lot-images/38M151125/normal/lucio-fontana-2222093.jpg'//Concetto Spaziale
        },
        {
            price: 13000,
            pictureName: '"LANDSCAPE" GLASS INSTALLATION, 20 PIECES',
            autorName: 'Martin Blank, 2011',
            imageSource: 'https://media.mutualart.com/Images/2020_02/06/15/154734256/d04aea58-ba30-469b-9c16-1875fac748d3.Jpeg?w=768'//"LANDSCAPE" GLASS INSTALLATION, 20 PIECES
        },
        {
            price: 56875,
            pictureName: 'TÊTE DE FEMME',
            autorName: 'Pablo Picasso, Executed  circa  1940-1944',
            imageSource: 'https://media.mutualart.com/Images//2020_01/15/13/135614890/1b4a84fc-06b6-4424-8a3e-3591d432f44c.Jpeg'// /src/lib/images/ImgGame/TÊTE DE FEMME.jpg
        },
        {
            price: 39505700,
            pictureName: 'ABSTRAKTES BILD',
            autorName: 'Gerhard Richter, 1986',
            imageSource: 'https://artlogic-res.cloudinary.com/w_1600,h_1600,c_limit,f_auto,fl_lossy,q_auto/artlogicstorage/vedovigallery/images/view/362671be6b3fd96e36253f631dc13c52j/vedovigallery-gerhard-richter-abstraktes-bild-1986.jpg'///src/lib/images/ImgGame/ABSTRAKTES BILD.jpg
        },
        {
            price: 1463500,
            pictureName: 'Il Parle',
            autorName: 'Jean Dubuffet, 1961',
            imageSource: 'https://www.artnet.com/WebServices/images/ll00018lldobCGFgUNECfDrCWvaHBOcomt/jean-dubuffet-il-parle.jpg'///src/lib/images/ImgGame/Il Parle.jpg
        },
        {
            price: 375000,
            pictureName: "LES OIES'",
            autorName: 'François-Xavier Lalanne, designed circa 1992',
            imageSource: "https://media.mutualart.com/Images/2019_05/09/01/010244717/0cf9b431-0d0a-4e05-805f-f78054e7369f_570.Jpeg"///src/lib/images/ImgGame/LES OIES'.jpg
        },
        {
            price: 26250,
            pictureName: 'Defense Against Banality',
            autorName: 'Rafal Olbinski',
            imageSource: 'https://www.artnet.com/WebServices/images/ll00079lldyemJFg1xjR3CfDrCWvaHBOcmC2F/rafa%C5%82-olbi%C5%84ski-defense-against-banality.jpg'///src/lib/images/ImgGame/Defense Against Banality.jpg
        },
        {
            price: 276250,
            pictureName: 'Spare Moment',
            autorName: 'Tschabalala Self, Executed in 2015',
            imageSource: 'https://www.artnet.com/WebServices/images/ll00003lldyemJFgPNECfDrCWvaHBOc0Z1F/tschabalala-self-spare-moment.jpg'///src/lib/images/ImgGame/Spare Moment.jpg
        },
        {
            price: 260000,
            pictureName: 'STRINGED OBJECT',
            autorName: 'Henry Moore, 1938',
            imageSource: 'https://media.mutualart.com/Images//2018_10/02/09/093850182/11047656-29db-4110-bca1-f251230cb040.Jpeg'///src/lib/images/ImgGame/STRINGED OBJECT.jpg
        },
        {
            price: 159408,
            pictureName: 'Lauriers blancs dans un vase Galle I',
            autorName: 'Bernard Buffet, 1990',
            imageSource: 'https://www.artnet.com/WebServices/images/ll00090lldp1VJFgJXECfDrCWvaHBOcvKeF/bernard-buffet-lauriers-blancs-dans-un-vase-galle-i.jpg'///src/lib/images/ImgGame/Lauriers blancs dans un vase Galle I.jpg
        },
        {
            price: 410400,
            pictureName: 'Crocefisso',
            autorName: 'Designed by Lucio Fontana, 1950 - 1955',
            imageSource: 'https://media.mutualart.com/Images/2019_11/26/11/111029165/fe7befe6-d7d1-4880-ac46-a3f402b70f6a_570.Jpeg'///src/lib/images/ImgGame/Crocefisso.jpg
        },
        {
            price: 79380,
            pictureName: 'Des Mandarins',
            autorName: 'Qing Dynasty 19th Century',
            imageSource: 'https://media.mutualart.com/Images/2017_07/27/12/124906352/e43c0f83-b31c-42d3-88d6-f757ed5ebbfe.Jpeg?w=768'///src/lib/images/ImgGame/Des Mandarins.jpg
        },
        {
            price: 2346500,
            pictureName: 'Figura de perfil',
            autorName: 'Salvador Dalí, 1925',
            imageSource: 'https://img1.bonhams.com/image?src=Images/live/2017-01/19/24111283-1-6.tif&height=430&quality=90'///src/lib/images/ImgGame/Figura de perfil.jpg
        },
        {
            price: 1870000,
            pictureName: 'Keep it Spotless',
            autorName: 'Banksy',
            imageSource: 'https://banksyexplained.com/wp-content/uploads/2021/04/KEEP-IT-SPOTLESS-2007-SOTHEBYS.jpg'///src/lib/images/ImgGame/Keep it Spotless.jpg
        },
        {
            price: 56875,
            pictureName: 'Moreton Bay Fig, Botanic Gardens',
            autorName: 'Brett Whiteley, 1984',
            imageSource: 'https://images-cdn.auctionmobility.com/is3/auctionmobility-static/Movx-1-95MRV//007_1.jpg?width=880&height=880&resizeinbox=true'///src/lib/images/ImgGame/Moreton Bay Fig, Botanic Gardens.jpg
        },
        {
            price: 2364050,
            pictureName: 'Reclining Figure',
            autorName: 'Henry Moore, 1945',
            imageSource: 'https://sfmoma-media-dev.s3.us-west-1.amazonaws.com/www-media/2022/05/02111825/52.6715_01_H02-Large-TIFF_4000-pixels-long.jpg'///src/lib/images/ImgGame/Reclining Figure.jpg
        },
        {
            price: 56875,
            pictureName: 'THE NUBIAN GUARD',
            autorName: 'Charles Knighton Warren',//Charles Knighton Warren
            imageSource: 'https://images.fineartamerica.com/images/artworkimages/mediumlarge/2/the-nubian-guard-1883-charles-knighton-warren.jpg'///src/lib/images/ImgGame/THE NUBIAN GUARD.jpg
        },
        {
            price: 346680,
            pictureName: 'Tête de femme penchée',
            autorName: 'Pablo Picasso, Executed  circa  1940-1944',//Pablo Picasso, Executed  circa  1940-1944
            imageSource: 'https://www.artnet.com/WebServices/images/ll00121lldpemJFgPNECfDrCWvaHBOcMD1F/pablo-picasso-t%C3%AAte-de-femme-pench%C3%A9e.jpg'///src/lib/images/ImgGame/Tête de femme penchée.jpg
        },
        {
            price: 372000,
            pictureName: 'PETUNIAS IN OVAL, NO. 2',
            autorName: "Georgia O'Keeffe",
            imageSource: 'https://www.artnet.com/WebServices/images/ll00057lld196FFgneECfDrCWvaHBOcZCM/georgia-okeeffe-petunias-in-oval,-no.2.jpg'///src/lib/images/ImgGame/PETUNIAS IN OVAL, NO. 2.jpg
        },
        {
            price: 16165000,
            pictureName:
                'Forme uniche della continuità nello spazio (Unique Forms of Continuity in Space)',
            autorName: 'Umberto Boccioni, 1972, Conceived in 1913 and cast in 1972',
            imageSource:
                'https://upload.wikimedia.org/wikipedia/commons/thumb/f/fd/%27Unique_Forms_of_Continuity_in_Space%27%2C_1913_bronze_by_Umberto_Boccioni.jpg/1200px-%27Unique_Forms_of_Continuity_in_Space%27%2C_1913_bronze_by_Umberto_Boccioni.jpg'///src/lib/images/ImgGame/Forme uniche della continuità nello spazio (Unique Forms of Continuity in Space).jpg
        },
        {
            price: 519000,
            pictureName: 'Year After Year',
            autorName: 'Ed Ruscha, 1973',
            imageSource: 'https://www.christies.com/img/LotImages/2019/NYR/2019_NYR_17648_0017_000(ed_ruscha_year_after_year035623).jpg?mode=max'///src/lib/images/ImgGame/Year After Year.jpg
        },
        {
            price: 432500,
            pictureName: 'Roses dans un vase de fleurs',
            autorName: 'Pierre-Auguste Renoir',
            imageSource: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Renoir_-_Roses_dans_un_vase_de_fleurs%2C_42.1_x_36.7_cm.jpg/771px-Renoir_-_Roses_dans_un_vase_de_fleurs%2C_42.1_x_36.7_cm.jpg?20190207115740'///src/lib/images/ImgGame/Roses dans un vase de fleurs.jpg
        },
        {
            price: 2081700,
            pictureName: 'Manteau de Cheminée',
            autorName: 'Designed by Jean Dunand, 1926',
            imageSource: 'https://media.mutualart.com/Images//2016_11/04/10/100510601/3c608953-3bc5-4599-a3bf-358ce6ceae91.Jpeg'///src/lib/images/ImgGame/Manteau de Cheminée.jpg
        },
        {
            price: 30875,
            pictureName: 'Roses',
            autorName: 'Yao Hua, 1924',
            imageSource: 'https://www.artnet.com/WebServices/images/ll01406lldSM5GFgSeECfDrCWvaHBOcEp9D/yao-hua-roses.jpg'///src/lib/images/ImgGame/Roses.jpg
        },
        {
            price: 56875,
            pictureName: 'GENERAL',
            autorName: 'Boris Orlov, dated 2004',
            imageSource: 'https://sothebys-md.brightspotcdn.com/dims4/default/b64d86b/2147483647/strip/true/crop/1142x2000+0+0/resize/2048x3587!/quality/90/?url=http%3A%2F%2Fsothebys-brightspot.s3.amazonaws.com%2Fmedia-desk%2Fa9%2Ff6%2Fa073a98b499c9ad1131e16547328%2F223n10226-b9534.jpg'///src/lib/images/ImgGame/GENERAL.jpg
        },
        {
            price: 1805000,
            pictureName: 'PETIT SERGENT MAJOR',
            autorName: 'Jean Dubuffet, 1943',
            imageSource: 'https://www.artnet.com/WebServices/images/ll00118lldob9GFgneECfDrCWvaHBOcamKE/jean-dubuffet-petit-sergent-major.jpg'///src/lib/images/ImgGame/PETIT SERGENT MAJOR.jpg
        },
        {
            price: 872625,
            pictureName: 'Segelschiff I',
            autorName: 'Walter Dexel, 1922, Painted in 1922',
            imageSource: 'https://media.mutualart.com/Images/2020_01/14/20/201640070/047dc227-efaf-4b20-b486-18e05e488ad2_570.Jpeg?w=480'///src/lib/images/ImgGame/Segelschiff I.jpg
        },
        {
            price: 3419500,
            pictureName: "Ram's Head, Blue Morning Glory",
            autorName: "Georgia O'Keeffe, 1938",
            imageSource: "https://www.georgiaokeeffe.net/assets/img/paintings/rams-head-blue-morning-glory.jpg"///src/lib/images/ImgGame/Ram's Head, Blue Morning Glory.jpg
        },
        {
            price: 2081700,
            pictureName: "J'accours",
            autorName: 'Jean Dubuffet, 1964',
            imageSource: "https://www.artnet.com/WebServices/images/ll00007lldpRRJFgVNECfDrCWvaHBOc7jOF/jean-dubuffet-jaccours.jpg"///src/lib/images/ImgGame/J'accours.jpg
        },
        {
            price: 52000,
            pictureName: 'Magnolia Door One',
            autorName: 'Gary Hume, Painted in 1988',
            imageSource: 'https://www.artnet.com/WebServices/images/ll00021lldzemJFg8YECfDrCWvaHBOcYn1F/gary-hume-magnolia-door-one.jpg'//  /src/lib/images/ImgGame/Magnolia Door One.jpg
        },
        {
            price: 22587500,
            pictureName: 'Ocean Park #137',
            autorName: 'Richard Diebenkorn, 1985',
            imageSource: 'https://www.artnet.com/WebServices/images/ll0031ClldZ3VJFgUNECfDrCWvaHBOc7QeF/richard-diebenkorn-ocean-park-137.jpg'///src/lib/images/ImgGame/Ocean Park 137.jpg
        }
    ];


    let CopiedArray = ImagesNames;
    function getRandomInt(min, max) {
        const minCeiled = Math.ceil(min);
        const maxFloored = Math.floor(max);
        return Math.floor(Math.random() * (maxFloored - minCeiled) + minCeiled); // The maximum is exclusive and the minimum is inclusive
    }
    let ChossenImage = getRandomInt(0, CopiedArray.length);
    function ChangeBidSprite() {
        bidSource = 'https://cdn-icons-png.flaticon.com/512/2570/2570154.png';
    }
    function ChangeDefaultBidSprite() {
        bidSource = 'https://cdn-icons-png.flaticon.com/512/2581/2581347.png';
    }

    function BidClick() {
        if (inputValue !== 0) {
            animateTo(CopiedArray[ChossenImage].price);
            binded = true; // Define como true quando o usuário clica na imagem Bid
            points = calcPoints(inputValue, CopiedArray[ChossenImage].price);
            showPoints = true;
        }
    }

    
    

    function toggleCurtains() {
        isOpen = !isOpen;
        curtainWidth.set(isOpen ? 0 : 50);
    }
    //-------------------------------------------------------
    // Cria uma store tweened com valor inicial 0
    

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

    function delayedFunction(delay) {
        return new Promise((resolve) => {
            setTimeout(resolve, delay);
        });
    }

    async function FullResetGame() {
        ControllDiv = true;
        await delayedFunction(100);
        CloseAnimation();
        await delayedFunction(1000);
        ShowGame = true;
        TotalPoints = 0;
        CopiedArray = ImagesNames;
        inputValue = 0;
        showPoints = false;
        binded = false;
        points = 0;
        console.log("ResetGame");
        OpenAnimation();
    }
    
    function calcPoints(userValue, originalPrice) {
        const difference = Math.abs(originalPrice - userValue);
        const score = Math.max(0, 100 - (difference / originalPrice) * 100);
        return Math.round(score);
    }

    async function NextPicture() {
        ControllDiv = true;
        await delayedFunction(100);
        CloseAnimation();
        await delayedFunction(1000);
        showPoints = false;
        binded = false;
        bidSource = 'https://cdn-icons-png.flaticon.com/512/2581/2581347.png';
        inputValue = 0;
        TotalPoints += points;
        points = 0;
        round++;
        if (round >= 9) {
            round = 1;
            ShowGame = false;
        }
        CopiedArray.splice(ChossenImage, 1);
        ChossenImage = getRandomInt(0, CopiedArray.length);

        await delayedFunction(100);
        
        OpenAnimation();
    }

    
    
   
    

    async function InitialOpenAnimation(){
        await delayedFunction(2000)
        isEaseInAnimation = !isEaseInAnimation;
        await delayedFunction(1000);

        ControllDiv = false;
    }
    
    async function OpenAnimation(){
       
        isEaseInAnimation = !isEaseInAnimation;
        
        await delayedFunction(1000);

        ControllDiv = false;
        
    }

    async function CloseAnimation(){
        
        inAnimation = !inAnimation;

        await delayedFunction(1000);//is

        if(isEaseInAnimation && !inAnimation)
        {
            
            isEaseInAnimation = false;
            inAnimation = true;
        }
    }
    
    

    InitialOpenAnimation();
</script>
{#if ShowGame}
<div class="pb-8 pt-16 text-center">
    <p class="pb-4 text-base sm:text-lg md:text-xl lg:text-2xl xl:text-4xl font-bold text-purple-400">
        Round {round}/8
    </p>
    <span class="inline-block bg-purple-300 p-4 rounded-lg">
		<p class="text-base sm:text-lg md:text-xl lg:text-3xl xl:text-6xl font-bold text-purple-950">
			{CopiedArray[ChossenImage].pictureName}
		</p>
	</span>
</div>
<div class="flex items-center justify-center flex-wrap">
    <img
            src={CopiedArray[ChossenImage].imageSource}
            alt="pintura bonita"
            class="container object-contain border-double border-purple-900 border-8"
    />
</div>
<p
        class="text-base sm:text-sm md:text-base lg:text-xl xl:text-2xl text-center font-semibold pb-8 pt-16 text-purple-600"
>
    {CopiedArray[ChossenImage].autorName}
</p>

<form id="numberForm" on:submit|preventDefault={BidClick}>
    <div class="flex items-center justify-center flex-wrap">
        {#if inputValue === 0 || !binded}
            <input
                    placeholder="$0"
                    type="number"
                    id="number"
                    name="number"
                    oninput="this.value = this.value.replace(/[^0-9]/g, '')"
                    bind:value={inputValue}
                    class="border-8 border-purple-700 bg-purple-300 text-purple-950 placeholder:text-purple-950 text-2xl number-input h-24 text-center appearance-none px-4 py-2 focus:outline-none focus:border-blue-500 placeholder-gray-400 no-spin"
                    required
            />
        {:else}
            <input
                    placeholder="$0"
                    type="text"
                    id="number"
                    name="number"
                    value={formatNumberWithSpaces($roundedCount)}
                    class="border-8 border-purple-700 bg-purple-300 text-purple-950 placeholder:text-purple-950 text-2xl number-input h-24 text-center appearance-none px-4 py-2 focus:outline-none focus:border-blue-500 placeholder-gray-400 no-spin"
                    required
            />
        {/if}
        <img
                src={bidSource}
                alt="Bid"
                on:mouseover={ChangeBidSprite}
                on:mouseout={ChangeDefaultBidSprite}
                on:click={BidClick}
                width="96"
                class="border-8 border-purple-700 cursor-pointer bg-fuchsia-200"
        />
    </div>
</form>

<div class="flex items-center justify-center flex-wrap pt-16 text-center">
    {#if showPoints}
        <div class="inline-flex bg-fuchsia-200 p-4 rounded-lg">
            <p class="text-2xl text-purple-950 mx-auto pr-20 my-auto">{points} points</p>
            <button
                    class="rounded-lg bg-purple-300 h-24 w-44 text-2xl font-extrabold text-purple-950 border-dashed"
                    on:click={NextPicture}>Next</button
            >
        </div>
    {/if}
</div>



{:else}
    <div class="border-double border-purple-950 inline-block bg-purple-300 p-4 rounded-lg">
    <h1 class="flex items-center justify-center flex-wrap text-base sm:text-1xl md:text-2xl lg:text-5xl xl:text-6xl font-bold text-purple-950 mt-14 mb-6 ">{TotalPoints} Points</h1>
    </div>
    <div class="flex items-center justify-center flex-wrap">
    
    <img src="https://blog.abac.org.br/wp-content/uploads/2023/12/auction-gavel-with-coins-on-violet-background-public-sale.jpg_s1024x1024wisk20crZUu8DnTej-HUfGg14EEAgvCHa5tPlLTsCOMRrJ_xTU-768x768.jpg"
    class="container object-contain border-double border-purple-900 border-8 mt-16"
    alt="Auction Img">
    </div>
    <div class="flex items-center justify-center flex-wrap pt-16">
        <button on:click={FullResetGame} 
                class="rounded-lg bg-purple-300 h-24 w-44 text-2xl font-extrabold text-purple-950 border-dashed hover:bg-fuchsia-200">
             Play Again
        </button>
    </div>
{/if}
{#if ControllDiv }
    <div class="absolute w-screen top-0 left-0">
        <div class="flex relative w-full h-screen">
            {#if isEaseInAnimation && !inAnimation}

                <div
                        in:fly={{
					delay: 0,
					duration: 1000,
					x: -900
				}}
                >
                    <img src="https://media.istockphoto.com/id/1387068345/vector/stage-curtain-background.jpg?s=612x612&w=0&k=20&c=g_wq5Kw7BcaWFJFzo584JCnPRQ6rR27ZMff2QmPbMGc=" alt="Imagem" class="object-cover h-full" style="right: 100%"/>
                </div>
                <div
                        in:fly={{
					delay: 0,
					duration: 1000,
					x: 900
				}}
                >
                    <img  src="https://media.istockphoto.com/id/1387068345/vector/stage-curtain-background.jpg?s=612x612&w=0&k=20&c=g_wq5Kw7BcaWFJFzo584JCnPRQ6rR27ZMff2QmPbMGc=" alt="Imagem" class="object-cover h-full"/>
                </div>
            {/if}

        </div>
    </div>

    <div class="absolute w-screen top-0 left-0">
        <div class="flex relative w-full h-screen">
            {#if !isEaseInAnimation }
                <div
                        out:fly={{
					delay: 0,
					duration: 1000,
					x: -900
				}}
                >
                    <img src="https://media.istockphoto.com/id/1387068345/vector/stage-curtain-background.jpg?s=612x612&w=0&k=20&c=g_wq5Kw7BcaWFJFzo584JCnPRQ6rR27ZMff2QmPbMGc=" alt="Imagem" class="object-cover h-full" style="right: 100%"/>
                </div>
                <div
                        out:fly={{
					delay: 0,
					duration: 1000,
					x: 900
				}}
                >
                    <img src="https://media.istockphoto.com/id/1387068345/vector/stage-curtain-background.jpg?s=612x612&w=0&k=20&c=g_wq5Kw7BcaWFJFzo584JCnPRQ6rR27ZMff2QmPbMGc=" alt="Imagem" class="object-cover h-full"/>
                </div>
            {/if}
        </div>
    </div>
{/if}
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

    

    @keyframes slideIn1 {
        from {
            transform: translateX(0%);
        }
        10% {
            transform: translateX(10%);
        }
        50% {
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
        10% {
            transform: translateX(150%);
        }
        50% {
            transform: translateX(10%);
        }
        to {
            transform: translateX(0);
        }
    }

   

    @keyframes slideIn {
        from {
            transform: translateX(0%);
        }
        10% {
            transform: translateX(-10%);
        }
        50% {
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
        10% {
            transform: translateX(-150%);
        }
        50% {
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