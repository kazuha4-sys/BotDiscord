# IA Criação de servidor de Discord 

## **Descrição**

Este projeto utiliza a biblioteca discord para integarir com a plataforma, Os para mexer com arquivos, e dotenv para carregar e ler o arquivo .env

##  **Sobre a biblioteca** 

### **O que é a biblioteca Discord.py?**

a biblioteca *Discord.py* é uma API (Interface de Programação de Aplicações) escritas em python que permite interagir com a plataforma Discord. Com ela, você pode criar bots personalizados que realizem tarefas automatizadas em servidores do Discord. Esses bpts poder ser usados para diversas finalidades, como:
 * **Moderação**: Automatizar a remoção de mensagens inapropriadas, banir ou silenciar membros problemáticos.

 * **Jogos e Diversão**: Criar jogos interativos no servidor, como quizzes, minigames ou sistemas de RPG.

 * **Música**: Reproduzir músicas em canais de voz.

 * **Automação**: Gerar notificações, agendar tarefas ou integagir com APis externcas, como APIs de clima, notícias ou esportes.

A biblioteca abstrai as interações complexas da API REST e WebSocket do Discord, permitindo que você se concentre no desenvolvimento do seu bot sem se preucupar com os detalhes de comunicação de baixo nível.

---

**Breve explicação sobre a importancia da biblioteca**:

 * **Facilidade de uso**: O Discord.py oferece uma interface simples e poderosa para tranalhar com os recursos do Discord.

 * **Flexibilidade**: Com ela, você pode personalizar comandos, eventos e integrações externas.
 * **Comunidade**: A biblioteca tem uma grande base de usúarios e uma documentação robusta, tornando mais fácil aprender e resolver problemas.

---

**Exemplos de casos de uso para bots**

## 1. ***Moderação**:
 * Banir, mutar ou silenciar membros automaticamente.

 * Filtrar mensagens ofensivas ou indesejadas.

## 2. **Jogos e Diversão**:
 * Criar comandos interativos, como:

 ```python 
    @bot.command()
    async def dado(ctx):
        import random
        numero = random.randint(1, 6)
        await ctx.send(f'Você rolou o número {numero}')
 ``` 
 Esse comando gera um n´mero aleatório simulando um dado.

## 3. **Música**:
 * Bots que tocam músicas de plataformas como Youtube ou spotify.
 * Criar comandos como ```!play```, ```!pause```, ```!ship```.

## 4. **Automação**:
 * Gerar relatórios automáticos, como logs de atividades no servidor.
 * Enviar mensagens programadar (lembreted, aniversários).

## 5. ***Ferramentas**:
 * Criar enquetes com reações.
 * Notidicar eventos ao vivo de plataformas externas (como twitch ou Youtube).

---

# Como inicar 

 ## 1. **Crie uma aplicação no Developer Portal do Dicord**:
  * Acesse o ****
  * Clique em "Nova aplicação" e dê um nome ao seu bot.
  * Navegue até a aba **Robo/Bot** e clique em "Adicionar bot" e depois em administrador.
  * Copie o token do bot para uso no código
    
 ## 2. **Salve o token**
  * Crie uma pasta em um diretório que vc saiba onde vai estar, como a Area de Trabalho.
  * Entre nesta pasta, execute algum editor de código da sua preferencia e crie um arquivo chamado **.env**
  * Nesse arquivo vc vai escrever a seguinte coisa
  ```env
  DISCORD_TOKEN=o-Token-do-bot-que-vc-copiou
  # Caso você ja tenha o ID do servidor coloque em # para faciliar o trabalho 
  ``` 
  * Em seguida crie outro arquivo chamado bot.py e cole o seguinte codigo e faça as mudanças necessarias
  ```python
  import discord
  from dotenv import load_dotenv
  from discord.ext import commands

  # Carregar o arquivo .env
  load_dotenv()


  # Configurando o prefixo e o bot
  bot = commands.Bot(command_prefix="!")

  @bot.event
  async def on_ready():
    print(f'Bot conectado como {bot.user}')

    @bot.command()
    async def ping(ctx):
        await ctx.send('Pong!')

    bot.run('DISCORD_TOKEN')  # Substitua 'YOUR_TOKEN' pelo token do seu bot

  ```

  * Coloque o bot no servidor e rode e digite **Pong!** e ele fara o comando.

## Para saber mais sobre a bibloteca e como fazer bots para servidor, leia todos os diretórios desse reposítorio, ou selecione qual te agrada mais.

# Espero ter ajudados vocês a fazer seus bots para o discord. Qualquer duvida entre em contato pelo meu instahtam
``` txt
Kauan2.04
```
