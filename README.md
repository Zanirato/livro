# Atividade livro

Foi produzida uma atividade em duplas para intuito pedagógico, que tinha como propósito a criação de um site que chamasse a atenção do usuário e faria-o se interessar pelo livro, página que seria produzida a partir do levantamento de requisitos entre as duplas.


## 1. Levantamento de Requisitos

Inicialmente, a dupla tinha que escolher um livro cada e uma forma de conseguir os dados necessários para a criação da página. No nosso caso, optamos pela entrevista, onde cada um produziria perguntas que poderiam trazer fatores importantes para a criação da página, seja o por quê de a pessoa se interessar pelo livro ou o motivo pelo qual recomendaria para outras pessoas. Com o livro escolhido - o da minha dupla sendo "A culpa é das estrelas" e o meu sendo "Sherlock Holmes" - e o levantamento dos requisitos feitos, podemos passar para a próxima parte do projeto.



<br>

## 2. Protótipo 

Ao todo, no projeto foram feitos 2 protótipos, o de baixa fidelidade - que foi produzido a mão em uma sulfite - e de alta fidelidade - produzido no Figma. O wireframe de baixa fidelidade foi produzido para entender onde cada elemento se encaixaria, podendo ser mudado ou não no protótipo de alta fidelidade e na página. Encaixamos os elementos e procuramos idéias do quê colocar em cada bloco, além de pensar em estratégias de chamar a atenção do usuário para a página. 

Seguindo, foi produzido o wireframe de alta fidelidade, que está mais próximo do que a página seria no futuro. Nesse protótipo foi escolhido as cores e as imagens. Quanto as cores, optei por cores que remetessem o livro, preto, azul e branco. Com os textos, cores e elementos separados, parti para a produção da página.


### 2.1 Wireframe Alta Fidelidade(Figma) - Desktop
![Captura de tela 2025-02-18 162109](https://github.com/user-attachments/assets/ebdab699-ecc4-48d2-bbf5-8f8dda574a5a)


### 2.2 Wireframe Alta Fidelidade(Figma) - Mobile
![Captura de tela 2025-02-17 120550](https://github.com/user-attachments/assets/1fccdd71-88c8-4bff-b452-0057bd628c1a)


<br>

## 3. HTML

Com a base feita, começamos a produzir o esqueleto da página. Com os protótipos feitos, ficou muito mais fácil organizar as divisões de elementos. Essa parte incluiu também a finalização dos textos que seriam utilizados na página, além da edição final das imagens. Finalizamos com rapidez a parte do HTML.


### 3.1 Exemplo da estrutura - Header e apresentação
![Captura de tela 2025-02-18 162448](https://github.com/user-attachments/assets/e2d2452c-0968-48d0-9d25-0f2389c119bd)

<br>

 ## 4. CSS

 A parte que passei mais tempo foi na estilização da página. Seguindo a paleta de cores escolhida do protótipo e definindo a posição dos objetos, a página foi feita. Foi adicionada a responsividade no site para que ele funcionasse em diferentes tipos de telas. Finalizada, o site estava assim:


 ### 4.1 Página com aplicação do CSS

https://github.com/user-attachments/assets/9ac82a73-5a6f-44ac-88af-86f760673f92

<br>

## 5. JavaScript

Por fim, chegamos na parte final do projeto. Para finalizarmos, foi pedido que adicionassemos alguma funcionalidade na página aplicando o JavaScript. Na imagem principal da capa do livro - que será a imagem principal - foram adicionadas mais outras duas imagens, que quando o usuário clicasse nas setas, as imagens mudariam.


### 5.1 Código do JavaScript

```Java

let lista = document.querySelectorAll('.item')

let next = document.getElementById('proximo')
let prev = document.getElementById('anterior')

let contar = lista.length
let ativo = 0

next.onclick=()=>{
    let desativar = document.querySelector('.ativo');
    desativar.classList.remove('ativo');
    if(ativo>=contar-1){
        ativo=0;
    }else{
        ativo=ativo+1
    }
    lista[ativo].classList.add('ativo');
}

prev.onclick = () => {
    let desativar = document.querySelector('.ativo');
    desativar.classList.remove('ativo');
    if (ativo <= 0) {
        ativo = contar - 1; 
    } else {
        ativo = ativo - 1;
    }
    lista[ativo].classList.add('ativo');
};
```


No código acima, é possivél observar a definição de variáveis dos itens(as imagens), dos botões das setas (anterior e próximo), da lista que conteria as imagens e o valor da imagem principal(ativo). No resto, apliquei a lógica para o que ocorreria quando um dos botões fosse clicado.

<br>

### 5.2 Página com JavaScript - Desktop 

https://github.com/user-attachments/assets/8459c8f9-8108-447b-9535-e0a4719052e1

<br>

### 5.3 Página com JavaScript - Mobile

https://github.com/user-attachments/assets/8ef72246-f48b-4693-98bb-365921b4544b



