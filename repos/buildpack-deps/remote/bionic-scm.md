## `buildpack-deps:bionic-scm`

```console
$ docker pull buildpack-deps@sha256:ba36fe023887a6023026eae58d6bba3447a045a77a4261c1a1f6db373cedac91
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
$ docker pull buildpack-deps@sha256:2acd0deb7308e5597b2b9d3b593ae7ea6e8f7fc346ce2d08ebddb9fbe54baad9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70376731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce9373357a8aec9ae1e9d9f45f397ff6c4a97a3beec687935474c737e6d687df`
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
# Wed, 01 Mar 2023 02:39:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:39:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:40:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c138257d410403a2127c08e269ac8467b8f2001b22a102934861b65b2f49bc1a`  
		Last Modified: Thu, 26 Jan 2023 10:12:17 GMT  
		Size: 21.4 MB (21395113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47096fe89b773c1646429c4d0b72c616d52ad8e417f6b22a7fffacbf9e543330`  
		Last Modified: Wed, 01 Mar 2023 03:12:33 GMT  
		Size: 5.7 MB (5680777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1cbacc1eb0f2444d8fe8e626335b90e377dba26148c5b1ba67d69a9966df71`  
		Last Modified: Wed, 01 Mar 2023 03:12:32 GMT  
		Size: 2.6 MB (2586738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a752d641cb559708d7e030aae9c70190dbf469ce25759b21c2c34db03cca6ac`  
		Last Modified: Wed, 01 Mar 2023 03:12:52 GMT  
		Size: 40.7 MB (40714103 bytes)  
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
$ docker pull buildpack-deps@sha256:8ca4f8a2693cdd7aff210955c3bbc8be8eef544578cac7e64a5908ab4a5aee1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83357410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4862a954bb62d0211b2e1de96a09b28b9c636bad9ecc51c55eda533a9b12b23`
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
# Wed, 01 Mar 2023 02:16:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:16:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:17:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:57a4d5aed2cd4a1f596f693a8fe5e135bd66dbf401ec169b1848d2316bdcfb2c`  
		Last Modified: Thu, 26 Jan 2023 10:12:23 GMT  
		Size: 26.1 MB (26096513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7a01875a8f61110b8a3987b128629884aa645fef18557175a3c73a79ecda62`  
		Last Modified: Wed, 01 Mar 2023 02:27:41 GMT  
		Size: 6.9 MB (6907847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9185b0869254fbcd22a9fab4d7b047d37171dc5b322e61abf872fcc068ecf472`  
		Last Modified: Wed, 01 Mar 2023 02:27:40 GMT  
		Size: 3.3 MB (3255765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79adfdfb2c964ed95f76337267ac66d2871db2f52647fd6f502bca4a71e16a92`  
		Last Modified: Wed, 01 Mar 2023 02:28:00 GMT  
		Size: 47.1 MB (47097285 bytes)  
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
