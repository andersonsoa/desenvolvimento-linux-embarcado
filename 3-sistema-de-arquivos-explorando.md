# Desenvolvimento Linux Embarcado

## 3. Sistema de Arquivos - Explorando

### 3.1. Explorando o /etc

```bash
ls -flh /etc/passwd /etc/shadow /etc/group
```
![image](https://user-images.githubusercontent.com/19675356/207753341-a54da732-7b96-4627-88ee-2ef17a10abe4.png)

```bash
cat /etc/hostname
```
![image](https://user-images.githubusercontent.com/19675356/207753474-04bafcc5-9eb8-4210-b3b1-373597cafa8f.png)

```bash
cat /etc/protocols | grep UDP
```
![image](https://user-images.githubusercontent.com/19675356/207753585-927ae3ae-a245-481d-bd10-a0484e16e9c9.png)

```bash
cat /etc/services | grep -P "ssh|http\t|https|ircd"
```
![image](https://user-images.githubusercontent.com/19675356/207753921-beec0880-530e-438d-b3c0-c4f735a30f75.png)

```bash
cat /etc/shells
```
![image](https://user-images.githubusercontent.com/19675356/207754014-271fddb7-f9aa-49b3-8a24-39b62ad3d7ac.png)

```bash
cat /etc/timezone
```
![image](https://user-images.githubusercontent.com/19675356/207754161-a89e6620-fd20-4ffc-ae70-bba7445fe3b9.png)
