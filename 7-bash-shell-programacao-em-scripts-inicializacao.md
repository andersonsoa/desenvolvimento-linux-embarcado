# Desenvolvimento Linux Embarcado

## 7. Bash - Shell, Programação em Scripts, Inicialização

### 7.1. Interpretadores de Comando7.1. Interpretadores de Comando

```bash
cat /etc/passwd | cut -f 7 -d: | sort | uniq -c
```
![image](https://user-images.githubusercontent.com/19675356/209022088-86d312ce-013f-49b0-9466-53c01aff7665.png)


```bash
/bin/false
echo $? # imprime o retorno do ultimo comando
/bin/true
echo $?
```
![image](https://user-images.githubusercontent.com/19675356/209022186-7512f85d-934f-4b46-a1be-3461246f6314.png)


```bash
/usr/sbin/nologin
echo $?
```
![image](https://user-images.githubusercontent.com/19675356/209022276-28de5107-17a8-4d56-b665-75f39007c993.png)


```bash
cat /var/log/auth.log | grep nologin | tail -1
```
![image](https://user-images.githubusercontent.com/19675356/209022332-28874587-a8cf-4e39-8e04-c4422b12e6b9.png)

### 7.2. Atalhos no Terminal

```bash
add # tab x2
```
![image](https://user-images.githubusercontent.com/19675356/209022479-0d1686c2-4a47-442a-b450-06e34245f1fb.png)


```bash
cat /etc/add # tab x2
```
![image](https://user-images.githubusercontent.com/19675356/209022584-b60c21c3-acbe-45ea-b8ad-8120b60cc74c.png)

### 7.3. Scripts Bash

```bash
head -1 /etc/init.d/cron
```
![image](https://user-images.githubusercontent.com/19675356/209022790-9d14ecac-f09d-411e-89a1-20bce28cfef2.png)


```bash
nano HelloWorld.sh
# #!/bin/bash
# echo "Hello World"
```
![image](https://user-images.githubusercontent.com/19675356/209022970-fe8c9eaa-b0c8-4ae0-a723-1500381a4f3d.png)


```bash
chmod 700 HelloWorld.sh
./HelloWorld.sh
```
![image](https://user-images.githubusercontent.com/19675356/209023028-82586a9c-d5bd-453d-bfcb-aa71e1883d09.png)


```bash
nano HelloWorld.sh
# #!/bin/bash
#
# PERSON="Barney Calhoun"
# echo "Hello, $PERSON!"
```
![image](https://user-images.githubusercontent.com/19675356/209023289-6413004b-48f4-4c21-80c3-112ab4a03004.png)


```bash
nano HelloWorld.sh
```
![image](https://user-images.githubusercontent.com/19675356/209023604-ca869e9c-3846-4741-b19c-fc83e04b8f73.png)
![image](https://user-images.githubusercontent.com/19675356/209023689-3d47e065-3248-400b-b6a7-5356c52bd969.png)


```bash
./HelloWorld.sh
```
![image](https://user-images.githubusercontent.com/19675356/209023731-d8839ba5-2782-4b17-8270-b85b31561eba.png)


```bash
echo "5" | ./HelloWorld.sh
echo "0" | ./HelloWorld.sh
echo "-5" | ./HelloWorld.sh
```
![image](https://user-images.githubusercontent.com/19675356/209023818-993be920-a084-402e-86ba-501c7093e26c.png)


```bash
while [ 1 ] ; do
echo "Loop infinito"
sleep 1
done
```
![image](https://user-images.githubusercontent.com/19675356/209023966-494d9a9d-7dd7-4327-9fcb-bbd137a3284e.png)


```bash
grep -r "^#\!/bin/sh" /etc 2> /dev/null
```
![image](https://user-images.githubusercontent.com/19675356/209024110-4a58e0ab-2703-4004-adf0-56a8312711de.png)

### 7.4. Inicialização do Bash

```bash
nano ~/.bashrc
```
![image](https://user-images.githubusercontent.com/19675356/209024311-787a7dad-c932-4455-b140-5a01a0b28638.png)

```bash
source ~/.bashrc
```
![image](https://user-images.githubusercontent.com/19675356/209024456-d151cdff-3074-4cc1-825d-a74fd2eddc0a.png)


```bash
nano ~/.bashrc
# echo "Bash iniciado!"
source ~/.bashrc
```
![image](https://user-images.githubusercontent.com/19675356/209024571-de7f5a44-a3ab-4d74-b446-e88fbd1db7b2.png)
![image](https://user-images.githubusercontent.com/19675356/209024585-41ed20d3-7b5f-48be-af34-fb9bd71e5cb6.png)


```bash
sudo apt install fortune cowsay
```
![image](https://user-images.githubusercontent.com/19675356/209024780-ae6e5ee9-786c-4c31-9422-5269f9e650d1.png)


```bash
nano ~/.bashrc
source ~/.bashrc
```
![image](https://user-images.githubusercontent.com/19675356/209025398-d95340d8-d765-4c77-9eb4-dd77b463516c.png)
![image](https://user-images.githubusercontent.com/19675356/209025571-94f3be86-e304-4661-8fef-57237c7ccee0.png)
