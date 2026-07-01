# 🐄 Farmtell Beef Analytics

Sistema integrado de **Gestão de Confinamento** com análise de dados em tempo real.

## 📋 Funcionalidades

- **Dashboard de Análise** - Visualização consolidada de KPIs
- **Dados de Carregamento** - Rastreamento de insumos e ingredientes
- **Distribuição de Ração** - Monitoramento de tratamento e conformidade
- **Registro de Ocorrências** - Documentação de eventos importantes
- **Análise de Estoque** - Autonomia vs projeção de consumo
- **Tendência Histórica** - Análise de consumo ao longo do tempo
- **Sincronização com Firebase Firestore** - Dados persistidos na nuvem
- **Autenticação por Google** - Acesso seguro aos dados

## 🔐 Autenticação

Acesse a aplicação com sua **Conta Google**. Todos os dados são salvos privativamente no Firebase Firestore sob sua conta.

## 📱 Como Usar

1. Acesse a aplicação pela web
2. Faça login com sua Conta Google
3. Navegue pelas abas:
   - **Dashboard** - Visualize métricas e KPIs
   - **Dados Brutos** - Veja as tabelas detalhadas
   - **Importar Dados** - Adicione novos dados em formato TSV
4. Os dados são salvos automaticamente no Firestore

## 🚀 Implantação no GitHub Pages

### Pré-requisitos
- Git instalado
- Conta no GitHub

### Passos

1. **Crie um repositório no GitHub**
   - Acesse [github.com/new](https://github.com/new)
   - Nomeie como `gestaoconfinamento` (ou seu nome preferido)
   - NÃO inicialize com README (já temos um)

2. **Configure o repositório local**
   ```bash
   cd gestaoconfinamento
   git init
   git add .
   git commit -m "Initial commit: Farmtell Beef Analytics com Firebase Firestore"
   git branch -M main
   git remote add origin https://github.com/seu-usuario/gestaoconfinamento.git
   git push -u origin main
   ```

3. **Ative GitHub Pages**
   - Vá para Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main`
   - Pasta: `/root`
   - Clique em "Save"

4. **Acesse sua aplicação**
   - URL: `https://seu-usuario.github.io/gestaoconfinamento/`

## 🔧 Tecnologias

- **Vanilla JavaScript** (sem dependências)
- **Tailwind CSS** - Estilos
- **Lucide Icons** - Ícones
- **Firebase Firestore** - Banco de dados
- **Google Auth** - Autenticação

## 📊 Estrutura de Dados no Firestore

```
gestao_confinamento/
  └─ {userId}/
     └─ dados/
        ├─ carregamento_LOCALIDADE_TIMESTAMP
        ├─ distribuicao_LOCALIDADE_TIMESTAMP
        ├─ ocorrencias_LOCALIDADE_TIMESTAMP
        └─ estoque_LOCALIDADE_TIMESTAMP
```

## ⚙️ Configuração Firebase

Seu projeto Firebase já está configurado em `index.html`. As regras de acesso garantem que:
- ✅ Usuários autenticados podem ler/escrever seus próprios dados
- ✅ Dados públicos (presecagem, paradas) são acessíveis

## 🐛 Troubleshooting

### "Erro ao fazer login"
- Verifique sua conexão com a internet
- Limpe cookies do navegador
- Tente em outra aba anônima

### "Dados não salvam"
- Confirme que está autenticado
- Verifique as regras do Firestore
- Abra o Console (F12) para ver erros

### GitHub Pages mostra apenas o HTML
- Certifique-se que o arquivo `index.html` está na raiz
- Vá em Settings → Pages e confirme o branch correto
- Pode levar alguns minutos para atualizar

## 📧 Contato

Para dúvidas ou relatório de bugs, abra uma [issue](https://github.com/seu-usuario/gestaoconfinamento/issues).

---

**Desenvolvido com ❤️ para Farmtell**
