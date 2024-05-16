## `hello-world:nanoserver-ltsc2022`

```console
$ docker pull hello-world@sha256:cbb8ca5fd29d2bd3aa59645da5cc22cc58a6ce592a47b9528c9c56e51b150260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `hello-world:nanoserver-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull hello-world@sha256:f4654ac0dc6f5131e8f45fe72cda1db4a5e793ad77c44b2e3d79481293f172d5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.4 MB (120428106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4631467d82ac6a5fa7217c695fd90da48c2e9b8e7fe9c33170c068b10f194ef5`
-	Default Command: `["cmd","\/C","type C:\\hello.txt"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Wed, 15 May 2024 21:51:29 GMT
RUN cmd /S /C #(nop) COPY file:cdba4efa08a1e42c8764fb75c060ef33719f72777fb28a7592f718539560d6d2 in C: 
# Wed, 15 May 2024 21:51:29 GMT
RUN cmd /S /C #(nop)  CMD ["cmd" "/C" "type C:\\hello.txt"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e645cb32b4955685922c4e20d98142adf1ddac9b4d357b568483c8f51ba2e76`  
		Last Modified: Wed, 15 May 2024 21:51:33 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be193c9d7cda6f2ebbc3f95e5894036d95a9c05b3155f65deda6b8c3e78f6543`  
		Last Modified: Wed, 15 May 2024 21:51:33 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
