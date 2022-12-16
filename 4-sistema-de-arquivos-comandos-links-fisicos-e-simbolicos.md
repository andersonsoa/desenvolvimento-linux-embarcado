# Desenvolvimento Linux Embarcado

## 4. Sistema de Arquivos - Comandos, Links Físicos e Simbólicos

### 4.1. Descobrindo a Localização dos Comandos

```bash
whereis who
```
![image](https://user-images.githubusercontent.com/19675356/207989673-35b2aaf1-9417-49d7-9c1b-412072af86cd.png)

```bash
whereis ls 
```
![image](https://user-images.githubusercontent.com/19675356/207990044-e02b0e5a-5d91-42f7-b156-cbf8bb2c9972.png)

```bash
where is hexdump
```
![image](https://user-images.githubusercontent.com/19675356/207990435-9ef0696c-88cd-4bb2-a8a8-0219ba06c667.png)

```bash
whereis grep
```
![image](https://user-images.githubusercontent.com/19675356/207990535-211b8698-403f-4f9d-8c2c-ad10f6e3c606.png)

```bash
whereis ifconfig
```
![image](https://user-images.githubusercontent.com/19675356/207990629-6932778e-373d-450a-8de5-00d7939c9c76.png)

```bash
whereis whereis
```
![image](https://user-images.githubusercontent.com/19675356/207990659-72087c27-0459-482a-9cb0-8119b5b13a66.png)

### 4.2. Buscando Arquivos no Sistema

```bash
find /etc
```
![image](https://user-images.githubusercontent.com/19675356/207990788-82f2a01c-4124-4426-ad18-aba1acc8c468.png)

```bash
find /etc | wc -l
```
![image](https://user-images.githubusercontent.com/19675356/207990861-b087e797-3598-4040-8499-7100875e4e4f.png)

```bash
find /etc 2> /dev/null | wc -l
```
![image](https://user-images.githubusercontent.com/19675356/207990940-9148c47a-757e-40f5-9612-63ca5231f600.png)

```bash
find /usr/include -name *org*
```
![image](https://user-images.githubusercontent.com/19675356/207991037-bf5f5dd9-cb20-4d72-810b-11cbda683661.png)

```bash
find /usr/include | grep org
```
![image](https://user-images.githubusercontent.com/19675356/207991194-82d97b25-50c2-4124-b6d7-676e5a3b31e9.png)

### 4.3. Espaço em Disco Consumido por um Diretório

```bash
cd /usr
du -s
```
![image](https://user-images.githubusercontent.com/19675356/207991382-2559ccf7-5db2-4e46-ab83-b3d871f65847.png)

```bash
du -sh
```
![image](https://user-images.githubusercontent.com/19675356/207991457-8d9f476a-6efa-4aa8-8259-5b8a8214a7be.png)

```bash
du -sh *
```
![image](https://user-images.githubusercontent.com/19675356/207991518-58d635cb-7efa-451c-a43f-ccb8261ff79c.png)

### 4.4. Links Físicos e Simbólico

```bash
cd
echo "Mensagem no arquivo original" > ArquivoOriginal.txt
ls -lh ArquivoOriginal.txt
```
![image](https://user-images.githubusercontent.com/19675356/207991792-14ca8201-9616-45bf-9a4b-4694fd9a6b42.png)

```bash
ln -s ArquivoOriginal.txt ArquivoLinkSimbolico.txt
ls -lh ArquivoLinkSimbolico.txt
```
![image](https://user-images.githubusercontent.com/19675356/207991946-46dc4c23-7b91-41d0-bd9c-30be2d9df43e.png)

```bash
cat ArquivoLinkSimbolico.txt
```
![image](https://user-images.githubusercontent.com/19675356/207992064-254aaf5f-7e31-4ddc-a04d-08b3830844b8.png)

```bash
echo "Mensagem contatenada no link simbolico" >> ArquivoLinkSimbolico.txt
cat ArquivoOriginal.txt
```
![image](https://user-images.githubusercontent.com/19675356/207992225-1a2313c8-40f3-4ab1-8024-852f85bc49a6.png)

```bash
rm ArquivoOriginal.txt
cat ArquivoLinkSimbolico.txt
```
![image](https://user-images.githubusercontent.com/19675356/207992360-a6b514b4-5b9d-401a-af37-a395ab071eae.png)

```bash
ls -lh ArquivoLinkSimbolico.txt
```
![image](https://user-images.githubusercontent.com/19675356/207992476-465db8a9-581a-4e9a-bf33-864a7ffd2cf8.png)

```bash
echo "Mensagem no arquivo original 2" > ArquivoOriginal2.txt
ls -lh ArquivoOriginal2.txt
```
![image](https://user-images.githubusercontent.com/19675356/207992595-26c9fedb-d109-4322-9ca1-1aaf5d2f5ba7.png)

```bash
ln ArquivoOriginal2.txt ArquivoLinkFisico.txt
ls -lh ArquivoOriginal2.txt ArquivoLinkFisico.txt
```
![image](https://user-images.githubusercontent.com/19675356/207992766-b43520bf-cf12-4942-8a81-4a57e6b764b8.png)

```bash
echo "Mensagem contatenada no link fisico" >> ArquivoLinkFisico.txt
ls -lh ArquivoOriginal2.txt ArquivoLinkFisico.txt
```
![image](https://user-images.githubusercontent.com/19675356/207992956-63207675-5222-48df-b782-9e37941e57ab.png)

```bash
rm ArquivoOriginal2.txt
ls -lh ArquivoLinkFisico.txt
cat ArquivoLinkFisico.txt
```
![image](https://user-images.githubusercontent.com/19675356/207993059-c94e9730-d629-405f-aed7-3fd66f7198fb.png)

### 4.5. Os Diretórios "." e ".." são Links Físicos

```bash
ls -alh | grep "\." | head -2
```
![image](https://user-images.githubusercontent.com/19675356/207993178-4b24bda2-4d57-40be-a13b-d37008351340.png)

```bash
mkdir NovoSubdiretorio
ls -alh | grep "\." | head -2
```
![image](https://user-images.githubusercontent.com/19675356/207993365-61a442cf-68f5-41bf-a4e5-e6f9fccdbb81.png)

```bash
ls -lh | grep NovoSubdiretorio
```
![image](https://user-images.githubusercontent.com/19675356/207993421-80e2aebb-4498-4a19-a43b-03e3de7d314b.png)

```bash
ls -alh NovoSubdiretorio/
```
![image](https://user-images.githubusercontent.com/19675356/207993512-dc0d448c-376a-4471-80df-a51a17dfab73.png)
