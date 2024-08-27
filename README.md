alternativas: [
    {
        texto: "Isso é assustador!",
        afirmacao: [
            "No início ficou com medo do que essa tecnologia pode fazer.",
            "Achou assustador pensar na velocidade na qual a tecnologia está avançando."
        ]
    },
    {
        texto: "Isso é maravilhoso!",
        afirmacao: [
            "Quis saber como usar IA no seu dia a dia.",
            "Pensou que IA pode ajudar em tarefas da sua vida."
        ]
    }
]function respostaSelecionada(opcaoSelecionada){
        const afirmacoes = aleatorio(opcaoSelecionada.afirmacao);
        historiaFinal += afirmacoes + " ";
        atual++;
        mostraPergunta();
}<!-- Trecho de código suprimido -->

<script type="module" src="js/aleatorio.js"></script>
<script type="module" src="js/perguntas.js"></script>
<script type="module" src="js/script.js"></script>
function mostraResultado() {
        caixaPerguntas.textContent = "Em 2049...";
        textoResultado.textContent = historiaFinal;
        caixaAlternativas.textContent = "";
        botaoJogarNovamente.addEventListener("click", jogaNovamente());
}.caixa-alternativas{
    display: flex;
    flex-direction: column;
    gap: 10px;
}substituiNome();function respostaSelecionada(opcaoSelecionada) {
    const afirmacoes = aleatorio(opcaoSelecionada.afirmacao);
    historiaFinal += afirmacoes + " ";
    if(opcaoSelecionada.proxima !== undefined){
        atual = opcaoSelecionada.proxima;
    }else{
        mostraResultado();
        return;
    }
    mostraPergunta();
}substituiNome();
// removemos o mostraPergunta();
