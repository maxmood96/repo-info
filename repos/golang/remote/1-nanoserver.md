## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:da1edf7ce992868c1a8ec2d564ebe1f5608013186c16cd4577643e57b162e929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `golang:1-nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull golang@sha256:9cc2ea377bc15123e3f44c1b3e2e03433695a0c5a7f8ed4dd399195e9d100e0d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241848544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2a520d10782dd4a6ee5ce1f3c383098aefb242b1d2b29dc48879e9c4bc90ae`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 12:49:37 GMT
SHELL [cmd /S /C]
# Wed, 09 Jun 2021 12:49:40 GMT
ENV GOPATH=C:\gopath
# Wed, 09 Jun 2021 12:49:43 GMT
USER ContainerAdministrator
# Wed, 09 Jun 2021 12:50:14 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 09 Jun 2021 12:50:17 GMT
USER ContainerUser
# Wed, 09 Jun 2021 12:50:19 GMT
ENV GOLANG_VERSION=1.16.5
# Wed, 09 Jun 2021 12:52:20 GMT
COPY dir:ae3d9e178792efeead02d2f25babdbd0198afbcffad94f186dc6859f7c7504fd in C:\go 
# Wed, 09 Jun 2021 12:52:48 GMT
RUN go version
# Wed, 09 Jun 2021 12:52:50 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2646c4431bb01c2667bc3bd1353d18b2632d04cc58ad53a79480ecdde4fd710d`  
		Last Modified: Wed, 09 Jun 2021 13:05:18 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb2068fe4d0d7f614dcebdadd3eb0af27aa70abda1ebb8dee1bfd37c791197a`  
		Last Modified: Wed, 09 Jun 2021 13:05:17 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8563765367d01f674014a0e8ad51aee3b3cf8967835b6f641d121994ccd72fb9`  
		Last Modified: Wed, 09 Jun 2021 13:05:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e027a5dbd9c579ecc14f1a4e5987be4fd5b701b2a4518041acd65713b2a3eb24`  
		Last Modified: Wed, 09 Jun 2021 13:05:17 GMT  
		Size: 68.6 KB (68632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6609d2c783fad47fae875fcad47c9339cb27ee403677d7de00729023bc437d`  
		Last Modified: Wed, 09 Jun 2021 13:05:15 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533badd004f9a9454559ad112ca015ed741a952fa5b5a9a7f1064a83d6739294`  
		Last Modified: Wed, 09 Jun 2021 13:05:15 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8713e494c134336663751da51e925bdb943532656827733395a2c6e16607ef`  
		Last Modified: Wed, 09 Jun 2021 13:05:50 GMT  
		Size: 139.0 MB (139032106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6488ca1d54af7b664950edcb9583b91ba8416e3c57dd519c20d52ed2681fa66`  
		Last Modified: Wed, 09 Jun 2021 13:05:15 GMT  
		Size: 69.2 KB (69209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf02087fd1130b622f83d374b1d1be401d024ac983850651b55e442af11839c`  
		Last Modified: Wed, 09 Jun 2021 13:05:15 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
