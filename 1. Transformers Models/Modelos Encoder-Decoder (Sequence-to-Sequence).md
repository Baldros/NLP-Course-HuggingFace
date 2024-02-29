# Modelos Encoder-Decoder (Sequence-to-Sequence):

Os modelos codificador-decodificador, também conhecidos como modelos sequência-sequência, representam uma categoria especializada de arquiteturas Transformer que integram tanto a parte do codificador quanto a do decodificador. Essa abordagem permite que, em cada estágio, as camadas de atenção do codificador acessem todas as palavras na sentença inicial, enquanto as camadas de atenção do decodificador podem apenas acessar as palavras posicionadas antes de uma dada palavra na entrada.

No pré-treinamento desses modelos, os objetivos podem derivar tanto de modelos de codificador quanto de decodificador, mas frequentemente envolvem estratégias mais complexas. Por exemplo, o T5 é pré-treinado substituindo trechos aleatórios de texto por uma única palavra especial de máscara, e o objetivo é prever o texto que essa palavra de máscara substitui.

Esses modelos sequência-sequência são particularmente eficazes em tarefas que exigem a geração de novas sentenças com base em uma entrada fornecida. Aplicações notáveis incluem resumos automáticos, tradução de idiomas e respostas generativas a perguntas, onde a capacidade de compreender e sintetizar informações para criar sequências significativas é crucial.
