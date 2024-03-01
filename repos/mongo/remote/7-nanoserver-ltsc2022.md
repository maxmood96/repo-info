## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:7fd4194cd3fb658787dab0e9625cadba6ba06a729cd3c049276c53aba22c9772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull mongo@sha256:0886f9e502bdb7ec6a1be161122ec1c203b3a810fd670105e7b9089529d52ffb
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **735.0 MB (735011252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e306ab1c5b7afd24ee194969daf44e24f7f1e4a240524951f077b74a783d714`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 07 Feb 2024 06:29:10 GMT
RUN Apply image 10.0.20348.2322
# Fri, 01 Mar 2024 01:50:19 GMT
SHELL [cmd /S /C]
# Fri, 01 Mar 2024 01:50:20 GMT
USER ContainerAdministrator
# Fri, 01 Mar 2024 01:50:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 01 Mar 2024 01:50:36 GMT
USER ContainerUser
# Fri, 01 Mar 2024 01:50:37 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Fri, 01 Mar 2024 01:50:38 GMT
ENV MONGO_VERSION=7.0.6
# Fri, 01 Mar 2024 01:51:09 GMT
COPY dir:760432e495467387aee1f5ff3c4832ced81799e4ea6e068f15089694b9856264 in C:\mongodb 
# Fri, 01 Mar 2024 01:51:22 GMT
RUN mongod --version
# Fri, 01 Mar 2024 01:51:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 01:51:23 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 01:51:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:ccff18da882d371921351307d169380d3ac22ef981f2bb4f14fb2b332b395439`  
		Last Modified: Tue, 13 Feb 2024 23:39:47 GMT  
		Size: 120.7 MB (120735093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d481fb96623af8e53965f8ed7a78d4b51ad02860719a7a3b98db0db0e6bd0ef1`  
		Last Modified: Fri, 01 Mar 2024 01:51:33 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc50c35516cf1d0963576fb5801c2bd8479e89507dad2e45ad9c4d9c6c642643`  
		Last Modified: Fri, 01 Mar 2024 01:51:32 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a271e983d1ff672d70c16e6b6840ba6ceb24225cffa86d68b35902db3410c4e`  
		Last Modified: Fri, 01 Mar 2024 01:51:31 GMT  
		Size: 75.1 KB (75071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ca601b0d8dc6d06949a8d92994c34409ffc3a88e5ad86cdea6061b3dc55543`  
		Last Modified: Fri, 01 Mar 2024 01:51:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3394e2492bb001a692d6d8851afeb0ada5b1bacd0e589214703fd5063701f02e`  
		Last Modified: Fri, 01 Mar 2024 01:51:31 GMT  
		Size: 267.1 KB (267081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa7fad85b702994fb4a67020cfab54536e2303a8772f25c4c5c1a3f7cf6e971`  
		Last Modified: Fri, 01 Mar 2024 01:51:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2cb433e215cc2dcf2e0459d29c8a6dc4e6b8619ff0a8581a724eaf25acc77a`  
		Last Modified: Fri, 01 Mar 2024 01:52:19 GMT  
		Size: 613.8 MB (613839132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc9aeee8e09c1c92f91c3193a23f7c5ae48b786712a6740eded141cfd6a10f1`  
		Last Modified: Fri, 01 Mar 2024 01:51:28 GMT  
		Size: 87.5 KB (87499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadec52a4248bbd06d1c51a324384659cc9fde36fa30e3dcc98867b0643af0e0`  
		Last Modified: Fri, 01 Mar 2024 01:51:28 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3b9d226c7a4839fcbc6bc0451578e07b406c90c02d12153af69e972f39b7f3`  
		Last Modified: Fri, 01 Mar 2024 01:51:28 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f34f3e5fef4c702c680b261c123a1944e8052d468074ba1a59bf85130f25fe`  
		Last Modified: Fri, 01 Mar 2024 01:51:28 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
