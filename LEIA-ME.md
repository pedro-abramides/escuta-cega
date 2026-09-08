# Escuta Cega · dinâmica de Telemarketing (Grupo 2)

Duas telas que conversam em tempo real:

- **`index.html`** é o telão. Toca as ligações, mostra o QR, conta os votos ao vivo e revela o gabarito.
- **`votar.html`** é o celular da turma. Cinco botões, estilo Kahoot, um voto por pessoa.

O placar da sala aparece no telão no instante em que a pessoa toca no número. Não precisa de conta, login, servidor nem cartão de crédito.

---

## 1. Publicar (uma vez, cerca de 10 minutos)

Precisa estar na web com HTTPS, senão o celular não alcança o telão. O caminho mais simples é o GitHub Pages.

1. Crie uma conta em **github.com** (gratuita).
2. Clique em **New repository**. Nome: `escuta-cega`. Marque **Public**. Crie.
3. Na tela do repositório vazio, clique em **uploading an existing file**.
4. Arraste **todo o conteúdo desta pasta** (`index.html`, `votar.html`, e as pastas `audio` e `lib`). Espere subir e clique em **Commit changes**.
5. Vá em **Settings › Pages**. Em *Source*, escolha **Deploy from a branch**, branch **main**, pasta **/ (root)**. Salve.
6. Espere um ou dois minutos e recarregue a página. Vai aparecer o endereço, algo como:
   `https://SEUUSUARIO.github.io/escuta-cega/`

Esse endereço é o telão. O QR que aparece na tela já aponta sozinho para o `votar.html` com o código da sala.

> Alternativas equivalentes: Netlify Drop, Cloudflare Pages ou Vercel. Qualquer hospedagem estática com HTTPS serve.

---

## 2. Testar antes da aula (importante)

Faça isso **na ESPM, na rede que vocês vão usar**, com pelo menos dois celulares.

1. Abra o endereço no notebook. No canto superior direito deve aparecer **Ao vivo** com uma bolinha piscando e o código da sala.
2. Clique em **Começar a dinâmica**, depois em **Abrir votação**.
3. Aponte a câmera de um celular para o QR. A tela de voto deve abrir com a bolinha verde.
4. Vote. O número no telão tem que subir na hora.

**Se aparecer "Modo local" em vez de "Ao vivo"**, a rede bloqueou o canal de tempo real. A tela tenta três servidores públicos em sequência, então geralmente um passa. Se nenhum passar, use o roteador do celular (4G compartilhado) para o notebook, ou rode a dinâmica no **modo local**: quem opera o telão toca na coluna da nota conforme as mãos sobem, ou aperta as teclas 1 a 5. A dinâmica funciona inteira assim, só sem os celulares.

---

## 3. Rodar em sala

| Momento | O que fazer |
|---|---|
| Abertura | Deixe a tela inicial no projetor enquanto a turma entra |
| Começar | **Começar a dinâmica** abre a primeira ligação |
| Escutar | Toque no play. A trilha mostra quem fala; quando as faixas se encostam, alguém interrompeu. A barra fina sob o topo acompanha o áudio |
| Votar | A votação abre sozinha quando o áudio acaba, ou clique em **Abrir votação** |
| Revelar | **Revelar** mostra a média, a distribuição e o gabarito |
| Fechar | Depois das cinco, **Ver a matriz** mostra o quadro final |

Atalhos no telão: **espaço** toca e pausa o áudio, **1 a 5** somam um voto manual, **Shift + número** tira um voto. A ligação no ar fica marcada em preto na barra de baixo, com a fase ao lado.

A ordem das ligações não segue a qualidade. Elas foram embaralhadas de propósito para a turma não pegar o padrão.

---

## 4. Trocar os áudios por vozes melhores

Os áudios que vieram na pasta são sintetizados com um motor offline e soam robóticos. Servem para ensaiar. Para a aula, vale trocar.

**Duas formas, as duas funcionam:**

**A. Gravar com o grupo.** São nove pessoas e cada ligação tem dois personagens. Gravem no celular, em ambiente silencioso, exportem em MP3.

**B. ElevenLabs.** Conta gratuita dá cerca de 10 mil caracteres por mês, e os cinco roteiros somam bem menos que isso. No Studio dá para colocar duas vozes na mesma faixa (uma para o operador, outra para o cliente). Vozes em português que funcionam bem: **Nicole**, **Rachel**, **Adam**, **Antoni**. Sugestão de ajuste: *Stability* 45, *Similarity* 75. Para a ligação do cartão, suba a velocidade; para a da cobrança, deixe o operador mais seco.

**Como substituir:** exporte em MP3, renomeie exatamente como abaixo e substitua os arquivos da pasta `audio/`.

| Arquivo | Ligação | Nota de referência |
|---|---|---|
| `lig3.mp3` | LIG 01 · A pesquisa | 3 |
| `lig1.mp3` | LIG 02 · O cartão | 1 |
| `lig5.mp3` | LIG 03 · O atraso | 5 |
| `lig2.mp3` | LIG 04 · A cobrança | 2 |
| `lig4.mp3` | LIG 05 · O plano | 4 |

Se a duração do novo áudio ficar muito diferente da original, a transcrição e a trilha saem de sincronia. A tela percebe isso sozinha e apaga as duas, o resto continua funcionando normalmente.

Os roteiros completos estão em **`ROTEIROS.md`**, prontos para colar.

---

## 5. Um detalhe do conteúdo

No slide do 0303 vocês escreveram que o prefixo é obrigatório desde 2022. Isso mudou: a Anatel tornou o uso **facultativo** pelo Acórdão nº 201, de 14 de agosto de 2025, e no lugar passou a exigir autenticação de chamadas de quem origina mais de 500 mil ligações por mês. Vale corrigir no slide ou citar a mudança na apresentação, porque é o tipo de detalhe que rende ponto.

Fonte: gov.br/anatel › Numeração › Telemarketing Ativo, Prefixo 0303.

---

Grupo 2 · Marketing de Relacionamento · ESPM
Beatriz Aoki, Carolina Perdigão, Chiara Rigamonti, Gabriela Navarro, Gabriela Silveira, Lígia Santoro, Luiza Fidelis, Mariana Ball, Rafaela Shayeb.
