## `buildpack-deps:noble-curl`

```console
$ docker pull buildpack-deps@sha256:60f0ba25efae8cc974ed113e1b9c9e62ae3f21fc63c6ea1aa41bc8af13704eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e871ce4fefe194ad023e3d00d740681e93aea65068d6e9e2ca35409605ee16ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44038436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9521c467ffb4e332766da6de9453b76f101586bd9c0becdb05ddd1be0114b5a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 15 Jan 2024 08:48:30 GMT
ARG RELEASE
# Mon, 15 Jan 2024 08:48:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 15 Jan 2024 08:48:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 15 Jan 2024 08:48:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 15 Jan 2024 08:48:31 GMT
ADD file:e5e7262b8cac5f725d4433779ecfbcadb4025759c5973a276b344033d087bfb3 in / 
# Mon, 15 Jan 2024 08:48:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc35f4f5ecaa073076bdb6773257cebc5c5f2ad32bf5f3c21b5f0f462cc825ab`  
		Last Modified: Wed, 17 Jan 2024 07:40:47 GMT  
		Size: 30.3 MB (30313466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fc63ab3c7470561d0ea5fde5977e2154db737dcd470c977cd0202fbe1cb86d`  
		Last Modified: Wed, 17 Jan 2024 08:04:45 GMT  
		Size: 13.7 MB (13724970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cc36a047bedb9cc2d55e5df5c556fea75120543f367636d278c86916503d230f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40634194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185cd3292d981b14a4a9da76e47837fc33c43a4f484df3f411d01accdf05ea73`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:22:39 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:22:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:22:39 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:22:42 GMT
ADD file:1a0a51108f4f8e0b235f7272452d282ea13f08d47f16682fe7692f82c4257d18 in / 
# Sat, 27 Jan 2024 16:22:42 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:04:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ac0f5659d9dfd5db0bb4d4c61abc9180fe37bd866eee19911008c648d692a0c4`  
		Last Modified: Fri, 02 Feb 2024 00:12:28 GMT  
		Size: 27.6 MB (27601561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecef6eb383bc18ee41099cc94d04bbad13554a3011ca70d490e046952db78372`  
		Last Modified: Fri, 02 Feb 2024 00:12:25 GMT  
		Size: 13.0 MB (13032633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c3ac3862c3e006742a029ecc60a2324222014ae8acf92a92e864451300f16eb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43129358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20e4cd1f5ca7574d960350c4476a93934e8b200b646786f0b1f5f0a1d2c9f50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:43 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:44 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:46 GMT
ADD file:adde4f5257d5ea38278d90dc23be17284b3c2333b30731e6b86080865fd59de9 in / 
# Sat, 27 Jan 2024 16:15:46 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ceb92793415662e19f5052b0757011d646031bdbf61f6bfa10f837029f4cebb8`  
		Last Modified: Fri, 02 Feb 2024 01:10:35 GMT  
		Size: 29.6 MB (29630733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78252bfb9c4675120fb2a320c323420049d3210b292a7e8e590c5126a658`  
		Last Modified: Fri, 02 Feb 2024 01:10:32 GMT  
		Size: 13.5 MB (13498625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5fe711c6d187cd2610330c0b96c0f9dec93528cc14f293b933464d372a3a34d9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51137492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3db055a19de7e40cf0853a4d278999e4b94b60b10682c6ad3299c116af6dc6c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:12:36 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:12:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:12:36 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:12:40 GMT
ADD file:8c4529e75ecb0afb5c75c9af064159ccac9d60e92fda7b7bc89c6efceaf9ce0f in / 
# Sat, 27 Jan 2024 16:12:40 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 02:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91cc9b0029ac8c87fcb7bd83a83d8bae90aee017cba86cd0c380295bf039d7fe`  
		Last Modified: Fri, 02 Feb 2024 02:35:55 GMT  
		Size: 35.1 MB (35134339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f09f6e4ff56b26367840241be4fe0f13bfba14856fd153dceadb831570cb779`  
		Last Modified: Fri, 02 Feb 2024 02:35:49 GMT  
		Size: 16.0 MB (16003153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1f366059ff359089d1d3b5fa5c8dbb3949f5a860a1145f6f4b9e45e1d2b843a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45248014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eceae813ef2bc4fe810bca45196a3a1dd14a5e691438a470cfca40405e46413`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:37 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:37 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:39 GMT
ADD file:7dd6a1a2ef765af3feba0e026e0d3c5c0d1793c106b572fe316a5265d8f715b6 in / 
# Sat, 27 Jan 2024 16:15:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 01:24:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:613ff254a56e5e32a5cef69ec3d0423f8c34e54c150269e6d7b755b5d2aa8515`  
		Last Modified: Fri, 02 Feb 2024 01:35:43 GMT  
		Size: 30.3 MB (30319501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeecfce9669b97c510f67dd6aa25593fbd474c1d056f87af305f67daca9644de`  
		Last Modified: Fri, 02 Feb 2024 01:35:41 GMT  
		Size: 14.9 MB (14928513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
