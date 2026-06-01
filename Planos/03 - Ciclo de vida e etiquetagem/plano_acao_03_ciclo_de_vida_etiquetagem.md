# Plano de Ação #03

## Implantar ciclo de vida + etiquetagem física

## 1) Identificação do Plano

| Campo                    | Valor                                                              |
| ------------------------ | ------------------------------------------------------------------ |
| Código da ação           | #03                                                                |
| Frente                   | Ativos & Conformidade                                              |
| Base metodológica        | ITIL 4 · ITAM / SACM / Change Enablement + DMAIC + 5W2H           |
| Responsável primário     | Marcone                                                            |
| Aprovação                | Kedymma / Fábio                                                    |
| Dependência obrigatória  | #02 — inventário com código definitivo concluído                   |
| Dependência secundária   | #01 — varredura Acronis consolidada (fonte de dados de entrada)    |
| Prioridade               | Alta — base estrutural da rastreabilidade de ativos para auditoria |
| Início previsto          | Imediatamente após conclusão de #02                                |
| Data-alvo                | 13/07/2026                                                         |

## 2) Objetivo do Plano

Garantir que 100% dos ativos de TI elegíveis estejam identificados fisicamente por etiqueta permanente e com ciclo de vida registrado no inventário — cobrindo aquisição, uso, movimentação, manutenção e descarte — de forma que qualquer ativo possa ser localizado, rastreado e auditado sem depender de memória individual ou controle informal.

## 3) Referência ITIL Aplicada

- **ITAM (IT Asset Management):** prática central. Define o ciclo de vida completo do ativo (aquisição → uso → movimentação → manutenção → descarte), os padrões de identificação física e a responsabilidade por cada item ao longo do tempo. É a base de tudo que esta ação constrói.
- **SACM (Service Configuration and Asset Management):** garante a integridade entre o ativo físico (etiqueta, localização, estado real) e o registro lógico no inventário. Sem SACM aplicado, o CMDB se desatualiza a cada movimentação não registrada — tornando o inventário inútil para auditoria.
- **Change Enablement:** toda movimentação, troca de usuário ou manutenção de ativo é uma mudança que precisa ser registrada formalmente. O procedimento de atualização obrigatória após cada evento é Change Enablement aplicado ao contexto de ativos físicos.

## 4) Escopo

### Inclui

- Definição e publicação dos status oficiais do ciclo de vida: **Em uso**, **Em manutenção**, **Reserva** e **Descarte**.
- Padrão definitivo de etiqueta: material alumínio resistente, código único, posição de fixação definida por tipo de equipamento e critério de substituição em caso de dano.
- POP de etiquetagem e atualização obrigatória de inventário após movimentação, troca de usuário e manutenção.
- Mutirão de regularização por ondas: Matriz → Vitória → Vila Velha, com checklist de aceite por unidade.
- Rotina de auditoria por amostragem com geração de evidência periódica e ação corretiva em até 5 dias úteis.

### Não inclui

