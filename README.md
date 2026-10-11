# Ergon Agente

Instaladores do **Ergon Agente**, o programa que faz as buscas no Google Maps para o
[Ergon Hub](https://ergonhub.com.br) a partir de um computador da sua agência.

Este repositório guarda só os instaladores publicados. O código do Ergon Hub não fica aqui.

## Baixar

**[Baixar o Ergon Agente para Windows](https://github.com/DavidFreitas0/ergon-hub-agent-releases/releases/latest/download/Ergon-Agente-Setup.exe)**
(sempre a versão mais nova)

O mesmo link está no Ergon Hub, em **Configurações → Agente → Baixar o agente**. As versões
anteriores ficam em [Releases](https://github.com/DavidFreitas0/ergon-hub-agent-releases/releases).

## Requisitos

- Windows 10 ou 11, 64 bits.
- Cerca de 600 MB livres em disco.
- Internet. O computador precisa ficar ligado enquanto houver extração na fila.
- Não precisa de Docker nem de permissão de administrador.

## Instalar e conectar

1. Rode o `Ergon-Agente-Setup.exe` e clique em **Instalar** e depois em **Concluir**.
2. No Ergon Hub, vá em **Configurações → Agente → Conectar um computador → Gerar código**.
3. Digite o código de 6 letras e números (ex.: `K7M-4QX`) na janela do Ergon Agente e clique em
   **Conectar**. O código vale por 10 minutos e só uma vez.
4. Em segundos o Ergon Hub mostra **"Conectado"**, e o computador aparece como **Online**.

Pronto. A partir daí o agente:

- fica escondido com um ícone perto do relógio;
- inicia junto com o Windows;
- pega as extrações da fila do Ergon Hub, uma por vez;
- se atualiza sozinho quando sai uma versão nova.

### Aviso "O Windows protegeu o computador"

Enquanto o instalador não tiver assinatura digital, o Windows pode mostrar esse aviso na primeira
vez. Clique em **Mais informações → Executar assim mesmo**. Baixe sempre por este repositório ou
pelo botão do Ergon Hub.

## Ícone perto do relógio

Clique com o botão direito no ícone do Ergon Agente para:

- ver o estado (online, buscando, sem conexão);
- **Abrir o Ergon Hub**;
- **Ver registro** do dia, útil para o suporte;
- **Sair**. O agente volta a abrir no próximo início do Windows.

## Problemas comuns

| O que aparece | O que fazer |
|---|---|
| "Código inválido ou vencido" | Gere um código novo no Ergon Hub; cada código vale 10 minutos e uma vez. |
| "Este computador foi desconectado no Ergon Hub" | Alguém revogou o computador em Configurações → Agente. Gere um código novo para conectar de novo. |
| Computador aparece como **Offline** no Ergon Hub | Confira se o computador está ligado e com internet e se o ícone está perto do relógio. Se não estiver, abra o **Ergon Agente** pelo menu Iniciar. |
| Extração parada em "Aguardando o agente" | Mesmo caso acima: nenhum computador conectado está online. |

## Onde ficam os arquivos

| O quê | Pasta |
|---|---|
| Programa | `%LOCALAPPDATA%\Programs\Ergon Agente` |
| Configuração e registros | `%LOCALAPPDATA%\Ergon Agente` |

A chave de conexão fica protegida pelo Windows: só o seu usuário, neste computador, consegue
lê-la. Os registros guardam números e erros, não os dados dos contatos encontrados.

## Desinstalar

Pelo Windows: **Configurações → Aplicativos → Ergon Agente → Desinstalar**. O programa, a
configuração, os registros e a inicialização automática são removidos. Para liberar o computador
também no Ergon Hub, use **Revogar** em Configurações → Agente.
