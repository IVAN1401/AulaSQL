# AulaSQL
SELECT * FROM produto; #mostrar tabela#

UPDATE produto SET id_produto = '1' WHERE ; #altera produto#

INSERT INTO produto (id_produto, nome, preco, codigo) VALUES ("1", "roupa", "12,00", "12");#adicionar produto#
INSERT INTO produto (id_produto, nome, preco, codigo) VALUES ("2", "luva", "12,00", "12");

INSERT INTO produto (id_produto, nome, preco, codigo) VALUES ("10", "Monitor", "850,00", "22");
DELETE FROM produto WHERE id_produto = "10" #deletar linha#


#Esse comando faz a alteração de um valor na tabela especificando a coluna pelo id.
UPDATE produto SET nome = "banho" WHERE id_produto = 1 #alterar produto#

SELECT *FROM produto  
WHERE produto.id_produto = 1049
AND produto.codigo = "13881"

SELECT *FROM produto  
WHERE produto.id_produto = 1049
OR produto.codigo = "13881"
 

 SELECT *FROM produto
 WHERE produto.id_produto IN (1029,5,10,56,87)
 
 SELECT *FROM produto
 WHERE produto.id_produto NOT IN (1049)
