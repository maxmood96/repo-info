## `buildpack-deps:kinetic-curl`

```console
$ docker pull buildpack-deps@sha256:0b845c8f71eaa2cb6dd3e91a62808783374c3eef834017ce3caeade608ec797a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:kinetic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:da70ff54bea6cd9936808ce0552bf93f193bbef5f7ff7a11148796a9834bdc6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41678954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e340cd9be93d35cc10cadead5e0d13b2be2f27cdb5ce784878baa1b87c78ff1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:03:38 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:03:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:03:38 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:03:39 GMT
ADD file:ba742ddbebcc8282f5094275969bfb2ff4b2973e385c198b6897bea2a9cb4b85 in / 
# Thu, 13 Apr 2023 13:03:39 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:25:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:318b284d262b8726296dca98d01be71ddfad412c987a7ecec4db3278eef82188`  
		Last Modified: Fri, 14 Apr 2023 09:51:30 GMT  
		Size: 27.5 MB (27482065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9524639683da060409afe52743a069e533470b29c731e57939b078d6ed1e81`  
		Last Modified: Wed, 17 May 2023 00:41:41 GMT  
		Size: 14.2 MB (14196889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a9cb2cadee31bab68630d64ed2c71280ad1ab875669d51606683d3a2a7a27a26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39034372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0ad582f81e3dbc9bc69dc23cf69cc02b504b26f307190ac10a7b154fc9c985`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:09:51 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:09:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:09:52 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:10:01 GMT
ADD file:7c943de57b75e515f072a13706b12ee97f17d22a120991f8effbc0615c544253 in / 
# Thu, 13 Apr 2023 13:10:02 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:05:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f98d8e30b5bcedb55e832c340c4accb90ea3b5319d99dd02667d1ae133fe0f01`  
		Last Modified: Fri, 14 Apr 2023 09:55:43 GMT  
		Size: 25.9 MB (25891251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b920c96303573225aded058cd081e94c75571fbc105df19e26a478d711fca4`  
		Last Modified: Wed, 17 May 2023 00:25:45 GMT  
		Size: 13.1 MB (13143121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9177cc6c6722e2a42b20e9da4a67f9841ecdaf87de9f62707586c42118ef05bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40434042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9317932280c5933863a419de7d90b496ba4df6472d197cc36b6feb98aa1985`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:20:37 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:20:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:20:37 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:20:38 GMT
ADD file:8b5c9a166ff42d52b423d188428558ea2bf225c42aeb3de339514e6ad9fdd504 in / 
# Thu, 13 Apr 2023 13:20:39 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:44:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:479b8cd2e9c97aa9b4eb9d8070207c8b64f471b3ec6bb582c7b09dacb55735a2`  
		Last Modified: Fri, 14 Apr 2023 09:53:52 GMT  
		Size: 26.7 MB (26702173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce5a0c1413473bd48a6e359ce099bb9fac129bce6960ed9b6aab520bedeb023`  
		Last Modified: Tue, 16 May 2023 23:58:10 GMT  
		Size: 13.7 MB (13731869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9ad1783434895628fc6b2c9256fbaf789666efed8c2d0cae4b4c4fc8f8d8587a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48341027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b53c3f99c30aee5990c57d1840f391fa1b54aa66151a4d3936b984515ba28f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:21:42 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:21:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:21:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:21:43 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:21:45 GMT
ADD file:2f24914c3a2e66342aa7cf589af143b01a1cd7532c92c4263d251fb826b8b810 in / 
# Thu, 13 Apr 2023 13:21:46 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:25:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b2b861f7bcaef2d589c1d8518a14da93644aafdcc9bfc5554895ed342bc341c`  
		Last Modified: Fri, 14 Apr 2023 09:57:14 GMT  
		Size: 32.1 MB (32098609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d450fd51c7629be6573e7233cf0ada6455652e3d003932193e395899b1b32e5d`  
		Last Modified: Wed, 17 May 2023 00:51:16 GMT  
		Size: 16.2 MB (16242418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:862409116dd6f88091fb63263981bdf73ea2710a45b847a8d15ca350f8fa2a3e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40386032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c248d7339a9978200db26fe6ece5bf19a87a09faa0cb0db10982d373481692a7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 13 Apr 2023 13:08:08 GMT
ARG RELEASE
# Thu, 13 Apr 2023 13:08:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 13 Apr 2023 13:08:08 GMT
LABEL org.opencontainers.image.version=22.10
# Thu, 13 Apr 2023 13:08:09 GMT
ADD file:df5733230d0258ecd0cbdcc7c2075865bc335200f2cafee8dacccfd082710b96 in / 
# Thu, 13 Apr 2023 13:08:10 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:46:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c450971bf0fd92eac91caf0b3126482e5fecadead22e59da08f9661a4b4f03be`  
		Last Modified: Fri, 14 Apr 2023 10:00:19 GMT  
		Size: 26.0 MB (26029287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f712e29cfb9c4e3fa37cc777de5ec3a547378889617b0615c8957c5af9efdc`  
		Last Modified: Tue, 16 May 2023 23:56:45 GMT  
		Size: 14.4 MB (14356745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
