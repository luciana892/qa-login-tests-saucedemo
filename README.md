**Projeto: qa-login-tests-saucedemo**  qa_metrics_animation.gif

```md
# 🧪 Projeto de Testes Manuais – Login & Recuperação de Senha (SauceDemo)

Repositório criado para demonstrar práticas profissionais de **QA em testes manuais**, incluindo planejamento, criação de casos de teste, execução, registro de evidências e documentação completa.  
O projeto segue boas práticas do **STLC**, princípios do **ISTQB** e diretrizes de documentação inspiradas na ISO/IEC/IEEE 29119.

---

# 🎯 Objetivo
Validar o comportamento das funcionalidades de **Login**, **Mensagens de Erro**, **Logout** e **Fluxo de Recuperação de Senha (simulado)** do site SauceDemo.

Site testado: https://www.saucedemo.com/

Este projeto tem como propósito demonstrar:
- Capacidade de análise funcional  
- Escrita clara de casos de teste  
- Execução estruturada  
- Comunicação eficaz de bugs  
- Organização e rastreabilidade de documentos  

---

# 📘 Escopo

### ✔️ Funcionalidades testadas
- Login com credenciais válidas  
- Login com credenciais inválidas  
- Login com usuário bloqueado  
- Campos obrigatórios  
- Mensagens de erro  
- Logout  
- Tentativa de recuperação de senha (página estática – comportamento observado)

### ❌ Fora do Escopo
- Testes de API  
- Testes Mobile  
- Segurança avançada  
- Testes de performance  
- Fluxos não relacionados ao login

---

# 📂 Estrutura do Repositório

```

qa-login-tests-saucedemo
├── README.md
├── Plano-de-Teste.md
├── Casos-de-Teste/
│     ├── CT-Login.xlsx
│     └── CT-RecuperacaoSenha.xlsx
├── Evidencias/
│     ├── login-sucesso.png
│     ├── erro-usuario-invalido.png
│     └── erro-campo-vazio.png
└── Relatorio-Final.md

```

---

# 🛠 Ferramentas e Ambiente
- Navegador: Chrome 121  
- Sistema Operacional: Windows 10  
- Ferramentas de documentação: Excel / Google Sheets  
- Captura de tela: Print Screen  
- Resolução: 1920×1080  

---

# 🧪 Casos de Teste
Todos os casos podem ser encontrados na pasta **Casos-de-Teste**.  
A estrutura segue boas práticas:

- ID único  
- Nome do cenário  
- Pré-condições  
- Passos detalhados  
- Dados de teste  
- Resultado esperado  
- Evidências associadas  

Exemplos:

### ✔️ CT01 – Login válido
```

Passos:

1. Inserir usuário standard_user
2. Inserir senha secret_sauce
3. Clicar em Login
   Resultado Esperado:
   Usuário deve acessar a página de produtos.

```

### ✔️ CT02 – Login com senha incorreta
```

Resultado Esperado:
Apresentar mensagem "Username and password do not match any user"

```

### ✔️ CT03 – Usuário bloqueado
```

Resultado Esperado:
Mensagem "Sorry, this user has been locked out."

```

---

# 🐞 Relatório de Bugs
O relatório detalhado está disponível em **Relatorio-Final.md**, incluindo:

- Título claro  
- Severidade  
- Prioridade  
- Passos para reproduzir  
- Resultado esperado vs obtido  
- Evidência  
- Ambiente  

Exemplo:

### ❌ Bug 01 – Mensagem incorreta para senha vazia
- Severidade: Média  
- Prioridade: Alta  
- Comportamento incorreto quando o campo de senha está vazio.

---

# 📸 Evidências
As evidências da execução estão em **/Evidencias**, organizadas por padrão:

```

CT01-login-sucesso.png
CT02-erro-usuario-invalido.png
CT04-erro-campo-vazio.png

