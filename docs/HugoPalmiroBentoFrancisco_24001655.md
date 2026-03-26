# Avaliação — Engenharia de Software
**Sistema Integrado de Gestão de Farmácia — MVP Definido pelo Estudante**

Aluno: Hugo Plamiro Bento Francisco
RA: 24001655
Data: 25/03/2026  

---

# 1. Definição do MVP
Processo de Venda integrado ao Estoque

Meu MVP cobre o processo de venda de produtos desde a identificação/cadastro do cliente até a e emissão do comprovante. incluindo a verificação e atualização automática do estoque.

Esta fora compras e fornecedores;contas a pagar;contas a receber; relatórios;gestão administrartiva

Escolhi esse MVP para focar no processo principal, garantindo um fluxo funcional e integrado entre atendimento e controle de estoque.

# 2. Regras de Negócio (mínimo: 5)

**RN01 —**  Verificar estoque antes da venda

O sistema deve conferir se tem o produto no estoque antes de vender.

**RN02 —**  Não vender sem estoque

Se não tiver quantidade suficiente, a venda não pode ser feita.

**RN03 —**  Atualizar estoque depois da venda

Quando a venda for finalizada, o estoque deve diminuir automaticamente.

**RN04 —**  Cadastro de cliente para venda a prazo

Se a venda for a prazo, o cliente precisa estar cadastrado.

**RN05 —**  Emitir comprovante

Toda venda deve gerar um comprovante.


---

# 3. Requisitos Funcionais (mínimo: 8)

**RF01 —**  Cadastrar cliente

O sistema deve permitir cadastrar cliente.

**RF02 —**  Buscar produto

O sistema deve permitir procurar produto pelo nome ou código.

**RF03 —**  Mostrar informações do produto

O sistema deve mostrar preço e quantidade.

**RF04 —**  Adicionar produto na venda

O atendente pode adicionar produtos na compra.

**RF05 —**  Verificar estoque

O sistema deve verificar automaticamente se tem no estoque.

**RF06 —**  Calcular total

O sistema deve mostrar o valor total da compra.

**RF07 —**  Finalizar venda

O sistema deve permitir finalizar a venda.

**RF08 —**  Atualizar estoque

O sistema deve atualizar o estoque depois da venda.

---

# 🛡 4. Requisitos Não Funcionais (mínimo: 4)

**RNF01 —**  Sistema rápido

O sistema deve ser rápido para não atrasar o atendimento.

**RNF02 —**  Fácil de usar

O sistema deve ser simples.

**RNF03 —**  Seguro

Somente pessoas autorizadas podem usar o sistema.

**RNF04 —**  Disponível

O sistema deve funcionar durante o horário da farmácia.

---

# 5. Casos de Uso (mínimo: 10)

<img width="808" height="338" alt="image" src="https://github.com/user-attachments/assets/769e36fb-2ba5-457c-86eb-cfe9dee47694" />

---

# 6. Documentação dos Casos de Uso
---

## **UC01 — Realizar Venda**
**Ator(es):** Atendente  
**Descrição:** Inicia o processo de venda.  
**Pré-condições:** Sistema funcionando.  
**Pós-condições:** Venda iniciada.  

### Fluxo Principal
1. Atendente inicia venda  
2. Sistema permite buscar produto  
3. Atendente adiciona produtos  
4. Sistema continua o processo  

### Fluxos Alternativos / Exceções
- FA01 — Erro no sistema  
- FA02 — Cancelar venda  

### Relacionamentos
- **Include:** Buscar Produto, Adicionar Produto  
- **Extend:** Cadastrar Cliente, Identificar Cliente  

## **UC02 — Buscar Produto**
**Ator(es):** Atendente  
**Descrição:** Permite procurar um produto.  
**Pré-condições:** Produto cadastrado.  
**Pós-condições:** Produto exibido.  

### Fluxo Principal
1. Atendente digita nome ou código  
2. Sistema realiza busca  
3. Sistema encontra produto  
4. Sistema exibe resultado  

### Fluxos Alternativos / Exceções
- FA01 — Produto não encontrado  
- FA02 — Erro na busca  

### Relacionamentos
- **Include:** —  
- **Extend:** —  
## **UC03 — Adicionar Produto**
**Ator(es):** Atendente  
**Descrição:** Adiciona produto à venda.  
**Pré-condições:** Produto encontrado.  
**Pós-condições:** Produto adicionado à venda.  

