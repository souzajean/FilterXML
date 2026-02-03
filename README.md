# Recebendo um XML e filtrando os dados com a função FILTER XPath

SAP BTP CPI - FILTER


## Filter dados no XML

Este iFlow foi desenvolvido no SAP BTP – Integration Suite (Cloud Integration) com o objetivo de filtrar e transformar os dados. dados para atender às necessidades do negócio.Aqui está um requisito real que abordamos recentemente no SAP CPI.

Visão geral dos requisitos:

Precisávamos:1️⃣ Classificar todos os dados dos funcionários que moram em SP. 


![Capa](imagens/capa-linkedin.png)


📊 Exemplo Prático do Fluxo

### Criando nosso Pacote
![Fluxo](imagens/Screenshot_1.png)

### Adicionando o nome para nosso Pacote
![Fluxo](imagens/Screenshot_2.png)

### Criando nosso Artefato do iFlow
![Fluxo](imagens/Screenshot_3.png)

### Adicionando o Integration Flow
![Fluxo](imagens/Screenshot_4.png)

### Editando nosso Iflow
![Fluxo](imagens/Screenshot_5.png)

### Removendo o Sender do nosso iFlow
![Fluxo](imagens/Screenshot_6.png)

### Removendo o Receiver do nosso iFlow
![Fluxo](imagens/Screenshot_7.png)

### Adicionando o Filter ao nosso Iflow
![Fluxo](imagens/Screenshot_8.png)

### Renomeando o Filter para Filter XML
![Fluxo](imagens/Screenshot_9.png)

### Realizando o Filter 
Nesta etapa iremos colocar o caminho do XML que queremos filtrar

> Filter - Processing

```
XPath Expression: /empregados/empregado[estado = 'SP']
```
![Fluxo](imagens/Screenshot_10.png)

### Arquivo do empregados.xml

``` empregados.xml
<?xml version='1.0' encoding='UTF-8'?>
<empregados>
    <empregado>
        <idUsuario>1001</idUsuario>
        <dataInicio>2016-03-26</dataInicio>
        <dataFim>2099-03-26</dataFim>
        <nome>Kleber</nome>
        <sobrenome>Silva</sobrenome>
        <tipoEmprego>CLT</tipoEmprego>
        <pais>BR</pais>
        <estado>SP</estado>
    </empregado>
    <empregado>
        <idUsuario>1002</idUsuario>
        <dataInicio>2018-01-15</dataInicio>
        <dataFim>2099-01-15</dataFim>
        <nome>Ana</nome>
        <sobrenome>Santos</sobrenome>
        <tipoEmprego>CLT</tipoEmprego>
        <pais>BR</pais>
        <estado>RJ</estado>
    </empregado>
    <empregado>
        <idUsuario>1003</idUsuario>
        <dataInicio>2019-06-10</dataInicio>
        <dataFim>2099-06-10</dataFim>
        <nome>Carlos</nome>
        <sobrenome>Pereira</sobrenome>
        <tipoEmprego>EST</tipoEmprego>
        <pais>BR</pais>
        <estado>MG</estado>
    </empregado>
    <empregado>
        <idUsuario>1004</idUsuario>
        <dataInicio>2017-11-01</dataInicio>
        <dataFim>2099-11-01</dataFim>
        <nome>Mariana</nome>
        <sobrenome>Oliveira</sobrenome>
        <tipoEmprego>TER</tipoEmprego>
        <pais>BR</pais>
        <estado>PR</estado>
    </empregado>
    <empregado>
        <idUsuario>1005</idUsuario>
        <dataInicio>2020-02-20</dataInicio>
        <dataFim>2099-02-20</dataFim>
        <nome>Lucas</nome>
        <sobrenome>Costa</sobrenome>
        <tipoEmprego>TER</tipoEmprego>
        <pais>BR</pais>
        <estado>RS</estado>
    </empregado>
    <empregado>
        <idUsuario>1006</idUsuario>
        <dataInicio>2015-08-05</dataInicio>
        <dataFim>2099-08-05</dataFim>
        <nome>Fernanda</nome>
        <sobrenome>Lima</sobrenome>
        <tipoEmprego>APRE</tipoEmprego>
        <pais>BR</pais>
        <estado>BA</estado>
    </empregado>
    <empregado>
        <idUsuario>1007</idUsuario>
        <dataInicio>2021-04-12</dataInicio>
        <dataFim>2099-04-12</dataFim>
        <nome>Rafael</nome>
        <sobrenome>Almeida</sobrenome>
        <tipoEmprego>APRE</tipoEmprego>
        <pais>BR</pais>
        <estado>SC</estado>
    </empregado>
    <empregado>
        <idUsuario>1008</idUsuario>
        <dataInicio>2014-09-30</dataInicio>
        <dataFim>2099-09-30</dataFim>
        <nome>Patricia</nome>
        <sobrenome>Rocha</sobrenome>
        <tipoEmprego>TER</tipoEmprego>
        <pais>BR</pais>
        <estado>PE</estado>
    </empregado>
    <empregado>
        <idUsuario>1009</idUsuario>
        <dataInicio>2016-12-01</dataInicio>
        <dataFim>2099-12-01</dataFim>
        <nome>Bruno</nome>
        <sobrenome>Martins</sobrenome>
        <tipoEmprego>PJ</tipoEmprego>
        <pais>BR</pais>
        <estado>GO</estado>
    </empregado>
    <empregado>
        <idUsuario>1010</idUsuario>
        <dataInicio>2022-07-18</dataInicio>
        <dataFim>2099-07-18</dataFim>
        <nome>Juliana</nome>
        <sobrenome>Ferreira</sobrenome>
        <tipoEmprego>PJ</tipoEmprego>
        <pais>BR</pais>
        <estado>SP</estado>
    </empregado>
</empregados>

```
![Fluxo](imagens/Screenshot_11.png)

