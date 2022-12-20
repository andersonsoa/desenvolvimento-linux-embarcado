# Desenvolvimento Linux Embarcado

## 5. Processos, Daemons, Serviços, Inicialização do Sistema

### 5.1. Listando os Processos em Execução

```bash
ps
```
![image](https://user-images.githubusercontent.com/19675356/208747884-735acd51-972e-461d-a6f0-07704c5db0d2.png)

```bash
cat &
ps
```
![image](https://user-images.githubusercontent.com/19675356/208748052-f2d9021f-8e89-4425-b4dc-02cc0df02dd5.png)

```bash
ps -f
```
![image](https://user-images.githubusercontent.com/19675356/208748490-87ae1458-d528-40e9-891f-3988a2aaba39.png)

```bash
ps -ef
```
![image](https://user-images.githubusercontent.com/19675356/208748572-10eef11e-a107-4ccb-8377-798563c20fa9.png)

```bash
ps -ef | wc -l
```
![image](https://user-images.githubusercontent.com/19675356/208748664-9816b9f2-b0f9-498e-b18b-a215f089c8b2.png)

```bash
top
```
![image](https://user-images.githubusercontent.com/19675356/208748766-007a952c-4a2e-4a5b-bab8-149d881fa024.png)

```bash
top -o %MEM
```
![image](https://user-images.githubusercontent.com/19675356/208748875-1ed4fa10-9297-4c48-97fa-a8d3ebbf848d.png)
