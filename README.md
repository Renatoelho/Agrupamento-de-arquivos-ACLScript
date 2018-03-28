## **Consolidação de vários arquivos em uma única base – ACLScript**

Objetivo desse projeto é criar uma base consolidada a partir de n arquivos, isso é útil quando por exemplo os relatórios de vendas são diários e você necessita consolidar todos eles para fazer uma determinada análise, essa lógica se aplica a qualquer base de dados que tenha o mesmo *layout* como *logs* de um sistema e outros tipos de dados que sejam armazenados em arquivos. 

Esse processo de consolidação é bastante elástico, pois é possível consolidar desde 2 arquivos até milhares deles em um único processamento.

Essa consolidação pode ser feita, tanto para ser consumida pelo *ACL for Windows* ou qualquer outra aplicação que você queira usar.

### **As extensões que podem ser usadas nas origens são:**
- TXT
- PDF
- XLSX
- XML
- DBF
- Outras

----------

### **Lógica da consolidação** 

**1° Passo:** Listar os arquivos que serão consolidados.

**2° Passo:** Contar quantos são os arquivos encontrados no diretório.

**3° Passo:** Criar uma variável de controle para interromper o comando *WHILE* ao fim do processo.

**4º Passo:** Começar a importação do primeiro arquivo, podendo ser aplicadas algumas regras de tratamento de dados e criado um campo computado para identificarmos a origem dos registros.

**5º Passo:** Esses dados serão consolidados em um arquivo delimitado, pois isso permitirá que essa base possa ser utilizada por qualquer aplicação.

**6° Passo:** Os passos 1 até 5 devem ser repetidos até ser importados e consolidados todos os arquivos (a partir do segundo arquivo até o último os dados serão inseridos ao fim da base consolidada).

> **Observação:** Existem detalhes que serão melhor explicados dentro dos *scripts* publicados no diretório do projeto.

----------

#### Arquivos originais

![](https://github.com/Renatoelho/Agrupamento-de-arquivos-ACLScript/blob/master/04-prints/print_relatorio_vendas_202001.JPG?raw=true)
![](https://github.com/Renatoelho/Agrupamento-de-arquivos-ACLScript/blob/master/04-prints/print_relatorio_vendas_202002.JPG?raw=true)
![](https://github.com/Renatoelho/Agrupamento-de-arquivos-ACLScript/blob/master/04-prints/print_relatorio_vendas_202003.JPG?raw=true)

----------

#### Arquivo consolidado

![](https://github.com/Renatoelho/Agrupamento-de-arquivos-ACLScript/blob/master/04-prints/print_relatorio_vendas_2020_consolidado.JPG?raw=true)


