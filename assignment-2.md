# CLI App Testing

:whale:
Use different Linux distro containers to check **curl** cli tool version

- [x] Use two different terminal windows to start bash in both _centos:7_ and **ubuntu:14.04**, using -it

  ```
  $ docker container run --name mycentos -it centos:7 bash
  ```

  ```
  $ docker container run --name myubunt -it ubuntu:14.04 bash
  ```

- [x] Learn the **docker container --rm** option so you can save cleanup

Automatically remove the container when it exits

```
$ docker container run --rm --name mycentos -it centos:7 bash
```

```
$ docker container run --rm --name myubunt -it ubuntu:14.04 bash
```

- [x] Ensure curl is installed and on latest version for that distro

  - ubuntu: apt-get update && apt-get install curl
  - centos: yum update curl

- [x] Check curl --version

  Centos:

  ```
  [root@355bb4c41158 /]# curl --version
  curl 7.29.0 (x86_64-redhat-linux-gnu) libcurl/7.29.0 NSS/3.36 zlib/1.2.7 libidn/1.28 libssh2/1.4.3
  Protocols: dict file ftp ftps gopher http https imap imaps ldap ldaps pop3 pop3s rtsp scp sftp smtp smtps telnet tftp
  Features: AsynchDNS GSS-Negotiate IDN IPv6 Largefile NTLM NTLM_WB SSL libz unix-sockets
  ```

  Ubuntu:

  ```
  root@0422f6d22f09:/# curl --version
  curl 7.35.0 (x86_64-pc-linux-gnu) libcurl/7.35.0 OpenSSL/1.0.1f zlib/1.2.8 libidn/1.28 librtmp/2.3
  Protocols: dict file ftp ftps gopher http https imap imaps ldap ldaps pop3 pop3s rtmp rtsp smtp smtps telnet tftp
  Features: AsynchDNS GSS-Negotiate IDN IPv6 Largefile NTLM NTLM_WB SSL libz TLS-SRP
  ```
