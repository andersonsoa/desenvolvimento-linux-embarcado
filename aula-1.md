# Desenvolvimento Linux Embarcado

## 1. Introdução ao Linux, Linha de Comando e Arquivos

### 1.3. Sobre o Terminal

```bash
ls
```
![image](https://user-images.githubusercontent.com/19675356/207481885-31b09a80-6932-4ff8-8be5-9707ea43e8ce.png)

```bash
pwd
```
![image](https://user-images.githubusercontent.com/19675356/207482032-c2eb0eb8-d0dc-4a1f-a011-815629015fc0.png)

```bash
cat user1.json
```
![image](https://user-images.githubusercontent.com/19675356/207482277-2a0ac5b4-d958-47f2-82b3-f2a63c743b37.png)

### 1.4. Listando Arquivos

```bash
ls -l /bin/ls
```
![image](https://user-images.githubusercontent.com/19675356/207482662-fcd2a680-1019-411c-b1fa-1134793addbc.png)

```bash
ls /etc/host*
```
![image](https://user-images.githubusercontent.com/19675356/207482734-084ebecf-feb8-4f6f-a787-1b1b06dc97b5.png)

```bash
ls -l /etc/host*
```
![image](https://user-images.githubusercontent.com/19675356/207482834-57ea11ba-f139-4b8f-82c3-eb0e02405869.png)

```bash
ls -lh /bin/ls
```
![image](https://user-images.githubusercontent.com/19675356/207482944-8820f028-b4ba-481c-8974-5f8e6ea7a429.png)

```bash
ls -la
```
![image](https://user-images.githubusercontent.com/19675356/207483020-a6ca2410-8f3f-42f9-8aa2-ff55031907eb.png)

### 1.5. Documentação dos Comandos

```bash
man ls
```
![image](https://user-images.githubusercontent.com/19675356/207483308-a1b3f5bb-2448-4391-b92e-89530f0164fd.png)

```bash
tldr ls
```
![image](https://user-images.githubusercontent.com/19675356/207483807-8f2cb43f-97c9-41e3-97e0-6c487df03ccc.png)

### 1.6. Navegando nos diretórios

```bash
cd /var/log
pwd
```
![image](https://user-images.githubusercontent.com/19675356/207484180-080bd81f-695c-42e0-91f0-260eb379b2ce.png)

```bash
cd ~
pwd
```
![image](https://user-images.githubusercontent.com/19675356/207484684-66e7b7d3-7a37-491f-ad99-b99cfec9eaba.png)

```bash
cd /var/log
cd
pwd
```
![image](https://user-images.githubusercontent.com/19675356/207484831-21848124-8db8-4546-a9f3-0f5ca20ba76d.png)

```bash
cd .
pwd
```
![image](https://user-images.githubusercontent.com/19675356/207485006-9977db31-4a9f-4f9d-8871-feadf9c45c95.png)

```bash
cd ..
pwd
```
![image](https://user-images.githubusercontent.com/19675356/207485080-78f4003a-2892-445f-ae56-0af01e7cebee.png)

```bash
cd -
pwd
```
![image](https://user-images.githubusercontent.com/19675356/207485167-05c29e73-39ab-4c75-a7cf-e95a670c4856.png)

### 1.7. Lendo Arquivos
```bash
cat /etc/hostname
```
![image](https://user-images.githubusercontent.com/19675356/207485414-88de4370-6918-43a3-a11f-b8b53099ce96.png)

```bash
more /etc/login.defs
```
![image](https://user-images.githubusercontent.com/19675356/207485599-f772df48-2537-42d3-9b17-f9525eb89d2d.png)

```bash
head -5 /etc/passwd
```
![image](https://user-images.githubusercontent.com/19675356/207485820-1b4f022a-0cc0-4a9a-a07b-8ea2376963d5.png)


```bash
tail -5 /etc/passwd
```
![image](https://user-images.githubusercontent.com/19675356/207485910-059bab5d-9a6d-4085-8358-f47cd1aaaa1f.png)
