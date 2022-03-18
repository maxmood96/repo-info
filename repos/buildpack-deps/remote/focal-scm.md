## `buildpack-deps:focal-scm`

```console
$ docker pull buildpack-deps@sha256:7f90e55c58e7b284347c238a6f68f97b263a0abdf90cb7e2cc7a5556e1707af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:70409f3775d04f8397e1f10229c9438fbce0293da8025c379209c085daa49aa5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100679028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bdb35d8abb8f4bb364cbfb500ba1e5f5d714d6648a0f83bfba6219a2b0c756`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:44:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:45:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e116ffc838f0cc3660ba0025acde46283eca99aa80f9c11e46acc54b9cdb38`  
		Last Modified: Fri, 18 Mar 2022 07:09:58 GMT  
		Size: 7.8 MB (7769076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3295af90e4ff2d1c9c70f7c1d5fa7237dc821ae85afe3acda9ad3ad1167c9a64`  
		Last Modified: Fri, 18 Mar 2022 07:09:57 GMT  
		Size: 3.6 MB (3624149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae303957626da270ae0a18ae12a485a84996eeb9ddaf8adc325f8ff08a5f9243`  
		Last Modified: Fri, 18 Mar 2022 07:10:18 GMT  
		Size: 60.7 MB (60719894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:aa7d7634c8e0830f4d2d198096c684d2aa0edb7e7551b33ff0b202d8d3e5b329
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89395957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ae85870f0d41449889f9ef9b8c29b50aa763d4b02a8c725bcd546285c8326a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:31 GMT
ADD file:984d3d8b31abd025bb9be52f42d60245a76b1ee991f286db819ae204da45390c in / 
# Thu, 03 Mar 2022 21:21:32 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 03:18:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:18:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 04 Mar 2022 03:19:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:12a77aaceb8aa1438ebb61cb4904d74fc225cfa20464a060980580674a0a31e9`  
		Last Modified: Thu, 03 Mar 2022 21:25:09 GMT  
		Size: 24.1 MB (24073718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f95bbeb0964a4dfab73961fd149020ba71ce9126e727bd4bdcc3459893584bd`  
		Last Modified: Fri, 04 Mar 2022 03:37:39 GMT  
		Size: 6.8 MB (6764147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2e94ebf7c26007ac748c1e312e5eead31afe68486073db400e6e58a3d42103`  
		Last Modified: Fri, 04 Mar 2022 03:37:37 GMT  
		Size: 3.1 MB (3104124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc904035dc2f42be66259d691ed0a7118713adecc6e02636dd531eba8afdcd59`  
		Last Modified: Fri, 04 Mar 2022 03:38:31 GMT  
		Size: 55.5 MB (55453968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d81545cb385870a4dfaac84b972106f99674318dd3de372e55e7c7991c44127f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.0 MB (98969293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c70c86f49d8e22a2f7f22615b0c384e5a8ad26f0db2b18780939ef469d2ff`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:02 GMT
ADD file:f2fffe739729839aa17484bc4d79d33425549c5052824eac12131b16c23565d3 in / 
# Thu, 03 Mar 2022 19:41:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:08:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:08:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:09:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a7855fb0d7ae372c824d9c76be5ad2f42ce178c1910fa54a8543036b5325fd5`  
		Last Modified: Thu, 03 Mar 2022 19:42:38 GMT  
		Size: 27.2 MB (27169631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423f6ab0d295508b63ce61e1987bff0c82460c3a08b182062c758da4dff33ad9`  
		Last Modified: Thu, 03 Mar 2022 20:17:14 GMT  
		Size: 7.6 MB (7635518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccf3179768ddeede50c028e84e91486f3fe53c57720562347abec869126f029`  
		Last Modified: Thu, 03 Mar 2022 20:17:13 GMT  
		Size: 3.4 MB (3386532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b318f725bdf258086733cb5c556b8600eaed1a1cb49ea41525660fab552ff6ad`  
		Last Modified: Thu, 03 Mar 2022 20:17:35 GMT  
		Size: 60.8 MB (60777612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:033a988910b7ddec83bc5bd81cd6226bfbd90f1899e35850fcaf45101a32f542
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.9 MB (115867607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03243ae9aac0c9227b0f8273b5d3570469aeea9a4999d996a668a704d53dae59`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:28:30 GMT
ADD file:039f04ac6c5dbbe3fb0a5eee16945cf7c5fb7565751d6bdf8ec0c1102798c1de in / 
# Thu, 03 Mar 2022 20:28:38 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:23:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:23:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 21:26:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a16b43de69d1e799ea2cb675e7e605db0ff3a8d692fd326fbde80a370e0676d5`  
		Last Modified: Thu, 03 Mar 2022 20:33:55 GMT  
		Size: 33.3 MB (33292195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014e0a1b9bbd2b2b029e920fa7af6ee761ebc38994d46eaa73805fad6046369f`  
		Last Modified: Thu, 03 Mar 2022 22:01:00 GMT  
		Size: 8.7 MB (8723922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08de314573707f75376790e410ddfcfc9415f9c94c9241d04fb519be643d5f7`  
		Last Modified: Thu, 03 Mar 2022 22:00:59 GMT  
		Size: 4.5 MB (4456149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9414f21b78a90f86dfa0b7f2c109f5774216a0661ee51bbc21c592da692e7a3`  
		Last Modified: Thu, 03 Mar 2022 22:01:28 GMT  
		Size: 69.4 MB (69395341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f2efa0654909e70027f396ed09f1e135e00edae3cf33ca9f1dcb9196ad65a5ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98062035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fa7778a84ea5f282bccd7a4b5191ffdc15c0eabc26045f129e9d7b7b1c6ad0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:52 GMT
ADD file:3162233da685a36a9f274a7fa1d99452cab76f37e3640d38851c782ca506f75b in / 
# Thu, 03 Mar 2022 19:41:53 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:34:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:35:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ade7e68f4e34f438527a34c9761a285c3c3864e3daab0544b2c4f4163c7c3f56`  
		Last Modified: Thu, 03 Mar 2022 19:43:22 GMT  
		Size: 27.1 MB (27084671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2f6077d3b963ce96bc8174d3e9e8f33ce0024d87a23a994efe4563358ccff0`  
		Last Modified: Thu, 03 Mar 2022 20:43:08 GMT  
		Size: 7.4 MB (7424101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91e0c9953595ffb025bd6da03d3008b901e4706b9864266efdef8f435d9ef42`  
		Last Modified: Thu, 03 Mar 2022 20:43:07 GMT  
		Size: 3.5 MB (3542212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f96887959d99e6a4d0a4c74760071ae67adcd21a9cbc245b54eb850311f4e7`  
		Last Modified: Thu, 03 Mar 2022 20:43:23 GMT  
		Size: 60.0 MB (60011051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
