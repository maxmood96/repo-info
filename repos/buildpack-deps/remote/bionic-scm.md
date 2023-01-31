## `buildpack-deps:bionic-scm`

```console
$ docker pull buildpack-deps@sha256:43f0573fac34efa6b2c4aeae49f13f5c8f642740c4409748a14114d87561f950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e7df5351980a3dfe768ac04e0c53fa513d73027ea35485119db202f58ebc8a22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81866795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc13147b59defbe2f266c1e16966187b3351b15e4260038e87564d6134d946c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:03 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:03 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:04 GMT
ADD file:365c129e10f7ef1594e8086543b45f524313e36dd6a25b68f4da542a09491f04 in / 
# Thu, 26 Jan 2023 10:03:05 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:39:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:39:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 17:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:456d651ccb276bafe702e453add4a4f15b511fd3234cb7db898c22540ad3c8c1`  
		Last Modified: Tue, 31 Jan 2023 17:46:32 GMT  
		Size: 26.7 MB (26711594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b21d603a94f829dcf240f93489b3359deed997929b46f2bf66146926bd3ef9f`  
		Last Modified: Tue, 31 Jan 2023 18:00:44 GMT  
		Size: 6.6 MB (6617506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b155ce8564683071c961a173c72705932177495f976f405ab77696ac5cd17b75`  
		Last Modified: Tue, 31 Jan 2023 18:00:43 GMT  
		Size: 3.0 MB (3026069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb0ace4785a8addeddef7444ff5ff46d73774811c1192c979da490211bc50fe`  
		Last Modified: Tue, 31 Jan 2023 18:01:01 GMT  
		Size: 45.5 MB (45511626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7fcf0465010135a70aeb61b9947d1dd41617b6c64b1eb86e36f4281944e4bab2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71286524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6031467929fc076622410c76e55d7579d0d8c6e1c7afae3a46c295568083126`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:56:13 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:56:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:56:13 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:56:18 GMT
ADD file:1cc75b54b9c4d0824203532d4bb0eea2aaeafed003e37057b21aa3713b6bb0ea in / 
# Thu, 26 Jan 2023 09:56:18 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:49:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 17:50:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec3bd771f252293c5a70a0e50b16a27aa4cc182d5d5c4944c803b38ad12da038`  
		Last Modified: Tue, 31 Jan 2023 18:14:25 GMT  
		Size: 22.3 MB (22306068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a02a1ae0bf2a4411e83c9bfdfe9958f2c8f8aeb835da00d766ac3048f70b0e3`  
		Last Modified: Tue, 31 Jan 2023 18:14:23 GMT  
		Size: 5.7 MB (5680010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db46e117d46603f8d76b377bca93d9cde280c81cf6b8a194c5b431d86cea41be`  
		Last Modified: Tue, 31 Jan 2023 18:14:22 GMT  
		Size: 2.6 MB (2586680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e5cd9449bf556891b984ada686e0a526b95d21643d1ca03ee546fb174eeb4a`  
		Last Modified: Tue, 31 Jan 2023 18:14:43 GMT  
		Size: 40.7 MB (40713766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0f7454305ad71cc1618ddc501c963f107e9e1ca383a9dc2e1f1d31db83de8952
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75896008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c594dd26e7b2f1c31896b626cffe79c629fcfd41f75e722dd4626f2f4088e64e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:04:53 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:04:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:04:53 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:04:56 GMT
ADD file:e7556a99ac088826f5ea581a0c5e2230c1f9a9deab7106e9cec6d1ae8594f19a in / 
# Thu, 26 Jan 2023 10:04:57 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 18:12:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 18:12:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 18:12:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c58359f0ed0774e1ace1315b1a5c48c0d40a2519a5d69c92eb49fab69b4ff6b8`  
		Last Modified: Tue, 31 Jan 2023 18:07:50 GMT  
		Size: 23.7 MB (23735530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c3db86e75ada5398a2d9a556625e3e0a4b73c36ab79cf21ccd1ffd35dd43fc`  
		Last Modified: Tue, 31 Jan 2023 18:33:13 GMT  
		Size: 6.1 MB (6055914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cd619a1ebf49880ce75b505030f48c0ab5b4904c5418bbc0145052802eaa63`  
		Last Modified: Tue, 31 Jan 2023 18:33:12 GMT  
		Size: 2.8 MB (2790620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6ed5bf2278606c14e4380d7510535f5bdad7a4e6b5bd6dddff29b256521546`  
		Last Modified: Tue, 31 Jan 2023 18:33:26 GMT  
		Size: 43.3 MB (43313944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:304ee6faebc7c4f2c61cba5c4e74bc2169cbda06fcd90fc8236a6b957a06c18e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84209797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c7e2ef964d858f46a7a7e01d0547d4e1bbcf7a1d08204d457bb9ae16a7bb7c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 10:03:01 GMT
ARG RELEASE
# Thu, 26 Jan 2023 10:03:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 10:03:01 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 10:03:03 GMT
ADD file:b9b814a7d1e7611a2c531fac3419a48c733c622470d3f275ce29f9ba8764eaeb in / 
# Thu, 26 Jan 2023 10:03:04 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:35:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:36:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 17:36:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1177ecacc42e51782037ed649a91241b82866cc72c6eb0f205cbcc350f44d43`  
		Last Modified: Tue, 31 Jan 2023 17:42:04 GMT  
		Size: 27.2 MB (27165349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c39de00ec60a997f2242a42cec80f97d8df9381f43258594c85d8574e20188c`  
		Last Modified: Tue, 31 Jan 2023 17:42:02 GMT  
		Size: 6.9 MB (6904851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49501dcdf14443501d048a845928327a68626b4a41383d485a040e5b5b7b4af`  
		Last Modified: Tue, 31 Jan 2023 17:42:01 GMT  
		Size: 3.0 MB (3042123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c1863e1a417658cd0de9ce6c386e5336ac6e0b2be2a6ac423d7433ccc53622`  
		Last Modified: Tue, 31 Jan 2023 17:42:22 GMT  
		Size: 47.1 MB (47097474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:98b56b01409cca65eb0051a74814eca3788d5a98d541104a5653f00cd973c18d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (94956625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ea247b997209a79cca6c45dfbc04979886790d6040979527e616c8e89d7185`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:44 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:44 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:47 GMT
ADD file:108aadd723beb46031bfaca610c036aea506955578347dda4a01cfb0c6bdc135 in / 
# Thu, 26 Jan 2023 09:55:48 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:40:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:41:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 17:42:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:15579125cdf95166fecb7637769c3c9eb2551401759fb21f44848947ead59cbd`  
		Last Modified: Tue, 31 Jan 2023 18:13:22 GMT  
		Size: 30.4 MB (30442586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74fea2fabde99e916cabf483638fbf3a31420ac919854738215aa0a52bf39fa`  
		Last Modified: Tue, 31 Jan 2023 18:13:16 GMT  
		Size: 7.0 MB (7035605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428b8a67c5ee9117982087fd7c1be5b763a8286ea404e24144bc6b0042fff348`  
		Last Modified: Tue, 31 Jan 2023 18:13:15 GMT  
		Size: 3.7 MB (3740488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491ab9254ea85bdf063c540c3096b71d4039f2039cf028e624dca83dec8a051f`  
		Last Modified: Tue, 31 Jan 2023 18:13:47 GMT  
		Size: 53.7 MB (53737946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ed5d0d1582ec32919d5650c6af855db2fc9de89b856a8e10fc4d226e285d1449
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79695365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737e17d3b58cd146e26376e8cc717a07041a325ff66cc553302b964fe2f1e252`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 26 Jan 2023 09:55:41 GMT
ARG RELEASE
# Thu, 26 Jan 2023 09:55:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 26 Jan 2023 09:55:41 GMT
LABEL org.opencontainers.image.version=18.04
# Thu, 26 Jan 2023 09:55:43 GMT
ADD file:04d4137c9183cee18560fc26a092e288ff403f3dde266237eab245bd38eb9b3a in / 
# Thu, 26 Jan 2023 09:55:43 GMT
CMD ["/bin/bash"]
# Tue, 31 Jan 2023 17:35:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Jan 2023 17:36:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Jan 2023 17:36:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4727db5881c26ec0d79df6d172cfc50624c09ca7869b8146052e0692734d2cac`  
		Last Modified: Tue, 31 Jan 2023 17:53:57 GMT  
		Size: 25.4 MB (25371457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e060d5ddd88a52d0a10b103bf4210855c9cc2daac45756f960fd90365af6542`  
		Last Modified: Tue, 31 Jan 2023 17:53:54 GMT  
		Size: 6.3 MB (6308650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4883942b852e1bd875f58749e4c99070639db9ac02867dfd13770796b06c8687`  
		Last Modified: Tue, 31 Jan 2023 17:53:54 GMT  
		Size: 3.0 MB (2976626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a824cce0d3d1e891d7b4b44e056c1b33ba9f719ad78192a3664800de0d266cd`  
		Last Modified: Tue, 31 Jan 2023 17:54:09 GMT  
		Size: 45.0 MB (45038632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
