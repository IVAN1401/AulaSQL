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


exercio 3

CREATE TABLE agencias (CodigoAg INT NOT NULL AUTO_INCREMENT, NomeAg VARCHAR (45), CidadeAg VARCHAR (45), PRIMARY KEY (CodigoAg))

CREATE TABLE clientes ( CodigoCli INT NOT NULL AUTO_INCREMENT, Nome VARCHAR(45), Rua VARCHAR(45), Cidade VARCHAR (45), CodigoAg INT, PRIMARY KEY (CodigoCli))

CREATE TABLE depositos (NumeroCont INT NOT NULL AUTO_INCREMENT, Saldo DOUBLE, CodigoAg INT, CodigoCli INT, PRIMARY KEY (NumeroCont))

CREATE TABLE emprestimos (NumeroEmp INT NOT NULL AUTO_INCREMENT, Quantia DOUBLE, CodigoAg INT, CodigoCli INT, PRIMARY KEY (NumeroEmp))

ALTER TABLE clientes ADD FOREIGN KEY(CodigoAg) REFERENCES agencias(CodigoAg);

ALTER TABLE depositos ADD FOREIGN KEY (CodigoAg) REFERENCES agencias(codigoAg);

ALTER TABLE depositos ADD FOREIGN KEY (CodigoCli) REFERENCES clientes(CodigoCli);

ALTER TABLE emprestimos ADD FOREIGN KEY (CodigoCli) REFERENCES clientes (CodigoCli);

ALTER TABLE emprestimos ADD FOREIGN KEY (CodigoAg) REFERENCES agencias (CodigoAg);

INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("Basa", "Adrianópolis")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BPR", "Abatiá")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES (" BNE", "Amaporã")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BBB", "Candoi")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BCI", "Capanema")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BPA", "Arapoti")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BMM", "Iporã")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BPA", "Ivaí")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BCN", "Juranda")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BDS", "Laranjal")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BSS", "Loanda")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BSU", "Lobato")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BMA", "Marilena")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BMI", "Mariluz")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BPE", "Maringá")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BBI", "Matinhos")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BCA", "Mato Rico")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BAC", "Nova Esperança" )
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BMF", "Palmas")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BGA", "Palmeira")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BCC", "Palotimna")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BIJ", "Paranavaí")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("BIJ", "Alto Paraná")
INSERT INTO agencias (Nomeag,Cidadeag) VALUES ("083", "Alto Paraná")


INSERT INTO clientes (Nome,rua,cidade) VALUES ("João","centro","Abatiá")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Pedro","Acre","Adrianópólis")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Maria","Alagoas","Amaporã")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Tamires","Sergipe","Candoi")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Tiago","centro","Capanema")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Thaís","Acre","Arapoti")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Mauro","Alagoas","Iporã")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Regina","Maceió","Ivaí")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Sindy","Pará","Laranjal")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Suzy","Laranjal","Ivaí")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Daniele","centro","Juranda")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Marcos","Piaui","Laranjal")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Jessica","Palmas","Loanda")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Amanda","Paris","Lobato")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Renata","Mexico","Marilena")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Damares","Chile","Mariluz")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Helena","EUA","Maringá")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Tomas","Argentina","Matinhos")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Elvis","Panama","Mato Rico")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Ester","Portugual","Nova Esperança")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Hugo","Estocolmo","Maringá")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Eraldo","Paraíba","Paranavaí")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Hugo","Rua A","Maringá")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Eraldo","Rua A","Paranavaí")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Eraldo","Rua A","Alto Paraná")
INSERT INTO clientes (Nome, rua, cidade) VALUES ("Juninho","Rua D","São Paulo")


INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (500.00,1,1)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (1.500.00,3,2)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (8.500.00,10,4)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (1.300.00,22,10)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (5.500.00,1,14)*
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (2.5000,4,2)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (11.500,4,6)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (1.800,3,2)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (10.000,8,9)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (100.0000,7,6)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (7000.00,7,11)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (45.500,3,20)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (22.500,4,8)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (8.500,22,3)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (78.500,20,8)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (11.8500,14,2)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (500.00,15,1)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (1500.00,16,2)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (50.000,17,1)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (15.000,19,2)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (8.500,21,1)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (6.500,22,2)
INSERT INTO depositos (Saldo,codigoAg,codigoCli) VALUES (6.500,20,2)


INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (10000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (40000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (50000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (80000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (90000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (100000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (100000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (16000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (18000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (12000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (16000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (14000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (20000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (90000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (30000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (90000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (60000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (30000.20,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (110000,1,2)
INSERT INTO emprestimos(Quantia,codigoAg,codigoCli) VALUES (120000.20,1,2)

SELECT nome FROM clientes

SELECT *FROM clientes WHERE cidade LIKE  "Maringá"


SELECT *FROM clientes  
WHERE clientes.rua ="Rua A"
AND clientes.cidade = "Alto Paraná" 


SELECT *FROM clientes  
WHERE clientes.rua ="Rua C"
AND clientes.cidade = "Alto Paraná" 

SELECT *FROM clientes
 WHERE clientes.rua  
 NOT IN  ("Rua C", "Maringa ")
 
 
 SELECT *FROM clientes
 WHERE clientes.cidade = "Maringá"  
 OR clientes.cidade =   "São Paulo"
 
 
 SELECT *FROM clientes
 INNER JOIN depositos 
 ON clientes.CodigoCli=depositos.NumeroCont
 INNER JOIN agencias 
 ON clientes.CodigoCli=depositos.NumeroCont
 WHERE 
 agencias.codigoAg = 11
 
 SELECT *FROM clientes
 INNER JOIN emprestimos 
 ON clientes.CodigoCli=depositos.Quantia
 INNER JOIN agencias 
 ON clientes.CodigoCli=depositos.Quantia
 
 SELECT COUNT(CodigoCli) AS quantia_clientes FROM clientes 
 
 SELECT MAX(quantia) FROM emprestimos
 
 
 
 




