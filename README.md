# 💰 Java Bank

## 🏦 Visão Geral
O **Java Bank** é uma aplicação desenvolvida em **Java**, durante o Bootcamp da Riachuelo em parceria com a DIO, que simula um sistema bancário, permitindo operações como criação de contas, movimentação de carteiras (wallets) e gestão de investimentos.  
O projeto foi criado com foco no **aprendizado de Programação Orientada a Objetos (POO)** e no uso de boas práticas de código.

---

## 👩‍💻 Autora
**Juliana Michelsen**  
Desenvolvido como parte de estudos em Java e modelagem de sistemas financeiros.

---

## ⚙️ Tecnologias Utilizadas
- ☕ **Java 17+**
- 🧩 **Lombok**
- 🏗️ **Gradle**
- 💻 **IntelliJ IDEA**
- 📦 **Paradigma de Orientação a Objetos**

---

## 📂 Estrutura do Projeto

```
br.com.dio
├── exception
│   ├── AccountWithInvestmentException.java
│   ├── InvestmentNotFoundException.java
│   ├── NoFundsEnoughException.java
│   └── WalletNotFoundException.java
│
├── model
│   ├── AccountWallet.java
│   ├── BankService.java
│   ├── Investment.java
│   ├── InvestmentWallet.java
│   ├── Money.java
│   ├── MoneyAudit.java
│   └── Wallet.java
│
├── repository
│   ├── CommonsRepository.java
│   ├── AccountRepository.java
│   └── InvestimentRepository.java
│
└── Main.java
```

---

## 🧠 Conceitos Principais

### 💼 `Wallet`
Classe abstrata que representa uma **carteira digital**.  
Gerencia o dinheiro (`Money`), operações de **depósito**, **saque** e **histórico de transações**.

### 💸 `Investment`
Classe que representa um **tipo de investimento**, com taxa de rendimento (`tax`) e valor inicial (`initialFunds`).  
É uma `record class`, garantindo imutabilidade e facilidade de criação de instâncias.

### 🏛️ `InvestmentRepository`
Responsável por **gerenciar os investimentos** criados e suas carteiras (`InvestmentWallet`).  
Controla operações como:
- Criação de investimentos
- Depósitos e retiradas
- Atualização de valores com base na taxa
- Busca e listagem de investimentos

### 🧱 `CommonsRepository`
Contém métodos utilitários para:
- Validar se há saldo suficiente para transações
- Gerar objetos `Money` associados a um histórico (`MoneyAudit`)

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
- Java 17 ou superior instalado
- IntelliJ IDEA (ou qualquer IDE compatível)
- Gradle configurado no projeto

### Passos
1. Clone o repositório:
   ```bash
   git clone https://github.com/JulianaMichelsen/java-bank.git
   ```
2. Abra o projeto na IDE.
3. Compile o projeto (`Build > Build Project`).
4. Execute a classe principal `Main.java`.

---

## 🧾 Exemplo de Uso

```java
var repository = new InvestimentRepository();

// Criar um investimento
var investment = repository.create(5, 10000);

// Iniciar um investimento para uma conta
var wallet = repository.initInvestment(conta, investment.id());

// Depositar em um investimento
repository.deposit("pix-do-cliente", 5000);

// Atualizar rendimentos
repository.updateAmount();
```

---

## 📊 Funcionalidades
✅ Criação e gerenciamento de contas e carteiras  
✅ Controle de fundos com histórico detalhado  
✅ Registro e simulação de investimentos  
✅ Validação de saldo e transações seguras  
✅ Atualização de rendimento sobre investimentos

---

## 🧱 Conceitos Aplicados
- Encapsulamento
- Imutabilidade (`record`)
- Streams e Lambdas
- Padrão Repository
- Boas práticas de POO

---

## 📜 Licença
Este projeto foi desenvolvido para fins educacionais e não possui licença comercial.  
Sinta-se à vontade para usar como referência em seus estudos.

---

> ✨ Desenvolvido com dedicação por **Juliana Michelsen** — aprendendo e evoluindo em Java todos os dias! ☕
