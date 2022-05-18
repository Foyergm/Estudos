# O que é  Git?

### Git é um sistema de controle de versão do arquivo. Com ele podemos desenvolver projetos de qualquer pessoa, e qualquer pessoa pode contribuir com o código.

# <br />Como eu posso ter o Git?

### Você precisa entrar no site do [Git](https://git-scm.com) e fazer o download do programa. Isso fará com que seja instalado o Git Bash, com ele, conseguimos fazer os comandos do Git.

# <br />Como posso fazer um repositório?

### Simples, você precisa abrir o CMD, depois procurar a pasta onde você quer fazer seu repositório, e criar uma pasta ".git".
### Para isso, você vai usar alguns comandos:

~~~html
cd [Nome do local onde do repositorio]
~~~

### <br />Depois que você realizar esse processo, está na hora de criar um arquivo ".md", que é o "README.md". Esse arquivo faz com que possa escrever e documentar sobre o projeto, e o que você está pensando e planejando fazer.

# <br />Mas como eu adiciono e salvo esses arquivos?

### Esses arquivos para envio são chamados de "commit", eles salvam o projento como ele está naquele momento. Para "commitar", é necessário adicionar um repositório vazio com o comando abaixo, para começar um repositório novo.

~~~html
git init
~~~

### Caso você tenha criado um repositório no GitHub, então, precisamos puxar os arquivos de lá, para a nossa máquina, para isso, primeiro precisamos associar os 2 projetos (o do seu projeto com o do GitHub):

~~~html
git remote add origin "Link do repositório no GitHub"
~~~

### Para poder puxar para sua maquina o repositório do Github (Em uma atualização recente, não se usa mais "master" em muito dos casos, pois, o github está criando seu repositorio no "main"). 

~~~
git pull origin main
~~~

## <br /> **Mas meu branch ainda está master, o que eu faço?**

### Você vai precisar trocar o branch no seu repositório para main, para sempre mandar os seus arquivos no repositório main do GitHub.

~~~
git checkout -b "main"
~~~

###  _Obs. Esse comando é utilizado para poder checar se existe um branch chamado "main", se não tiver, o git faz uma alteração no branch e coloca ele como "main"._

## <br />**Depois disso, você ira seguir os proximos passos.**

### <br /> Para saber como está o status do arquivo.

~~~html
git status
~~~

### Depois disso, é só adicionar o arquivo no repositório.

~~~html
git add [Nome do arquivo]
~~~

### <br />Depois disso, você usar o seguinto comando para "commitar":

~~~html
git commit -m "comentário sobre esse commit"
~~~

### <br />Agora, com os arquivos adicionados e salvos, é preciso criar um repositório no GitHub.

# <br />Como eu faço para criar um repositório no GitHub?

### Para isso, você precisa entrar na sua conta do GitHub, e clicar no "+" do lado esquerdo da sua foto de perfil, e cliar em "New repository". Nessa etapa você começa a criar seu repositório onde vão ficar seus arquivos.

### Primeiramente, escolha um **título** para o seu repositório, logo abaixo, coloque uma **descrição** do seu prejeto. Existem 2 opções abaixo da descrição, que são, **"Pública"** e **"Privada"**, a opção pública faz com que o seu repositório fica visível para todos, já o privado, apenas quem você escolheu pode ver esse commit.

### É sempre bom ter o arquivo **"README.dm"** habilitado, pois com ele, você consegue documentar e escrever sobre seu projeto.

# <br />Como faço para colocar meu projeto no GitHub?

### Depois de ter feito o repositório no GitHub, você vai precisar copiar o link HTTPS, como mostra a foto abaixo.
![HTTPS](https://lh3.googleusercontent.com/pw/AM-JKLW8jD7jxsj9VgfIOQFBz4YXs27R_tWh1A9_95YPyS99PLahVCaO_H2QKVBHGDw_O3CZzaFQVqgy7lr3pZm5ide9nodAz163UsNCrU9DdhVBFB3HDIGl3EZH02anO9sIrU6B2yYIFIo4RnEa3XF5nquK=w886-h71-no?authuser=0)

### <br />Agora, vamos voltar no terminal para mandar o nosso projeto com o HTTPS, para isso, utilizaremos o código:

~~~html
git remote add origin 'link do HTTPS'
~~~

### <br />**Caso esse comando não funcione, use o comando abaixo.**

~~~html
git remote set-url origin 'link do HTTPS'
~~~

### <br />Se não apareceu nada, quer dizer que deu certo, para verificar se realmente foi adicionado, use o código:

~~~html
git remote show origin -n
~~~

### <br />Seguindo caso conseguiu fazer sem ter mais nenhum erro, iremos usar um comando para mandar o projeto do seu computador direto para o GitHub. Logo em seguida, mostrara uma mensagem informando o envio.
~~~html
git push origin master
~~~

### <br />E pronto, seu projeto foi mandado para o GitHub e está visível para todos (ou não) e poderá fazer o que precisar a partir de agora.

# <br />Mas, e se eu precisar adicionar algo novo?

### <br />Bem, para isso, usaremos uma sequência de comandos para fazer isso.

~~~html
git status
~~~

~~~html
git add .
~~~
### **Obs. O ponto significa que você ira adicionar todas as novas modificações.**
#
~~~html
git status
~~~

~~~html
git commit -m "algum comentário"
~~~

~~~html
git push origin master
~~~

### <br />E pronto, você adicionou as novas modificações do seu projeto, mesmo sendo comandos simples, é algo muito importante para o começo e para você conseguir colocar seus projetos em um local seguro.