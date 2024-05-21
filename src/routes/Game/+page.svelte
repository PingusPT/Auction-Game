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
            pictureName: "Forme uniche della continuità nello spazio (Unique Forms of Continuity in Space",
            autorName: "Umberto Boccioni, 1972, Conceived in 1913 and cast in 1972",
            imageSource: "/src/lib/images/ImgGame/Forme uniche della continuità nello spazio (Unique Forms of Continuity in Space.jpg"
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
            imageSource: "/src/lib/images/ImgGame/Magnolia Door One"
        },
        {
            price: 22587500,
            pictureName: "Ocean Park #137",
            autorName: "Richard Diebenkorn, 1985",
            imageSource: "/src/lib/images/ImgGame/Ocean Park #137"
        }
    
    ]
    let CopiedArray = ImagesNames;

    function getRandomInt(min, max) {
        const minCeiled = Math.ceil(min);
        const maxFloored = Math.floor(max);
        return Math.floor(Math.random() * (maxFloored - minCeiled) + minCeiled); // The maximum is exclusive and the minimum is inclusive
    }
    function Write(){
        ImagesNames.forEach((element) => console.log(element.pictureName));

    }
    
    let bidSource = "/src/lib/images/BidUnColor.png";
    function ChangeBidSprite()
    {
        bidSource = "/src/lib/images/bidColor.png";
    }
    function ChangeDefaultBidSprite()
    {
        bidSource = "/src/lib/images/BidUnColor.png";
    }
    function BidClick()
    {
        
    }

    import { tweened } from 'svelte/motion';
    import { cubicOut } from 'svelte/easing';
    import { derived } from 'svelte/store';

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
        return number.toLocaleString('en-US').replace(/,/g, ' ');
    }

    Write();

    const ChossenImage = getRandomInt(0, CopiedArray.length)

</script>
<p class="text-9xl">{CopiedArray[ChossenImage].pictureName}</p>
<img src="{CopiedArray[ChossenImage].imageSource}" alt="pintura bonita" height="1000" width="1000">

<p>{CopiedArray[ChossenImage].autorName}</p>
<form id="numberForm"  >
   
    <div class="flex items-center justify-center ">
        <input placeholder="$0" type="text" id="number" name="number" class="number-input h-8 mr-5 text-center appearance-none px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:border-blue-500 placeholder-gray-400 text-sm" required>
        <img src="{bidSource}" alt="Bid" on:mouseover={ChangeBidSprite} on:mouseout={ChangeDefaultBidSprite} on:click={BidClick} width="100" >
    </div>
    <input type="submit" value="Enviar">
</form>

<div >
    <!-- Botão para iniciar a animação -->
    <button on:click={() => animateTo(CopiedArray[ChossenImage].price)}>Animar para 100</button>
    

    <!-- Exibição do valor animado arredondado -->
    <div class="counter">{formatNumberWithSpaces($roundedCount)}</div>
</div>