- **Aquisição de ferramenta de discovery automático** — avaliada como melhoria futura fora do horizonte da auditoria de 13/07/2026; o mapeamento braçal (ação #24) supre a necessidade no curto prazo.
- **Regularização de licenças de software** — escopo da ação #05, que corre em paralelo e compartilha a base do inventário gerada por #02.
- **Identificação e quarentena de Shadow IT** — ações #19 e #24. Dependem desta ação: o SACM atualizado é a referência que permite identificar o que está "fora do padrão".

## 5) Ciclo DMAIC

### D - Define (Definir)

- Problema: ativos sem rastreabilidade uniforme e sem identificação física padronizada.
- Meta: 100% dos ativos elegíveis com etiqueta validada e registro atualizado.
- Clientes do processo: TI, auditoria interna, diretoria, áreas usuárias.
- Critérios críticos (CTQ): legibilidade, unicidade do código, aderência de localização, histórico de movimentação.

### M - Measure (Medir)

- Levantar baseline:
  - Percentual de ativos sem etiqueta.
  - Percentual de ativos com divergência entre físico e registro.
  - Tempo médio para localizar ativo por solicitação.
- Criar planilha de medição inicial e checkpoints semanais.

### A - Analyze (Analisar)

- Causas raiz prováveis:
  - Ausência de padrão único de identificação física.
  - Movimentações sem registro formal.
  - Falta de ponto de controle na entrada e saída de ativos.
- Análise de risco:
  - Perda patrimonial.
  - Não conformidade em auditoria.
  - Aumento de tempo de suporte e inventário.

### I - Improve (Melhorar)

- Implantar padrão de etiqueta de alumínio com código único.
- Publicar POP do ciclo de vida com responsáveis por etapa.
- Executar mutirão de regularização por unidade/setor.
- Incluir checagem obrigatória em onboarding/offboarding e manutenção.

### C - Control (Controlar)

- Auditoria interna mensal por amostragem.
- Indicadores de conformidade acompanhados em reunião de governança.
- Ação corretiva em até 5 dias úteis para divergências.
- Revisão trimestral do padrão de etiquetagem e procedimento.

## 6) Plano 5W2H

| 5W2H                    | Definição para a ação #03                                                                                                  |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| What (O que)            | Implantar processo de ciclo de vida de ativos com etiquetagem física padronizada e rastreável.                             |
| Why (Por que)           | Garantir conformidade, reduzir risco patrimonial e gerar evidência auditável de governança de ativos.                      |
| Where (Onde)            | Todas as unidades e áreas com ativos de TI (incluindo filiais).                                                            |
| When (Quando)           | Início imediato, com estabilização antes da auditoria de 13/07/2026.                                                       |
| Who (Quem)              | Marcone (owner), equipe TI (execução), gestores locais (validação de localização), diretoria (patrocínio).                 |
| How (Como)              | POP de ciclo de vida, padrão de etiqueta, inventário de regularização, conciliação físico x registro e rotina de controle. |
| How much (Quanto custa) | Baixo a moderado: etiquetas de alumínio, insumos de fixação, horas de execução e conferência.                              |

## 7) Gráfico de Fluxo (Processo Operacional)

```mermaid
flowchart TD
    A[Receber ativo novo ou ativo em uso sem etiqueta] --> B{Código definitivo existe?}
    B -- Não --> C[Gerar código único no padrão de inventário]
    B -- Sim --> D[Validar código existente]
    C --> E[Preparar etiqueta de alumínio]
    D --> E[Preparar etiqueta de alumínio]
    E --> F[Fixar etiqueta no ponto padrão do equipamento]
    F --> G[Registrar ou atualizar dados do ativo no inventário]
    G --> H{Dados físicos e lógicos conferem?}
    H -- Não --> I[Corrigir cadastro e revalidar]
    I --> H
    H -- Sim --> J[Ativo liberado para operação]
    J --> K[Movimentação, manutenção ou troca de usuário]
    K --> L[Atualizar registro e evidência]
    L --> M[Auditoria periódica por amostragem]
    M --> N{Divergência encontrada?}
    N -- Sim --> O[Ação corretiva em até 5 dias úteis]
    O --> M
    N -- Não --> P[Manter controle e monitoramento]
```

## 7.1) Fluxo de Implantação (Projeto)

```mermaid
flowchart TD
  A[Início do projeto #03] --> B[Validar dependência da ação #02]
  B --> C{Inventário com código definitivo concluído?}
  C -- Não --> D[Tratar pendências com owner da ação #02]
  D --> C
  C -- Sim --> E[Planejar cronograma por unidade/setor]
  E --> F[Definir padrão de etiqueta e materiais]
  F --> G[Pilotar implantação em área controle]
  G --> H{Piloto aprovado?}
  H -- Não --> I[Ajustar padrão e procedimento]
  I --> G
  H -- Sim --> J[Executar roll-out por ondas]
  J --> K[Consolidar indicadores e evidências]
  K --> L[Apresentar status em governança]
  L --> M[Encerrar implantação e entrar em controle contínuo]
```

## 7.2) Fluxo de Criação e Aprovação da Documentação

```mermaid
flowchart TD
  A[Levantar requisitos com TI e auditoria] --> B[Redigir POP de ciclo de vida]
  B --> C[Redigir padrão de etiquetagem]
  C --> D[Definir formulários e checklists]
  D --> E[Revisão técnica interna TI]
  E --> F{Conforme ITIL e controles internos?}
  F -- Não --> G[Ajustar documentos]
  G --> E
  F -- Sim --> H[Submeter para validação de gestão]
  H --> I[Publicar versão oficial]
  I --> J[Controlar versão e histórico de alterações]
  J --> K[Distribuir para setores impactados]
```

## 7.3) Fluxo de Comunicação do Processo

```mermaid
flowchart TD
  A[Definir público-alvo por setor] --> B[Criar plano de comunicação]
  B --> C[Preparar kit: resumo, POP, FAQ e responsabilidades]
  C --> D[Reunião de kick-off com gestores]
  D --> E[Comunicado oficial para colaboradores]
  E --> F[Canal de dúvidas e feedback]
  F --> G{Dúvidas críticas recorrentes?}
  G -- Sim --> H[Atualizar FAQ e reforçar mensagem]
  H --> E
  G -- Não --> I[Registrar evidência de comunicação]
  I --> J[Follow-up periódico até estabilização]
```

## 7.4) Fluxo de Adoção pelos Setores

```mermaid
flowchart TD
  A[Setor recebe orientação oficial] --> B[Nomear ponto focal local]
  B --> C[Treinar equipe do setor no processo]
  C --> D[Executar etiquetagem inicial do setor]
  D --> E[Validar físico x inventário com TI]
  E --> F{Aderência ao processo atingida?}
  F -- Não --> G[Aplicar plano de correção e reforço]
  G --> C
  F -- Sim --> H[Setor homologado para operação padrão]
  H --> I[Monitorar indicadores de conformidade]
  I --> J[Reconduzir para correção se houver desvio]
```

## 8) Entregáveis e Evidências para Auditoria

- Plano de implantação por ondas (unidade/setor, datas, responsáveis e critérios de aceite).
- Cronograma executivo da ação #03 com baseline e replanejamentos registrados.
- POP do ciclo de vida de ativos aprovado e publicado (com controle de versão).
- Padrão de etiqueta definido (modelo, posição, regra de codificação e critérios de substituição).
- Instrução de trabalho para etiquetagem física (passo a passo operacional).
- Checklist oficial de movimentação/troca de usuário com atualização obrigatória no inventário.
- Matriz RACI da ação (TI, gestores setoriais, diretoria e apoio administrativo).
- Relatório de cobertura de etiquetagem por unidade, setor e tipo de ativo.
- Relatório de ativos não etiquetados com plano de regularização e prazo.
- Amostra fotográfica de ativos etiquetados (antes/depois por unidade).
- Registro de conciliação físico x inventário com taxa de divergência por rodada.
- Registro de não conformidades, ações corretivas, responsável e prazo de fechamento.
- Kit de comunicação oficial (comunicado, resumo executivo, FAQ e instruções para gestores).
- Evidências de comunicação por setor (lista de distribuição, atas, prints ou protocolo de envio).
- Registro de sessões de alinhamento com gestores de área (pauta, presença e decisões).
- Lista de pontos focais nomeados por setor e termo de responsabilidade funcional.
- Evidências de treinamento por setor (presença, conteúdo aplicado e avaliação rápida).
- Termo de homologação de adoção por setor (go-live do processo local).
- Dashboard de indicadores de adoção (cobertura, acurácia, pendências e reincidência).
- Relatório de lições aprendidas do piloto e ajustes incorporados ao roll-out.

## 9) KPIs de Controle

- Cobertura de etiquetagem (%): ativos etiquetados / ativos elegíveis.
- Acurácia do inventário (%): ativos sem divergência / ativos auditados.
- Tempo de atualização de movimentação (horas).
- Taxa de reincidência de divergência por unidade.

## 10) Riscos e Mitigações

- Risco: etiqueta danificada ou removida.
  - Mitigação: padrão de material resistente e inspeção periódica.
- Risco: movimentação sem atualização de registro.
  - Mitigação: bloqueio processual (checklist obrigatório em mudança de local/usuário).
- Risco: baixa adesão das áreas.
  - Mitigação: comunicação formal + validação com gestores locais + reporte de pendências.

## 11) Critério de Conclusão da Ação #03

A ação será considerada concluída quando:

- 100% dos ativos elegíveis estiverem etiquetados.
- Inventário apresentar acurácia minima de 98% na amostragem de auditoria interna.
- Procedimento estiver publicado, em uso e com evidência de controle mensal.

## 12) Próximo Encadeamento

Após estabilizar a ação #03, usar os dados consolidados para fortalecer:

- #04 Homologação de sistemas ativos.
- #19 Tratamento de Shadow IT (quarentena e controle).
- #14 Catálogo padronizado para expansão de filiais.