### Selecionando Conector
![Fluxo](imagens/Screenshot_12.png)

### Clicar no icone de iniciar Simulação
Para adicionar nosso XML
![Fluxo](imagens/Screenshot_13.png)

### Adicionando o conteúdo do empregados.xml
![Fluxo](imagens/Screenshot_14.png)

### Clicar no Conector e adicionar o End Simulação
![Fluxo](imagens/Screenshot_15.png)

### Clicar para iniciar nossos teste de simulação
![Fluxo](imagens/Screenshot_16.png)

### Clicar no Envelope para ver o resultado
![Fluxo](imagens/Screenshot_17.png)

### Resultado com o filtro do XML
Com todos os dados que são do estado de SP
![Fluxo](imagens/Screenshot_18.png)

### XML do resultado
![Fluxo](imagens/Screenshot_19.png)

``` Resultado do Filtro de SP
<?xml version='1.0' encoding='UTF-8'?>
<empregados>
    <empregado>
        <idUsuario>1001</idUsuario>
        <dataInicio>2016-03-26</dataInicio>
        <dataFim>2099-03-26</dataFim>
        <nome>Kleber</nome>
        <sobrenome>Silva</sobrenome>
        <tipoEmprego>CLT</tipoEmprego>
        <pais>BR</pais>
        <estado>SP</estado>
    </empregado>
    <empregado>
        <idUsuario>1010</idUsuario>
        <dataInicio>2022-07-18</dataInicio>
        <dataFim>2099-07-18</dataFim>
        <nome>Juliana</nome>
        <sobrenome>Ferreira</sobrenome>
        <tipoEmprego>PJ</tipoEmprego>
        <pais>BR</pais>
        <estado>SP</estado>
    </empregado>
</empregados>
```



## 📦 Exemplo prático – iFlow para baixar

📦 [Download do iFlow – Package/FilterwithXML.zip](Package/FilterwithXML.zip)



> O arquivo pode ser importado diretamente no SAP Integration Suite (CPI).
