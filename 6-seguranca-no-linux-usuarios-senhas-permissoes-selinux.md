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

```

```bash

```

```bash

```

```bash

```
