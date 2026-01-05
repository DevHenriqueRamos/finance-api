# 📑 Checklist de Desenvolvimento: FinanceAPI

Este documento serve como guia de implementação e acompanhamento do progresso do projeto.

---

## 1. Requisitos Funcionais (RF)
- [ ] **RF01: Gestão de Usuários** - Cadastro de usuários (Nome, CPF/CNPJ, E-mail, Senha).
- [ ] **RF02: Abertura de Conta** - Criação de conta vinculada com número e agência.
- [ ] **RF03: Depósito** - Realização de aportes financeiros em contas.
- [ ] **RF04: Saque** - Retirada de valores conforme saldo disponível.
- [ ] **RF05: Transferência Interna** - Movimentação entre contas do sistema.
- [ ] **RF06: Histórico/Extrato** - Consulta de transações com filtro de período.
- [ ] **RF07: Emissão de Comprovante** - Geração de UUID e resumo por transação.

---

## 2. Requisitos Não Funcionais (RNF)
- [ ] **RNF01: Persistência** - Configuração do banco de dados (PostgreSQL/H2).
- [ ] **RNF02: Segurança** - Implementação de BCrypt e autenticação JWT.
- [ ] **RNF03: Performance** - Implementação de paginação nos endpoints de listagem.
- [ ] **RNF04: Padronização** - Arquitetura REST (Verbos HTTP e Status Codes).
- [ ] **RNF05: Validações** - Validação de Bean (Jakarta Validation) para CPF/CNPJ e E-mail.

---

## 3. Regras de Negócio (RN)
- [ ] **RN01: Saldo Insuficiente** - Bloquear transações de saída maiores que o saldo.
- [ ] **RN02: Unicidade de Identidade** - Impedir duplicidade de CPF/CNPJ e E-mail.
- [ ] **RN03: Valor Mínimo** - Validar se operações são maiores que zero.
- [ ] **RN04: Imutabilidade** - Garantir que transações não sejam editáveis/excluíveis.
- [ ] **RN05: Integridade Transacional** - Uso de `@Transactional` para operações atômicas.
- [ ] **RN06: Status da Conta** - Validar se a conta está ativa para operar.
