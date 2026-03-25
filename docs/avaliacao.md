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

**RN03 —**  Atualizar estoque após venda

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
O sistema deve mostrar preço e quantidade disponível.
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
O sistema deve ser simples para qualquer atendente usar.
**RNF03 —**  Seguro
Somente pessoas autorizadas podem usar o sistema.
**RNF04 —**  Disponível
O sistema deve funcionar durante o horário da farmácia.

---

# 5. Casos de Uso (mínimo: 10)
### Inserir **diagrama de casos de uso geral**, demonstrando claramente:
- os 10 casos
- relação entre eles e atores
- pelo menos 3 includes
- pelo menos 3 extends

---

# 6. Documentação dos Casos de Uso
Para **cada caso de uso**, utilize o template abaixo:
---

## **UCXX — Nome do Caso de Uso**
**Ator(es):**  
**Descrição:**  
**Pré-condições:**  
**Pós-condições:**  

### Fluxo Principal
1.  
2.  
3.  
4.  

### Fluxos Alternativos / Exceções
- FA01 —  
- FA02 —  

### Relacionamentos
- **Include:** (listar quando aplicável)  
- **Extend:** (listar quando aplicável)  

### Inserir o diagrama de atividades do Caso de Uso, demonstrando tudo o fluxo princial e alternativos/exceções.

---

> Repita essa estrutura para **todos os seus casos de uso** (mínimo 10).


