# Udacity: Configuring Linux Web Servers

Completed 08/16/2015

Packages to install: `apache2Http`, `wsgi` and `PostgreSQL`

```
sudo addUser student
```

login server:

```
ssh student@127.0.0.1 -p 2222
```

in local machine(not server):

```
ssh-keygen 
```

check ssh file:

```
cat .ssh/id_rsa
```

security measure:

```
student@vagrant-ubuntu-trusty-64:~$ chmod 700 .ssh
student@vagrant-ubuntu-trusty-64:~$ chmod 644 .ssh/authorized_keys
```

login:

```
Anyi@Anyis-MacBook-Pro:~/Github_Repos/Udacity/Linux_Server$ ssh student@127.0.0.1 -p 2222 -i ~/.ssh/id_rsa
```


```
sudo service ssh restart
```

check firewall status:

```
student@vagrant-ubuntu-trusty-64:/usr/local/share/man$ sudo ufw status
Status: inactive

student@vagrant-ubuntu-trusty-64:/usr/local/share/man$ sudo ufw default allow outgoing
Default outgoing policy changed to 'allow'
(be sure to update your rules accordingly)


student@vagrant-ubuntu-trusty-64:/usr/local/share/man$ sudo ufw allow ssh
Rules updated
Rules updated (v6)

student@vagrant-ubuntu-trusty-64:/usr/local/share/man$ sudo ufw allow www
Rules updated
Rules updated (v6)


student@vagrant-ubuntu-trusty-64:/usr/local/share/man$ sudo ufw allow 2222/tcp
Rules updated
Rules updated (v6)

student@vagrant-ubuntu-trusty-64:/usr/local/share/man$ sudo ufw enable
Command may disrupt existing ssh connections. Proceed with operation (y|n)? y
Firewall is active and enabled on system startup

student@vagrant-ubuntu-trusty-64:/usr/local/share/man$ sudo ufw status
Status: active

To                         Action      From
--                         ------      ----
22                         ALLOW       Anywhere
2222/tcp                   ALLOW       Anywhere
80/tcp                     ALLOW       Anywhere
22 (v6)                    ALLOW       Anywhere (v6)
2222/tcp (v6)              ALLOW       Anywhere (v6)
80/tcp (v6)                ALLOW       Anywhere (v6)
```
