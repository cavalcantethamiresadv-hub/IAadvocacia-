# Caso 01: Análise da documentação do cliente

[← Voltar ao início](../README.md)

> **Resumo:** a IA realizou em 10 minutos a leitura e o cruzamento de 75 holerites, cartões de ponto, TRCT e extratos do FGTS. A revisão jurídica, porém, afastou ou corrigiu o alcance de 4 dos 6 achados, demonstrando que o resultado só adquire valor jurídico após a validação da advogada.

## Contexto

O cliente fictício, aqui identificado como Trabalhador A, exerceu a função de auxiliar de logística em uma empresa de distribuição entre março de 2020 e junho de 2026, quando foi dispensado sem justa causa. Ao procurar o escritório, apresentou um volume considerável de documentos, composto por setenta e cinco holerites, cartões de ponto de todo o período contratual, o Termo de Rescisão do Contrato de Trabalho, extratos do FGTS e a CTPS digital, relatando, em síntese, que trabalhava habitualmente além da jornada e que nem sempre usufruía integralmente do intervalo para refeição.

Diante desse cenário, o objetivo da análise era verificar, com rapidez e precisão, a viabilidade de uma reclamação trabalhista, identificando possíveis diferenças de horas extras, supressão de intervalo intrajornada, reflexos em verbas rescisórias e eventuais irregularidades nos depósitos fundiários. Tradicionalmente, a leitura manual desse material consumiria diversas horas de trabalho, razão pela qual a etapa de triagem inicial foi delegada à IA, reservando-se à advogada a validação jurídica dos achados.

## Preparação e anonimização dos documentos

Antes de qualquer interação com a ferramenta, os documentos foram submetidos a um procedimento de anonimização, com a supressão de nome, CPF, PIS, endereço, dados bancários e razão social do empregador, substituídos por identificadores genéricos. Essa cautela decorre diretamente do dever de sigilo previsto no Estatuto da Advocacia e no Código de Ética e Disciplina da OAB, bem como dos princípios da finalidade, da necessidade e da segurança consagrados no artigo 6º da Lei nº 13.709/2018.

Além disso, a escolha da ferramenta considerou suas políticas de retenção de dados, privilegiando-se ambientes que não utilizam o conteúdo inserido para treinamento de modelos. Desse modo, o uso da tecnologia se mantém compatível com as orientações do Conselho Federal da OAB sobre IA generativa na advocacia, que enfatizam a confidencialidade das informações do cliente e a supervisão humana sobre os resultados produzidos.

## Prompt utilizado

Com os documentos devidamente anonimizados, o comando foi redigido de forma a atribuir à ferramenta um papel definido, delimitar o escopo da análise e exigir que cada achado viesse acompanhado da indicação do documento de origem, o que facilita a conferência posterior pela advogada.

```text
Você é um assistente jurídico especializado em Direito do Trabalho brasileiro.
Analise os documentos anexos (holerites, cartões de ponto, TRCT, extratos do FGTS
e CTPS) referentes ao contrato de trabalho do Trabalhador A, vigente de 03/2020
a 06/2026, com jornada contratual de 44 horas semanais.

Identifique:
1. Dias e meses em que a jornada registrada excedeu 8h diárias ou 44h semanais,
   comparando com as horas extras efetivamente pagas nos holerites.
2. Dias em que o intervalo intrajornada registrado foi inferior a 1 hora.
3. Divergências entre as verbas do TRCT e os valores devidos na dispensa sem justa causa.
4. Competências sem depósito ou com depósito a menor do FGTS.

Para cada achado, indique o documento e a competência de origem.
Não faça cálculos de liquidação. Sinalize expressamente qualquer documento
ilegível ou ausente. Apresente o resultado em tabela.
```

Cumpre destacar que a vedação expressa a cálculos de liquidação foi intencional, pois essa etapa exige parâmetros jurídicos, como divisor, adicional normativo e base de cálculo, que devem ser definidos pela advogada e executados em ferramenta própria.

## Resultado bruto entregue pela IA

Em poucos minutos, a ferramenta processou todo o acervo documental e devolveu a síntese reproduzida abaixo, sem qualquer intervenção da advogada. Por se tratar do resultado bruto, ele é apresentado justamente para evidenciar, na seção seguinte, quais conclusões se sustentaram e quais exigiram correção técnica.

| Item | Achado apontado pela IA | Origem indicada |
| --- | --- | --- |
| 1 | Horas extras habituais não pagas em todo o contrato, de 03/2020 a 06/2026, com média de 1h10 diária excedente | Cartões de ponto x holerites |
| 2 | Variações de 3 a 4 minutos na entrada e na saída em cerca de 300 dias, classificadas como horas extras não pagas | Cartões de ponto |
| 3 | Intervalo intrajornada de 30 minutos em 412 dias, com direito ao pagamento de 1 hora integral acrescida de 50%, nos termos da Súmula 437 do TST | Cartões de ponto |
| 4 | Aviso prévio pago com 48 dias no TRCT, quando o correto seriam 30 dias, havendo pagamento a maior pela empresa | TRCT |
| 5 | Ausência de depósito do FGTS nas competências 04/2023 e 05/2023 | Extrato analítico do FGTS |
| 6 | Cartão de ponto de 11/2024 ilegível, impossibilitando a análise do mês | Cartões de ponto |

## Revisão crítica da advogada

