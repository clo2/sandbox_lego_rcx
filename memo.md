
# memo(備忘録)

## 概要
### 環境
lubuntu 14.04

```
sudo apt-get install nqc
```


### usb ir接続
dmesg
```
[  540.271322] usb 3-2: USB disconnect, device number 2
[  540.271565] legousbtower 3-2:1.0: LEGO USB Tower #-160 now disconnected
[  541.387298] usb 3-2: new low-speed USB device number 4 using xhci_hcd
[  541.421278] usb 3-2: New USB device found, idVendor=0694, idProduct=0001
[  541.421286] usb 3-2: New USB device strings: Mfr=4, Product=26, SerialNumber=0
[  541.421290] usb 3-2: Product: LEGO USB Tower
[  541.421293] usb 3-2: Manufacturer: LEGO Group
[  541.422529] legousbtower 3-2:1.0: LEGO USB Tower #-160 now attached to major 180 minor 0
[  541.423671] legousbtower 3-2:1.0: LEGO USB Tower firmware version is 1.0 build 134
```
lsusb
```
Bus 003 Device 004: ID 0694:0001 Lego Group Mindstorms Tower
```
### firmware送信
```
sudo nqc -Susb -firmware firm0309.lgo
```
約３分程度。送信完了時にRCXからピロリンという音声再生。

### プログラムのビルド＆転送
```
sudo nqc -Susb -d test001.nqc
```


### 参考サイト
− http://yakushi.shinshu-u.ac.jp/robotics/?NQC%C6%FE%CC%E7
