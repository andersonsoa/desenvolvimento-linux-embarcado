# Avaliação Final
---
1. Descubra para que servem os comandos abaixo e liste suas opções de uso
mais comuns. Exemplo: * ls função: serve para listar os arquivos do diretório
corrente uso mais comum: $ ls -la, que lista todos os arquivos do diretório
corrente, incluindo arquivos ocultos, se houver, no formato de lista.

* cal 
  - Exibe um calendário simples no terminal, por padrão ele exibe o mes atual, ao utilizando o argumento '-y' é exibido na tela o calendário do ano inteiro Ex: cal -y  

* date
  - Exibe a data atual no terminal do usuário, é possivel tambem setar a data do computador e formatar a saida. Para alterar a data do sistema utiliza-se o argumento --set Ex: date --set="<DATA_VALIDA>"

* clear
  - Serve para limpar o terminal e exclui o buffer atual fazendo com que seja impossivel rolar a tela para cima e ver os comandos digitados anteriormente, para preservar o buffer utiliza-se o argumento '-x' Ex: clear -x

* exit
  - Exit encerra o bash que esta rodando atualmente, é possivel passar um argumento que é retornado quando o fechamento do bash e concluído, esse retorno e tratado como o código referente ao fechamento. Ex: exit 110 (110 sera retornado para o programa que executou esse bash) 

* uname
  - Exibe o nome da sua distribuição linux, porem é possivel passar varios argumentos para exibir informações adicionais, como o argumento -a que exibe todas as informações do sistema. Ex: uname -a

---
2. Usando o comando adequado:

