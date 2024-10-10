## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:a27d4eb5691e98e083f0b884044e05dd6db9cfc727fa58e870835b21c140c3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:6216edce19a91a6ec5c2e454509d186872fd7fc0ece442e103ca34b890ef2de0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **729.4 MB (729418969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01a3127b7a322b05cb566a51eeeaca8bf57aaf3b126ea5107a1cffae76e57e7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:01:04 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:01:04 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:01:06 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Oct 2024 00:01:07 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:01:08 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 10 Oct 2024 00:01:09 GMT
ENV MONGO_VERSION=7.0.14
# Thu, 10 Oct 2024 00:01:28 GMT
COPY dir:569dc595e568429f713bfa17916f5a0425b14e2551565b8dcffbac1d9a45d806 in C:\mongodb 
# Thu, 10 Oct 2024 00:01:44 GMT
RUN mongod --version
# Thu, 10 Oct 2024 00:01:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 10 Oct 2024 00:01:46 GMT
EXPOSE 27017
# Thu, 10 Oct 2024 00:01:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370d12217143fe181ca9c26783b6aaa68c89c7400f216894711362fc4427ec69`  
		Last Modified: Thu, 10 Oct 2024 00:01:52 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e976fb00e6fbf26b09484cd85e4e97df638efd14258e5da27f81c6c3df312b35`  
		Last Modified: Thu, 10 Oct 2024 00:01:52 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4a93b2304af2a41eaf0b06cff393d550aa7a68af365ac9e7588bf2a25b7e4c`  
		Last Modified: Thu, 10 Oct 2024 00:01:51 GMT  
		Size: 75.4 KB (75410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a98ee142c8b8688c8c14110df65fa7f0209ead56d5c4234ebf718267ba52b19`  
		Last Modified: Thu, 10 Oct 2024 00:01:51 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542b5863a25ae219f8c568ebfb34ff0145420fe0503d8d29182482fbbed5c8a`  
		Last Modified: Thu, 10 Oct 2024 00:01:51 GMT  
		Size: 275.2 KB (275166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a46329a1c9c00d09e58c49406520c56619e13b964262ff4252c22d446eb84989`  
		Last Modified: Thu, 10 Oct 2024 00:01:51 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b316234867668ea71b506c224c7dd8d38c99396fbdd8c995682de587082625`  
		Last Modified: Thu, 10 Oct 2024 00:02:37 GMT  
		Size: 608.5 MB (608452565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2952e2bd9fc5778aa20885ace11148c5eef67bdde7a4ff7e0b9af340c55c3026`  
		Last Modified: Thu, 10 Oct 2024 00:01:50 GMT  
		Size: 97.6 KB (97608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6354488ae527347951d011ccdf031e70d09c52dc10a7ca8cfddf55ca7622660c`  
		Last Modified: Thu, 10 Oct 2024 00:01:50 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa64f1e3beb2aa659fc3c66ae6683e01fd12a892d1a7260970f858cba4c8f85`  
		Last Modified: Thu, 10 Oct 2024 00:01:49 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30edba0ba4ca7f678146a593f56cba9b40cd9499bb6ce4af991723f5b5dac1c3`  
		Last Modified: Thu, 10 Oct 2024 00:01:49 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
