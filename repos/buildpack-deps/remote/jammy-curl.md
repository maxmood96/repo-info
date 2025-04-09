## `buildpack-deps:jammy-curl`

```console
$ docker pull buildpack-deps@sha256:f32f2ed74d01bd244b63182b3fa48b70a2f862907fc29203f84a8a23d94b957f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:74ad7fb2ebb2b7f1787e20005c568dd06d0f2fffe6e70c4d2764c44fe367ab87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36635152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b0e0fc2950f04ab6340254eaf9cd549c9cd9577df58c7320f5420143a49db3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340d07249a0b63b75c4a83ce1639f4f99213cb0868bed6fe3ee40cc7d6ba08d`  
		Last Modified: Wed, 09 Apr 2025 01:11:28 GMT  
		Size: 7.1 MB (7102787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d18aedaeb0b1f1e3a02a9711f4cceb47e962bd6ef5778e8e6561c2c5a0fa74f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b66edc7193df30be4536139da6c4ad9ef734485e14b0a9a3f50b2af175cd90f`

```dockerfile
```

-	Layers:
	-	`sha256:3f467da4ff9c7f2f5c83ff55c2a7a965a1cad217dbf5521a52ebeac89ddb6190`  
		Last Modified: Wed, 09 Apr 2025 01:11:27 GMT  
		Size: 3.1 MB (3050434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0fc2bc2983a785a2eb006117dbe0c0b7c67bebcf2b6104d3e8c9ce9ed5a67e3`  
		Last Modified: Wed, 09 Apr 2025 01:11:27 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:17d0d3dd1f949640b03303b80a650627955b363a2f9d06d9f4380ca3fc45903c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33637804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d8b2934575515d0bb55b5c063d6c24cd529eee32e94c81894b2b659b3b3fca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:7e9e4d557a66a31de2a39930803dbe849ba710af36b4731e9cbc856f55c10018 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:eeaefd3c974dfe1d5e1b8eb1929496ae7befe434399b37e601701f6d012e3169`  
		Last Modified: Sun, 26 Jan 2025 07:02:14 GMT  
		Size: 26.6 MB (26639267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03a59df32a3c278c1a8e1b5a42ec5159ca064a182a7ceee73e4ebe1d86afa12`  
		Last Modified: Tue, 04 Feb 2025 10:44:17 GMT  
		Size: 7.0 MB (6998537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1081500fc1be6fc3b8945ee99cb880cad574141933dbf2029a9a700a348a715e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0464e0de96691547f00ea8cde65d4ce20b5600e2c75c0e12c4aa3273df345a`

```dockerfile
```

-	Layers:
	-	`sha256:be68de876ccd100fac7c846b873154fb9e5fd89aba869bb04540f87213adae7a`  
		Last Modified: Tue, 04 Feb 2025 10:44:16 GMT  
		Size: 3.1 MB (3050163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7e8cd613a05f23ccfbaa6b9282044f16d5b355c4674cb7f486f198d68be570c`  
		Last Modified: Tue, 04 Feb 2025 10:44:16 GMT  
		Size: 7.0 KB (6984 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bfc1286868210b112fbabc6ebf06a440667c7cbe9267f032f8d099270c4e9f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34403195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6574538bc3b2dd2be2ba395cfb3d068ef7d870d12f513e01f427ff4f24edbbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f703d53cd8b130dc420fba33c6a4fce11f87eea59e2f21fc764d5a37af184bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3057705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab2c81a8a26aa255f0fd9935e25ad4a258d5e9f7fac1c281b1590ccafbdfdd9`

```dockerfile
```

-	Layers:
	-	`sha256:19239555617e12795d4e58e236a739ee22eca0c7c6f47115d76e3349926d8439`  
		Last Modified: Wed, 09 Apr 2025 06:09:40 GMT  
		Size: 3.1 MB (3050701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfeddebe81da58dab6b894383a62d0635846eaa95cd8c5cd54c5a709d477450`  
		Last Modified: Wed, 09 Apr 2025 06:09:40 GMT  
		Size: 7.0 KB (7004 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:394f8323bdf015d5fd67984872a67d6fb08589071c05acadae9a9fe1cfd04334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42623388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edf5af962042b8933d5043cd19cc9082f0e73841d0eadb3aa2ce36d62d91cf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ffa4d0393caf877e61e6700b1ae1bbad96ecd37d30084744cf639ecf44dc94`  
		Last Modified: Wed, 09 Apr 2025 04:28:15 GMT  
		Size: 8.2 MB (8180692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f58fe966bd20b3121e8cf09e8b6819765996a2737fbf55595ab0213563f13fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3061886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b061cc9891e95d965d3e4e90bbfd8e97cbc52d5b92bed1746929a4e47f0255b`

```dockerfile
```

-	Layers:
	-	`sha256:cae85960ff1a578076cd8a4a0e159ae1748d614841d7f2417295318548d9a9d9`  
		Last Modified: Wed, 09 Apr 2025 04:28:15 GMT  
		Size: 3.1 MB (3054930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68dd2ad91ab73ac0a63ea9958018c872d99f8fcc0efc277832a064843ebc60cf`  
		Last Modified: Wed, 09 Apr 2025 04:28:14 GMT  
		Size: 7.0 KB (6956 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:aeaf9d22071a9a40d3e526158838390a78b0e3e6af261fc8171ac6f0667228b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34155100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c01c3c9d2830dc1259f4e70db6f65205db2010b860d84669208b26947e23e4fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:438dc93fcaaee8b419e6a993c9ac3f3b30ca2c5b6b0c14df470faabc73e2a987 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e243dbf3d7e76afa075ed871906b2ada05fe2b8fdf244d349ead2e46f8b1c53`  
		Last Modified: Mon, 07 Apr 2025 08:26:52 GMT  
		Size: 27.0 MB (27039440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6701cae8eb10ef3d43e8f7780239a93a4d57d7d57a697ef28cf34010815ea34`  
		Last Modified: Wed, 09 Apr 2025 05:15:22 GMT  
		Size: 7.1 MB (7115660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:73aeab69e085508efc30eab2739aada9fac3ee29c27536d53b9faf3acc08010b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3051429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a500fea3eb93b9fe843318c3354ab389491e379281fb89c8ecb5adfefc388f`

```dockerfile
```

-	Layers:
	-	`sha256:cac4b808b9d42064c78d232ec6ff24807142cf7f6136a293fe1aaf83475b4c41`  
		Last Modified: Wed, 09 Apr 2025 05:15:21 GMT  
		Size: 3.0 MB (3044474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9428fa53864880bf5fff451a614d3a1138d648792149f978b1b8eed82730c077`  
		Last Modified: Wed, 09 Apr 2025 05:15:21 GMT  
		Size: 7.0 KB (6955 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d3e1b83b3380d7d38a62417d427371657c13a8c9c75d71ced06a845e32d3f23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35013637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec2ba32180d0917ac4683fa5aea59cb521f7f65fa0a3837f85199e2080328a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5d8d436f6811fd1894d694e7df7d347b9bd021b38bd57e01718331911c43a656 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:25cf79adc8d2979d397edb23d9d8f0127bc0edfd1addfa501b8a0cc74338576b`  
		Last Modified: Mon, 07 Apr 2025 08:26:58 GMT  
		Size: 28.0 MB (28000118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735fb272dbfe25822659e29ed1a2882170147c9ba32a1f6b7176ba8ce67d75b2`  
		Last Modified: Wed, 09 Apr 2025 04:11:42 GMT  
		Size: 7.0 MB (7013519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cd49cc59e5f97ffbaa6d4486d95d9c38efc03df2c89843fb3b8f806a7586fd23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3059575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d625e6b367fcc605dad883e461e12ac0e6f8fd364027dbc01076f26c56c12e`

```dockerfile
```

-	Layers:
	-	`sha256:58d33cf2f4e5abb7627757fe14fa82305cec9eed232eb789ab3cbeb01aa44b1d`  
		Last Modified: Wed, 09 Apr 2025 04:11:42 GMT  
		Size: 3.1 MB (3052651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c67946604794ab3bea27b99f7f896996e313b959744af3a77e594f810951385`  
		Last Modified: Wed, 09 Apr 2025 04:11:42 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json