A conferência dos achados revelou que a ferramenta cumpriu com eficiência a tarefa de leitura e cruzamento de dados, mas incorreu em equívocos de natureza jurídica que, se transpostos para a petição inicial, comprometeriam a credibilidade da demanda e poderiam expor o cliente a pedidos improcedentes. Por essa razão, cada item foi examinado à luz da legislação vigente e da jurisprudência consolidada do Tribunal Superior do Trabalho.

| Item | Avaliação | Fundamento |
| --- | --- | --- |
| 1 | Corrigido | Prescrição quinquenal (CF, art. 7º, XXIX; CLT, art. 11; Súmula 308, I, TST) |
| 2 | Descartado | CLT, art. 58, § 1º; Súmula 366 do TST |
| 3 | Corrigido | CLT, art. 71, § 4º, com redação da Lei nº 13.467/2017 |
| 4 | Descartado | Lei nº 12.506/2011, art. 1º, parágrafo único |
| 5 | Confirmado | Extrato analítico do FGTS |
| 6 | Confirmado | CLT, art. 74, § 2º; Súmula 338 do TST |

No tocante às horas extras do item 1, a IA desconsiderou a prescrição quinquenal. Com efeito, o artigo 7º, inciso XXIX, da Constituição Federal e o artigo 11 da CLT limitam a pretensão aos cinco anos anteriores ao ajuizamento, contados retroativamente da data de propositura da ação, conforme a Súmula 308, I, do TST. Assim, considerando o ajuizamento previsto para novembro de 2026, as parcelas anteriores a novembro de 2021 encontram-se fulminadas pela prescrição, o que reduz sensivelmente o período postulado e evita a formulação de pedido manifestamente inexigível.

Por outro lado, as variações de três a quatro minutos apontadas no item 2 não configuram horas extras. O artigo 58, § 1º, da CLT, em harmonia com a Súmula 366 do TST, afasta o cômputo das variações de horário no registro de ponto que não excedam cinco minutos por marcação, observado o limite máximo de dez minutos diários. Desse modo, o achado foi descartado, ressalvados os dias em que o somatório ultrapassou esse limite, hipótese em que a totalidade do tempo excedente passa a ser devida.

Sob esse aspecto, o equívoco mais relevante residiu no item 3. A ferramenta aplicou a Súmula 437, I, do TST, que assegurava o pagamento integral da hora de intervalo suprimida, sem atentar para o fato de que todo o contrato do Trabalhador A se desenvolveu sob a vigência da Lei nº 13.467/2017. Isso porque a nova redação do artigo 71, § 4º, da CLT determina que a supressão parcial do intervalo enseja o pagamento apenas do período suprimido, com acréscimo de 50%, e atribui a essa parcela natureza indenizatória. Por conseguinte, o pedido foi corrigido para trinta minutos diários, sem reflexos em outras verbas, o que altera de forma significativa o valor da causa.

Ainda, o item 4 continha erro de premissa, uma vez que a IA ignorou a proporcionalidade do aviso prévio. Nos termos do artigo 1º, parágrafo único, da Lei nº 12.506/2011, aos trinta dias básicos acrescem-se três dias por ano completo de serviço, de modo que seis anos de contrato resultam exatamente nos quarenta e oito dias pagos pela empresa. Portanto, não há pagamento a maior, e o registro do TRCT está correto, conclusão que impediu a inclusão de uma tese equivocada na estratégia do caso.

No que se refere aos itens 5 e 6, os achados foram confirmados. A ausência de depósitos do FGTS nas competências de abril e maio de 2023 foi verificada no extrato analítico e será objeto de pedido específico, acrescido da multa de 40% incidente sobre esses valores. Quanto ao cartão de ponto ilegível, cumpre destacar que, tratando-se de empregador com mais de vinte empregados, recai sobre ele o ônus de manter os registros de jornada, nos termos do artigo 74, § 2º, da CLT e da Súmula 338 do TST, razão pela qual será requerida a exibição do documento original.

## Resultados e conclusão

Consolidada a revisão, a triagem completa da documentação foi concluída em aproximadamente uma hora e meia, contra uma estimativa de seis horas para a leitura integralmente manual, conforme demonstra o comparativo abaixo, cujos tempos são estimativas ilustrativas.

| Etapa | Sem IA (estimado) | Com IA (estimado) |
| --- | --- | --- |
| Anonimização dos documentos | não se aplica | 20 min |
| Leitura e cruzamento de dados | 5h | 10 min |
| Revisão jurídica dos achados | 1h | 1h |
| **Total** | **6h** | **1h30** |

Nota-se que o tempo dedicado à revisão jurídica permaneceu idêntico, o que não é coincidência, mas reflexo direto da metodologia adotada. A economia concentrou-se exclusivamente na etapa mecânica de leitura, enquanto a análise técnica, responsável por afastar quatro das seis conclusões da ferramenta ou corrigir-lhes o alcance, continuou integralmente a cargo da advogada.

Portanto, o caso evidencia que a inteligência artificial é uma aliada valiosa na organização de grandes volumes documentais, mas que seus resultados só adquirem valor jurídico após a validação por profissional habilitado. Sem essa revisão, a petição inicial teria incluído parcelas prescritas, pedidos contrários à legislação vigente e uma tese inexistente sobre o aviso prévio, ao passo que, com ela, o cliente obteve um diagnóstico preciso, ágil e juridicamente seguro sobre a viabilidade de sua demanda.

---

*Caso fictício elaborado para fins de portfólio. Os dados, nomes e valores não correspondem a nenhuma situação real.*
