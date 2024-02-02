## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:b81fdade78b8b1e869074cce995fa469e91098620b052116ffd5e447a749e70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b6073290ef0f60f574d99cee8ba218b5aba7a28aad18a2479d69b0e25a96bea3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89511003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612678d4ea5037c12149c14ef1ebc742351224680e67be24b209970346cc7975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 27 Jan 2024 16:15:22 GMT
ARG RELEASE
# Sat, 27 Jan 2024 16:15:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Jan 2024 16:15:22 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 27 Jan 2024 16:15:24 GMT
ADD file:dc9fb0ed3a650c89a500aae31f5c47e13e9ec29bfe109f890faf9e86f8c49cbc in / 
# Sat, 27 Jan 2024 16:15:24 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:17:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 06:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c7b0d57ce5e9ca2a7fec0ccf889c85acec4f977152802e1d84c4359f4f0cf7a4`  
		Last Modified: Fri, 02 Feb 2024 02:17:16 GMT  
		Size: 30.4 MB (30405589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce34b814e1d4069681e2c3b5c647e27920db44fd6bc67e19a3918dc34b075cc`  
		Last Modified: Fri, 02 Feb 2024 06:25:52 GMT  
		Size: 13.7 MB (13712421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2accc45dfab8442a66b0b0fe52964433bb916c6f2b1bb82fa2b89be9c71044c7`  
		Last Modified: Fri, 02 Feb 2024 06:26:10 GMT  
		Size: 45.4 MB (45392993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fac4169eae6a3f6283eafacaa645e32354bc56bbedc8da044333e32267cd1130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90223032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f565b6c40c58d5dda1e1db5b668136d39e000e914133e327904c544859ddbb4`
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
# Fri, 02 Feb 2024 00:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:23569f813ab6f239b230aecd3b3f680f19a5269e8d75eac5b6d08abd958163a8`  
		Last Modified: Fri, 02 Feb 2024 00:12:44 GMT  
		Size: 49.6 MB (49588838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:61276946f6f4513a27445e72c96098c78ffe9c710109368316d9e0bc0dce7220
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88566245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0655810e0ec8369892b7d36859a679a4888cdbf9ec433c61d9d3da88f15332d`
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
# Fri, 02 Feb 2024 01:03:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:8159f43017c60d8344e15f48838483bd0c388de3ec837523fa33997c5abcf747`  
		Last Modified: Fri, 02 Feb 2024 01:10:50 GMT  
		Size: 45.4 MB (45436887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5eaa7f8b58b6d2c825bbba41bfbb85982b92b1960ff9459d28c461c6e3122b7a
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101622059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48d71384d4a15432f007a06fdfb41ef88f3e52c81e42193a54ca861be9acd51`
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
# Fri, 02 Feb 2024 02:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:bba806b1584e9dffae35ccf06c2af9e7cbfd293a0fab95bbaf06abb4786f1004`  
		Last Modified: Fri, 02 Feb 2024 02:36:15 GMT  
		Size: 50.5 MB (50484567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:75586fcdbd103426a67ed8ba26a9e6adf2e9331c80b6c31075c9927178766d16
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92111580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7b796bcb4409b4e58436d933a27a24e749e933c6a5a267d513b6081fc4e5cb`
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
# Fri, 02 Feb 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:850e1ed4384dfa6da051412846b24fc4182a18620863cd54092878378deef24d`  
		Last Modified: Fri, 02 Feb 2024 01:35:55 GMT  
		Size: 46.9 MB (46863566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
