# Criação de site estático no AWS S3

<img width="976" height="371" alt="image" src="https://github.com/user-attachments/assets/421f92e9-eacc-44f4-8737-a11093677b64" />

## Objetivos de Ensino

Exercitar os seguintes conceitos:

1- Criar e configurar um bucket S3 para hospedagem de site estático.

2- Fazer upload de arquivos estáticos (HTML e imagem).

3- Configurar políticas de acesso e permissões seguras no S3.

4- Personalizar conteúdo dinâmico simples (nome do aluno).

5- Limpar recursos para evitar custos.

## Enunciado

Neste laboratório, você aprenderá como publicar um site estático simples na AWS, usando apenas o serviço Amazon S3.
O objetivo é criar uma página HTML personalizada, usando como plano de fundo uma imagem , onde o aluno poderá inserir o seu nome em destaque.
Você vai praticar conceitos importantes de armazenamento, permissões e publicação de arquivos estáticos em nuvem.

Sua organização está treinando novas equipes para hospedar páginas institucionais em nuvem de forma econômica, escalável e segura.

## Diagrama de arquitetura
<img width="1005" height="600" alt="image" src="https://github.com/user-attachments/assets/4c11181c-0ee4-4fb6-bf0d-6af7a35f14d0" />



 Atividades

Tarefa 1: Baixar os arquivos do Lab

Baixe o arquivo HTML modelo:

Baixar index.html

Tarefa 2: Personalizar o arquivo HTML

Abra o arquivo index.html em um editor de texto (por exemplo, Notepad, VS Code).

Localize onde está escrito:

Arquiteto Cloud [seu nome]

Substitua [seu nome] pelo seu nome completo.

Salve o arquivo.

Tarefa 3: Criar o bucket no Amazon S3

* No console da AWS, acesse S3.
  
* Clique em Create bucket.
  
Preencha:

* Bucket name: ex: site-estatico-seunome
* Region: escolha sua região (ex: us-east-1)
* Clique em Create bucket.

  
Tarefa 4: Fazer upload dos arquivos para o bucket

* Clique no nome do bucket criado.
* Clique em Upload > Add files.
* Selecione os arquivos index.html e faculdade-xpe.png.
* Clique em Upload.

  
Tarefa 5: Ativar hospedagem de site estático

* No bucket, vá em Properties.
* Role até Static website hosting e clique em Edit.
* Marque Enable (Ativar).
* Em Index document, coloque: index.html
* Clique em Save changes.
* Copie o endpoint do site que aparecerá.

  
Tarefa 6: Configurar permissão pública

No bucket, vá em Permissions > Bucket Policy > Edit.

Cole a Bucket Policy neste repositório, trocando site-estatico-seunome pelo nome do seu bucket:
