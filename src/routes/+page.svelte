<script>
    function navigateToGame() {
        window.location.href = '/Game';
    }
</script>

<h1 class="font-extrabold text-purple-950 border-8 pt-2.5 pb-2.5 border-purple-950 bg-fuchsia-200 rounded-3xl mt-14 text-4xl sm:text-5xl md:text-6xl lg:text-7xl xl:text-8xl 2xl:text-9xl">
    Auction Game
</h1>

<div class="flex items-center justify-center h-screen">
    <button on:click={navigateToGame} class="rounded-lg bg-fuchsia-200 text-4xl font-extrabold text-purple-950 hover:text-purple-600 hover:border-purple-700 border-purple-950 border-8 p-4 sm:p-6 md:p-8 lg:p-10 xl:p-12 w-full max-w-sm sm:max-w-md md:max-w-lg lg:max-w-xl xl:max-w-2xl h-auto ">
        Enter The Auction
    </button>
</div>

<div class="background-image"></div>

<style>
    .background-image {
        background-image: url('https://d3jlwjv6gmyigl.cloudfront.net/images/2020/10/auct.jpg');
        background-size: cover;   /* Faz com que a imagem cubra todo o contêiner */
        background-position: center; /* Centraliza a imagem */
        background-repeat: no-repeat; /* Evita a repetição da imagem */
        position: fixed; /* Fixa a posição em relação à janela de visualização */
        top: 0;
        left: 0;
        width: 100vw; /* Largura total da janela de visualização */
        height: 100vh; /* Altura total da janela de visualização */
        z-index: -1; /* Coloca a imagem atrás do conteúdo */
    }
</style>