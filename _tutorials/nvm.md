---
title: "NVM: Gerenciando versões do Node.js"
date: 2026-02-27
description: "Guia rápido para instalar, listar e alternar versões do Node com NVM sem dor de cabeça."
tags: [node, nvm, tooling, setup]
layout: post
---

## O que é NVM?

O **NVM** (Node Version Manager) permite instalar e alternar entre múltiplas versões do Node.js no mesmo sistema. Essencial quando você trabalha em projetos com versões diferentes de Node.

---

## Comandos Essenciais

### Listar versões disponíveis para instalar

```bash
nvm ls-remote
# Filtrar apenas LTS:
nvm ls-remote --lts
```

### Instalar uma versão

```bash
nvm install 20          # instala a versão 20.x mais recente
nvm install --lts       # instala a LTS mais recente
nvm install 18.19.0     # versão exata
```

### Listar versões instaladas

```bash
nvm ls
```

### Usar uma versão específica (na sessão atual)

```bash
nvm use 20
nvm use --lts
```

### Verificar qual versão está ativa

```bash
nvm current
node --version
```

### Definir versão padrão (persiste entre sessões)

```bash
nvm alias default 20
```

### Desinstalar uma versão

```bash
nvm uninstall 18
```

### Ver onde o NVM está instalado

```bash
nvm root
```

---

## Fluxo Típico

```bash
# 1. Instalar a LTS mais recente
nvm install --lts

# 2. Definir como padrão
nvm alias default --lts

# 3. Verificar
node --version
npm --version
```

---

## 💡 Dica: `.nvmrc` por projeto

Crie um arquivo `.nvmrc` na raiz do projeto com a versão desejada:

```
20
```

Aí basta rodar `nvm use` na pasta do projeto e o NVM lê o arquivo automaticamente.
