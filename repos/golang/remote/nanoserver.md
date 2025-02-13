## `golang:nanoserver`

```console
$ docker pull golang@sha256:53a383eb3614267406be2dd5d218b13d3cd7ec08a7539bcb7175581c915aa509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `golang:nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull golang@sha256:52ababc2efde4064537df7ea2e4ba399944e2e83ffecfa7c5563a904cdafafa1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280953608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c70995099409a625393d3da1e987ceb7784ece2f42d6e716c4bf40474fbe58`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 12 Feb 2025 18:36:22 GMT
SHELL [cmd /S /C]
# Wed, 12 Feb 2025 18:36:23 GMT
ENV GOPATH=C:\go
# Wed, 12 Feb 2025 18:36:24 GMT
USER ContainerAdministrator
# Wed, 12 Feb 2025 18:36:28 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Feb 2025 18:36:30 GMT
USER ContainerUser
# Wed, 12 Feb 2025 18:36:31 GMT
ENV GOLANG_VERSION=1.24.0
# Wed, 12 Feb 2025 18:37:38 GMT
COPY dir:c62b8dc6e9060a1c90492bd4af0627f1fb2ef88d5b0c6bad980916fff57ef6a8 in C:\Program Files\Go 
# Wed, 12 Feb 2025 18:37:43 GMT
RUN go version
# Wed, 12 Feb 2025 18:37:44 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Wed, 22 Jan 2025 08:02:27 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7e580b02806b6cec2f45d8d66a98d3047392fc136cfc5ad89a714cff0db517`  
		Last Modified: Wed, 12 Feb 2025 21:33:50 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66720ca73a9edb718d5c808a6dfc03a8aa3219a87f01839cc6077e822944603c`  
		Last Modified: Wed, 12 Feb 2025 21:33:51 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55051291d9a9afc1583abe84ab93e08fabf385d002bd871236d43f87131d8403`  
		Last Modified: Wed, 12 Feb 2025 21:33:52 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49909a5df324fff246268c761d5c398f96008722b9a34c044b6e45be2fb384db`  
		Last Modified: Wed, 12 Feb 2025 21:33:53 GMT  
		Size: 75.7 KB (75735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595771deb3470cf10d7b9620669b6648421f0fa358f758b2f8f09f5256cd3f10`  
		Last Modified: Wed, 12 Feb 2025 21:33:54 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e552d43b2d5eb3a460bf5a9bef4795696afcd8f9e432a20e5b773a333cc77362`  
		Last Modified: Wed, 12 Feb 2025 21:33:55 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c393312ffeaa89bf7c8f2a49889d603a60e4efb0b7f3df321d1a0ba7f60803ac`  
		Last Modified: Wed, 12 Feb 2025 21:34:05 GMT  
		Size: 81.7 MB (81727671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf81d01f2fd43dd97e0a5d0dee31e1662109c2db3499889694658f62fa36d53`  
		Last Modified: Wed, 12 Feb 2025 21:34:09 GMT  
		Size: 89.5 KB (89461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9341e9e039b56ae9bc67506c7d742e62d9f7163f3c7f237428a237fdd49418f`  
		Last Modified: Wed, 12 Feb 2025 21:34:10 GMT  
		Size: 1.2 KB (1245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull golang@sha256:b19780b52c320f5d575ab4334bed183a18a51db22f7f5a357b2cd95efe99402e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.5 MB (202526903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5651eb9da5ab1e70a69b0a564e7ff5c7e72dfa1a2877b0cb60934d8bd6e6d65`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Wed, 12 Feb 2025 18:33:36 GMT
SHELL [cmd /S /C]
# Wed, 12 Feb 2025 18:33:36 GMT
ENV GOPATH=C:\go
# Wed, 12 Feb 2025 18:33:37 GMT
USER ContainerAdministrator
# Wed, 12 Feb 2025 18:33:57 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Feb 2025 18:33:57 GMT
USER ContainerUser
# Wed, 12 Feb 2025 18:33:58 GMT
ENV GOLANG_VERSION=1.24.0
# Wed, 12 Feb 2025 18:35:50 GMT
COPY dir:c62b8dc6e9060a1c90492bd4af0627f1fb2ef88d5b0c6bad980916fff57ef6a8 in C:\Program Files\Go 
# Wed, 12 Feb 2025 18:35:54 GMT
RUN go version
# Wed, 12 Feb 2025 18:35:55 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Wed, 15 Jan 2025 01:24:28 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21b284e7894cba78b2187f0a9062a1e69204efa965b7c855617d787df369ce2`  
		Last Modified: Wed, 12 Feb 2025 21:33:34 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f92e181bd8460c11e614ac219b4c68f5c90a3de855041ceee9041d868d5a7b`  
		Last Modified: Wed, 12 Feb 2025 21:33:34 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f439609f9a8d353329ffeddf0ec4450cda1b81b6c46e1f3098afae4e1ae263a`  
		Last Modified: Wed, 12 Feb 2025 21:33:35 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7034a06868e5d7f0b988613cee82059b35ea96c0592d39e4b5903e26541ded72`  
		Last Modified: Wed, 12 Feb 2025 21:33:35 GMT  
		Size: 85.6 KB (85646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0447259a259f842f4f16d80529d5799e476195452a69cdde341967d756f738`  
		Last Modified: Wed, 12 Feb 2025 21:33:35 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e9bb59ca15c75b71efe31bb236c8f3bf178590b745dc1e71ce48e0016ab051`  
		Last Modified: Wed, 12 Feb 2025 21:33:44 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69df5060323147e8a7d5e4f04f82db7a32bf26ca6ca8dc77b08c6bcac84ed7d9`  
		Last Modified: Wed, 12 Feb 2025 21:33:45 GMT  
		Size: 81.7 MB (81687553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88713095d8653fcd36d451881d7cab3c2deae9c7091aa4e98df111a04f9182ad`  
		Last Modified: Wed, 12 Feb 2025 21:33:37 GMT  
		Size: 85.7 KB (85748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79d6527b036667faa1f26677beebf77c32933404749d68655c55d74e0ad146b`  
		Last Modified: Wed, 12 Feb 2025 21:33:38 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull golang@sha256:110b97f8ca6b2fc0b94536dc92dbb5c84c93f1587dbc4bc74ed886462e2772d4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237094684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df05420060f5945de3a5efac38c979e1043edf71340bde397d00cffde446bb66`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 12 Feb 2025 18:31:56 GMT
SHELL [cmd /S /C]
# Wed, 12 Feb 2025 18:31:58 GMT
ENV GOPATH=C:\go
# Wed, 12 Feb 2025 18:31:58 GMT
USER ContainerAdministrator
# Wed, 12 Feb 2025 18:32:08 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 12 Feb 2025 18:32:09 GMT
USER ContainerUser
# Wed, 12 Feb 2025 18:32:09 GMT
ENV GOLANG_VERSION=1.24.0
# Wed, 12 Feb 2025 18:33:11 GMT
COPY dir:c62b8dc6e9060a1c90492bd4af0627f1fb2ef88d5b0c6bad980916fff57ef6a8 in C:\Program Files\Go 
# Wed, 12 Feb 2025 18:33:14 GMT
RUN go version
# Wed, 12 Feb 2025 18:33:15 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Wed, 15 Jan 2025 07:23:16 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b68b2823163ecfb785399015ad879d0a832984e9ecb3e53a91234731842bbdc`  
		Last Modified: Wed, 12 Feb 2025 21:33:44 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23f99071263612f7bd104223ca292889bcc0997ba3f0a5490104f889d7c556a`  
		Last Modified: Wed, 12 Feb 2025 21:33:46 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cdb412ddd055b48f06d95c9dc1847b3f747d5f221ccc54b5c0bd2085bead17`  
		Last Modified: Wed, 12 Feb 2025 21:33:46 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2530054e818ee1248724d9c91a73a80cd1e6723d74c71573d23e1c8b42fb92f2`  
		Last Modified: Wed, 12 Feb 2025 21:33:48 GMT  
		Size: 66.3 KB (66321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c8c5d88bb1acd07f4707661ee9970e3bb0a50d261607980fed383161f6ed32`  
		Last Modified: Wed, 12 Feb 2025 21:33:49 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d153455dd7a13f97e8c904ce3175a7c1ee7d30e424246bd5c9a614700c0086e1`  
		Last Modified: Wed, 12 Feb 2025 21:33:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c342ba90bdb0b47ee7f613594a98ba54e941403d38d1baa51dc146fb5a59e4e7`  
		Last Modified: Wed, 12 Feb 2025 21:33:58 GMT  
		Size: 81.7 MB (81686520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c24d0205217ac9f421e7f3e48d082e738ff66d7791d807822eec2f3ff78604`  
		Last Modified: Wed, 12 Feb 2025 21:34:02 GMT  
		Size: 67.8 KB (67790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945780a676d0aefea0c58a87477269db964d87233cb2f50447706f8e69f35dd8`  
		Last Modified: Wed, 12 Feb 2025 21:34:02 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
