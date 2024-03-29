# LazyLoad para Carregamento de Imagens

Este script JavaScript implementa a funcionalidade de *lazy loading* para carregar imagens em uma página HTML. *Lazy loading* é uma técnica que adia o carregamento de recursos não essenciais (como imagens) até que sejam necessários, o que pode melhorar significativamente o desempenho da página, especialmente em conexões de internet lentas.

## Como Funciona

O script utiliza a classe `IntersectionObserver` para observar quando as imagens entram na área visível da página. Quando uma imagem está prestes a ser exibida, o script substitui sua URL de imagem por uma versão de maior qualidade, ideal para o contexto de visualização, neste caso, trocando os parâmetros de largura. Isso permite carregar uma versão de menor qualidade inicialmente e, em seguida, carregar uma versão de alta qualidade conforme o usuário rola a página e as imagens ficam visíveis.

## Como Usar

1. Inclua o script em seu arquivo HTML:

```html
<script>
// Insira o script aqui
</script>
```

2 - Certifique-se de que suas imagens estejam dentro de elementos com a classe .image-container e tenham a tag <img>:

```html
<div class="image-container">
    <img src="imagem-pequena.jpg" alt="Descrição da imagem">
</div>
```

3 - Certifique-se de que as imagens tenham uma URL que possa ser ajustada com parâmetros, como no exemplo abaixo:

```html
  <img src="imagem.jpg?w=10&" alt="Descrição da imagem">
```
O script fará o restante do trabalho automaticamente, substituindo as URLs das imagens conforme necessário.

## Benefícios

Melhora o desempenho da página: Ao adiar o carregamento de imagens, especialmente em conexões lentas, a página é exibida mais rapidamente para o usuário, melhorando a experiência de navegação.
Economiza largura de banda: Carregar versões de baixa qualidade inicialmente economiza largura de banda, especialmente em dispositivos móveis ou em conexões de internet limitadas.
Aumenta a eficiência: Ao carregar imagens apenas quando são necessárias, o script reduz a carga desnecessária no servidor, aumentando a eficiência do site.

## Compatibilidade

Este script é compatível com navegadores modernos que suportam a classe IntersectionObserver, como Chrome, Firefox, Safari e Edge

