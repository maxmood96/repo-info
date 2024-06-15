## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:f66bfda2b4b8ddfbe8dfdb90f09868ec63960dd214c55ea5f4d48f5f2dc6575b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:93610dfa1f66a3f7c317f10df7cb3fc951116400ae8428c452d1577431bc74f3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.9 MB (466926855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b1f8c225474522873234cb45f7530d7d72d20606880c815c36ea3bfb6e80c8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Sat, 15 Jun 2024 00:00:41 GMT
SHELL [cmd /S /C]
# Sat, 15 Jun 2024 00:00:42 GMT
USER ContainerAdministrator
# Sat, 15 Jun 2024 00:00:44 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 15 Jun 2024 00:00:45 GMT
USER ContainerUser
# Sat, 15 Jun 2024 00:00:46 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Sat, 15 Jun 2024 00:00:47 GMT
ENV MONGO_VERSION=5.0.27
# Sat, 15 Jun 2024 00:01:03 GMT
COPY dir:a6cc57be35b0b4e87dfd208aad2e6306c874b8418531c7b4d2f073d45bf72812 in C:\mongodb 
# Sat, 15 Jun 2024 00:01:07 GMT
RUN mongo --version && mongod --version
# Sat, 15 Jun 2024 00:01:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 15 Jun 2024 00:01:09 GMT
EXPOSE 27017
# Sat, 15 Jun 2024 00:01:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de763f6e5d609393331b2f2f0661e899c06f48aa2b554904ac591ca64ef1e793`  
		Last Modified: Sat, 15 Jun 2024 00:01:18 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a439648f132273d20b710890f2b327608a0569caf2b6ee5714e185ba217fdd37`  
		Last Modified: Sat, 15 Jun 2024 00:01:18 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45cbaf454468298d152258ec18e9010a2648c1e088db684359008f1d346e0e1a`  
		Last Modified: Sat, 15 Jun 2024 00:01:17 GMT  
		Size: 71.7 KB (71656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ce6890de2f771c6493b989f93f8f85a8e3fc4dbfb5ed3165c3e1623db08e07`  
		Last Modified: Sat, 15 Jun 2024 00:01:16 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d358cc3484fe900a91fa75eba0bf7003cb3529f31245e59d9c8f329d03ac554`  
		Last Modified: Sat, 15 Jun 2024 00:01:16 GMT  
		Size: 275.3 KB (275344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18df3b11a276b52077366fad460fcbf409d52d9c66065dc2f8968d25a734b87`  
		Last Modified: Sat, 15 Jun 2024 00:01:16 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4183ff01179ecf1a64ea35d0c3c69696ca58d4f504b50aa7866dcb1696b34b`  
		Last Modified: Sat, 15 Jun 2024 00:01:44 GMT  
		Size: 311.5 MB (311452714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481e6ff09e45e609cd21f9aa7924084985891f483649656ea1d2de0e1a546ad0`  
		Last Modified: Sat, 15 Jun 2024 00:01:14 GMT  
		Size: 86.7 KB (86655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d547b32d29d0c513a37f7fc356d44e217b102202b846877aa6b763400d8e15f6`  
		Last Modified: Sat, 15 Jun 2024 00:01:15 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9e5408720049d97d657436b48db0553e4496a332660bc31d21cbd60c52eb11`  
		Last Modified: Sat, 15 Jun 2024 00:01:14 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a7bae88df3a5324e548b23814574cdf8c5a99e9644d083e2f8b89a53f59826`  
		Last Modified: Sat, 15 Jun 2024 00:01:14 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
