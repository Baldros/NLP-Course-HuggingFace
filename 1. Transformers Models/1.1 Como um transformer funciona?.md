# Como um fransformer funciona?

Redes Neurais (ou neuronais, a depender do autor) é uma técnica de aprendizado de máquina
que foi se refinando ao longo do tempo. Desde os perceptrons de Rosenblatt, desenvolvidos
entre os anos 50 e 60, muita coisa aconteceu, mas poucas coisas foram tão importantes para
a técnica quanto a elaboração dos transformers e o seu mecanismo de atenção. Aqui, o curso
faz uma abordagem teorica sobre a construção do conceito, dando uma uma olhada de alto nível
na arquitetura dos modelos Transformer. 

## Um pouco de história:
**Junho de 2018: GPT**, o primeiro modelo Transformer pré-treinado, usado para ajuste fino em
várias tarefas de PNL e obteve resultados de última geração;
https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf

**Outubro de 2018: BERT**, outro grande modelo pré-treinado, projetado para produzir melhores
resumos de frases (mais sobre isso no próximo capítulo!);
https://arxiv.org/pdf/1810.04805.pdf

**Fevereiro de 2019: GPT-2**, uma versão melhorada (e maior) do GPT que não foi divulgada
publicamente imediatamente devido a questões éticas;
https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf

**Outubro de 2019: DistilBERT**, uma versão destilada do BERT que é 60% mais rápida, 40% mais
leve na memória e ainda mantém 97% do desempenho do BERT;
https://arxiv.org/pdf/1910.01108.pdf

**Outubro de 2019: BART e T5**, dois grandes modelos pré-treinados usando a mesma arquitetura 
do modelo Transformer original (o primeiro a fazê-lo);
Bart: https://arxiv.org/pdf/1910.13461.pdf
T5: https://arxiv.org/pdf/1910.10683.pdf

**Maio de 2020, GPT-3**, uma versão ainda maior do GPT-2 que é capaz de funcionar bem em
uma variedade de tarefas sem a necessidade de ajuste fino (chamado aprendizado zero-shot);

Esta lista está longe de ser abrangente e serve apenas para destacar alguns dos diferentes
tipos de modelos de Transformer. Em termos gerais, eles podem ser agrupados em três categorias:

1. GPT-like (também chamados de modelos de Transformer auto-regressivos)
2. BERT-like (também chamados de modelos Transformer de codificação automática)
3. BART/T5-like (também chamados de modelos de transformador sequência a sequência)
