## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:a199355e9b3fc8b0f7cd0ba1c31e5a068d60f3f385563bfd101b10186b60f652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4423ef2aa5ad0446a7cc76587cd342d87f123ed08794fb62fc80c2082e21bdf6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138757342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8e31a3319585811c7242dc1d4ca488790a5e0f75ebd144e49230dbc0a522f0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:46:33 GMT
ADD file:168af20819ee8d7bc6ca3fd35873fe0b65f567f6fc4763ae2fed655e04826ef6 in / 
# Tue, 02 May 2023 23:46:33 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:20:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:879480f6969a02afb639ba9b35bc2df992fec064538a2e8af5e14cf6b6fbeac3`  
		Last Modified: Tue, 02 May 2023 23:49:26 GMT  
		Size: 49.3 MB (49299247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73663ba97809331f57a06963909241b165e4c1774ebdca8a3d2c670b5230d8e6`  
		Last Modified: Wed, 17 May 2023 00:39:29 GMT  
		Size: 25.4 MB (25350325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a590ab8f0f74bc2b269288b7c9cece582db61883544acdff037cf01308e4452`  
		Last Modified: Wed, 17 May 2023 00:39:45 GMT  
		Size: 64.1 MB (64107770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:43862d80af198296ae0489e096edb75413809a4ff19abf282b5d8f4f6a14eeb9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132734481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b27fd6e9f52ba61dd0b98409d99861eb6efd0ddb0a1a3b619e2792a517b862`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:48:29 GMT
ADD file:1ecd266ebf23430d2ea2417b92ebee6029d940fbe99297183c4f811e24fdffb7 in / 
# Tue, 02 May 2023 22:48:32 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:48:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:49:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cbca433c216350213a8b219e118cb55f422acfc53f49c76c44e044b42a5c0aa6`  
		Last Modified: Tue, 02 May 2023 22:50:27 GMT  
		Size: 47.2 MB (47167199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a510f555be9d50bf04a0e432e1da4122711987bdbb2544b99200d53b8ca8e2f`  
		Last Modified: Tue, 16 May 2023 23:54:02 GMT  
		Size: 24.0 MB (24015755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950725180093057d483f89fe8bfacea282810272b072b61ab35a44c9ccbc17b8`  
		Last Modified: Tue, 16 May 2023 23:54:21 GMT  
		Size: 61.6 MB (61551527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:84b42b9ed8300cea840175d87c8ff51940928c0e26337fab6c27910588206350
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127463114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcc6f9e63b42972b8b5f9b4f62623a5be08255432e153a6755aa3c57bcc46a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:28 GMT
ADD file:222aad59c348a6e07dd607ba4626497e12e5054fb651c9c30d5a4c5a8b3e4c82 in / 
# Tue, 02 May 2023 23:47:28 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:00:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:326cff266909348fa4e168fc7e76fbd52cc4855403565526a5ecd2e6bdb9d26c`  
		Last Modified: Tue, 02 May 2023 23:50:34 GMT  
		Size: 45.0 MB (44988072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55abb83f097438eeb001ad7afc4116735e243a512d7cfda49cdb7b6bd1f009b9`  
		Last Modified: Wed, 17 May 2023 00:23:16 GMT  
		Size: 23.2 MB (23218068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f50f8d763268ba1b4d8d7363b0b478fbfca7dcc73fca7947c65853b1788813d`  
		Last Modified: Wed, 17 May 2023 00:23:39 GMT  
		Size: 59.3 MB (59256974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1e4fd4adc8d135512fa0806338069ddb4b2e8d4a239752529bfdeb2edec2fefb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138229402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b810d068f2c2ddbb0ac47a859b6fc4fe6dab6f24c229855085bdefded0a84202`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:25 GMT
ADD file:1af23b8894efa507a47bf873cf69ecaa5ea13b618cae85b8c46125af6399b4fb in / 
# Wed, 03 May 2023 00:22:26 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:39:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:40:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:15c964cdaf05fdeddcf9bddd79eba05f71f2859fee9c193ba5d19a237f7fb92e`  
		Last Modified: Wed, 03 May 2023 00:25:01 GMT  
		Size: 49.3 MB (49345335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1426a52e9479646762d18e7a8f0b801f6ba0cd16196e4619fd66dee64a27715`  
		Last Modified: Tue, 16 May 2023 23:56:18 GMT  
		Size: 24.9 MB (24898492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cd095d9f8a0dbe9574d92083852c11e0a6a6cd230364b19fec3cf45f8388a33`  
		Last Modified: Tue, 16 May 2023 23:56:33 GMT  
		Size: 64.0 MB (63985575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7b168b75007d09bc465bed32299c0f4e468fbddd286a88fca6d80f7afa489f75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142484902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca937da73af18b891dcdab3f71d1cfde9f3ab7bf495d333fc72a5ed16f24cfc7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:00:17 GMT
ADD file:cd02b45138959c7ec7d466eff66efaa68d03b2e72f294b468f08c576643ac084 in / 
# Wed, 03 May 2023 00:00:18 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:40:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:41:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:028db28caf3d2a0b3bc8b8281c9f370a6ca8a97954f596e2b27e20ebf7f3b578`  
		Last Modified: Wed, 03 May 2023 00:04:07 GMT  
		Size: 50.3 MB (50321827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3febc6af3fad6009c9ea3e2a5a4f667dfb01b41d973376f8783dc1a8cb0386c3`  
		Last Modified: Tue, 16 May 2023 23:45:46 GMT  
		Size: 26.2 MB (26193060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60344d83adb7cf7104ca2b29577e316196e7dae83aebdf7fa67c6684c8a08d17`  
		Last Modified: Tue, 16 May 2023 23:46:08 GMT  
		Size: 66.0 MB (65970015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:48f8fed339b3d8434de8a8d78e3663d42c1ac73065d42cd2b8ebdaf2ffe8e994
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 MB (136457203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb7ae52eda72438e2cfbf1412ed36b36bc21f33c1186f58e95a3328bdb9f760`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:29 GMT
ADD file:ff6384c951ff8b6254c1c1f02c689314e2f30a43e4b60dcbf54c82df826f734d in / 
# Tue, 02 May 2023 23:47:33 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:45:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc6b7fd1001cc2b329d98b8ea6ca86f4be0bff6654b36678fc5fa01f2f599145`  
		Last Modified: Tue, 02 May 2023 23:56:18 GMT  
		Size: 49.3 MB (49301357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d31482ac1d01bb4da186f1d7d1efabcbad13ce3186c1582781afa6d72d5b3b`  
		Last Modified: Wed, 17 May 2023 00:02:50 GMT  
		Size: 24.2 MB (24207182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3717ed704e113fc09bf9a700960dcb46a11b9d156a368932badfd8b579415c8`  
		Last Modified: Wed, 17 May 2023 00:03:39 GMT  
		Size: 62.9 MB (62948664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:282c61eb2cbfeb5e098e6ca57d2134cbf2f4a062893759df1b3305d4d88c6c63
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149924139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4232ed86499c0514ee599bd9e511a681955668a8dd66933d3e5a220e520278f6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:30:45 GMT
ADD file:25d67bdf8a8d7f1826107ec67b95338418561c0fd3833ca3065cf965e82b87f7 in / 
# Wed, 03 May 2023 00:30:47 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:17:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:17:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2e614e0d26e774be63c67b7f9f168ad3982d113da743f11dd74fec77e268d7e0`  
		Last Modified: Wed, 03 May 2023 00:35:40 GMT  
		Size: 53.3 MB (53307301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8724ecf8c2848df51f9cb617bd52bdb8ed65adc7e8bda710d71b7f440ed57ef4`  
		Last Modified: Wed, 17 May 2023 00:47:43 GMT  
		Size: 27.0 MB (27049758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1940f34b2c35af501a8608288a77830d02b370b3ca6267a44309132a7e993954`  
		Last Modified: Wed, 17 May 2023 00:48:11 GMT  
		Size: 69.6 MB (69567080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7a1f44bc69e4fdfdc35cd1132e60cf090df46229f85de4e53b154c450409294f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136141105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d776cc668adc1cc56929240cc2477c0d11f991b60f4113c992f0164ed452121d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 03:41:05 GMT
ADD file:2b13279140b98de657b363865f9ee14f0c5c26df191533d1c5438dd1df5948ca in / 
# Wed, 03 May 2023 03:41:11 GMT
CMD ["bash"]
# Tue, 16 May 2023 23:41:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 May 2023 23:42:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f966d911ea531e8d55499ff0d85338412ff6e8012a1639d691e4bc5ecf08d42`  
		Last Modified: Wed, 03 May 2023 03:44:23 GMT  
		Size: 47.7 MB (47675931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a0c25941897af74b548e8b3030a4f6d12d7e0540497c20305c519e8b6a89e1`  
		Last Modified: Tue, 16 May 2023 23:54:59 GMT  
		Size: 25.4 MB (25354263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c26bb6b06f66508d8f39d4e0ebc7216ae69662d6a748faeb8e1bc37e112d24`  
		Last Modified: Tue, 16 May 2023 23:55:13 GMT  
		Size: 63.1 MB (63110911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
