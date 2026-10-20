# Nosso Calendário de Amor

Calendário do ano inteiro onde cada dia guarda uma mensagem de amor. Para duas pessoas — cada uma escreve a sua e vê a da outra. Tudo em marsala. Funciona 100% no GitHub (Pages + API), sem nenhum outro serviço.

## O que tem

- Calendário completo dos 12 meses (navegue entre anos)
- Cada dia pode ter uma mensagem de cada uma
- **Dias futuros estão bloqueados** — só dá pra escrever quando o dia chega (com contagem regressiva)
- Dois perfis (botões "Ela" / "Amor") — nomes personalizáveis na engrenagem
- **Sincronização via GitHub**: as mensagens são salvas no próprio repositório, as duas veem pelo mesmo link
- Funciona também no modo local (sem sincronização)
- Backup em arquivo JSON

## Passo 1 — Publicar no GitHub Pages (5 min)

1. Crie um repositório **público** no GitHub (ex: `nosso-calendario`).
2. Faça upload do `index.html` para a raiz (Add file → Upload files).
3. Vá em **Settings → Pages**.
4. Source: `Deploy from a branch`, branch `main`, pasta `/ (root)` → Save.
5. Aguarde 1–2 min. Seu link: `https://SEU-USUARIO.github.io/nosso-calendario/`

## Passo 2 — Ativar a sincronização (1 min, só uma vez)

Sem isso, cada uma só vê as próprias mensagens no próprio celular. Para compartilhar:

1. No GitHub, clique na sua **foto → Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Dê um nome; em **Expiration** escolha **No expiration**.
3. **Repository access** → Only select repositories → selecione o repositório do calendário.
4. **Permissions → Repository permissions → Contents** → mude para **Read and write**.
5. Clique em **Generate token** e copie o token (começa com `github_pat_`).
6. No site, clique na **engrenagem** → seção "Sincronização" → preencha:
   - Seu usuário do GitHub
   - Nome do repositório
   - O token que você copiou
7. Clique em **Conectar e sincronizar**.
8. A outra pessoa faz o mesmo (cola os **mesmos** 3 dados no celular dela).

Pronto! Quando uma escreve, a outra vê em até 30 segundos. Tudo fica salvo em um arquivo `dados.json` no próprio repositório.

> O token fica salvo apenas no navegador de cada uma (não no código do site). Pode revogar a qualquer momento no GitHub.

## Como usar

- No topo, cada uma seleciona o **seu** botão (Ela / Amor — troque pelos nomes reais na engrenagem).
- Clique em qualquer dia que já chegou → escreva → **Salvar mensagem**.
- Dias futuros têm cadeado e contagem regressiva — abrem sozinhos.
- Dias com mensagem ganham uma bolinha dourada; se as duas escreveram, a bolinha é marsala+dourada.

## Dicas

- Quer mudar a cor? Troque `--marsala:#7B2D43;` no topo do `index.html`.
- O ano é automático. Use as setinhas ao lado do ano para ver anos anteriores.
- Faça backup de vez em quando: engrenagem → Exportar mensagens.
- Se o token expirar ou for revogado, é só criar um novo e colar de novo.
