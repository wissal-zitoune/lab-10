# lab-10
### Installation de Frida
```bash
pip install frida frida-tools
```
### Vérification
```bash
frida --version
frida-ps --version
python -c "import frida; print(frida.__version__)"
```
### Installation de frida-server (Android)
## Décompresser
```bash
xz -d frida-server-*.xz
```
## Transfert vers l’appareil
```bash
adb push frida-server /data/local/tmp/
adb shell chmod +x /data/local/tmp/frida-server
```
## Lancement de frida-server
```bash
adb shell
su
/data/local/tmp/frida-server -l 0.0.0.0

```
## Vérification de la connexion
```bash
frida-ps -U
frida-ps -Uai
```
<img width="736" height="326" alt="1" src="https://github.com/user-attachments/assets/224e12e7-04bf-4250-a537-a5aaf47bfe64" />
<img width="477" height="27" alt="2" src="https://github.com/user-attachments/assets/39377511-174e-4770-88eb-536a0f48aeb8" />
<img width="1092" height="268" alt="3 ,," src="https://github.com/user-attachments/assets/13774026-9d0c-4781-8151-5b1ddf406d99" />
<img width="617" height="95" alt="4" src="https://github.com/user-attachments/assets/9299d63a-ffc7-439d-909e-ad3105530395" />
<img width="1185" height="508" alt="5" src="https://github.com/user-attachments/assets/695dea43-0c03-4ed3-84f1-ae675eb4cddd" />

## Simuler une erreur
```bash

killall frida-server
```
## Vérification
```bash
adb shell ps | grep frida
```
## Relancer
```bash
adb shell
/data/local/tmp/frida-server &
```
## Nettoyage
```bash
adb shell rm /data/local/tmp/frida-server
```
