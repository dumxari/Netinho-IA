import os
from google.colab import userdata

os.environ['GOOGLE_API_KEY'] = userdata.get('GOOGLE_API_KEY')

from google import genai

client = genai.Client()

for model in client.models.list():
    print(model.name)




    system_instruction = "Você é um assistente pessoal que sempre responde como se fosse um netinho bagunceiro."




print("Olá, vovô. Sou seu Netinho IA que sempre te ajuda a entender as tecnologias da nova geração. Em que posso ajudar o senhor hoje?")
resposta_do_vovo = input("Digite aqui o que o senhor precisa: ")

if resposta_do_vovo == "ligar para alguém":
  print("Ok, vovô. Para isso, vá até a tela inicial do seu aparelho e procure pelo APP TELEFONE. Em seguida, digite o telefone nas teclas e pressione o botão verde para ligar!")
if resposta_do_vovo == "ligar":
  print("Ok, vovô. Para isso, vá até a tela inicial do seu aparelho e procure pelo APP TELEFONE. Em seguida, digite o telefone nas teclas e pressione o botão verde para ligar!")
if resposta_do_vovo == "ligar para alguém":
  print("Ok, vovô. Para isso, vá até a tela inicial do seu aparelho e procure pelo APP TELEFONE. Em seguida, digite o telefone nas teclas e pressione o botão verde para ligar!")
elif resposta_do_vovo == "ligar":
  print("Ok, vovô. Para isso, vá até a tela inicial do seu aparelho e procure pelo APP TELEFONE. Em seguida, digite o telefone nas teclas e pressione o botão verde para ligar!")
elif resposta_do_vovo == "aumentar o volume":
  print("Para isso, o senhor precisa procurar os botões laterais no seu celular. O botão para aumentar o volume está logo acima do de diminuir. Clique nele conforme precisar.")
elif resposta_do_vovo == "diminuir o volume":
  print("Para isso, o senhor precisa procurar os botões laterais no seu celular. O botão para diminuir o volume está logo abaixo do de aumentar. Clique nele conforme precisar.")
elif resposta_do_vovo == "desligar celular":
  print("Já candado das redes sociais vovô? Hehe! Para isso, você precisa pressionar a tecla lateral DESLIGAR do seu celular por alguns segundos! Após isso, uma mensagem irá aparecer na tela perguntando se quer desligar o aparelho. Confirme o desligamento!")
elif resposta_do_vovo == "whatsapp":
  print("Para abrir o WhatsApp, você precisa procurar um ícone na sua tela inicial com um formato verde e um símbolo de telefone branco no centro. Clique nele e seu zapzap estará aberto!")
elif resposta_do_vovo == "enviar mensagem":
  print("Você pode enviar mensagens pelo app Whatsapp. Assim que ele abrir, você precisa clicar no contato da pessoa que procura e, na barra que fica bemmm embaixo, você consegue escrever e enviar suas imagens com o ícone de seta!")
elif resposta_do_vovo == "ver vídeos no youtube":
  print("Para assistir vídeos no YouTube, procure o ícone vermelho com um triângulo branco dentro e toque nele. Depois, você pode digitar o que quer assistir na barra de pesquisa.")
elif resposta_do_vovo == "tirar uma foto":
  print("Para tirar fotos, procure o aplicativo da câmera (geralmente um ícone de uma câmera) e toque nele. Depois, é só apontar para o que você quer fotografar e apertar o botão!")
elif resposta_do_vovo == "ver as fotos":
  print("Para ver as fotos que você tirou, procure o aplicativo da galeria (geralmente um ícone de uma flor ou várias fotos pequenas) e toque nele.")
elif resposta_do_vovo == "mandar um áudio":
  print("Para mandar um áudio no WhatsApp, abra a conversa com quem você quer falar, procure o ícone de um microfone e segure ele enquanto fala. Depois, solte para enviar.")
elif resposta_do_vovo == "abrir um aplicativo":
  print("Qual aplicativo o senhor gostaria de abrir, vovô? ")


chat = client.chats.create(model=modelo)

resposta = chat.send_message("Oi, tudo bem?")

resposta.text
