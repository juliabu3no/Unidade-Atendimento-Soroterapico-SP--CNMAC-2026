# Localização de Unidades de Atendimento Soroterápico no Estado de São Paulo

Notebook desenvolvido para o **XLV CNMAC (2026)**, com foco na avaliação e na otimização da cobertura de unidades de atendimento para acidentes com animais peçonhentos no estado de São Paulo.

O estudo analisa dados de acidentes, demanda municipal por soros, localização das unidades de atendimento e tempos de deslocamento. A partir desses dados, compara a rede atual com cenários de otimização para ampliar a cobertura da demanda.

## Principais etapas

- Importação e tratamento de dados geográficos, epidemiológicos e de deslocamento;
- Análise dos registros do SINAN;
- Cálculo da cobertura da rede atual em até **50 minutos**;
- Modelo de cobertura total com o menor número de postos;
- Modelo de Máxima Cobertura Ponderada (MCLP), preservando a quantidade de postos por tipo de soro e realocando-os para maximizar a demanda atendida;
- Geração de mapas, tabelas comparativas e arquivos com as alocações resultantes.

## Como executar

1. Clone este repositório.
2. Instale as dependências:

```bash
pip install numpy pandas geopandas matplotlib gdown gurobipy
```

3. Crie a pasta `dados/` na raiz do projeto.
4. Abra e execute o arquivo `CNMAC_Modelo_Cobertura.ipynb` em Jupyter Notebook ou Google Colab.

Os dados espaciais, de demanda, tempos de deslocamento e notificações do SINAN devem estar disponíveis na pasta `dados/`. Parte deles é baixada pelo próprio notebook via `gdown`.

## Observação sobre o Gurobi

O modelo utiliza o otimizador **Gurobi**. Para executá-lo, é necessário ter uma licença válida e configurada no seu ambiente.
## Autores

Júlia Perez, Julia Ortiz, Maristela Santos, Cibele Russo, Oilson G. Junior e Hellen Santos.

