# Desenvolvimento Linux Embarcado

## 2. Entrada e Saída Padrões, Redirecionamento, Pipes

### 2.1. Redirecionando a Saída para Arquivos

```bash
ls -lh /usr/bin > ArquivoDoBin.txt
```
![image](https://user-images.githubusercontent.com/19675356/207736571-7fbf6255-9499-499e-b1d5-b571e8a3d396.png)

```bash
tail -5 ArquivoDoBin.txt
```
![image](https://user-images.githubusercontent.com/19675356/207736645-637b9583-8057-4a36-8771-c23d21a2c7d4.png)

```bash
echo -e "(\(\\ \n(-.-)\no_(\")(\")"
```
![image](https://user-images.githubusercontent.com/19675356/207736914-1a798589-be6b-46f5-a0d2-271b6e5d5552.png)

```bash
echo "Primeira linha do arquivo" > ArquivoTeste.txt
cat ArquivoTeste.txt
```
![image](https://user-images.githubusercontent.com/19675356/207737132-f593775f-71ca-4404-9891-fdbdcf67c821.png)

```bash
echo "Segunda linha do arquivo (só que não)" > ArquivoTeste.txt
cat ArquivoTeste.txt
```
![image](https://user-images.githubusercontent.com/19675356/207737303-1503f10a-55a1-489f-93fc-53df93a92f84.png)

```bash
echo "Segunda linha do arquivo (de verdade)" >> ArquivoTeste.txt
cat ArquivoTeste.txt
```
![image](https://user-images.githubusercontent.com/19675356/207737787-fa9b7ae9-847f-4f90-a265-820d11762cfb.png)

```bash
ls ArquivoInvalido.txt ArquivoTeste.txt > LsStdout.txt
```
![image](https://user-images.githubusercontent.com/19675356/207738021-6fa96638-fde0-4a77-9a4c-6e803ded5d5a.png)


```bash
ls ArquivoInvalido.txt ArquivoTeste.txt 2> LsStderr.txt
```
![image](https://user-images.githubusercontent.com/19675356/207738237-aaa235e6-1919-496e-aef6-ca72a4dce5f0.png)


```bash
cat LsStderr.txt
```
![image](https://user-images.githubusercontent.com/19675356/207738410-394e3320-6376-4197-9660-e6a4e306f440.png)

```bash
ls ArquivoInvalido.txt ArquivoTeste.txt > LsStdout.txt 2> LsStderr.txt
```
![image](https://user-images.githubusercontent.com/19675356/207738596-f9c2af11-2f62-4fa8-90cf-5e561c68f3f7.png)

```bash
ls ArquivoInvalido.txt ArquivoTeste.txt &> LsStdoutStderr.txt
```
![image](https://user-images.githubusercontent.com/19675356/207738739-61ac181a-5842-4586-b684-567263647003.png)

```bash
ls ArquivoInvalido.txt ArquivoTeste.txt 2> /dev/null
```
![image](https://user-images.githubusercontent.com/19675356/207738875-ca223065-d510-4037-a714-6e94612f8c5c.png)

### 2.2. Redirecionando a Saída para a Entrada de Outro Programa

```bash
grep a
Goofy Goober Rock
Dovahkiin
```
![image](https://user-images.githubusercontent.com/19675356/207739563-da243d36-a3b0-42af-b179-f1398534c77a.png)

```bash
cat /proc/cpuinfo | grep "model name"
```
![image](https://user-images.githubusercontent.com/19675356/207739706-cec40751-69f4-4571-a723-bf067e75452c.png)

```bash
cat /proc/cpuinfo | grep "model name" | head -1
```
![image](https://user-images.githubusercontent.com/19675356/207739783-b5733682-1661-4dbd-be9f-18423c9b096b.png)

```bash
cat /proc/cpuinfo | grep "model name" | head -1 | cut -d: -f2
```
![image](https://user-images.githubusercontent.com/19675356/207739995-151cefa3-d98f-4d07-947e-f98bfe263931.png)

```bash
cat /proc/cpuinfo | grep "model name" | head -1 | cut -d: -f2 | cut -c2-
```
![image](https://user-images.githubusercontent.com/19675356/207740115-b50fe525-f5b7-49e1-877f-765bccec3ccd.png)

### 2.3. Desafios (Prática)

```bash
cat /etc/passwd | grep h | wc -l
```
![image](https://user-images.githubusercontent.com/19675356/207740536-f194a4cd-b705-4c62-976d-939560454318.png)

- comando para contar somente os usuarios que possuem a letra "h" em seu nome 
```bash
cat /etc/passwd | cut -d: -f1 | grep h | wc -l
```
![image](https://user-images.githubusercontent.com/19675356/207741190-e88a7f6d-e7a7-4d3f-af6e-d49982484ec0.png)
