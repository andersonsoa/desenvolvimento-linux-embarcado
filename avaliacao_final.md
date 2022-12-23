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
![image](https://user-images.githubusercontent.com/19675356/209243302-c2862675-3091-41b6-b147-80e31fdd958d.png)


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
![image](https://user-images.githubusercontent.com/19675356/209242570-7e6eb5e4-4c1f-4cc1-ad54-274af15194b8.png)

---

11. Crie a pasta palomakobabackup no home do usuário e copie o conteúdo da
pasta palomakoba, para dentro do /home/seu_usuario/palomakobabackup
![image](https://user-images.githubusercontent.com/19675356/209242872-2cfd11c5-c164-4a9a-bf41-897859ff7fd6.png)

---

12. Deletar os arquivos com extensão .txt
![image](https://user-images.githubusercontent.com/19675356/209242931-9129a772-e093-49be-b49e-fdeb06c8bc67.png)

---

13. Apagar a pasta exemplos que está dentro de palomakoba
![image](https://user-images.githubusercontent.com/19675356/209243400-dda03449-adf3-44df-b49b-88eb742f6e3b.png)

---

14. Entrar na pasta /home/seu_usuario/palomakoba
![image](https://user-images.githubusercontent.com/19675356/209243437-6299c07b-b81f-47e8-a0cf-2364acd2d267.png)

---

15. Renomear o arquivo numeros.txt para sequencia.txt
![image](https://user-images.githubusercontent.com/19675356/209243533-8c6fe813-3f71-4e8a-8df3-ab696cbc8d1e.png)

---

16. Listar todos os arquivos da pasta /bin e guardar essa lista em um arquivo
chamado “listabin.txt”
![image](https://user-images.githubusercontent.com/19675356/209243689-7939ddba-0cab-4a06-b020-055cb176ef3f.png)

---

17. Qual é o comando que apaga uma pasta vazia?
```bash
rmdir
```
---

18. Identifique a data atual e salve esta informação no diretório data em um
arquivo chamado “data-atual.txt”;
![image](https://user-images.githubusercontent.com/19675356/209244008-3e6509b2-ad0b-4137-b66b-28d28c13cf3e.png)

---

19. Crie um diretório usando seu primeiro nome como nome do diretório;
![image](https://user-images.githubusercontent.com/19675356/209244124-da6b79de-0850-40b0-9c82-ab8db0178932.png)

---

20. Renomeie o diretório com seu primeiro nome para seu nome-sobrenome;
![image](https://user-images.githubusercontent.com/19675356/209244205-5431cb24-6767-4197-b4a5-2ff56e482ff4.png)

---

21. Dentro do diretório nome-sobrenome, crie 3 diretórios: documentos, imagens
e musicas; *Use o comando mkdir, porém, estruture o comando para criar os
3 diretórios ao mesmo tempo.
![image](https://user-images.githubusercontent.com/19675356/209244353-74995b98-2588-4149-9675-45a832d7ce6d.png)

---

22. Liste o conteúdo do diretório raíz do Linux (o “/“) em forma de lista vertical e,
após, salve estas informações em um arquivo chamado “ls-root.txt”;
![image](https://user-images.githubusercontent.com/19675356/209244555-ff7f4a8f-2731-4bf8-b462-b6fcf5040d9a.png)

---

23. Copie os arquivos /etc/passswd, /etc/group e /etc/protocols para o diretório
documentos;
![image](https://user-images.githubusercontent.com/19675356/209244724-affd3a1c-94ed-4f29-b561-a4fca926fad2.png)

---

24. Conte o número de linhas e palavras do arquivo passwd;
![image](https://user-images.githubusercontent.com/19675356/209244961-efefa440-ccb2-4b51-b4b4-36b9ef5598d5.png)

---

25. Identifique o tipo do arquivo passwd; *Use o comando file.
![image](https://user-images.githubusercontent.com/19675356/209245218-ea4c48ff-eac3-45da-ac25-0f3cc7ec67cb.png)

---

26. Identifique somente o usuário root no arquivo passwd; *Use o comando cat e,
junto dele, o comando grep.
![image](https://user-images.githubusercontent.com/19675356/209245395-f347cb26-34a5-40a7-b40d-7221fbaacf7e.png)

---

27. Liste o conteúdo do diretório /home/seu_usuario/ em forma de lista, incluindo
seus subdiretórios e, após, salve estas informações em um arquivo chamado
“ls-exercicio-1.txt”; *Use o comando ls -lhR.
![image](https://user-images.githubusercontent.com/19675356/209245490-b327ac4e-5446-4bf5-9cc6-c1145d1d224b.png)

---

28. A seguinte estrutura de diretórios deve ser criada: “/ -> home -> seu_usuario
-> modulo6 -> principais -> comandos”. Como podemos criar tal estrutura
com apenas um comando?
![image](https://user-images.githubusercontent.com/19675356/209245740-02096981-9d30-46ad-8c76-4c80b3fe6033.png)

---

29. Qual comando irá exibir as últimas linhas de um arquivo
/var/log/cups/access_log?
```bash
tail /var/log/cups/access_log
```
---

30. Escreva em um arquivo a quantidade de arquivos com formato pdf salvos em
um diretório.
![image](https://user-images.githubusercontent.com/19675356/209246244-4cf6b536-8061-4a33-a396-89b04097a1cb.png)

---

31. Especifique o comando que é utilizado para dar permissão de leitura, escrita
e execução de um arquivo a um usuário. E se fosse apenas leitura e escrita,
qual seria o comando?
```bash
chmod 700 prog.sh # leitura, escrita e execução
chmod 600 prog.sh # leitura e escrita
```
---

32. Faça um bash shell script chamado vars para experimentar com variáveis.
Explique o funcionamento do script. 
```bash
#!/bin/bash
# variaveis de ambiente
echo $PATH
echo $USER $HOME
# pode-se ver todas as variáveis do ambiente com o comando env | less
#variaveis locais
ola="bom dia"
echo "$ola Paulo"
echo "$olaPaulo" $Texto Pegado a variavel ..
echo "${ola}Paulo" #proteger a variável com as chavetas
mesg="$ola $USER"
echo $mesg
# input
echo "Introduza qualquer Coisa" ; read var
echo "Introduziu $var"
# execução
data=`date`
echo $data
info='echo $HOME ; echo " estamos em "; pwd'
echo $info
# contas
x=1
let x=x*2+3
echo "x=$x"
let x--
echo "x=$x"
#variaveis especiais
echo "Numero de Arguments para este script $#"
echo "Todos os argumentos para este script $*"
echo "O primeiro $1 e segundo $2 argumentos"
echo "O nome deste ficheiro $0"echo "O Processo ID deste script $$"
echo "Exit status do comando anterior $"”
```
![image](https://user-images.githubusercontent.com/19675356/209247145-9a9853ca-3cca-4e4b-8fae-3dac3cc91e08.png)

O shellscript imprime na tela duas variaveis de ambiente ($PATH e $HOME), após isso ele cria uma variavel chamada 'ola' com o valor 'bom dia' e imprime esta variavel junto com a string paulo e depois com o $USER (usuario logado no momento). Apos tudo isso o script pede que o usuario entre com dados e imprime eles logo em seguida. Depois define mais algumas variaveis e faz algumas contas com as mesmas e exime a data de hoje. Tambem conta a quantidade de argumentos informados na execução do script

---

33. Execute o script abaixo e explique o que ele faz. Qual a saída do programa?
```bash
#!/bin/bash
# mywho verão inicial

echo "Introduza Nome (userid) da Pessoa " ; read nome

echo "Procurando "$nome
# comando who seguido por um filtro
who | grep $nome

# Nota : exit status of previous comand is stored in $?
# Default is valor 0 indicates sucess.

if [ $? -eq 0 ] ; then
echo "$nome Foi Encontrado "
else 
echo "$nome Não Foi Encontrado "
fi
echo
```
![image](https://user-images.githubusercontent.com/19675356/209247746-fa677c21-355e-4cfb-9e24-72b1824d7fb1.png)

Pede que o usuario informe um nome e verifica se o nome informado e um usuario logado no sistema e apos isso retorna para o usuario se encontrou ou nao o usuario

---

34. Faça um script que imprima quantos processos estão atualmente em
execução na sua máquina. Use os comandos ps e wc para isso.
```bash
# !/bin/bash

# Script que conta a quantidade de processos rodando atualmente.

TOTAL_DE_PROCESSOS=`ps -a | wc -l`

echo "Neste momento existem $TOTAL_DE_PROCESSOS processo(s) em execução"
echo 
```
![image](https://user-images.githubusercontent.com/19675356/209248691-0514f538-f3ec-4d35-af15-58c752f18977.png)

---

35. Crie um script para mostrar (cat) todos os usuários cadastrados no sistema
(/etc/passwd/) ordenados em ordem alfabética.
```bash
  GNU nano 4.8                                  user-count.sh                                              
#!/bin/bash

# Conta os usuarios no sistema e ordena por ordem alfabetica.

TOTAL=`cat /etc/passwd | wc -l`

echo "Lista de usuarios do sistema"
echo
cat /etc/passwd | cut -d: -f1 | sort
echo "----------------------------------"
echo "Exite $TOTAL usuario(s) registrados no sistema"
echo
```
![image](https://user-images.githubusercontent.com/19675356/209249498-016b33cc-1588-474e-8f0f-0fcd76021af2.png)

---

36. Um dos parâmetros de cada linha do arquivo (/etc/passwd/) é o shell usado
pelo usuário (o sétimo campo). Escreva um programa capaz de listar todos
shells únicos existentes no passwd. O comando uniq pode ser útil.
```bash
#!/bin/bash

# Lista os caminhos do shell usado por cada usuario

cat /etc/passwd | cut -d: -f7 | sort -u

TOTAL=`cat /etc/passwd | cut -d: -f7 | sort -u | wc -l`

echo 
echo "$TOTAL shels diferentes"
```
![image](https://user-images.githubusercontent.com/19675356/209250075-ca294b59-3169-4500-b503-9f513f289328.png)

---

37. Criar um programa que mostre o espaço utilizado pelos arquivos dentro de
cada diretório da sua conta no sistema, colocando em ordem numérica o
resultado. Use os comando du e sort.
```bash
#!/bin/bash

# Lista os arquivos em cada diretorio seu junto com o espaço comsumido

du -h | sort

echo
```
![image](https://user-images.githubusercontent.com/19675356/209250624-c3304b0b-bcf6-442d-a000-f3281a64cfa3.png)

---

38. Qual a saída do script abaixo? Explique o funcionamento!
```bash
#!/bin/bash
a=9
b=2
[ $a -lt $b ] && echo $ ( (a/b) )
echo "FIM"
```
define duas variaveis ('a' e 'b') e verifica se $a é menor que $b, caso seja ele imprime o resultado da divisao de $a por $b

---

39. Qual a saída do script abaixo? Explique o funcionamento!
```bash
#!/bin/bash
x=0
while [ $x -le 2 ]
do
echo valor: $x
((x++))
done
```
Imprime o valor atual de $x até que ele seja maior que 2. Ex:
0, 1, 2 --end--

---

40. Qual a saída do script abaixo? Explique o funcionamento!
```bash
#!/bin/bash
echo "Resultado..."
for i in {0..12..2}
do
a=$(($i%3))
if [ $a -eq 0 ]
then
echo "Alo valor $i"
fi
done
```
percore de 0 a 12 de 2 em 2 (somente os pares), cria uma variavel $a que é igual ao modulo de $i por 3 (verifica se o numero e divisivel por 3), se for imprime "Alo valor $i"

