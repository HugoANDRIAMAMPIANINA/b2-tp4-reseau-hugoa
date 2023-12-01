# TP4 : I'm Socketing, r u soketin ?

## I. Simple bs program

### 1. First steps

[bs_server_I1.py](bs_server_I1.py)
[bs_client_I1.py](bs_client_I1.py)

```
[hugoa@server ~]$ git clone https://github.com/HugoANDRIAMAMPIANINA/b2-tp4-reseau-hugoa.git

[hugoa@client ~]$ git clone https://github.com/HugoANDRIAMAMPIANINA/b2-tp4-reseau-hugoa.git
```

```
# Côté serveur
[hugoa@server ~]$ python bs_server_I1.py
Meooooo !

# Côté client
[hugoa@client ~]$ python bs_client_I1.py
Hi mate!
```

```
[hugoa@server ~]$ ss -alntp | grep 13337
LISTEN 0      1          10.1.1.11:13337      0.0.0.0:*    users:(("python",pid=3407,fd=3))
```

## II

### 2. A. Logs serveur

```
# Création du fichier de log et modification des permissions

[hugoa@server ~]$ sudo mkdir /var/log/bs_server/
[hugoa@server ~]$ sudo touch /var/log/bs_server/bs_server.log
[hugoa@server ~]$ sudo chown -R hugoa:hugoa /var/log/bs_server/
[hugoa@server ~]$ sudo chmod +x /var/log/bs_server/
```

### 2. B. Logs client

```
# Création du fichier de log et modification des permissions

[hugoa@client ~]$ sudo mkdir /var/log/bs_client/
[hugoa@client ~]$ sudo touch /var/log/bs_client/bs_client.log
[hugoa@client ~]$ sudo chmod -R +x /var/log/bs_client/
[hugoa@client ~]$ sudo chown -R hugoa:hugoa /var/log/bs_client/
```