# 📚 Guia de Publicação no GitHub Pages

## ✅ Pré-requisitos

- [Git for Windows](https://git-scm.com/download/win) instalado
- Conta no [GitHub](https://github.com)

## 🚀 Passo a Passo

### Passo 1: Criar Repositório no GitHub

1. Acesse [github.com/new](https://github.com/new)
2. **Repository name**: `gestaoconfinamento` (ou seu nome preferido)
3. **Description** (opcional): "Sistema de Gestão de Confinamento com Firebase Firestore"
4. Deixe como **Public**
5. ❌ **NÃO** marque "Initialize this repository with: README"
6. Clique em **Create repository**

### Passo 2: Configurar Git Localmente

1. Abra o PowerShell/Terminal na pasta do projeto:
   ```bash
   cd "c:\Users\Ian Italo\OneDrive\Área de Trabalho\gestaoconfinamento"
   ```

2. Configure seu nome e email (primeira vez apenas):
   ```bash
   git config --global user.name "Seu Nome"
   git config --global user.email "seu-email@example.com"
   ```

3. Configure o origen remoto:
   ```bash
   git remote add origin https://github.com/SEU-USUARIO/gestaoconfinamento.git
   ```
   
   ⚠️ **Substitua `SEU-USUARIO` pelo seu username no GitHub!**

4. Faça push do código:
   ```bash
   git branch -M main
   git push -u origin main
   ```
   
   Será pedida sua senha do GitHub (ou token de acesso)

### Passo 3: Ativar GitHub Pages

1. Abra seu repositório no GitHub
2. Vá em **Settings** → **Pages**
3. Em **Build and deployment**:
   - **Source**: Selecione `Deploy from a branch`
   - **Branch**: Selecione `main`
   - **Pasta**: Deixe como `/ (root)`
4. Clique em **Save**

### Passo 4: Acessar a Aplicação

Aguarde 2-5 minutos e acesse:

```
https://SEU-USUARIO.github.io/gestaoconfinamento/
```

⚠️ **Substitua `SEU-USUARIO` pelo seu username do GitHub!**

## 🔐 Usar Personal Access Token (se senha não funcionar)

Se o Git pedir "fatal: Authentication failed", use um **Personal Access Token**:

1. GitHub → Settings → Developer settings → Personal access tokens
2. Clique em **Generate new token (classic)**
3. Nome: `gestaoconfinamento-push`
4. Permissões: ✅ `repo` (todas)
5. Clique em **Generate token**
6. **Copie o token** (não mostrará novamente!)
7. Ao fazer push, quando pedir senha, cole o token

## 📝 Fazer Novos Commits Após Mudanças

Sempre que fazer mudanças no código:

```bash
git add .
git commit -m "Descrição das mudanças"
git push origin main
```

GitHub Pages atualiza automaticamente em 1-2 minutos!

## 🆘 Troubleshooting

### "fatal: could not read Username"
- Use um **Personal Access Token** (veja seção acima)
- Ou use HTTPS com token

### GitHub Pages não atualiza
- Aguarde 2-5 minutos
- Vá em Settings → Pages e confirme o branch correto
- Try a Ctrl+Shift+R (força atualização do cache)

### "Error: ENOENT: no such file or directory"
- Certifique-se que `index.html` está na raiz da pasta
- Execute: `ls -la` no terminal para listar arquivos

### Aplicação carrega mas não funciona
- Abra o **Console** (F12) procure por erros
- Verifique se Firebase está configurado corretamente
- Cheque a autenticação do Google

## 🎯 Resultado Final

Após completar os passos acima, você terá:

✅ Repositório Git no GitHub
✅ Código sincronizado na nuvem
✅ Aplicação acessível via GitHub Pages
✅ Firebase Firestore como banco de dados
✅ Autenticação por Google integrada

## 📱 Como Usar a Aplicação

1. Acesse: `https://SEU-USUARIO.github.io/gestaoconfinamento/`
2. Clique em **"Entrar com Google"**
3. Selecione sua conta Google
4. Pronto! A aplicação está pronta para usar

Todos os dados são salvos automaticamente no Firestore sob sua conta.

---

**Sucesso na publicação! 🎉**
