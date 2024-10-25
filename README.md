# Dashboard de Vendas com Power BI utilizando Star Schema - NTT DATA

![](https://github.com/julianazanelatto/power_bi_analyst/blob/main/M%C3%B3dulo%204/Desafios%20de%20Projeto/der_universidade.png)

````
1. Identificação da Tabela Fato

A tabela fato deve capturar os eventos ou medições que você deseja analisar. No caso, o foco são os professores,
e a tabela fato deve conter dados como:

ID do professor

Cursos ministrados

Departamentos

Disciplinas

Horas/Aulas ministradas (ou outro dado quantitativo relevante)

Datas dos eventos analisados (ex: data do curso ministrado)


A tabela fato será algo como Fato_Professores ou Fato_CursosMinistrados,
dependendo da granularidade que deseja dar à análise.

2. Criação das Tabelas Dimensão

A partir do diagrama relacional, as seguintes dimensões podem ser criadas:

Dimensão Professor

ID_Professor

Nome

Titulação

Departamento (chave estrangeira para a dimensão Departamento)


Dimensão Departamento

ID_Departamento

Nome do Departamento

Localização


Dimensão Disciplina

ID_Disciplina

Nome da Disciplina

Carga Horária


Dimensão Curso

ID_Curso

Nome do Curso

Tipo do Curso (graduação, pós-graduação, etc.)

Departamento (chave estrangeira para a dimensão Departamento)


Dimensão Data

ID_Data

Dia, Mês, Ano

Trimestre, Semestre



3. Esquema Estrela

Essas dimensões se conectam à tabela fato, permitindo uma análise multidimensional dos 
dados dos professores.
A granularidade da tabela fato será algo como “curso ministrado pelo professor
em determinada data”.

Estrutura Proposta

Tabela Fato (Fato_CursosMinistrados):

ID_Professor (FK para Dimensão Professor)

ID_Disciplina (FK para Dimensão Disciplina)

ID_Curso (FK para Dimensão Curso)

ID_Departamento (FK para Dimensão Departamento)

ID_Data (FK para Dimensão Data)

Horas_Aulas (ou outro dado quantitativo)



4. Modelo Visual (Esquema Estrela)

Agora que temos as tabelas e suas chaves, a estrutura ficaria assim:

Fato_CursosMinistrados no centro, conectada a:

Dimensão Professor

Dimensão Departamento

Dimensão Disciplina

Dimensão Curso

Dimensão Data
````

STAR SCHEMA
![Star Schema](https://github.com/IvoJucaBezerra/Dashboard-de-Vendas-com-Power-BI-utilizando-Star-Schema/blob/main/star_schema-desafio1.png)


