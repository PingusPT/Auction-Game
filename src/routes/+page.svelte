<script>
    function navigateToGame() {
        window.location.href = '/Game';
    }
</script>

<h1>Auction Game</h1>

<div class="flex items-center justify-center flex-wrap">
<button on:click={navigateToGame} class="rounded-lg bg-fuchsia-200 h-24 w-44 text-4xl font-extrabold text-purple-950 border-dashed">
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