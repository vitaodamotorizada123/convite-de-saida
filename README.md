Projeto “Sai Comigo?”

Um projeto divertido, romântico e interativo feito em **HTML, CSS e JavaScript puro**, criado para convidar alguém especial para sair de uma forma criativa, animada e inesquecível.
Ao abrir a página, o visitante é recebido com um lindo fundo animado, botões interativos (“SIM” e “NÃO”) e corações flutuando pela tela — tudo pensado para gerar uma experiência visual marcante e cheia de charme.




Visão Geral

Este código foi desenvolvido como uma forma criativa de convite digital.
Quando a pessoa acessa a página, ela vê a pergunta:

> “Aceita sair comigo?”

Há dois botões:

* O botão **“SIM”** gera uma mensagem positiva e redireciona para um link personalizado (neste caso, uma música no YouTube).
* O botão **“NÃO”** tenta fugir do cursor, tornando impossível clicar — o que reforça a brincadeira de forma leve e bem-humorada.

Enquanto isso, **corações sobem flutuando** no fundo, criando um clima romântico e encantador.

Funcionalidades

 Fundo com **gradiente animado** em movimento constante
 **Corações flutuantes** gerados aleatoriamente com animação suave
 Texto principal com **animação de flutuação contínua**
 Botão “SIM” com **efeito pulsante e hover interativo**
 Botão “NÃO” com **movimento aleatório de fuga**
 Redirecionamento para uma **música romântica** após clicar “SIM”
 Interface totalmente **responsiva** e visualmente harmoniosa
 Código leve, sem dependências externas

---


sai-comigo/
│
├── index.html   → Código principal da página (HTML, CSS e JS integrados)




O **CSS** cria um ambiente visual romântico e animado, com efeitos suaves e modernos.

### Principais elementos estilizados:

| Elemento       | Descrição                                                                        |
| -------------- | -------------------------------------------------------------------------------- |
| **body**       | Fundo com gradiente animado em 4 cores, alternando de forma contínua             |
| **#conteudo**  | Centraliza o conteúdo vertical e horizontalmente com flexbox                     |
| **h2**         | Texto flutuante com leve animação “vai e vem”                                    |
| **.btn**       | Botões com gradiente, sombra e transição de escala                               |
| **.heart**     | Corações gerados dinamicamente com animação ascendente e rotação                 |
| **@keyframes** | Define as animações: gradiente, texto flutuante, pulsar e movimento dos corações |

### Paleta de Cores:

*  Rosa claro (`#ff9a9e`)
*  Roxo suave (`#a18cd1`)
*  Lilás (`#fbc2eb`)
*  Rosa bebê (`#fad0c4`)

Essas cores formam um **degradê harmônico e romântico** em movimento.

---

##  Lógica e Interatividade (JavaScript)

O projeto usa **JavaScript puro** para três funções principais:

### 1. `sim()`

* Exibe uma mensagem afirmando que a pessoa aceitou o convite.
* Redireciona o usuário para um link (música romântica).

```js
function sim() {
    alert("Você aceitou sair comigo! Para mais detalhes acesse o WhatsApp :)");
    location.href = "https://music.youtube.com/watch?v=izGwDsrQ1eQ";
}
```

---

### 2. `desvia(btn)`

* Faz o botão “NÃO” mudar de posição aleatoriamente sempre que o mouse se aproxima.
* Utiliza a função auxiliar `geraPosicao()` para calcular posições aleatórias entre 10% e 90% da tela.

```js
function desvia(btn) {
    btn.style.position = 'absolute';
    btn.style.bottom = geraPosicao(10, 90);
    btn.style.left = geraPosicao(10, 90);
}
```

---

### 3. `criarCoracao()`

* Gera elementos `<div>` com classe `.heart`, posicionados aleatoriamente.
* Cada coração tem um tamanho e duração de animação distintos.
* Corações somem automaticamente após 6 segundos.

```js
function criarCoracao() {
    const heart = document.createElement("div");
    heart.classList.add("heart");
    document.body.appendChild(heart);
    const size = Math.random() * 20 + 10 + "px";
    heart.style.width = size;
    heart.style.height = size;
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.animationDuration = Math.random() * 4 + 4 + "s";
    setTimeout(() => { heart.remove(); }, 6000);
}
setInterval(criarCoracao, 400);
```

---

##  Música e Mensagem

Ao clicar em **“SIM”**, o visitante é levado a uma música (neste caso, “Careless Whisper” no YouTube Music).
Você pode alterar o link de destino conforme quiser:

```js
location.href = "https://music.youtube.com/watch?v=SEU_LINK_AQUI";
```

Sugestões:

*  Uma música romântica do casal
*  Um link para conversa no WhatsApp (`https://wa.me/seunumerodetelefone`)
*  Um vídeo surpresa no YouTube

---

##  Como Executar

1. Baixe o arquivo `index.html`.
2. Dê um duplo clique no arquivo para abrir no navegador.


>  Dica: se quiser hospedar online, basta enviar para plataformas como **GitHub Pages**, **Netlify** ou **Vercel** — o projeto funciona 100% em front-end.



##  Personalizações Sugeridas

*  **Troque o link** da função `sim()` para um WhatsApp ou outro vídeo.
*  **Substitua as cores** do gradiente para um tema mais pessoal.
*  **Mude o texto** para algo mais personalizado, como “Quer ser meu amor?” ou “Namora comigo?”.
*  **Adicione música de fundo** com um `<iframe>` oculto ou um `<audio>` HTML5.
*  **Adicione emojis animados** () via CSS ou SVG.



 Créditos e Inspiração

*  Desenvolvido em **HTML + CSS + JavaScript** puro
*  Inspiração em convites interativos e interfaces românticas
*  Música: *Careless Whisper* (George Michael)
*  Animações e efeitos feitos do zero, com técnicas de **CSS moderno** e **DOM dinâmico**

---

##  Licença

Este projeto é **livre para uso pessoal e educacional**.



>  “O código é simples, mas o gesto é inesquecível.” 
