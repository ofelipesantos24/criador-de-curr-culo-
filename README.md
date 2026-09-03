# Currículo Certo

Monte um currículo limpo, direto e compatível com leitores automáticos (ATS) — sem depender de templates travados no Canva, planilhas do Word que desmontam, ou ferramentas pagas com marca d'água.

## A dor real que isso resolve

Montar um currículo do zero é frustrante de um jeito específico:

- Templates bonitos no Word/Canva costumam ter colunas, ícones e caixas de texto que **quebram quando um sistema de triagem automática (ATS) tenta ler o currículo** — e boa parte das empresas usa esse tipo de sistema antes de um humano ver o documento.
- Ferramentas online de currículo, em geral, escondem o PDF final atrás de um plano pago.
- Editar em processador de texto é lento: mudar uma palavra desalinha a formatação inteira.

O Currículo Certo resolve isso com um formato só, deliberadamente simples: **uma coluna, sem tabelas, sem ícones, sem imagens** — o tipo de estrutura que tanto um recrutador quanto um ATS conseguem ler sem esforço. Você digita de um lado e vê o resultado pronto do outro, em tempo real.

## Como usar

1. Abra o `index.html` no navegador.
2. Preencha os campos à esquerda: dados pessoais, resumo profissional, experiências, formação e habilidades.
3. Acompanhe o currículo pronto se atualizando ao vivo, à direita.
4. Use **"+ adicionar experiência"** e **"+ adicionar formação"** para incluir quantos itens precisar; use **"remover"** para tirar um item.
5. Em habilidades, digite uma palavra-chave e clique em **Adicionar** (ou aperte Enter) para criar uma etiqueta.
6. Quando estiver satisfeito, clique em **"Exportar em PDF"** — isso abre a caixa de impressão do navegador; escolha "Salvar como PDF" como destino.
7. Use **"Limpar tudo"** para começar um currículo do zero.

Seu progresso é salvo automaticamente neste dispositivo (usando o armazenamento próprio do artefato), então você pode fechar a aba e continuar de onde parou.

## Por que essa estrutura é "ATS-friendly"

Sistemas de triagem automática costumam extrair o texto do currículo lendo de cima para baixo, coluna única. Currículos com múltiplas colunas, tabelas ou texto dentro de caixas gráficas frequentemente saem embaralhados ou incompletos desse processo. Por isso, o layout aqui é:

- Uma coluna só, sem tabelas.
- Seções com títulos claros em texto simples (Resumo, Experiência profissional, Formação, Habilidades).
- Sem ícones substituindo texto (nenhuma informação depende de um símbolo para ser entendida).

## Estrutura do projeto

```
.
├── index.html   # aplicativo completo (HTML + CSS + JS), sem dependências além de fontes web
└── README.md    # este arquivo
```

Não há back-end nem build step. É um único arquivo HTML autocontido; a exportação em PDF usa a função de impressão nativa do navegador (sem bibliotecas externas).

## Design

A ideia central: o formulário é ferramenta de trabalho, o currículo é o produto. Por isso os dois lados têm tratamentos visuais bem diferentes — o editor parece uma prancheta neutra, e a pré-visualização parece uma página impressa de verdade, com sombra sutil, como se estivesse sobre a mesa.

- **Tipografia:** Lora (serifada, para nome e títulos de seção — remete a tipografia clássica de currículo impresso) + Inter (para o restante do texto e para toda a interface do editor).
- **Cor de ação:** um marrom-nogueira (`#8B5E3C`) usado só nos botões do editor — nunca dentro do currículo em si.
- **Cor de apoio no currículo:** um verde-petróleo (`#2F5D50`) discreto, usado apenas nos títulos de seção e no cargo desejado — mantém o documento legível e sério, sem depender de decoração.

## Limitações conhecidas

- Um único modelo de layout (não há troca entre "templates" diferentes ainda).
- Não valida formato de e-mail ou telefone.
- O rascunho é salvo por dispositivo/navegador, não é sincronizado entre aparelhos.
- A exportação depende da caixa de diálogo de impressão do navegador; a aparência exata do PDF pode variar levemente entre navegadores.

## Possíveis evoluções

- Mais de um modelo visual para escolher.
- Reordenar experiências e formações por arrastar e soltar.
- Exportação direta para `.docx`.
- Sugestões automáticas de verbos de ação para as descrições de experiência.
