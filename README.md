Neste arquivo README, vou explicar as várias consultas SQL que foram executadas no código fornecido. Cada consulta se concentra em diferentes aspectos dos dados da tabela "Animais". Aqui está uma breve descrição de cada consulta:

Selecionar todos os animais:
SELECT * FROM Animais;
Esta consulta retorna todas as informações de todos os animais na tabela "Animais". Ela serve para visualizar todos os registros na tabela.

Selecionar todos os animais que pesam menos que 13.1:
SELECT * FROM Animais WHERE PESO < 13.1;
Esta consulta retorna os registros de animais cujo peso é inferior a 13.1.

Selecionar todos os animais nascidos entre fevereiro e dezembro de 2015:
SELECT * FROM Animais WHERE EXTRACT(YEAR FROM NASC) = 2015 AND EXTRACT(MONTH FROM NASC) BETWEEN 2 AND 12;
Esta consulta retorna os registros de animais nascidos em 2015, entre os meses de fevereiro e dezembro.

Selecionar todos os animais brancos que pesam menos que 15.0:
SELECT * FROM Animais WHERE COR = 'branco' AND PESO < 15.0;
Esta consulta retorna os registros de animais de cor branca que pesam menos de 15.0.

Selecionar nome, cor e peso de todos cujo nome comece com 'B':
SELECT NOME, COR, PESO FROM Animais WHERE NOME LIKE 'B%';
Esta consulta retorna o nome, cor e peso de animais cujo nome começa com a letra 'B'.

Selecionar nome, cor e peso de todos com cor vermelha, amarela, marrom e laranja:
SELECT NOME, COR, PESO FROM Animais WHERE COR IN ('vermelho', 'amarelo', 'marrom', 'laranja');
Esta consulta retorna o nome, cor e peso de animais cuja cor é vermelha, amarela, marrom ou laranja.

Selecionar nome, cor, data de nascimento e peso de todos ordenados pelos mais jovens:
SELECT NOME, COR, NASC, PESO FROM Animais ORDER BY NASC;
Esta consulta retorna o nome, cor, data de nascimento e peso de todos os animais na tabela, ordenados por data de nascimento, do mais jovem ao mais velho.

Selecionar todos os animais cujo nome comece com 'C' e não sejam brancos:
SELECT * FROM Animais WHERE NOME LIKE 'C%' AND COR != 'branco';
Esta consulta retorna os registros de animais cujo nome começa com 'C' e que não são brancos.

Selecionar todos os animais cujo nome contenha 'ba':
SELECT * FROM Animais WHERE NOME LIKE '%ba%';
Esta consulta retorna os registros de animais cujo nome contém a sequência de caracteres 'ba' em qualquer lugar do nome.

Selecionar todos os animais com peso entre 13.0 e 15.0:
SELECT * FROM Animais WHERE PESO BETWEEN 13.0 AND 15.0;
Esta consulta retorna os registros de animais com peso entre 13.0 e 15.0.

Selecionar todos os animais que o peso não seja maior que 30, com cor amarelo ou roxo e nascidos depois de 2012:
SELECT * FROM Animais WHERE PESO <= 30 AND (COR = 'amarelo' OR COR = 'roxo') AND EXTRACT(YEAR FROM NASC) > 2012;
Esta consulta retorna os registros de animais com peso inferior a 30, que são de cor amarela ou roxa e que nasceram após 2012.

Selecionar todos os capricornianos:
SELECT * FROM Animais WHERE (EXTRACT(MONTH FROM NASC) = 12 AND EXTRACT(DAY FROM NASC) >= 22) OR (EXTRACT(MONTH FROM NASC) = 1 AND EXTRACT(DAY FROM NASC) <= 19);
Esta consulta retorna os registros de animais que têm datas de nascimento correspondentes ao signo do zodíaco de Capricórnio.

Selecionar todos os animais com nome formado por mais de uma palavra:
SELECT * FROM Animais WHERE INSTR(NOME, ' ', 1) > 0;
Esta consulta retorna os registros de animais cujo nome é composto por mais de uma palavra, identificados pela presença de um espaço em branco.

![Código SQL](Table_Animais.png)

E com os Seguintes DER abaixo que envolver as CREATE TABLE das TABELAS de:

PRODUTO E MARCA 

![Código SQL](https://github.com/SamuelJorgetto/Tabela-Animais/blob/main/DER%20-%20Produto_Marca.png)


ESPECIES E ANIMAIS 

![Código SQL](https://github.com/SamuelJorgetto/Tabela-Animais/blob/main/DER%20-%20Animais_Especie.png)



FILMES E CATEGORIAS

![Código SQL](https://github.com/SamuelJorgetto/Tabela-Animais/blob/main/DER%20-%20Filmes_Categoria.png)







