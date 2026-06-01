# RUN-GTI-01 - Instalacao do Agente Acronis

## 1) Objetivo

Padronizar a instalacao do agente Acronis em todas as maquinas elegiveis, garantindo cobertura de inventario, consistencia de dados e rastreabilidade.

## 2) Escopo

- Endpoints corporativos Windows/macOS/Linux elegiveis.
- Estacoes on-premises, filiais e notebooks corporativos.

## 3) Pre-requisitos

- Console Acronis configurada e politicas basicas criadas.
- Credenciais administrativas para deploy remoto.
- Regras de firewall/proxy liberadas para comunicacao do agente.
- Lista de maquinas por setor/unidade e dono inicial.

## 4) Metodos permitidos de instalacao

- Deploy remoto via console Acronis (preferencial).
- Deploy por GPO/Intune (ambiente gerenciado).
- Instalacao assistida/manual para excecoes tecnicas.

## 5) Procedimento operacional

1. Exportar lista base de endpoints por setor.
2. Classificar endpoints por criticidade e definir onda de implantacao.
3. Executar instalacao em lote por onda.
4. Validar status "online/healthy" do agente.
5. Aplicar politica padrao de inventario.
6. Verificar coleta de dados minima obrigatoria:
   - hostname, serial, SO, setor, usuario responsavel, localizacao.
7. Corrigir endpoints com falha em fila de remediacao.
8. Reprocessar endpoints corrigidos.
9. Fechar onda com relatorio de cobertura e pendencias.

## 6) Criterio de aceite da instalacao

- 98%+ da base da onda com agente ativo.
- 100% dos ativos da onda com dados obrigatorios preenchidos.
- Excecoes documentadas com justificativa, dono e prazo.

## 7) Troubleshooting padrao

- Falha de credencial: validar conta de deploy local/dominio.
- Falha de comunicacao: validar DNS, proxy, porta e firewall.
- Falha de compatibilidade: validar versao de SO suportada.
- Falha persistente: escalar para fila de excecao e agendar instalacao assistida.

## 8) Evidencias geradas

- Relatorio de cobertura por onda.
- Lista de falhas por causa raiz.
- Lista de excecoes com prazo de regularizacao.
