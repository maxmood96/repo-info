## `mongo:8-nanoserver`

```console
$ docker pull mongo@sha256:f702d2321b8c846adb8ac8cc6468b164194e2271594376c4045cf8157bb5b3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `mongo:8-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull mongo@sha256:e7d0fc674ddb15a9c7c00f5cf1f369e80d7e74685ccd6fdc2066e1150c72f9f3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.5 MB (941537816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b2443821a69ca00d7891de66d9577f1773f5917afd0b74a2daa72ab66e33b9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Wed, 11 Feb 2026 00:13:31 GMT
SHELL [cmd /S /C]
# Wed, 11 Feb 2026 00:13:33 GMT
USER ContainerAdministrator
# Wed, 11 Feb 2026 00:13:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Feb 2026 00:13:40 GMT
USER ContainerUser
# Wed, 11 Feb 2026 00:13:42 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Wed, 11 Feb 2026 00:13:43 GMT
ENV MONGO_VERSION=8.2.5
# Wed, 11 Feb 2026 00:14:24 GMT
COPY dir:a0b1e52802eea6e71b140810e76e3ccf3bfdb8657e849479e93df0cd3a9bf7bb in C:\mongodb 
# Wed, 11 Feb 2026 00:14:48 GMT
RUN mongod --version
# Wed, 11 Feb 2026 00:14:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Feb 2026 00:14:49 GMT
EXPOSE 27017
# Wed, 11 Feb 2026 00:14:49 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4e0062633a2362b09d13f6f7799e44f547275c9fc568f1e93f4ff28f39e112`  
		Last Modified: Wed, 11 Feb 2026 00:14:57 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cd74519a5d08bf7101ced968b56386bb5c78299e4ba890952fe653a66bd956`  
		Last Modified: Wed, 11 Feb 2026 00:14:57 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:464ee72837c0894334a516377cd8f371224394b08fee6189fa789c3e145336cc`  
		Last Modified: Wed, 11 Feb 2026 00:14:56 GMT  
		Size: 71.7 KB (71741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e031c68f53444f3e223ed76469a28bd326ab625225a95e9983701ab00ba01486`  
		Last Modified: Wed, 11 Feb 2026 00:14:56 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6388cd23cbf4091b3679d37a7f8a40a1aac03d1b21029f0c37575a1b58660a`  
		Last Modified: Wed, 11 Feb 2026 00:14:56 GMT  
		Size: 275.2 KB (275183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d8badf651c5e99c17d71a4abebbbfa4bd4df2df7ecefeb298e8be4ba51c05e`  
		Last Modified: Wed, 11 Feb 2026 00:14:56 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4b86375df19adec6faf4264ca80f4732a137a19962e1deb85f96077140f665`  
		Last Modified: Wed, 11 Feb 2026 00:16:13 GMT  
		Size: 814.4 MB (814448461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c809682b7e8581e2419f100885b5629768ad71245c25440b0cd8ea0df20131`  
		Last Modified: Wed, 11 Feb 2026 00:14:54 GMT  
		Size: 89.1 KB (89087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17262bb80519bc34b6a5c88ea967720bfdaf4e153ea3cf8fe5365194f94407d`  
		Last Modified: Wed, 11 Feb 2026 00:14:54 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4231493506123b8986181566a5637b2bc8bc25cca0807e3307008b293cc0527`  
		Last Modified: Wed, 11 Feb 2026 00:14:54 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281969d5ea8885fe89195d47aae5c34808e0ff2d2ec8a520a8f6e581a7fd3b02`  
		Last Modified: Wed, 11 Feb 2026 00:14:54 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