```

---

# 📘 Boas Práticas Aplicadas no Projeto
- Casos de teste claros, objetivos e rastreáveis  
- Escopo bem definido (inclui e exclui)  
- Padrão de escrita consistente  
- Evidências nomeadas de forma organizada  
- Registro claro de bugs  
- Estrutura limpa e profissional de pastas  
- Documentação seguindo referências ISTQB  

---

# 📊 Resultados da Execução
| Métrica                 | Quantidade |
|-------------------------|------------|
| Casos criados           | 12         |
| Casos executados        | 12         |
| Casos aprovados         | 9          |
| Casos reprovados        | 3          |
| Bugs encontrados        | 3          |


# 🐞 Relatório Final de Bugs – Projeto Login & Recuperação de Senha (SauceDemo)

Este documento consolida todos os defeitos identificados durante a execução dos testes manuais.

---

## 📊 Resumo Geral

| Métrica          | Quantidade |
| ---------------- | ---------- |
| Casos Executados | 12         |
| Casos Aprovados  | 9          |
| Casos Reprovados | 3          |
| Bugs Encontrados | 3          |

---

# 🐞 Bug 01 – Mensagem incorreta para senha vazia

**ID:** BUG01
**Severidade:** Média
**Prioridade:** Alta

### Descrição

Ao tentar efetuar login deixando o campo de senha vazio, o sistema exibe mensagem genérica de credenciais inválidas.

### Passos para Reproduzir

1. Acessar a página de login
2. Preencher usuário válido
3. Deixar senha vazia
4. Clicar em *Login*

### Resultado Esperado

Mensagem clara indicando que o campo *Senha* é obrigatório.

### Resultado Obtido

Mensagem: *"Username and password do not match any user"*

### Evidência

`erro-campo-vazio.png`

---

# 🐞 Bug 02 – Falha visual no ícone de erro

**ID:** BUG02
**Severidade:** Baixa
**Prioridade:** Baixa

### Descrição

O ícone de erro fica sobreposto ao campo de input em resoluções menores.

### Passos para Reproduzir

1. Redimensionar janela para 1280×720
2. Executar login inválido
3. Observar alinhamento do ícone

### Resultado Esperado

Ícone posicionado corretamente ao lado da mensagem.

### Resultado Obtido

Ícone sobreposto ao campo de texto.

### Evidência

`erro-icone-ui.png`

---

# 🐞 Bug 03 – Logout não funcionando no Firefox

**ID:** BUG03
**Severidade:** Média
**Prioridade:** Média

### Descrição

O botão de logout não responde no Firefox 122.

### Passos para Reproduzir

1. Logar com usuário válido
2. Abrir menu lateral
3. Clicar em *Logout*

### Resultado Esperado

Redirecionamento para página de login.

### Resultado Obtido

Nenhuma ação ocorre.

### Observação

Comportamento não reproduzido no Chrome.

---

## ✔️ Conclusão

Os bugs identificados não impedem o funcionamento básico do sistema, porém impactam a experiência do usuário e devem ser corrigidos para garantir clareza, consistência e comportamento esperado nas principais interações da aplicação.

Documentado por **Luciana Valeriana** – QA em formação.

# 📸 Evidências de Execução – Projeto Login & Recuperação de Senha (SauceDemo)

Este documento lista as evidências geradas durante a execução dos testes manuais. As imagens devem ser adicionadas na pasta **/Evidencias** do repositório.

---

## 📁 Estrutura Recomendada de Arquivos

```
Evidencias/
 ├── CT01-login-sucesso.png
 ├── CT02-erro-senha-invalida.png
 ├── CT03-usuario-bloqueado.png
 ├── CT04-campo-usuario-vazio.png
 ├── CT05-campo-senha-vazio.png
 ├── CT06-logout-sucesso.png
 ├── CT08-ui-mensagem-erro.png
 ├── BUG01-erro-campo-vazio.png
 ├── BUG02-falha-icone-ui.png
 └── BUG03-logout-firefox.png
