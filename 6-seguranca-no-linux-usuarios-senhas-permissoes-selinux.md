# Desenvolvimento Linux Embarcado

## 6. Segurança no Linux, Usuários, Senhas, Permissões, SELinux

### 6.1. Usuários no Linux

```bash
tail -5 /etc/passwd
```
![image](https://user-images.githubusercontent.com/19675356/208793765-e33e6e10-27ca-493a-94f3-09082ce292f2.png)

```bash
head -1 /etc/passwd
```
![image](https://user-images.githubusercontent.com/19675356/208794064-66596cd4-ad4e-42a5-a762-4e94fbd8dc2b.png)

```bash
cat /etc/passwd | grep "mail\|www-data\|syslog\|sshd"
```
![image](https://user-images.githubusercontent.com/19675356/208794308-1e09ebfd-4562-474e-b9ca-1e7e6a6a4f1c.png)

```bash
cat /etc/passwd | wc -l
```
![image](https://user-images.githubusercontent.com/19675356/208794444-f8f28a6a-01ff-4c59-b4cb-a60202297fb0.png)

```bash
sudo adduser laboratorio6
```
![image](https://user-images.githubusercontent.com/19675356/208794698-c0eaeb81-5ad6-4cb1-addc-17548393e12d.png)

```bash
cat /etc/passwd | grep "laboratorio6"
```
![image](https://user-images.githubusercontent.com/19675356/208794773-884b1375-8f97-4af1-a7de-cf2d2c54b2ba.png)

### 6.2. Senhas no Linux

```bash
cat /etc/shadow
```
![image](https://user-images.githubusercontent.com/19675356/208795184-3fe9b876-eae6-416c-aeed-510738a6bfeb.png)

```bash
sudo cat /etc/shadow
```
![image](https://user-images.githubusercontent.com/19675356/208795090-2d7fc104-273b-4c18-bbb7-4a1c11b57e50.png)

```bash
sudo cat /etc/shadow | grep "laboratorio6"
```
![image](https://user-images.githubusercontent.com/19675356/208795306-ae4f6c7b-0876-46b6-9487-44a27a66a270.png)

```bash
echo -n "ncc1701" | mkpasswd --stdin --method=sha-512 --salt=".33aS4lt030sd"
```
![image](https://user-images.githubusercontent.com/19675356/208795978-9193da0a-777b-472c-9fce-901ace84fe12.png)

```bash
export HISTFILE=/dev/null
```
![image](https://user-images.githubusercontent.com/19675356/208796251-d9efbfd2-e9b2-40fd-89ba-70dad02512ee.png)

- Desafio
![image](https://user-images.githubusercontent.com/19675356/208796582-2121428b-50fc-468e-8ab8-c4b09f5ae058.png)

### 6.3. Grupos

```bash
cat /etc/group
```
![image](https://user-images.githubusercontent.com/19675356/208796791-45d2854e-dcc7-4e56-bca2-4297e5a1615c.png)

```bash
head -3 /etc/group
```
![image](https://user-images.githubusercontent.com/19675356/208796852-c22462df-a722-4789-9cce-613cbf7b8004.png)

```bash
cat /etc/group | grep "^laboratorio6:"
```
![image](https://user-images.githubusercontent.com/19675356/208796955-15a3988c-2fd4-4332-8132-bd1421a612e9.png)

```bash
cat /etc/group | grep "^adm:"
```
![image](https://user-images.githubusercontent.com/19675356/208797078-2cf7cd34-9607-4e3d-9729-643d71cae28f.png)

```bash
sudo addgroup palomakoba-lab6 
```
![image](https://user-images.githubusercontent.com/19675356/208797304-e716af0c-9045-4645-8fbb-c6aaa422a12f.png)

```bash
cat /etc/group | grep "^palomakoba-"
```
![image](https://user-images.githubusercontent.com/19675356/208797402-b5cebf81-07c7-4faf-8146-b0ad5ea53411.png)

```bash
sudo usermod -a -G palomakoba-lab6 laboratorio6 
cat /etc/group | grep "^palomakoba-"
```
![image](https://user-images.githubusercontent.com/19675356/208797570-d131dcae-4580-476d-bce3-6dadb8a3e78a.png)

```bash
groups laboratorio6
```
![image](https://user-images.githubusercontent.com/19675356/208797695-c843d981-dac4-46c5-9adc-271e6be004c0.png)

### 6.4. Permissões de Arquivos

```bash
id
```
![image](https://user-images.githubusercontent.com/19675356/208797789-c82eb183-015d-49ae-8e6c-789156d93c2b.png)

```bash
echo '#!/bin/bash' > helloBash.sh
echo 'echo "Hello Bash"' >> helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208798130-61a31186-c70d-4b47-a5e9-955d26bc67ee.png)

```bash
cat helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208798237-8a7c4e67-6db3-4803-b382-891a18abc0b2.png)

```bash
ls -l helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208798297-dda482e5-329e-410e-a8d9-dcbbd3b77e77.png)

```bash
./helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208798338-dd37ba79-35c2-4909-937b-a904d6872bdd.png)

```bash
chmod u+x helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208798442-1b42b129-aa27-43e0-8c14-4538d5b26437.png)

```bash
ls -l helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208798493-5c704c15-dd85-49fe-9f06-bcc1b3ce57c4.png)

```bash
./helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208798554-d2cc4ec6-d801-4e8c-bac1-4330ae9a19bf.png)

```bash
chmod 700 helloBash.sh
ls -l helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208798776-3310c76c-1abc-4718-8e42-b274b05638c0.png)

```bash
chmod 755 helloBash.sh
ls -l helloBash.s
```
![image](https://user-images.githubusercontent.com/19675356/208798902-8a454f61-87e6-41d2-b4d8-e3ef1d226a9b.png)

### 6.5. Mudando o Dono e o Grupo de um Arquivo

```bash
ls -l helloBash.sh
sudo chgrp palomakoba-lab6 helloBash.sh
ls -l helloBash.sh
```
![image](https://user-images.githubusercontent.com/19675356/208799260-b976ac5c-0305-4144-aee8-0ad6dc43aabe.png)

### 6.6. Executando Comandos como Root

```bash
sudo cat /etc/sudoers
```
![image](https://user-images.githubusercontent.com/19675356/208799441-ebe3000f-8e44-4891-b0c2-f0c321f6e0ef.png)
