# Fusao_FBDS
Processamento de Dados Geoespaciais da FBDS para o Estado de Rondônia

Este repositório contém scripts adaptados para baixar e processar os dados geoespaciais da Fundação Brasileira para o Desenvolvimento Sustentável (FBDS) especificamente para o estado de Rondônia.


Adaptado de https://github.com/fronzag/fbds_database

Também consultei as informções disponibilizadas no script original do Michel Metran https://github.com/michelmetran

Descrição do Projeto

O objetivo deste projeto é facilitar o download e o processamento dos dados geoespaciais fornecidos pela FBDS, consolidando as informações de todos os municípios de Rondônia em um único geopacote (.gpkg).

Passo a Passo

1- Acesso ao Portal FBDS Geo
Acesse o site geo .fbds .org .br e selecione o estado de Rondônia para obter os dados geoespaciais disponíveis.

2- Download do Notebook Original
Baixei o notebook 02_processar_dados_estado_FBDS.ipynbdo repositório original fronzag /br_fbds .

3- Configuração do Ambiente
Importei o notebook para o meu ambiente Anaconda, utilizando o Jupyter Notebook.

4- Adição dos Diretórios de Dados
Adicionei os diretórios contendo os arquivos do FBDS para o estado de Rondônia ao meu ambiente de trabalho.

5- Ajuste no Script
Identifiquei um erro no script original ao listar as pastas dos municípios. Para corrigir isso, adicionei a seguinte linha de código:

# Gerar dicionário de estados dinamicamente percorrendo subpastas
states_root = {estado.name: estado for estado in input_path.iterdir() if estado.is_dir()}

Esse ajuste permite listar corretamente todas as pastas correspondentes aos municípios, corrigindo o erro encontrado no script original.

6- Consolidação das Camadas
No final, adicionei uma função para unificar todas as camadas iguais provenientes de diferentes municípios em uma única camada para o estado, já que os dados são exportados por município.

Script funcionando com todos os ajustes: https://github.com/neurojunior/Fusao_FBDS/blob/main/FBDS.ipynb

Agradecimentos
Michel Metran e José Guilherme Fronza : Pelo desenvolvimento do script original.
