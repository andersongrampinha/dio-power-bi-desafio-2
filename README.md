### **Desafio de Projeto - Processando e Transformando Dados com Power BI**

#### **-Passos adotados para solução do desafio**

#### **Foi criado uma instância no MS Azure, com base no script disponíbilizado foi criado a base de dados e incluído os dados para teste nas tabelas.**

#### **O script para inclusão** 

**Parte 1 - Criação Base de Dados**

- **Adicionado os scripts utilizados na criação da base de dados;**
    script [Criação da Base de Dados / Tabelas]: (https://github.com/andersongrampinha/dio-power-bi-desafio-2/blob/main/scripts/script%20cria%C3%A7%C3%A3o%20base%20de%20dados.sql)
- **Adicionado os scripts corrigidos para inserção dos dados de teste;**
    script [Criação Inserção dos Dados]: (https://github.com/andersongrampinha/dio-power-bi-desafio-2/blob/main/scripts/script%20inser%C3%A7%C3%A3o%20dos%20dados.sql)

  #### **Obs.: O script para inclusão dos dados da tabela EMPLOYEE foi reordenado pelo campo Super_ssn para evitar erro de violação de foreign key.**

**Parte 2 - Transformação dos dados**

**Tabela: Dependent**
>1- **Sem necessidade de alterações.**

**Consulta: Departament**
>1- **Consulta departament e dept_locations mescladas em uma nova consulta: departament_locations, utilizando a coluna Dnumber;**

**Consulta: departament_locations**
>1- **As colunas Dname e Dlocation foram mescladas na nova coluna departament_location;**

**Consulta: dept_locations**
>1- **Sem necessidade de alterações.**

**Consulta: Employee**
>1- **Removido a coluna Minit;**
>2- **Colunas Fname e Lname mescladas na nova coluna Fname;** 
>3- **Coluna Adress: Dividida por Delimitador nas novas colunas: Number, Street, City e State;**
>4- **Coluna Salary: Alterado tipo de dados para Número decimal fixo;**
>5- **Consulta employee e departament mescladas em uma nova consulta: employee_departament.** 

**Consulta: employee_departament**
>1- **Realizado a junção (PowerBi) dos colaboradores com os respectivos gerentes na própria Consulta, a ligação foi feita utilizando-se os campos Super_ssn e Ssn.**

**Consulta: employee_manager**
>1- **Duplicado a consulta employee_departament e renomeado para employee_manager e feito o agurpamento da coluna Fmanager para sabermos quantos colaboradores existem por gerente.**

**Consulta: workd_on**
>1- **Coluna Hours: Alterado tipo de dados para Número decimal.**

**Consulta: project**
>1- **Sem necessidade de alterações.**

**Em todas as colunas desnecessárias foram removidos**

**Parte 3 - Criação do Relatório Power BI**

**Foram criadas algumas visões no PowerBI para teste e visualização dos dados tratados na etapa anterior.

- **Página 1 do relatório:**
    ![Página 1](https://github.com/andersongrampinha/dio-power-bi-desafio-2/blob/main/images/relat_pagina_1.png)

- **Página 2 do relatório:**
    ![Página 2](https://github.com/andersongrampinha/dio-power-bi-desafio-2/blob/main/images/relat_pagina_2.png)