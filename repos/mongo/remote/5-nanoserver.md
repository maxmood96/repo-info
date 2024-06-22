## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:4840821166b7bfae2fd4df685f9a23adbefdeab41b8a3e41e1c14d5413352b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:2bb648fcf45758e663f37b68716db2923a5745166a9e115635138063f49a25e1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.4 MB (432411281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d0e1f566db3564913c15e8c00fd210ecf7305c7d7f55ef23c5a998cd5d7a56`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 19 Jun 2024 19:27:30 GMT
RUN Apply image 10.0.20348.2529
# Sat, 22 Jun 2024 01:05:50 GMT
SHELL [cmd /S /C]
# Sat, 22 Jun 2024 01:05:51 GMT
USER ContainerAdministrator
# Sat, 22 Jun 2024 01:05:53 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 22 Jun 2024 01:05:54 GMT
USER ContainerUser
# Sat, 22 Jun 2024 01:05:56 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Sat, 22 Jun 2024 01:05:56 GMT
ENV MONGO_VERSION=5.0.27
# Sat, 22 Jun 2024 01:06:07 GMT
COPY dir:a6cc57be35b0b4e87dfd208aad2e6306c874b8418531c7b4d2f073d45bf72812 in C:\mongodb 
# Sat, 22 Jun 2024 01:06:18 GMT
RUN mongo --version && mongod --version
# Sat, 22 Jun 2024 01:06:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 22 Jun 2024 01:06:20 GMT
EXPOSE 27017
# Sat, 22 Jun 2024 01:06:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a8c295c425a912de308ded279124ae45fec44d55a451843fe5877155417f453c`  
		Last Modified: Fri, 21 Jun 2024 02:24:34 GMT  
		Size: 120.5 MB (120499549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9139f30fa9658e1cb31bd146e44254a43cf56082783612db02ea4d52c9ce33ef`  
		Last Modified: Sat, 22 Jun 2024 01:06:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4d8860e119520bcdc235c0395b8b25c9a06f32703ede3d2952a97f3d2992fb`  
		Last Modified: Sat, 22 Jun 2024 01:06:25 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc34564acfa9150bca7e8cb5740b66889dcd057ffb9549e4ad1b2a0611114d1b`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 78.5 KB (78461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50df23d63d6ab8a26fed52129325c9c8b75f283617893b9f6d1f4783e25265c`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e19d06e8da77570b6dab56ff849a29ff372bd9711ef028014308222fe3f1ef`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 275.4 KB (275350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6624382032227b55c33e33d1f63c6355d3048d65edb367e6785b29825b2945`  
		Last Modified: Sat, 22 Jun 2024 01:06:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaada9a797e02aec3c95d26d34b36f660211a2ed1150825e8a4bdc3101917db9`  
		Last Modified: Sat, 22 Jun 2024 01:06:53 GMT  
		Size: 311.5 MB (311452648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4527734013c656e63dc3a0de09362732a3426711d530885c317a246799034195`  
		Last Modified: Sat, 22 Jun 2024 01:06:23 GMT  
		Size: 98.1 KB (98051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd21db0086e641002d40aee7b2cf98866c22f052123e182210aa0e6548e6836`  
		Last Modified: Sat, 22 Jun 2024 01:06:23 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7161931e4647033af52042b82ad9d5ef95e9b49844c191b4a5dc05620a1fa2`  
		Last Modified: Sat, 22 Jun 2024 01:06:23 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54948d5ebb34108381d1218a720fd8da1a6d99eaa57eec2c5aa5562c2ada7b28`  
		Last Modified: Sat, 22 Jun 2024 01:06:23 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.5936; amd64

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