### Fluxo Principal
1. Atendente seleciona produto  
2. Informa quantidade  
3. Sistema verifica quantidade  
4. Produto é adicionado  

### Fluxos Alternativos / Exceções
- FA01 — Quantidade inválida  
- FA02 — Produto indisponível  

### Relacionamentos
- **Include:** Verificar Estoque  
- **Extend:** —  


## **UC04 — Verificar Estoque**
**Ator(es):** Sistema  
**Descrição:** Verifica se há produto disponível.  
**Pré-condições:** Produto selecionado.  
**Pós-condições:** Estoque validado.  

### Fluxo Principal
1. Sistema consulta estoque  
2. Sistema verifica quantidade  
3. Sistema valida disponibilidade  
4. Retorna resultado  

### Fluxos Alternativos / Exceções
- FA01 — Sem estoque  
- FA02 — Erro no sistema  

### Relacionamentos
- **Include:** —  
- **Extend:** —  


## **UC05 — Calcular Total**
**Ator(es):** Sistema  
**Descrição:** Calcula o valor total da compra.  
**Pré-condições:** Produtos adicionados.  
**Pós-condições:** Total calculado.  

### Fluxo Principal
1. Sistema soma valores  
2. Sistema calcula total  
3. Sistema atualiza valor  
4. Exibe total  

### Fluxos Alternativos / Exceções
- FA01 — Erro de cálculo  
- FA02 — Dados inválidos  

### Relacionamentos
- **Include:** —  
- **Extend:** —  


## **UC06 — Finalizar Venda**
**Ator(es):** Atendente  
**Descrição:** Finaliza a venda.  
**Pré-condições:** Produtos adicionados.  
**Pós-condições:** Venda concluída.  

### Fluxo Principal
1. Atendente confirma venda  
2. Sistema calcula total  
3. Sistema processa venda  
4. Venda finalizada  

### Fluxos Alternativos / Exceções
- FA01 — Cancelamento da venda  
- FA02 — Erro no sistema  

### Relacionamentos
- **Include:** Calcular Total, Emitir Comprovante  
- **Extend:** Registrar Venda a Prazo  


## **UC07 — Emitir Comprovante**
**Ator(es):** Sistema  
**Descrição:** Gera comprovante da venda.  
**Pré-condições:** Venda finalizada.  
**Pós-condições:** Comprovante emitido.  

### Fluxo Principal
1. Sistema gera comprovante  
2. Sistema prepara dados  
3. Sistema exibe comprovante  
4. Sistema imprime ou salva  

### Fluxos Alternativos / Exceções
- FA01 — Erro na geração  
- FA02 — Falha na impressão  

### Relacionamentos
- **Include:** —  
- **Extend:** —  


## **UC08 — Cadastrar Cliente**
**Ator(es):** Atendente  
**Descrição:** Permite cadastrar cliente.  
**Pré-condições:** Cliente não cadastrado.  
**Pós-condições:** Cliente registrado.  

### Fluxo Principal
1. Atendente informa dados  
2. Sistema valida dados  
3. Sistema salva cliente  
4. Cadastro concluído  

### Fluxos Alternativos / Exceções
- FA01 — Dados inválidos  
- FA02 — Cliente já existe  

### Relacionamentos
- **Include:** —  
- **Extend:** Realizar Venda  


## **UC09 — Identificar Cliente**
**Ator(es):** Atendente  
**Descrição:** Identifica cliente na venda.  
**Pré-condições:** Cliente cadastrado.  
**Pós-condições:** Cliente vinculado à venda.  

### Fluxo Principal
1. Atendente busca cliente  
2. Sistema encontra cliente  
3. Sistema seleciona cliente  
4. Cliente vinculado  

### Fluxos Alternativos / Exceções
- FA01 — Cliente não encontrado  
- FA02 — Erro na busca  

### Relacionamentos
- **Include:** —  
- **Extend:** Realizar Venda  


## **UC10 — Registrar Venda a Prazo**
**Ator(es):** Atendente  
**Descrição:** Registra venda a prazo.  
**Pré-condições:** Cliente cadastrado.  
**Pós-condições:** Venda registrada a prazo.  

### Fluxo Principal
1. Atendente escolhe venda a prazo  
2. Sistema verifica cliente  
3. Sistema registra venda  
4. Venda concluída  

### Fluxos Alternativos / Exceções
- FA01 — Cliente não cadastrado  
- FA02 — Erro no registro  

### Relacionamentos
- **Include:** —  
- **Extend:** Finalizar Venda  


---




