## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:b0177a900502e016454a0addafb345f8fe9670e39a5bf2828bb69b6b192f76a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull mongo@sha256:cf9042c9810f2cd08010816684d4d2773e7d6280f081976303679c9120413820
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.7 MB (468693939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23542444c8db4cc386a80ba5216bed4ea5304501d4420291c008fde75f5237ac`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Tue, 16 Jul 2024 00:59:40 GMT
SHELL [cmd /S /C]
# Tue, 16 Jul 2024 00:59:40 GMT
USER ContainerAdministrator
# Tue, 16 Jul 2024 00:59:42 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 16 Jul 2024 00:59:43 GMT
USER ContainerUser
# Tue, 16 Jul 2024 00:59:44 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Tue, 16 Jul 2024 00:59:45 GMT
ENV MONGO_VERSION=5.0.28
# Tue, 16 Jul 2024 01:00:00 GMT
COPY dir:c6fb9bb5026b802847b6d98141fdf6e729cdbfa7e4090c9061f0a80c174c27e2 in C:\mongodb 
# Tue, 16 Jul 2024 01:00:09 GMT
RUN mongo --version && mongod --version
# Tue, 16 Jul 2024 01:00:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 16 Jul 2024 01:00:11 GMT
EXPOSE 27017
# Tue, 16 Jul 2024 01:00:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec55a647dd19179c2ccf1afd39a4b36eb1484fffc9b37e5f8778502f6937702`  
		Last Modified: Tue, 16 Jul 2024 01:00:16 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f89df96bb84a4e35d81f2575b141957b46e5a43df99265a83abbb1db7e6697`  
		Last Modified: Tue, 16 Jul 2024 01:00:16 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2194069b12fe98205f37183634bcab83fcdff5cc64606612c08cbb60a297030`  
		Last Modified: Tue, 16 Jul 2024 01:00:15 GMT  
		Size: 72.6 KB (72609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c913654b0f1fcd5ec3e9325177999cdf0f96490a6f2267e45c740b9a3bd472a`  
		Last Modified: Tue, 16 Jul 2024 01:00:15 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0aa5a7fe95dd5c27a737b5465306a4be948c68f5499563dc52fbd1123a62c82`  
		Last Modified: Tue, 16 Jul 2024 01:00:15 GMT  
		Size: 275.3 KB (275332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f71451ea80a538bc3b88c23a5ec1792770b70f6ce7417d0a8e6faba3311d255`  
		Last Modified: Tue, 16 Jul 2024 01:00:15 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2d6f914bc1088124e2096dfe07404d66eb4b1ec48e00a086d3f90cf1029547`  
		Last Modified: Tue, 16 Jul 2024 01:00:43 GMT  
		Size: 312.1 MB (312075884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b20f37fc5b0dddfe86770b87a11a0eb94a1c7e240bd16ac863c18f4f37dd41`  
		Last Modified: Tue, 16 Jul 2024 01:00:14 GMT  
		Size: 1.2 MB (1181452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196f74ecdf2f8e11e09a484eb3e0d5349f36ba0f581dde9cc58c1b17f936d8ea`  
		Last Modified: Tue, 16 Jul 2024 01:00:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad3fedfc31be9a4d6301cdb5ee1c2df51a4d56c21322e4b51b7835e5996a301`  
		Last Modified: Tue, 16 Jul 2024 01:00:14 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb42c7469f3700c965519f353f5c5ca130be5bfef4fcb6969cdaba3a578cfc91`  
		Last Modified: Tue, 16 Jul 2024 01:00:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
