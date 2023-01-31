## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:b78493c4672fb21859537461c188d75ec6d0d7ad370f91737ac792646bce8930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:eefb4a7c8e274ca65671f877f62a858f8fd0844f35fd6d8cab3be4ab9381518a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36355169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e8e203a6674cdf500bddc5275d68fb9a2bcc4fb09aef4179d4cb0031dd23f2`
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

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:07ff5d1026caf406732871da4f10ee2393a5d53c150544fdf0d84ea585e36972
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30572758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fc7a2f87139aa6fbc6a1751db2585e1cd734ee31ab65b2ca9a692dbb3d879d`
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

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3ca6d0747171417678ed64f5386ecb852fcde4e72a1461446a931f6a09ed6846
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32582064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54f779279d1503cb962c0a72b798187b208e7b91f6bfa1507768b86cbefd709`
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

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4533cc2035f245487c5d105eac0a228bb5f296bacb67002d4b3afb438ec9ddcc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37112323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95aa38ff4e9345254d0c95827c9da0e2b15cd8be8473102acc5679ce96eb3640`
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

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9f86ff85ce09457dbf0f1f65da193c6aeff8cfc85fbb30dc0a6162051eeeacf2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41218679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b1c204ad4d256ee762cc2bb63546a154b975ead673362bb7cc0c6779857e4d3`
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

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c86ef5326c34545c4f4f53fea242951a4457f014933db0817669765075d68c87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34656733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8846013a5b74eb1fd3072a9091d0e1ad91f04a48853e4d84d2c77d240414725`
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
