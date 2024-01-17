## `buildpack-deps:jammy-scm`

```console
$ docker pull buildpack-deps@sha256:b0ba0c946dae1f01cf6feceed702887e6b1d4374023005aff14f6083e721f571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:jammy-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d2ec9d5e77fca2e25694581edc7384ddcabbf54effe845515dfd1eeceee103e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77022432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06508ce5069f41f2ef1a5b557c8bab3798f16e825f168376e29ba085f2c23b42`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jan 2024 17:08:09 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:08:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:08:09 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:08:11 GMT
ADD file:c646150c866c8b5ece67bc79c610718acf858034fa22502b0dba3d38c53fc9a9 in / 
# Thu, 11 Jan 2024 17:08:11 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:56:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df2fac849a4581b035132d99e203fd83dc65590ea565435a266cb0e14a508838`  
		Last Modified: Thu, 11 Jan 2024 22:28:44 GMT  
		Size: 30.4 MB (30447114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2647588b39c1ae97d7d86da7aedf16b58f01f8e641498f2c56841a73562414a6`  
		Last Modified: Wed, 17 Jan 2024 08:03:47 GMT  
		Size: 7.1 MB (7124790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeee2c0e955dc3243d8d42730a80feac6d9c5a8f97661af30a37628ae59f1b12`  
		Last Modified: Wed, 17 Jan 2024 08:04:02 GMT  
		Size: 39.5 MB (39450528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d89cc9dbce16a004ea0bf696fa2d6b2c58e8a2227ea1936ad2ee919dbf826d43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76786402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a782b4f6ca411dfc5268b81c0271bb2c4a35bd601c770dc3567b19689329c94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bd71537214026ea993ab6e8967640e8c1258fb3402403fb3f72092e6b932621e`  
		Last Modified: Tue, 12 Dec 2023 18:24:48 GMT  
		Size: 27.5 MB (27524114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f559c61726ab4c77beb9643a16071b714621010ce892e4b513e2f661afd80fc`  
		Last Modified: Sat, 16 Dec 2023 09:28:45 GMT  
		Size: 7.0 MB (7020312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7466dfabd4c33ed2d2c28622506ac89b77492431ede47afb99c18da6ffd3b35`  
		Last Modified: Wed, 17 Jan 2024 02:26:05 GMT  
		Size: 42.2 MB (42241976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8a9677ccc988b79659abd1fdd08fb5c96d732e108267a72d98390313c2f535d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74835494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b642460571a2fe40728c2e8b7e0e4e88b38c257e3043055a445e786afc19097c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jan 2024 17:03:13 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:03:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:03:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:03:15 GMT
ADD file:5703a6689620ec495e864cfc12e80f8b2ee9e69b1a7b7365bf80955ba05a53ab in / 
# Thu, 11 Jan 2024 17:03:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:16:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:16:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc8daefb9978b7f23cfc73ae68e998e85ee72a68588997321b1697cb0b9926df`  
		Last Modified: Thu, 11 Jan 2024 22:46:38 GMT  
		Size: 28.4 MB (28399616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214d6f1ae0d04803143a94a87787945df12a6d7f69a0dfb259206bc41ad52b99`  
		Last Modified: Wed, 17 Jan 2024 07:26:35 GMT  
		Size: 7.1 MB (7070014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad1e6015026b96db79bdeec38b82ab7b61900c949fad1ee47aec4b5a88d8a8a`  
		Last Modified: Wed, 17 Jan 2024 07:26:47 GMT  
		Size: 39.4 MB (39365864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9f8b7dc1b718fe84e2fd9a0f4808f1cfe25f5dd1b1f20cf483e146fe7277d45c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87666594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eea317379886f86b9d03df1ccfdb125a20c2c7ca3d58dae1ed9096b75705a7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jan 2024 17:10:02 GMT
ARG RELEASE
# Thu, 11 Jan 2024 17:10:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 11 Jan 2024 17:10:02 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 11 Jan 2024 17:10:06 GMT
ADD file:4da6fb9ba29da03fa46ed73abfae01fa7c87f2c26044ee297c88359085392aef in / 
# Thu, 11 Jan 2024 17:10:06 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 07:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 07:42:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:898e4a5fe680690395e7fd9d920dfa248b7508ec0573741c491bf250179ddbda`  
		Last Modified: Wed, 17 Jan 2024 05:26:53 GMT  
		Size: 35.7 MB (35657152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deefa4f7a96d6263924ac0bec9c236b9ad2714d4067b4f5242e3a30e4d63359b`  
		Last Modified: Wed, 17 Jan 2024 07:57:37 GMT  
		Size: 8.2 MB (8246088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae567add9697d98202161b02ff9529b6aa5347992bd168ae2af36a618dc148f`  
		Last Modified: Wed, 17 Jan 2024 07:57:52 GMT  
		Size: 43.8 MB (43763354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jammy-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b2271ea8de3eb467d6e153560a451338701f678c6e6a6156d5cfd324144bbf90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75105038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46daba83613435538f0cfe4a10c93e13270d6600b3d38249cc0c0582b92f05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:39:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4f71268cf82327e178d918af83f77f72e772a9c3aa221dc9ab4b5ca43e1485`  
		Last Modified: Sat, 16 Dec 2023 07:42:39 GMT  
		Size: 7.0 MB (7034212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a82b0cb967f75c8219badebd3a82aadc0a08c918062c30325af18eeb6ac787`  
		Last Modified: Wed, 17 Jan 2024 04:07:28 GMT  
		Size: 39.4 MB (39416273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
