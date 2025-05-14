# 🧪 erp-versioning-test-suite

**Testes de validação de versões e releases em ambiente ERP, com foco em varejo e integração PDV x Web Manager x NFC-e.**

Este repositório organiza um histórico de testes funcionais manuais realizados a cada novo *codfon* exportado do backlog, assegurando que operações críticas como vendas, trocas, contingências e rejeições fiscais estejam funcionais em todas as versões.

---

## 📂 Estrutura do Repositório

```
erp-versioning-test-suite/
│
├── README.md
├── CHANGELOG.md
├── test-plan/
│   ├── VERSAO_2.14.128.120e_RADEX57.md
│   └── ...
├── templates/
│   └── test-template.md
├── docs/
│   └── instrucoes-ambiente.md
└── LICENSE
```

---

## 📋 Exemplo de Teste: `test-plan/VERSAO_2.14.128.120e_RADEX57.md`

```markdown
# 🧪 Teste de Versão: 2.14.128.120.e (RADEZ-57)
- 📅 Data: 24/04/2018
- ⏱️ Hora: 15:35
- 💾 CODFON: 1_x_x_430 [CZ]
- ⚙️ Kernel: 1.14.124.404

## ✔️ Itens Testados

| ID | Teste | Status | Observações |
|----|-------|--------|-------------|
| 01 | Venda NFC-e Normal | ✅ OK | |
| 02 | Venda em Contingência | ✅ OK | |
| 03 | Cancelamento de nota no meio da venda | ⛔ Falhou | Erro 500 no manager |
| 04 | Cancelamento via Manager (R.I.) | ⚠️ Não testado | Ambiente fora do ar |
| 05 | Subida de movimento | ✅ OK | Listagem correta no Manager |
| 06 | Busca de cliente por CPF/CNPJ | ✅ OK | CNPJ testado: `04832721000119` |
| 07 | Troca e fechamento no PDV | ✅ OK | |
| 08 | Vasilhame no PDV (7898223370207) | ✅ OK | Testado com Borrachudo |
| 09 | Integração via WebService | ✅ OK | |
| 10 | Teste Contra-Vale | ⚠️ Parçial | |
| 11 | Carga Parcial | ✅ OK | |
| 12 | Carga Completa | ✅ OK | |
| 13 | Puxar carga no PDV | ✅ OK | |
| 14 | Empenho com CNPJ | ✅ OK | VE-19=517992, VE-35=520284 |
| 15 | Empenho com CPF iniciando com 0 | ✅ OK | Ex: 041.273.812-05 |
| 16 | Biometria no PDV | ✅ OK | Abertura e fechamento |
| 17 | Venda com CPF iniciando com 0 | ✅ OK | Ex: 67.084.122-68 |
| 18 | Itens agrupados (promoção, cancelamento) | ✅ OK | |
| 19 | Lock de notas em novo servidor | ✅ OK | |
| 20 | Importador atualiza tab_nota_header | ✅ OK | |
| 21 | Consulta de CEP na troca/devolução | ✅ OK | |
| 22 | Rejeição 394 - envio forçado | ❌ Não autorizado | Ambiente hom indisponível |
| 23 | Filtro ativo relatório de promoção | ✅ OK | Processos > Promoção > Relatórios |
```

---

## 🛠️ Tecnologias e Sistemas Relacionados

* TOTVS PDV
* TOTVS Web Manager
* TOTVS RMS
* NF-e / NFC-e
* Integração via WebService
* QA Manual e Validação Fiscal
* SQL para consulta de dados de movimentação

---

## 👨‍💼 Autor

Desenvolvido por [devraphaelbezerra](https://github.com/devraphaelbezerra), especialista em varejo, automações com Fluig, TOTVS e processos críticos de PDV e gestão operacional.

---

Deseja agora que eu gere o `test-template.md` dentro da pasta `/templates` com os campos prontos para replicar os testes?
