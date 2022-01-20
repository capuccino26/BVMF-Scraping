<div align="center">
<h1>
  Raspagem de dados da B3
  </h1>
  <a href="https://www.b3.com.br/pt_br/">
  <img src="https://i.imgur.com/3LURIFu.png" width="200">
  </a>
  </div>
  
# PT-BR
## Sobre
Raspagem e manipulação de dados para ações brasileiras utilizando dados do site da BVMF-B3.

[Repositório](https://github.com/capuccino26/BVMF-Scraping)

## Pré-requisitos
* O código utiliza o Firefox como webdriver, será necessário o arquivo geckodriver.exe no Path, já incluso no repositório, porém é recomendado o download da versão mais recente: [GeckoDriver](https://github.com/mozilla/geckodriver/releases).

## Utilização
* O usuário insere os códigos CVM das empresas que deseja buscar;
* O usuário insere o período em anos, separados por vírgula, que deseja buscar:
  * Caso queira buscar todos os anos disponíveis o usuário deverá deixar este campo vazio.
* As seguintes mensagens de confirmação serão exibidas com o andamento do programa:
  * Código CVM válido/inválido.
  * Listagem de datas: total ou inseridas pelo usuário.
  * Confirmação do modelo de formulário antigo/novo de acordo com o obtido da BVMF.
  * Confirmação da ausência de dados para informações individuais, ano específico, empresa específica.
  * Confirmação do não carregamento da página por instabilidade da BVMF.
  * Confirmação de finalização para cada empresa.
  * Confirmação de finalização geral.
* Para os dados extraídos com sucesso será gerada uma nova pasta em Path chamada "BVMF" onde cada empresa será listada separadamente.
* Cada empresa possui os arquivos brutos no formato ".xlsx" e gráficos com dados relevantes.

## Observações
* O site da B3 encontra instabilidades constantemente, o que prejudica a raspagem de dados. Entretanto, os dados podem ser coletados individualmente posteriormente para datas faltantes por instabilidade.

# Exemplo
  * Usuário insere os códigos: Códigos CVM separados por vírgula:  23264
  * Usuário insere as datas/não insere nada para todas as datas serem buscadas:
  * Output mostra:
  ```
  ```
  * Pasta principal gerada:
  
  ![alt text](https://i.imgur.com/PfoF2z8.png)
  
  * Pasta gerada para cada empresa:
  
  ![alt text](https://i.imgur.com/zwwU6ax.png)
  
  * Gráficos gerados:
  
  ![alt text](https://i.imgur.com/xdM2BDL.png)
