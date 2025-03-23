# 📌 Git Flow para o Projeto Vite + React + Tailwind CSS

Este documento descreve o fluxo de trabalho utilizando Git para manter a organização do desenvolvimento do projeto.

## 🔀 Organização das Branches

- **`main`**: Branch principal, contendo apenas versões estáveis e prontas para produção.
- **`develop`**: Branch de desenvolvimento onde todas as novas funcionalidades e correções são integradas antes de serem enviadas para a `main`.
- **`feature/nome-da-feature`**: Branches criadas para cada nova funcionalidade ou melhoria no projeto.

## 🚀 Fluxo de Trabalho

### 1️⃣ Clonar o Repositório
```sh
  git clone https://github.com/seu-usuario/seu-repositorio.git
  cd nome-do-projeto
```

### 2️⃣ Criar a Branch de Desenvolvimento (Caso Ainda Não Exista)
```sh
  git checkout -b develop
```

### 3️⃣ Criar uma Nova Branch para a Funcionalidade
```sh
  git checkout -b feature/nome-da-feature develop
```

### 4️⃣ Implementar a Funcionalidade e Comitar as Mudanças
```sh
  git add .
  git commit -m "feat: adiciona nova funcionalidade X"
```

### 5️⃣ Enviar as Alterações para o Repositório Remoto
```sh
  git push origin feature/nome-da-feature
```

### 6️⃣ Criar um Pull Request para `develop`
- No GitHub/GitLab, abra um **Pull Request (PR)** de `feature/nome-da-feature` para `develop`.
- Aguarde a revisão e aprovação do código.

### 7️⃣ Mesclar as Mudanças na `develop`
Após a aprovação do PR:
```sh
  git checkout develop
  git merge feature/nome-da-feature
  git push origin develop
```

### 8️⃣ Publicação na `main`
Quando todas as features estiverem testadas e validadas:
```sh
  git checkout main
  git merge develop
  git push origin main
```

## 🛠️ Boas Práticas
- Use **nomes descritivos** para as branches (`feature/gerador-senhas`, `feature/calculadora` etc.).
- Faça **commits pequenos e descritivos**.
- Sempre atualize a branch `develop` antes de criar uma nova feature:
  ```sh
  git checkout develop
  git pull origin develop
  ```
- **Revise o código** antes de aprovar um Pull Request.

---
📌 Seguindo esse fluxo, o projeto manterá um desenvolvimento organizado e eficiente! 🚀

