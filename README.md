# Gerando SSH e subindo no github

1)Abra o git bash e digite:

ssh-keygen -t ed25519 -C seuemail

2)Digite uma senha para a chave.

A chave estará na pasta /c/Users/seuusuario/.ssh/id_ed25519.pub

3)Vá até o diretório e digite cat id_ed25519.pub para visualizar o conteúdo da chave pública. Copie o conteúdo e cole na configuração de nova chave dentro da plataforma do github (web).

<img src="https://github.com/fpreviatti/github-gerando-ssh/blob/main/chave.png" width="400px" height="auto">

# Ativando o SSH Agent

4)No git bash digite:

eval $(ssh-agent -s)

5)Em seguida digite o seguinte comando para adicionar a chave:

ssh-add id_ed25519     <= (passar a chave privada, não a pública .pub)

6)E por fim digite a senha da chave (gerada no passo 2).

# Clonando repositórios após ter configurado a chave SSH

Ao acessar um projeto no github escolha a opção SSH.

<img src="https://github.com/fpreviatti/github-gerando-ssh/blob/main/ssh.png" width="400px" height="auto">

e ao efetuar o git clone com este valor, será preciso informar a chave SSH
