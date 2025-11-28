# Sidebar Fixa com CSS Puro

Um estudo de caso para criar uma barra lateral (sidebar) fixa e responsiva, garantindo que o conteúdo principal corra ao seu lado, utilizando apenas HTML e CSS.

O objetivo principal deste projeto foi desenvolver uma estrutura de layout de duas colunas onde a sidebar permanece fixa na lateral esquerda, cobrindo 100% da altura da tela, enquanto o conteúdo principal rola e se ajusta ao espaço restante.

---

## Solução do Problema

Durante o desenvolvimento de menus laterias(sidebar) sempre apareciam os mesmos problemas:
- O menu não ficava fixo
- O menu não tinha a altura desejada
- Conteúdo por baixo do menu
- Elementos estourando o tamanho

---

#### *1. Corrigindo a Sidebar*

Para que a sidebar fique fixa foi fácil, era só usar a propriedade `position: fixed` e para corrigir a altura `height: 100vh`.

> Tentei fazer uma versão com uma \<div> pai usando .grid separado em duas colunas, mas o menu mantinha a altura do conteudo principal e não ficava fixo.

*Resolução:*
```css
	.sidebar { 
		position: fixed; /* Mantém a sidebar fixa na tela */ 
		top: 0; 
		left: 0; 
		
		width: 20vw; /* Utiliza 'vw' (viewport width) para ser responsiva */ 
		height: 100vh; /* Ocupa 100% da altura da tela, 'vh' (viewport height) */
```

----

#### *2. Posicionando o Conteúdo*

Para corrigir a sobreposição do menu com o conteúdo só precisei pegar a largura da sidebar e empurrar o conteúdo com `margin-left: 20vw`, mantendo o `width` em `auto` para ele se ajustar ao espaço restante.

*Resolução:*
```css
	.conteudo{ 
		margin-left: 20vw;
		width: auto;
```