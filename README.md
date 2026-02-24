# 📈 Análise de ROE (Return on Equity) - Empresas CVM 2024/2025



Este projeto automatiza a extração, tratamento e análise de indicadores de rentabilidade (ROE) das empresas listadas na B3, utilizando os dados oficiais da CVM (Comissão de Valores Mobiliários).



## 🚀 Objetivo do Projeto
O script processa arquivos compactados (ZIP) da CVM contendo as Demonstrações Financeiras Padronizadas (DFP), extrai os dados de Lucro Líquido e Patrimônio Líquido, e calcula o ROE para identificar as empresas mais eficientes do mercado brasileiro.



## 🛠️ Tecnologias Utilizadas
* **Python 3.x**
* **Pandas**: Manipulação e tratamento de dados.
* **Matplotlib**: Geração de gráficos de barras para o TOP 20.
* **XlsxWriter**: Criação de relatórios Excel formatados com gráficos embutidos.
* **Requests/Zipfile**: Download e extração automatizada de dados.



## 📊 Metodologia de Cálculo
O cálculo segue a fórmula financeira padrão, com correções de escala para os dados da CVM (que vêm expressos em milhares de Reais):



$$ROE = \left( \frac{\text{Lucro Líquido}}{\text{Patrimônio Líquido}} \right) \times 100$$



* **DRE (Conta 3.11):** Lucro Líquido consolidado do exercício.
* **DMPL (Conta 5.05):** Patrimônio Líquido consolidado.
* **Filtros:** Empresas com Patrimônio Líquido negativo ou nulo são sinalizadas no relatório de auditoria para evitar distorções estatísticas.



## 📁 Estrutura do Repositório
* `analise_roe.py`: Script principal de processamento.
* `Relatorio_ROE_2024.xlsx`: Relatório final com tabela de dados e gráficos.
* `Audit_Dados_CVM.xlsx`: Relatório de consistência (total de empresas vs. dados válidos).
* `README.md`: Documentação do projeto.



## ⚙️ Como Executar
1. Certifique-se de ter o Python instalado.
2. Instale as dependências necessárias:
   ```bash
   pip install pandas matplotlib xlsxwriter requests
