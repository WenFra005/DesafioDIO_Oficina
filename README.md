# 📚 **DesafioDIO_Oficina Database** 🛠️

## 💡 **Introdução**

O banco de dados **DesafioDIO_Oficina** foi projetado para gerenciar uma oficina mecânica, incluindo clientes, veículos, ordens de serviço e mecânicos. Ele facilita a organização e o controle dos serviços prestados, incluindo peças e serviços realizados, bem como o status das ordens de serviço.

## 🏛️ **Estrutura do Banco**

O banco de dados é composto pelas seguintes tabelas:

1. **Endereco** 🏡  
   Contém informações sobre o endereço, como logradouro, número, CEP e bairro.

2. **Cliente** 👤  
   Armazena dados dos clientes, como nome, e-mail, telefone e o endereço associado.

3. **Veículo** 🚗  
   Registra os veículos dos clientes, incluindo placa, modelo, marca e ano.

4. **Equipe** 👥  
   Contém os dados das equipes que prestam serviços na oficina.

5. **Mecânico** 🔧  
   Armazena informações sobre os mecânicos, suas especialidades e as equipes nas quais trabalham.

6. **OrdemDeServico** 📝  
   Registra as ordens de serviço, com data de emissão, status e valor total, associando cada ordem a um veículo e uma equipe.

7. **Servico** ⚙️  
   Contém a descrição dos serviços realizados, como manutenção de motor, freios, entre outros, e seus respectivos valores.

8. **Peca** 🔩  
   Armazena informações sobre as peças utilizadas nas ordens de serviço, incluindo descrição e preço.

9. **ItensOS** 📦  
   Registra os itens (peças e serviços) associados a cada ordem de serviço, com quantidade e subtotais.

## 🔄 **Relacionamentos**

- **Cliente** tem **Veículos** 🏎️.
- **Veículos** têm **Ordens de Serviço** 🛠️.
- **OrdemDeServico** possui **Servicos** e **Pecas**.
- **Equipe** tem **Mecânicos** 🧑‍🔧.
- **Mecânicos** realizam **Servicos**.

## 🧑‍💻 **Procedimentos Armazenados**

1. **ListarServicosPorMecanico**:  
   Exibe os serviços realizados por um mecânico específico.

2. **ListarOrdensPorStatus**:  
   Exibe ordens de serviço filtradas por seu status (Pendente, Em andamento ou Concluído).

3. **ListarPecasMaisUtilizadas**:  
   Exibe as peças mais utilizadas nas ordens de serviço.

## 📝 **Exemplo de Inserção de Dados**

```sql
-- Inserindo um novo cliente
INSERT INTO `cliente` (`nome_cliente`, `email_cliente`, `telefone_cliente`, `Endereco_codigo_Endereco`) 
VALUES ('João Silva', 'joao.silva@example.com', '(11) 91234-5678', 1);
```

## 📊 **Exemplo de Consultas**

- **Listar todos os serviços realizados por um mecânico**:
```sql
CALL ListarServicosPorMecanico(1);
```

- **Listar ordens de serviço com status 'Pendente'**:
```sql
CALL ListarOrdensPorStatus('Pendente');
```

- **Listar as peças mais utilizadas**:
```sql
CALL ListarPecasMaisUtilizadas();
```

## ⚙️ **Tecnologias Utilizadas**

- **MySQL** 🐬: Sistema de gerenciamento de banco de dados relacional.
- **Procedimentos Armazenados**: Para consultas e relatórios dinâmicos.

## 🏁 **Conclusão**

Este banco de dados é uma solução eficaz para gerenciar informações sobre clientes, veículos, serviços e mecânicos em uma oficina. Ele permite realizar operações de inserção, consulta e relatórios de maneira eficiente, facilitando o gerenciamento do dia a dia da oficina.
