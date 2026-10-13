Atue como um especialista em N8N.

Crie uma automação para atualizar os preços da tabela de vendas do SQL Server.

Público:
Minha equipe.

Ferramentas envolvidas:
SQL Server.

Fluxo:
1. Agendar execução toda sexta-feira às 02:00 da manhã.
2. Executar o comando UPDATE que sincroniza os preços da tabela 3 com os preços da tabela 2.
3. Registrar um log da execução.

Comando SQL:
UPDATE LSTVENDAPRODUTO SET PRECOVENDA = t2.PRECOVENDA FROM LSTVENDAPRODUTO 
INNER JOIN (SELECT * FROM LSTVENDAPRODUTO WHERE IDTPLSTVENDA = 2) t2 ON t2.idproduto = LSTVENDAPRODUTO.idproduto
where LSTVENDAPRODUTO.IDTPLSTVENDA = 3

Regras:
Executar apenas uma vez por semana, na sexta-feira às 02:00.
Registrar um log com a data/hora da execução e quantos registros foram atualizados.

Explique quais nós do N8N devem ser utilizados e a lógica de funcionamento do workflow.