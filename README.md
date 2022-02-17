<div align="center">
<h1>
  Raspagem de dados da B3
  </h1>
  <a href="https://www.b3.com.br/pt_br/">
  <img src="https://i.imgur.com/3LURIFu.png" width="200">
  </a>
  </div>
  
# Obsoleto
O site da B3 foi alterado em fevereiro de 2022, os dados anteriores a 2010 foram bloqueados pelo sistema ENAT, desta forma, o código não será modificado para a nova versão.

# PT-BR
## Sobre
Raspagem e manipulação de dados para ações brasileiras utilizando dados do site da BVMF-B3.

[Repositório](https://github.com/capuccino26/BVMF-Scraping)

## Pré-requisitos
* O código utiliza o Firefox como webdriver, será necessário o arquivo geckodriver.exe no Path, já incluso no repositório, porém é recomendado o download da versão mais recente: [GeckoDriver](https://github.com/mozilla/geckodriver/releases).

## Sobre a CVM
A CVM (Comissão de Valores Mobiliários) é responsável pelo funcionamento do mercado de valores mobiliários brasileiro, sendo responsável diretamente pela listagem de novas companhias, assim, definindo seus respectivos códigos que são aqui utilizados para identificação da empresa e busca para raspagem de dados. Os códigos podem ser obtidos [aqui](https://cvmweb.cvm.gov.br/SWB/Sistemas/SCW/CPublica/CiaAb/FormBuscaCiaAb.aspx?TipoConsult=c).

## Utilização
* O usuário insere os códigos CVM das empresas que deseja buscar;
* O usuário insere o período em anos, separados por vírgula, que deseja buscar:
  * Caso queira buscar todos os anos disponíveis o usuário deverá deixar este campo vazio.
* O usuário insere se deseja ou não manter os arquivos brutos;
* As seguintes mensagens de confirmação serão exibidas com o andamento do programa:
  * Código CVM válido/inválido.
  * Listagem de datas: total ou inseridas pelo usuário.
  * Confirmação do modelo de formulário antigo/novo de acordo com o obtido da BVMF.
  * Confirmação da ausência de dados para informações individuais, ano específico ou empresa específica.
  * Confirmação de falha do carregamento da página por instabilidade da BVMF.
  * Confirmação de finalização para cada empresa.
  * Confirmação de finalização geral.
* Para os dados extraídos com sucesso será gerada uma nova pasta em Path chamada "BVMF" onde cada empresa será listada separadamente.
* Cada empresa possui os arquivos brutos no formato ".xlsx" e gráficos com dados relevantes.

### Obtendo códigos de arquivo excel
* Para maior facilidade do usuário, a versão alternativa "BVMF_SCRAPING_FROMEXCEL" foi criada, nesta versão é possível criar um arquivo com os códigos desejados e o programa irá buscar por todos de uma vez, sem a necessidade de digitar.
* Nesta versão existe uma nova caixa de diálogo onde o usuário deverá digitar o nome do arquivo com os códigos localizado no Path, com os códigos na primeira coluna como no exemplo "CÓDIGOS_CVM" anexado.

## Observações
* O site da B3 encontra instabilidades constantemente, o que prejudica a raspagem de dados. Entretanto, os dados podem ser coletados individualmente posteriormente para datas faltantes por instabilidade.

# Exemplo
  * Usuário insere os códigos: 23264,9512
  * Usuário insere as datas/não insere nada para todas as datas serem buscadas:
  * Exemplo de output:
  ```
Código CVM válido: 23264 (AMBEV S.A.).
Datas: 2012,2013,2014,2015,2016,2017,2018,2019,2020,2021.
Formulário de AMBEV S.A. em 2012 no modelo BVMF novo.
Formulário de AMBEV S.A. em 2013 no modelo BVMF novo.
Formulário de AMBEV S.A. em 2014 no modelo BVMF novo.
Formulário de AMBEV S.A. em 2015 no modelo BVMF novo.
Formulário de AMBEV S.A. em 2016 no modelo BVMF novo.
AMBEV S.A. não possui dados para 2016.
Formulário de AMBEV S.A. em 2017 no modelo BVMF novo.
AMBEV S.A. não possui dados para 2017.
Formulário de AMBEV S.A. em 2018 no modelo BVMF novo.
Formulário de AMBEV S.A. em 2019 no modelo BVMF novo.
Formulário de AMBEV S.A. em 2020 no modelo BVMF novo.
AMBEV_ completo.
Código CVM válido: 9512 (PETROLEO BRASILEIRO S.A. PETROBRAS).
Datas: 1998,1999,2000,2001,2002,2003,2004,2005,2006,2007,2008,2009,2010,2011,2012,2013,2014,2015,2016,2017,2018,2019,2020,2021.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 1998 no modelo BVMF antigo.
Fluxo de Caixa de PETROLEO BRASILEIRO S.A. PETROBRAS em 1998 sem dados.
Valor adicionado de PETROLEO BRASILEIRO S.A. PETROBRAS em 1998 sem dados.
Página não carregada para PETROLEO BRASILEIRO S.A. PETROBRAS em 1999.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2000 no modelo BVMF antigo.
Fluxo de Caixa de PETROLEO BRASILEIRO S.A. PETROBRAS em 2000 sem dados.
Valor adicionado de PETROLEO BRASILEIRO S.A. PETROBRAS em 2000 sem dados.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2001 no modelo BVMF antigo.
Fluxo de Caixa de PETROLEO BRASILEIRO S.A. PETROBRAS em 2001 sem dados.
Valor adicionado de PETROLEO BRASILEIRO S.A. PETROBRAS em 2001 sem dados.
Página não carregada para PETROLEO BRASILEIRO S.A. PETROBRAS em 2002.
Página não carregada para PETROLEO BRASILEIRO S.A. PETROBRAS em 2003.
Página não carregada para PETROLEO BRASILEIRO S.A. PETROBRAS em 2004.
Página não carregada para PETROLEO BRASILEIRO S.A. PETROBRAS em 2005.
Página não carregada para PETROLEO BRASILEIRO S.A. PETROBRAS em 2006.
Página não carregada para PETROLEO BRASILEIRO S.A. PETROBRAS em 2007.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2008 no modelo BVMF antigo.
Página não carregada para PETROLEO BRASILEIRO S.A. PETROBRAS em 2009.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2010 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2011 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2012 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2013 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2014 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2015 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2016 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2017 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2018 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2019 no modelo BVMF novo.
Formulário de PETROLEO BRASILEIRO S.A. PETROBRAS em 2020 no modelo BVMF novo.
PETROLEO_BRASILEIRO__PETROBRAS completo.
Finalizado.
  ```
  * Pasta principal gerada:
  
  ![alt text](https://i.imgur.com/e2PTnMk.png)
  
  * Pasta gerada para cada empresa:
  
  ![alt text](https://i.imgur.com/zwwU6ax.png)
  
  * Gráficos gerados:
  
  ![alt text](https://i.imgur.com/IipYYsk.png)

# EN-US
## About
Scraping and managing data for brazilian (B3) stocks from BVMF-B3 website.

[Repository](https://github.com/capuccino26/BVMF-Scraping)

## Pre-Requisites
* The script uses Firefox as the webdriver, you need to have geckodriver.exe in the path, its already included in the repository but you can download the lastest version from [GeckoDriver](https://github.com/mozilla/geckodriver/releases)

## About CVM
CVM (Comissão de Valores Mobiliários - freely translated as "Securities and Exchange Commission") is responsible for the regiment of the brazilian stock market, being directly responsible for the listing of companies, thus, defining their codes, which are used here for the identification and search for scraping. The codes can be found [here](https://cvmweb.cvm.gov.br/SWB/Sistemas/SCW/CPublica/CiaAb/FormBuscaCiaAb.aspx?TipoConsult=c).

## How-to
* The user inserts the CVM codes of the desired companies;
* The user inserts the desired dates, in years, separeated by commas:
  * If the user desires to get all the available dates this field must be left empty.
* The user inserts if the raw data should be kept (type "SIM" for keep);
* The following confirmating messages will show accordingly:
  * CVM code valid/invalid.
  * Dates listed: total or inserted by user.
  * Confirmation of new/old template accordingly to BVMF.
  * Confirmation of missing data for individual information, year or company.
  * Confirmation of failure to load page due to BVMF instability.
  * Confirmation for completion of individual company.
  * Confirmation for general completion.
* For the successfully scraped data a new folder will be generated named "BVMF" with each company listed individually.
* Each company have the raw data in ".xlsx" format and the plots of relevant data.

### Obtaining CVM codes from excel file
* For an easier use the alternative version "BVMF_SCRAPING_FROMEXCEL" has been released, in which it is possible to gather the CVM codes directly from an excel file in the Path directory, with each code in one line of the first column, similar to the attached example "CÓDIGOS_CVM".
* In this version a new popup will be shown asking the name of the file in the Path folder ("CÓDIGOS_CVM" in the example).
