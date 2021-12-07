
# About:
Open source bot for BombCrypto.
Bots are now banned by the game developers.
Use at your own risk.

### Smart Chain Wallet:
#### -

# Instalation:
### Download and install Ptyhon 3.10 - [site](https://www.python.org/downloads/).

Mark the option add Python to path:
![Check Add python to PATH](https://github.com/mpcabete/bombcrypto-bot/raw/ee1b3890e67bc30e372359db9ae3feebc9c928d8/readme-images/path.png)

### Download code as zip.

### Copy the path to the bot folder:

![caminho](https://github.com/mpcabete/bombcrypto-bot/raw/main/readme-images/address.png)

### Open the terminal.

Press the key windows + r and type "cmd":

![launch terminal](https://github.com/mpcabete/bombcrypto-bot/raw/main/readme-images/cmd.png)

### Navigate to the bot folder:
Type "cd" + path you copyed:

![cd](https://github.com/mpcabete/bombcrypto-bot/raw/main/readme-images/cd.png)

### Install project dependencies:

```
pip install -r requirements.txt
```

  
![pip](https://github.com/mpcabete/bombcrypto-bot/raw/main/readme-images/pip.png)

### Start the Bot:

```
python index.py
```

![run](https://github.com/mpcabete/bombcrypto-bot/raw/main/readme-images/run.png)


## Ajustando o bot

### Por que uns ajustes podem ser necessários?

O bot usa reconhecimento de imagem para tomar decisões e movimentar o mouse e
clicar nos lugares certos. 
Ele realiza isso comparando uma imagem de exemplo com um screenshot da tela do
computador.
Este método está sujeito a inconsistências devido a diferenças na resolução da
sua tela e de como o jogo é renderizado no seu computador comparado com o
meu(o que usei para pegar as imagens exemplo).
É provável que o bot não funcione 100% logo de cara, e que você precise fazer
alguns ajustes aqui ou ali.

### Threshold na config

O parâmetro “threshold” regula o quanto o bot precisa estar confiante para
considerar que encontrou a imagem que está procurando.
Este valor de 0 a 1 (0% a 100%).
Ex:

Um threshold de 0.1 é muito baixo, ele vai considerar que encontrou a imagem
que esta procurando em lugares que ela não está aparecendo ( falso positivo ).
O comportamento mais comum pra esse problema é o bot clicando em lugares
aleatórios pela tela. 


Um threshold de 0.99 ou 1 é muito alto, ele não vai encontrar a imagem que
está procurando, mesmo quando ela estiver aparecendo na tela. O comportamento
mais comum é ele simplesmente não mover o cursor para lugar nenhum, ou travar
no meio de um processo, como o de login.

### Substituição da imagem na pasta targets

As imagens exemplo são armazenadas na pasta “targets”. Estas imagens foram
tiradas no meu computador e podem estar um pouco diferente da que aparece no
seu. Para substituir alguma imagem que não esta sendo reconhecida
propriamente, simplesmente encontre a imagem correspondente na pasta targets,
tire um screenshot da mesma área e substitua a imagem anterior. É importante
que a substituta tenha o mesmo nome, incluindo o .png.

### Alguns comportamentos que podem indicar um falso positivo ou negativo

#### Falso positivo:

- Repetidamente enviando um herói que já esta trabalhando para trabalhar em um
  loop infinito.
  - Falso positivo na imagem “go-work.png”, o bot acha que esta vendo o botão
    escuro em um herói com o botão claro.

- Clicando em lugares aleatórios(geralmente brancos) na tela
  - Falso positivo na imagem sign-button.png

 
 #### Falso negativo:

- Não fazendo nada
	- Talvez o bot esteja tendo problemas com a sua resolução e não esta
    reconhecendo nenhuma das imagens, tente mudar a configuração do navegador
    para 100%.

- Não enviando os heróis para trabalhar
	- Pode ser um falso negativo na imagem green-bar.png caso a opção
    “select_heroes_mode” estiver como “green”.


### Algumas configuraçoes podem ser mudadas no arquivo config.yaml, nao se
### esqueça de reiniciar o bot caso mude as configuraçoes.
