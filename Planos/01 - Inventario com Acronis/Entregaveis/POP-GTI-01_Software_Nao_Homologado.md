# POP-GTI-01

## Tratamento de Software Nao Homologado

## 1) Objetivo

Padronizar as acoes da TI quando for identificado software nao homologado em qualquer ativo corporativo, assegurando rastreabilidade, avaliacao de risco, regularizacao por licenciamento e responsabilizacao formal da area quando houver negativa de compra.

## 2) Escopo

- Estacoes, notebooks e servidores inventariados.
- Softwares identificados por ferramenta de inventario, varredura tecnica ou auditoria.

## 3) Definicoes

- Software nao homologado: aplicacao sem aprovacao previa da TI e/ou sem conformidade com padroes de seguranca, compliance, arquitetura ou licenciamento.
- Responsavel do setor: gestor formal da area onde o software foi identificado.

## 4) Responsabilidades

- TI:
  - identificar, registrar e classificar risco do software encontrado;
  - notificar formalmente o responsavel do setor;
  - solicitar regularizacao via autorizacao de compra de licenca;
  - acompanhar prazo de 15 dias corridos;
  - coletar termo de responsabilidade em caso de negativa.
- Responsavel do setor:
  - responder formalmente a notificacao;
  - aprovar compra de licenca ou remover/parar uso do software;
  - quando negar compra, assinar termo de responsabilidade e ciencia de risco.
- Compras:
  - conduzir aquisicao quando autorizada.
- Juridico/Compliance (quando acionado):
  - revisar risco legal e aderencia contratual.

## 5) Gatilhos de abertura do POP

- Achado em inventario Acronis.
- Achado em auditoria interna/externa.
- Achado em atendimento tecnico (service desk).
- Achado em monitoramento de seguranca.

## 6) Procedimento detalhado (passo a passo)

1. TI registra o achado no ticket de governanca de ativos com:
   - equipamento, usuario, setor, software, versao, evidencias (print/log), data e origem do achado.
2. TI classifica criticidade e risco (baixo, medio, alto, critico), considerando:
   - risco de seguranca;
   - risco legal de licenciamento;
   - risco operacional e de continuidade.
3. TI emite Documento de Notificacao ao Responsavel do Setor contendo:
   - identificacao do software nao homologado;
   - riscos tecnicos, legais e operacionais;
   - opcoes de tratamento (compra de licenca, substituicao homologada ou remocao);
   - prazo de resposta e regularizacao.
4. TI envia a notificacao ao responsavel do setor (com copia para Compras e Gestao TI) e registra protocolo de envio.
5. TI solicita formalmente a autorizacao de compra da licenca, quando aplicavel.
6. Contagem de prazo:
   - prazo maximo de 15 dias corridos a partir do protocolo de notificacao.
7. Durante o prazo, TI acompanha status e executa follow-up em D+5 e D+10.
8. Se houver aprovacao da compra dentro do prazo:
   - Compras inicia aquisicao;
   - TI acompanha regularizacao e valida licenciamento;
   - TI atualiza inventario e encerra ticket com evidencias.
9. Se houver negativa da compra ou ausencia de aprovacao ate o D+15:
   - TI emite Termo de Responsabilidade e Ciencia de Risco;
   - responsavel do setor assina o termo;
   - termo deve declarar que o setor assume integralmente os riscos do uso do software e isenta a TI de danos, incidentes, multas, indisponibilidades e demais impactos decorrentes do software nao homologado;
   - TI arquiva termo assinado e comunica Compliance/Gestao para ciencia.
10. Se o risco for classificado como critico, a TI pode determinar bloqueio ou remocao imediata, independentemente do prazo, com escalonamento para diretoria.

## 7) SLA e prazos

- Emissao da notificacao pela TI: ate 2 dias uteis apos identificacao.
- Prazo de resposta/autorizacao do setor: 15 dias corridos apos protocolo.
- Atualizacao de status no ticket: no minimo semanal.

## 8) Criterios de encerramento

- Caso 1: software regularizado (licenca adquirida/aprovada e validada) ou removido/substituido.
- Caso 2: termo de responsabilidade assinado pelo responsavel do setor e anexado ao ticket.

## 9) Evidencias obrigatorias

- Ticket do achado com logs e classificacao de risco.
- Documento de notificacao enviado ao responsavel do setor.
- Resposta formal do setor.
- Solicitacao de compra de licenca (quando aplicavel).
- Nota fiscal/contrato da licenca ou comprovante de remocao.
- Termo de responsabilidade assinado (quando houver negativa/omissao).

## 10) Modelo minimo do Termo de Responsabilidade

O termo deve conter:

- identificacao do setor e responsavel;
- software, versao e ativo impactado;
- descricao objetiva dos riscos apontados pela TI;
- declaracao de negativa de compra no prazo de 15 dias;
- declaracao de assuncao integral de riscos pelo setor;
- declaracao de isencao da TI por danos diretos e indiretos causados pelo software nao homologado;
- data, assinatura e cargo do responsavel.

## 11) Modelos oficiais vinculados

- Notificacao ao setor: `MODELO-GTI-01_Notificacao_Software_Nao_Homologado.md`
- Termo de responsabilidade: `MODELO-GTI-01_Termo_Responsabilidade_Software_Nao_Homologado.md`
