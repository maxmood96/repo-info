## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:adb8ed8626b392e75551a728379eb14f3d620fb2c886ca4fddf4ce5351cd8d0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:e033a63af1cb7fd4335b27eff971292f1332af20b17f79cf7d5b1b47bf025353
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.0 MB (468032795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972eb2d9154a37bfdacad0612cb77d5b85dc7d7b9b51e5ca983b9b86201c8d90`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Wed, 15 Jan 2025 18:02:44 GMT
SHELL [cmd /S /C]
# Wed, 15 Jan 2025 18:02:46 GMT
USER ContainerAdministrator
# Wed, 15 Jan 2025 18:02:49 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 15 Jan 2025 18:02:49 GMT
USER ContainerUser
# Wed, 15 Jan 2025 18:02:51 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Wed, 15 Jan 2025 18:02:51 GMT
ENV MONGO_VERSION=5.0.30
# Wed, 15 Jan 2025 18:03:04 GMT
COPY dir:fd2d6ad81427e0643ec75c35c5a2885caf2411f586ffac83d1ecef0ad3256227 in C:\mongodb 
# Wed, 15 Jan 2025 18:03:10 GMT
RUN mongo --version && mongod --version
# Wed, 15 Jan 2025 18:03:11 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Jan 2025 18:03:12 GMT
EXPOSE 27017
# Wed, 15 Jan 2025 18:03:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88cd48f3272d95bd9629261944cd03ef6f390359e3abb733248d093cbecee171`  
		Last Modified: Wed, 15 Jan 2025 18:03:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7951693f406bc99298239aed5df1982684ede58962126db9dc59ccd4b8d843cd`  
		Last Modified: Wed, 15 Jan 2025 18:03:17 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02260f179d81f182fa12e11b2f6e5ecb819977ad4a41f5d9ab17e2b796a9256d`  
		Last Modified: Wed, 15 Jan 2025 18:03:17 GMT  
		Size: 83.4 KB (83391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab0102bde680959fb17ba75bfb9bfb83075e228cde59e106097a42e78048bd0`  
		Last Modified: Wed, 15 Jan 2025 18:03:17 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b4e97ce7b056fcd5a4caef2cb0dc6d309c431f39fd8f4f3aad67bfcb7dd469`  
		Last Modified: Wed, 15 Jan 2025 18:03:16 GMT  
		Size: 275.4 KB (275409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95053eccd029a0911267010e2570031c984686c1ea2f092a967b3f0ce82370bd`  
		Last Modified: Wed, 15 Jan 2025 18:03:16 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520b321afcc96e0e5a6ca129dc0b2b4c9d50a4f88dcf168f2bb4bcb4aaa696da`  
		Last Modified: Wed, 15 Jan 2025 18:03:46 GMT  
		Size: 312.3 MB (312323778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10141b7d88f75cc6b44ece35d398af9ad17961980c64f157db96661f6e80d9e4`  
		Last Modified: Wed, 15 Jan 2025 18:03:16 GMT  
		Size: 75.1 KB (75074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c26ca8ef96a9928311762d66fcfee8bd0966dcac63c1e7d1fe073fd6d60fa94`  
		Last Modified: Wed, 15 Jan 2025 18:03:15 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94c5af3a73455c2daafdd53cc002add54fb052265c893b69fbcc01add947113`  
		Last Modified: Wed, 15 Jan 2025 18:03:15 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6d98c92c02b7cf7b03709a0d2031836dac7d5a200203812fe82588303e33da`  
		Last Modified: Wed, 15 Jan 2025 18:03:15 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
