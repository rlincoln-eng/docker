# 🐋 Criando um dockerfile do zero

O dockerfile é o arquivo de instruções de criação de imagem (Sistema Operacional, Pacotes, cópia de arquivos e até mesmo estabelecer ponto de montagem de volumes).

1. Crie um arquivo sem extensão, neste arquivo será informado a configuração do que é esperado no container que irá utilizar essa imagem. No exemplo abaixo será criada uma imagem com base Ubuntu + Ferramenta Terraform + Instalação do AWS CLI.
2. Abra o Prompt de comando, navegue até a pasta onde o arquivo foi criado e salvo e execute o comando:<br>
    <b>docker build -t lab-terraform-image:lab01 .  </b>
3. Após a criação da imagem é necessário criar o container que irá utilizar essa imagem. Para esta etapa use o comando abaixo:<br>
   <b>docker run -dit --name tf-lab -v ./lab01:/lab1 lab-terraform-image:lab01 /bin/bash </b>
