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

```bash
ls -alh ~
```
![image](https://user-images.githubusercontent.com/19675356/207979954-df9b6a6e-bbe9-44bd-a344-12eaed0b467b.png)

### 3.2. Explorando o /dev, /proc e /sys

```bash
cat /dev/random
```
![image](https://user-images.githubusercontent.com/19675356/207980233-b0b5a534-37f6-4e05-9c6e-1cfbf7eea047.png)

```bash
echo $RANDOM
echo $RANDOM
echo $RANDOM
echo $RANDOM
```
![image](https://user-images.githubusercontent.com/19675356/207980706-51f08068-8f0e-4514-a250-a2be8751d95e.png)

```bash
echo "Timber Hearth" > /tmp/OuterWilds.txt
cat /tmp/OuterWilds.txt > /dev/stdout
```
![image](https://user-images.githubusercontent.com/19675356/207981504-e1fbf31f-1d1a-4a0d-8cb8-7a2f6b302fdc.png)

```bash
cat /proc/diskstats | grep -v loop
```
![image](https://user-images.githubusercontent.com/19675356/207981659-24d2949b-ca68-4745-9499-e21b3d3be45b.png)

```bash
iostat | grep -v loop
```
TODO


```bash
cat /sys/block/<DEVICE>/queue/hw_sector_size
```
TODO


```bash
cat /proc/cmdline
```
![image](https://user-images.githubusercontent.com/19675356/207982185-42edca88-bcac-4d74-bfed-2816c4b9c51a.png)


```bash
cat /proc/loadavg
```
![image](https://user-images.githubusercontent.com/19675356/207982290-9ef85598-6601-4138-be9c-93892396becb.png)

```bash
cat /proc/meminfo | grep Mem
```
![image](https://user-images.githubusercontent.com/19675356/207982441-1b34e54b-b4c3-4559-be75-f7377b862be1.png)

```bash
cat /proc/uptime
```
![image](https://user-images.githubusercontent.com/19675356/207982546-8660eee6-e189-42c8-bdf2-3eb6aa85d27e.png)

```bash
cat /proc/version
```
![image](https://user-images.githubusercontent.com/19675356/207982601-e6860ace-855b-41cf-9eea-a6c0a6f4b4d0.png)
