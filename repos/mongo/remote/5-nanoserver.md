## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:46b1918bd62576da4cbbcf9198247ce58daff41b08d2e783467943415faa229b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:f56c81de75fa7cc1e856d753f7c2ba10743d773b39d616390776580601d8ddae
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.3 MB (433299801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43338eb4453294ab602cbbb391339759d142b760460b6e9f256c6a8a6f7867f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Sat, 26 Oct 2024 00:49:16 GMT
SHELL [cmd /S /C]
# Sat, 26 Oct 2024 00:49:17 GMT
USER ContainerAdministrator
# Sat, 26 Oct 2024 00:49:30 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 26 Oct 2024 00:49:31 GMT
USER ContainerUser
# Sat, 26 Oct 2024 00:49:32 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Sat, 26 Oct 2024 00:49:33 GMT
ENV MONGO_VERSION=5.0.30
# Sat, 26 Oct 2024 00:49:43 GMT
COPY dir:fd2d6ad81427e0643ec75c35c5a2885caf2411f586ffac83d1ecef0ad3256227 in C:\mongodb 
# Sat, 26 Oct 2024 00:49:51 GMT
RUN mongo --version && mongod --version
# Sat, 26 Oct 2024 00:49:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 26 Oct 2024 00:49:52 GMT
EXPOSE 27017
# Sat, 26 Oct 2024 00:49:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1f04081b73f180a0e6ab4dca8e2a0215475c2a48b7c0afdda8f6dbd4c0d7e`  
		Last Modified: Sat, 26 Oct 2024 00:50:00 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb508b8fbba356d8fbe78809de4ab23b72430ca141775419004fa8c7b9362140`  
		Last Modified: Sat, 26 Oct 2024 00:50:00 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce128bb2ecc2512b418ede664d96bc9997378d7a480fc05dca3bc4df769abb04`  
		Last Modified: Sat, 26 Oct 2024 00:49:58 GMT  
		Size: 85.5 KB (85490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813b6bdf854e7292b736a6af8d3f354a46bf0c057fa51bce0a91dadf189d5aa`  
		Last Modified: Sat, 26 Oct 2024 00:49:58 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2952101b246a9aefea36077db48b32d7f905378b731d0f17523748ebec4b32`  
		Last Modified: Sat, 26 Oct 2024 00:49:59 GMT  
		Size: 275.3 KB (275347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f1eb1b66efe048ca0efa449975d99292719b0c78790dcd1406985607487b7f`  
		Last Modified: Sat, 26 Oct 2024 00:49:58 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ae58c21fd8af769c17e5a24a1866585494a42cd5870fa53d157b124b08b9ac`  
		Last Modified: Sat, 26 Oct 2024 00:50:28 GMT  
		Size: 312.3 MB (312323784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8199af6c2aab755bfad9c5bed19276dbdb195d2d504996e3fb46757cdcc75703`  
		Last Modified: Sat, 26 Oct 2024 00:49:57 GMT  
		Size: 96.7 KB (96712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556c24939123fe883d291d1ae31f09ce265ad33dd10e2749bd2fa128990dff55`  
		Last Modified: Sat, 26 Oct 2024 00:49:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9798563d4fc3100b0677627158f8e739b27ce2aa33727bea2c2080321e90c50b`  
		Last Modified: Sat, 26 Oct 2024 00:49:56 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19ff394268233578620e6d38649d6ae8532a2a45088056ef272ded1b7831354`  
		Last Modified: Sat, 26 Oct 2024 00:49:57 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:0ba88d9c11799bf78b6ac6feacd2de1014a35350f432f6a48cd918d0a4bf0edf
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.8 MB (467840241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d075523a8847c80120dabd189e5eb9628af395e0fdbc58c2532cff6e58d25ebf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Sat, 26 Oct 2024 00:49:11 GMT
SHELL [cmd /S /C]
# Sat, 26 Oct 2024 00:49:11 GMT
USER ContainerAdministrator
# Sat, 26 Oct 2024 00:49:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 26 Oct 2024 00:49:21 GMT
USER ContainerUser
# Sat, 26 Oct 2024 00:49:23 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Sat, 26 Oct 2024 00:49:24 GMT
ENV MONGO_VERSION=5.0.30
# Sat, 26 Oct 2024 00:49:47 GMT
COPY dir:fd2d6ad81427e0643ec75c35c5a2885caf2411f586ffac83d1ecef0ad3256227 in C:\mongodb 
# Sat, 26 Oct 2024 00:49:50 GMT
RUN mongo --version && mongod --version
# Sat, 26 Oct 2024 00:49:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 26 Oct 2024 00:49:51 GMT
EXPOSE 27017
# Sat, 26 Oct 2024 00:49:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51620adaceb2cb5a891597652042c56576b475a269371cc2b08ebd905e85c0ea`  
		Last Modified: Sat, 26 Oct 2024 00:49:58 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bde32ada453ebc4725e467e02f32dad4bd1f9dc52c15667b03df423d261cbb1`  
		Last Modified: Sat, 26 Oct 2024 00:49:58 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:488334957e3d84eab5107e4f7f263556bfe574984b5fc58524510bd62b6fe9b1`  
		Last Modified: Sat, 26 Oct 2024 00:49:56 GMT  
		Size: 66.0 KB (66044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b6f63e35ffadc3e7145feb3d4abc4d571dd17c5eb354c7db6a7b5fb14fab1f`  
		Last Modified: Sat, 26 Oct 2024 00:49:56 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24115b8f2f357eb05f055f39ee4d31f4f8d9f42a8b294b97ed666bc5d09fcb94`  
		Last Modified: Sat, 26 Oct 2024 00:49:57 GMT  
		Size: 275.3 KB (275335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cdeb08c8ebd8a3c5947725db56b07fb73b48fc8389a9cc94c31578d149f53b`  
		Last Modified: Sat, 26 Oct 2024 00:49:56 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d626fca5873ab91ea135286bcb43d0a5c2bedcd185799ece0f6e0d77cf2fc88c`  
		Last Modified: Sat, 26 Oct 2024 00:50:26 GMT  
		Size: 312.3 MB (312323863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e63f12c58de2f1d2ea8a31834be122c2f2e98ec2a2e0ca1d94576c910e7745`  
		Last Modified: Sat, 26 Oct 2024 00:49:55 GMT  
		Size: 74.0 KB (74018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad93cb744e8fcf9884edf94e641ac1bb7ee19c555d6bef7cc6b2e6bc71197a2`  
		Last Modified: Sat, 26 Oct 2024 00:49:55 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417c64d8eaf15291b3149c7a6307fc7f6e59e5a42a111aaff2f2a914df209558`  
		Last Modified: Sat, 26 Oct 2024 00:49:55 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c6aa2e9f65399a9b212c9c708be655ca24d8b1e8bba9a29ebc099eb144d0da`  
		Last Modified: Sat, 26 Oct 2024 00:49:55 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
