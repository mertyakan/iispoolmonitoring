# iispoolmonitoring

C dizini altında poolsh klasörü yaratıp ps1 dosyalarını içeri atınız,

Zabbix agent conf dosyası içerisinde 


USER DEFINE PARAMATERS


UserParameter=apppool.discovery,powershell -NoProfile -ExecutionPolicy Bypass -File "C:\poolsh\get_apppool.ps1"
UserParameter=apppool.state[*],powershell -NoProfile -ExecutionPolicy Bypass -File C:\poolsh\get_apppoolstate.ps1 "$1"
UserParameter=site.discovery,powershell -NoProfile -ExecutionPolicy Bypass -File "C:\poolsh\get_sites.ps1"
UserParameter=site.state[*],powershell -NoProfile -ExecutionPolicy Bypass -File C:\poolsh\get_sitestate.ps1 "$1"


Bölümü ekleyin.
