## `golang:nanoserver`

```console
$ docker pull golang@sha256:24f22cbc251620f4e4ad6e00af2c66ba01bb089bfc2e06efa0ee912eec9a4268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `golang:nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull golang@sha256:ae3f381d01034f0b54c120bd536522b0905327ae5744958634594ee99ecb22be
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 MB (197609533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c04e96819f1be406b0d9fd985da7be33ca60efb4862373994808023187aaa4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 07 Nov 2024 03:48:30 GMT
SHELL [cmd /S /C]
# Thu, 07 Nov 2024 03:48:30 GMT
ENV GOPATH=C:\go
# Thu, 07 Nov 2024 03:48:31 GMT
USER ContainerAdministrator
# Thu, 07 Nov 2024 03:48:36 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 07 Nov 2024 03:48:37 GMT
USER ContainerUser
# Thu, 07 Nov 2024 03:48:38 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 03:49:58 GMT
COPY dir:d7d597c32e0f94f5ef9191a04cf49682b3853beb64463026d6a674e969c30a19 in C:\Program Files\Go 
# Thu, 07 Nov 2024 03:50:01 GMT
RUN go version
# Thu, 07 Nov 2024 03:50:05 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15022c40e002b2df9126e5f5e63a18fa685c0526e5b5898fa58c55989e7a933`  
		Last Modified: Thu, 07 Nov 2024 03:50:11 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf252aa4ac251b9ada46a4d50318be011690c9aa6b4ae7683367f5c1fda46f5`  
		Last Modified: Thu, 07 Nov 2024 03:50:11 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfc20bcc95ced11bfd1ae696c983bfab1c828eb56e230f95b364f012b422948`  
		Last Modified: Thu, 07 Nov 2024 03:50:11 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76209ef4309b01f242a1858b6b3a35f029342392bb437c3174f6f3684acab10b`  
		Last Modified: Thu, 07 Nov 2024 03:50:11 GMT  
		Size: 79.6 KB (79563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27414f4305dfebc357817a78f36dd32145efa404fe060a5886e216734c55da6c`  
		Last Modified: Thu, 07 Nov 2024 03:50:09 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c245bf98e1bead28e8862257b44f21216166ef2d9cf8dbf7abb3d62bb86492d`  
		Last Modified: Thu, 07 Nov 2024 03:50:09 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde55473f43e021e8145b2bfa776509ba5a61a54c94925654630cf1e103cee4c`  
		Last Modified: Thu, 07 Nov 2024 03:50:20 GMT  
		Size: 76.9 MB (76925304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d4cd4f1f5b71464cf0a74c90dec22b83eead3825af55c3f3fe8586a250d0b9`  
		Last Modified: Thu, 07 Nov 2024 03:50:09 GMT  
		Size: 87.2 KB (87243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfa40328448bddf79e3e3618c4d44d3854b0014160c54187f2bc2609900a612`  
		Last Modified: Thu, 07 Nov 2024 03:50:09 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull golang@sha256:a31c76f97d24d33ec257d50a3fef811f8923165b199e70cfb8161f6dfefca46a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232154757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b450370616b09f2c9180e54ed8ea829db4902c75d642c3b3550cca68bf0b00`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 07 Nov 2024 03:49:48 GMT
SHELL [cmd /S /C]
# Thu, 07 Nov 2024 03:49:50 GMT
ENV GOPATH=C:\go
# Thu, 07 Nov 2024 03:49:50 GMT
USER ContainerAdministrator
# Thu, 07 Nov 2024 03:50:03 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 07 Nov 2024 03:50:03 GMT
USER ContainerUser
# Thu, 07 Nov 2024 03:50:03 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 03:51:44 GMT
COPY dir:d7d597c32e0f94f5ef9191a04cf49682b3853beb64463026d6a674e969c30a19 in C:\Program Files\Go 
# Thu, 07 Nov 2024 03:51:47 GMT
RUN go version
# Thu, 07 Nov 2024 03:51:47 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4caae26edbf1663bdb789489462f8a80a4cb373fd6d23f4352a2df063c7641`  
		Last Modified: Thu, 07 Nov 2024 03:51:53 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d49053925e9689f8393527db2f28e95ed85092ed477ea67c62f8fa6b02c075`  
		Last Modified: Thu, 07 Nov 2024 03:51:53 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100291190cf2ef9bd5868e0bcde0af44c0259f9dd3902588c445f8362fa4e658`  
		Last Modified: Thu, 07 Nov 2024 03:51:53 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca38236bb4a3571ecc6142c500465a3d413e7e140737a67ecb97a13308bba871`  
		Last Modified: Thu, 07 Nov 2024 03:51:53 GMT  
		Size: 65.1 KB (65149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e3b6ec4d5b016297f07b3d4046a0ccd0bda4ff1c994a59ed90a01903183a9f`  
		Last Modified: Thu, 07 Nov 2024 03:51:51 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab8309f99a8d31066a064d9bc37711fc6bbf4b39aa3a6bf6331b1789da84e5d`  
		Last Modified: Thu, 07 Nov 2024 03:51:51 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd61758f01bb300d3cbd62bc6be593329f81190bdbf87603457ba76ed90dbb21`  
		Last Modified: Thu, 07 Nov 2024 03:52:03 GMT  
		Size: 76.9 MB (76924740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e814b46cae8cd2d7022daaedb743a2a17f08af92f245c3d13b7521666f1c6084`  
		Last Modified: Thu, 07 Nov 2024 03:51:51 GMT  
		Size: 64.9 KB (64858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88aa5e647cc8c6016f3b0a4d01db3e888a89d0321ae9a687911893d4753bbbf8`  
		Last Modified: Thu, 07 Nov 2024 03:51:51 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
