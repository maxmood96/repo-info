## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:7033252bbf8f674defe3abb4ccf9776d33f5b1a448e6e2eeb8db1c84d9684ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2322; amd64

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

### `mongo:7-nanoserver` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:ce5d35ff388d78003452f9e18d19c6bb1d60c44f6a7de67008fba5db6ad2a1c1
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.9 MB (718870106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f80f84bc1175a956b53e71d1212890fb674e4f88d100aa9aaf5ceadd5dcf6c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 04 Feb 2024 03:35:01 GMT
RUN Apply image 10.0.17763.5458
# Fri, 01 Mar 2024 01:50:29 GMT
SHELL [cmd /S /C]
# Fri, 01 Mar 2024 01:50:31 GMT
USER ContainerAdministrator
# Fri, 01 Mar 2024 01:50:44 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 01 Mar 2024 01:50:44 GMT
USER ContainerUser
# Fri, 01 Mar 2024 01:50:46 GMT
COPY multi:445ddc7f71a3d8383cf14aa8dec6f6b258e3dd2f8f8ff8d8cc45274175ab98de in C:\Windows\System32\ 
# Fri, 01 Mar 2024 01:50:47 GMT
ENV MONGO_VERSION=7.0.6
# Fri, 01 Mar 2024 01:51:33 GMT
COPY dir:760432e495467387aee1f5ff3c4832ced81799e4ea6e068f15089694b9856264 in C:\mongodb 
# Fri, 01 Mar 2024 01:51:44 GMT
RUN mongod --version
# Fri, 01 Mar 2024 01:51:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 01:51:45 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 01:51:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:81be0bec766f944241448cd25317f59edcb12514e41b43288302e3e88d5462ad`  
		Last Modified: Tue, 13 Feb 2024 20:17:19 GMT  
		Size: 104.6 MB (104621606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f9db237f3065ad930f0954f00204d03ace32dc7e7baf52bb04dd02db3a5320`  
		Last Modified: Fri, 01 Mar 2024 01:51:54 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6813022c95dde79847239f26f6c6909c5b5f6e94cf83495c45c14f8c136d3b0d`  
		Last Modified: Fri, 01 Mar 2024 01:51:54 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a035cf52539676ed9ccde85bfe776e12edd50b9c96a8bfeaac83806933f3216`  
		Last Modified: Fri, 01 Mar 2024 01:51:52 GMT  
		Size: 67.2 KB (67221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f903509fc43a51dc21a1b357592eece9918b0fb8d7cd2ef4ddf236ed329465`  
		Last Modified: Fri, 01 Mar 2024 01:51:52 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d69d4cb95d7c5021290942eb5b6b49533eac67b0c14e58c86ed9ea594c2e82`  
		Last Modified: Fri, 01 Mar 2024 01:51:52 GMT  
		Size: 267.1 KB (267074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5fb83e8a85d5ca2598e65941228d8fb9f77d35f7b0a45cd738a6378f290388e`  
		Last Modified: Fri, 01 Mar 2024 01:51:52 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12a8f5e2e25dcf9183eb80a2f4c93b716710217cb2f8dbb5e3a51a16ae249d3`  
		Last Modified: Fri, 01 Mar 2024 01:52:42 GMT  
		Size: 613.8 MB (613839337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d56a0d79b89f1b828c35814daa42c0936847cca36d1d3e68f17921aca879e65f`  
		Last Modified: Fri, 01 Mar 2024 01:51:50 GMT  
		Size: 67.6 KB (67604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:970b96435cc8d976bb5e6a0cb811e9f82d4b3cc01dd1e0f59c7107b62acc15be`  
		Last Modified: Fri, 01 Mar 2024 01:51:50 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c38e73e43e346ba90b95f2a13e434513b0ee8acda0b7c06c10451a690bfafba`  
		Last Modified: Fri, 01 Mar 2024 01:51:50 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf79908930778a9eb253d9b04ec61be0aa20ea3de98f7672d9d14b42e3b50e8`  
		Last Modified: Fri, 01 Mar 2024 01:51:50 GMT  
		Size: 1.0 KB (1021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