- descubra qual o seu diretório atual ao logar em um terminal Linux
```bash
pwd
```
![image](https://user-images.githubusercontent.com/19675356/209035546-8b888036-47d2-436b-8d8b-ead05b46d6d7.png)

- Navegue até a pasta /home/seu_usuario
```bash
cd ~
```
![image](https://user-images.githubusercontent.com/19675356/209035617-143864f3-cb94-475f-a90b-5c553480fab7.png)

- liste todos os arquivos da pasta /home/seu_usuario
```bash
ls
```
![image](https://user-images.githubusercontent.com/19675356/209035810-eb9b1a5a-061b-48bc-a71a-7120db956f4b.png)

- navegue até a pasta /bin
```bash
cd /bin
```
![image](https://user-images.githubusercontent.com/19675356/209035859-93f2c3e0-3133-4660-a710-9d8974dcd7d4.png)

- certifique-se de qual diretório você se encontra
```bash
pwd
```
![image](https://user-images.githubusercontent.com/19675356/209035885-3c3bc912-e57d-47a8-8aad-ee5af5c8494a.png)

- a partir do diretório corrente, liste o conteúdo da pasta /etc
```bash
ls -la /etc
```
![image](https://user-images.githubusercontent.com/19675356/209036076-298aedc1-b962-4ede-9bac-36245277b5c0.png)

- agora liste os arquivos da pasta atual
```bash
ls -la
```
![image](https://user-images.githubusercontent.com/19675356/209036163-9889ee68-87cb-4ffe-ba9b-574e41e8f1a3.png)

- volte ao diretório home/seu_usuario
```bash
cd ~
```
![image](https://user-images.githubusercontent.com/19675356/209036199-65e694fc-7e27-49c7-a3fc-e7eed3623987.png)

- crie uma pasta com o seu nome
```bash
mkdir anderson
```
![image](https://user-images.githubusercontent.com/19675356/209036250-68dddcee-b5a3-43ba-b864-b36b2d25437d.png)

- crie um arquivo texto dentro da pasta que você criou com o seu nome
```bash
touch /anderson/anderson.txt
```
![image](https://user-images.githubusercontent.com/19675356/209036422-cbc27bb1-6cbd-4297-aff2-9b625cd36c9d.png)

- copie este arquivo para a pasta /home/seu_usuario.
```bash
cp /anderson/anderson.txt .
```
![image](https://user-images.githubusercontent.com/19675356/209036546-cf034e2d-75f4-4833-93e1-ae65a23642e7.png)

- renomeie o arquivo criado na pasta home/seu_usuario
```bash
mv anderson.txt renomeado.txt
```
![image](https://user-images.githubusercontent.com/19675356/209036671-26d8d31e-cd3b-42c4-b0e8-b0876c521fd7.png)

- mova este arquivo que está na pasta que você criou com o seu nome
para a pasta home/seu_usuario
```bash
mv /anderson/anderson.txt .
```
![image](https://user-images.githubusercontent.com/19675356/209036769-016e62c1-d8ef-438f-8ea7-92d553138962.png)

- exclua o diretório que você criou com o seu nome
```bash
rmdir anderson/
```
![image](https://user-images.githubusercontent.com/19675356/209036907-8b62c24c-d511-40af-994a-031ab619ab46.png)

---

3. Criar a seguinte estrutura de diretórios dentro do /home/seu_usuario:
- ./palomakoba
- ./projetos
- ./palomakoba/exemplos
![image](https://user-images.githubusercontent.com/19675356/209037263-f8d19f7f-7265-4231-8320-cf6006d41890.png)

---

4. Entrar na pasta palomakoba.
![image](https://user-images.githubusercontent.com/19675356/209037303-3eeba096-67d4-4e5b-bfea-2544c0753a25.png)

---

5. Criar um arquivo chamado “numeros.txt”, usando o comando echo, contendo os seguintes números: 10 100 50 25 1 2
![image](https://user-images.githubusercontent.com/19675356/209037363-ee6cf8f9-7260-4ca4-beec-e2282d4006e8.png)

---

6. Duplicar o arquivo numeros.txt para numeros1.txt e numeros2.txt
![image](https://user-images.githubusercontent.com/19675356/209037607-8bcac6a1-a388-41c8-9388-16d593a97ad5.png)

---

7. Copiar os arquivos com extensão .txt para a pasta Documentos no home do
usuário (/home/seu_usuario).
![image](https://user-images.githubusercontent.com/19675356/209037980-10b9a1ff-47d9-47d2-b330-69db0e310832.png)

---

8. Exibir todos os arquivos com seus detalhes ( permissões de acesso, data,
hora de criação, tamanho)
![image](https://user-images.githubusercontent.com/19675356/209038182-f9223f69-1d01-496c-bfca-c353816b8735.png)

---

9. Mudar a permissão de acesso do arquivo numeros.txt para –rwxr-xr-x
![image](https://user-images.githubusercontent.com/19675356/209038473-1508bacb-9432-4629-bc0b-c56109e3fbca.png)

---

10. Mudar a permissão de acesso do arquivo numeros.txt para -rw-r—r--

---

11. Crie a pasta palomakobabackup no home do usuário e copie o conteúdo da
pasta palomakoba, para dentro do /home/seu_usuario/palomakobabackup

---

12. Deletar os arquivos com extensão .txt

---

13. Apagar a pasta exemplos que está dentro de palomakoba
14. Entrar na pasta /home/seu_usuario/palomakoba
15. Renomear o arquivo numeros.txt para sequencia.txt
16. Listar todos os arquivos da pasta /bin e guardar essa lista em um arquivo
chamado “listabin.txt”
17. Qual é o comando que apaga uma pasta vazia?
18. Identifique a data atual e salve esta informação no diretório data em um
arquivo chamado “data-atual.txt”;
19. Crie um diretório usando seu primeiro nome como nome do diretório;
20. Renomeie o diretório com seu primeiro nome para seu nome-sobrenome;
21. Dentro do diretório nome-sobrenome, crie 3 diretórios: documentos, imagens
e musicas; *Use o comando mkdir, porém, estruture o comando para criar os
3 diretórios ao mesmo tempo.
22. Liste o conteúdo do diretório raíz do Linux (o “/“) em forma de lista vertical e,
após, salve estas informações em um arquivo chamado “ls-root.txt”;
23. Copie os arquivos /etc/passswd, /etc/group e /etc/protocols para o diretório
documentos;
24. Conte o número de linhas e palavras do arquivo passwd;
