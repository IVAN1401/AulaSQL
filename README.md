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
 
 SELECT *FROM categoria 
CREATE TABLE categoria(id INT NOT NULL AUTO_INCREMENT, nome VARCHAR(255),endereco VARCHAR(55),idade INT, PRIMARY KEY (id))  
INSERT INTO categoria (nome,endereco,idade) VALUES ("Jean","são paulo","40")
DELETE FROM categoria WHERE id = "2"

ALTER TABLE produto ADD PRIMARY KEY(id_produto) 

ALTER TABLE produto ADD id_categoria INT 

ALTER TABLE produto ADD FOREIGN KEY (id_categoria) REFERENCES categoria(id);

SELECT*FROM produto WHERE nome LIKE "teste%"

ALTER TABLE produto ADD COLUMN (id_categoria int)

TRUNCATE TABLE produto

SELECT * FROM produto
INNER JOIN categoria
ON produto.id_categoria = categoria.id;

CREATE TABLE agencia (codigoage INT NOT NULL AUTO_INCREMENT, NomeAg VARCHAR(45),cidadeAg VARCHAR(55), PRIMARY KEY (codigoAge));  
CREATE TABLE cliente (codigocli INT NOT NULL AUTO_INCREMENT, codcliente VARCHAR(45), VARCHAR(55), PRIMARY KEY (codigocli));  