```

---

## 🖼️ Detalhamento das Evidências

A seguir, a descrição de cada evidência sugerida.

---

### ✔️ CT01 – Login com sucesso

**Arquivo:** `CT01-login-sucesso.png`
**Descrição:** Exibe a página *Products* após login realizado corretamente com o usuário `standard_user`.

---

### ✔️ CT02 – Erro de senha inválida

**Arquivo:** `CT02-erro-senha-invalida.png`
**Descrição:** Tela mostrando a mensagem vermelha *"Username and password do not match any user"* após tentar login com senha incorreta.

---

### ✔️ CT03 – Usuário bloqueado

**Arquivo:** `CT03-usuario-bloqueado.png`
**Descrição:** Evidência da mensagem *"Sorry, this user has been locked out."*.

---

### ✔️ CT04 – Campo usuário vazio

**Arquivo:** `CT04-campo-usuario-vazio.png`
**Descrição:** Mensagem de erro solicitando o preenchimento do campo usuário.

---

### ✔️ CT05 – Campo senha vazio

**Arquivo:** `CT05-campo-senha-vazio.png`
**Descrição:** Mensagem inadequada exibida (BUG01) quando senha é deixada vazia.

---

### ✔️ CT06 – Logout funcionando

**Arquivo:** `CT06-logout-sucesso.png`
**Descrição:** Evidência da volta à tela de login após realizar logout.

---

### ✔️ CT08 – Validação visual (UI)

**Arquivo:** `CT08-ui-mensagem-erro.png`
**Descrição:** Tela com mensagem de erro para validar alinhamento, cor e ícone.

---

# 🐞 Evidências dos Bugs

### ❌ BUG01 – Mensagem incorreta para senha vazia

**Arquivo:** `BUG01-erro-campo-vazio.png`
**Descrição:** Demonstra a mensagem genérica incorreta ao tentar logar sem preencher senha.

---

### ❌ BUG02 – Falha visual no ícone de erro

**Arquivo:** `BUG02-falha-icone-ui.png`
**Descrição:** Ícone sobreposto ao campo de input em telas menores.

---

### ❌ BUG03 – Logout não funcionando no Firefox

**Arquivo:** `BUG03-logout-firefox.png`
**Descrição:** Tentativa de logout sem resposta no navegador Firefox.

---

## ✔️ Observações

* As evidências devem ser capturadas sempre com boa resolução.
* Utilize nomes padronizados para facilitar rastreabilidade.
* Recomenda-se registrar também data/hora da execução.

# ✔️ Checklist de Execução – Projeto Login & Recuperação de Senha (SauceDemo)

Este checklist foi criado para garantir que todas as etapas necessárias da execução de testes manuais sejam realizadas de forma organizada, consistente e rastreável.

---

## 🧪 Antes da Execução

* [ ] Ambiente acessível ([https://www.saucedemo.com/](https://www.saucedemo.com/))
* [ ] Conexão estável com a internet
* [ ] Navegador atualizado (Chrome 121 ou superior)
* [ ] Dados de teste revisados
* [ ] Casos de teste disponíveis e atualizados
* [ ] Evidências organizadas na pasta correta
* [ ] Plano de teste revisado

---

## ▶️ Durante a Execução

* [ ] Executar cada caso seguindo exatamente os passos descritos
* [ ] Validar mensagens de erro e comportamento esperado
* [ ] Registrar status (Aprovado / Reprovado)
* [ ] Registrar comportamento inesperado mesmo que o teste passe
* [ ] Capturar evidências com boa resolução
* [ ] Nomear evidências seguindo o padrão definido
* [ ] Validar campos obrigatórios
* [ ] Testar cenários positivos e negativos
* [ ] Anotar observações relevantes

---

## 🐞 Registro de Bugs

* [ ] Criar bug com título claro
* [ ] Descrever passos detalhados para reprodução
* [ ] Informar resultado esperado e obtido
* [ ] Anexar evidências
* [ ] Classificar severidade
* [ ] Definir prioridade
* [ ] Registrar ambiente de execução

---

## 📤 Após a Execução

* [ ] Salvar todas as evidências
* [ ] Atualizar status dos casos de teste
* [ ] Consolidar relatório final
* [ ] Revisar bugs abertos
* [ ] Verificar consistência da documentação
* [ ] Organizar pastas do repositório
* [ ] Commitar alterações no GitHub com mensagens claras

---
# 🧪 Projeto de Testes Manuais – Login & Recuperação de Senha (SauceDemo)

Este repositório demonstra práticas profissionais de QA em testes manuais, incluindo planejamento, casos de teste, execução, relatório de bugs e checklist de execução.

---


























