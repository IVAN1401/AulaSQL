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

exercicio 02


CREATE TABLE agencias (CodigoAg INT NOT NULL AUTO_INCREMENT, NomeAg VARCHAR (45), CidadeAg VARCHAR (45), PRIMARY KEY (CodigoAg))

CREATE TABLE clientes ( CodigoCli INT NOT NULL AUTO_INCREMENT, Nome VARCHAR(45), Rua VARCHAR(45), Cidade VARCHAR (45), CodigoAg INT, PRIMARY KEY (CodigoCli))

CREATE TABLE depositos (NumeroCont INT NOT NULL AUTO_INCREMENT, Saldo DOUBLE, CodigoAg INT, CodigoCli INT, PRIMARY KEY (NumeroCont))

CREATE TABLE emprestimos (NumeroEmp INT NOT NULL AUTO_INCREMENT, Quantia DOUBLE, CodigoAg INT, CodigoCli INT, PRIMARY KEY (NumeroEmp))

ALTER TABLE clientes ADD FOREIGN KEY(CodigoAg) REFERENCES agencias(CodigoAg);

ALTER TABLE depositos ADD FOREIGN KEY (CodigoAg) REFERENCES agencias(codigoAg);

ALTER TABLE depositos ADD FOREIGN KEY (CodigoCli) REFERENCES clientes(CodigoCli);

ALTER TABLE emprestimos ADD FOREIGN KEY (CodigoCli) REFERENCES clientes (CodigoCli);

ALTER TABLE emprestimos ADD FOREIGN KEY (CodigoAg) REFERENCES agencias (CodigoAg);

INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Almirante Tamandaré")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Bancopr", "Altamira do Parana")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BNE", "Amaporã")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BBB", "Andirá")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BCI", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BPA","Arapoti")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BMM", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Arapongas")

INSERT INTO clientes (Nome, rua, cidade) VALUES ("João","centro","Arapongas")

INSERT INTO depositos(Saldo,codigoAg,codigoCli) VALUES (500.00,1,01)

INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (1.000,1,1)




