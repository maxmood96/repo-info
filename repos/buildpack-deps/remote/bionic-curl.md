## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:9bcc1e251c57f785a2334e0b5b0346d7fbc25281dfd33b98b46a901a15573a8d
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
$ docker pull buildpack-deps@sha256:964d3829f262359dc2b06a990b5d348090712bdc869e7cb6be442515e97f27e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36057314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa38387be463143f66f336a6d21d45768734c0565d1185330184c1a08885e6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:41:51 GMT
ARG RELEASE
# Fri, 12 May 2023 09:41:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:41:51 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:41:52 GMT
ADD file:47682dd3869ca8e57ceb15f69a6ac7c9048d4d42c7a99a976e597cf072423c12 in / 
# Fri, 12 May 2023 09:41:53 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c67806d7e72dd941e600bad2eabe920a17ba1852b325b63900c819ffeae646fb`  
		Last Modified: Tue, 16 May 2023 01:01:48 GMT  
		Size: 26.7 MB (26715509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcb28dc5d7a6065807bdaa5cbff1c2a3066793dabe65b5f074ccd3a22365b7e`  
		Last Modified: Tue, 16 May 2023 01:37:06 GMT  
		Size: 9.3 MB (9341805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:83886958e59b44a8d57191a4b5bb58bee41bf7be6c21e4249e021626577df1eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30304823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac5b0f63d565611008af26df30e54aa3108c9bae6c42cfc8259f5ea89ed5739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:52:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:52:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:52:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:52:20 GMT
ADD file:d570ab6bd7d664cc6547b6ae228cf825333d9d841969911c7d62afe3ed440803 in / 
# Tue, 30 May 2023 09:52:21 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:36:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76bc0c6b06fc92c1f911be6147b55b6430301b80e4062178329c4fa8a0f79f51`  
		Last Modified: Thu, 01 Jun 2023 23:54:31 GMT  
		Size: 22.3 MB (22312178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac315a15c6caa9f2db89ffed1a891d0860513de0245cba82c144f0b316bfb55e`  
		Last Modified: Thu, 01 Jun 2023 23:54:29 GMT  
		Size: 8.0 MB (7992645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e7abf481b78dae1dc02698f46a8c3d7ed8b60f3eb0c498ca340f946394b81c57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.3 MB (32304310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b219367776e17313569a9286a2288a786b6ee8e87073973d2c0ac1a907503b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:39:04 GMT
ARG RELEASE
# Tue, 30 May 2023 09:39:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:39:04 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:39:09 GMT
ADD file:f56078e320535ad36864a2a30efa5b760ae65dd324cea9d75f01388b17e1183c in / 
# Tue, 30 May 2023 09:39:10 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7f8ef08e85adb2e0a8e170480033b585598619a5675768da9972914138e520de`  
		Last Modified: Thu, 01 Jun 2023 23:17:46 GMT  
		Size: 23.7 MB (23740900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1fdcfccb3b903da923c00d9a2fb8e7291dfdc71de70fab1120a8f20326f4d0`  
		Last Modified: Fri, 02 Jun 2023 00:04:16 GMT  
		Size: 8.6 MB (8563410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d7d7ee1857a8c788a8d4dfa5fdd958f54b33ddd78a9e68f7c25b3dd2c08077bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37056873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cba6f907f73d0736c11011d005da2c800f1f303c05130b95f07ef8fc576d3d9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:32:11 GMT
ARG RELEASE
# Tue, 30 May 2023 09:32:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:32:12 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:32:14 GMT
ADD file:1f856710b4bf82e95a940e08c6167ef4775a430a38fd2fb575ad7743bacb39b6 in / 
# Tue, 30 May 2023 09:32:15 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 22:56:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:69f31bfb16537ef7adee6e0ba9f5ec28a58d51deecde164034a1b4a0e0c7d371`  
		Last Modified: Thu, 01 Jun 2023 23:00:08 GMT  
		Size: 27.2 MB (27170810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4928e6a80d2ff2c70a02c0eaeef3be857ef694a1da1ece8056a3ecda768a7bd2`  
		Last Modified: Thu, 01 Jun 2023 23:00:05 GMT  
		Size: 9.9 MB (9886063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:771a1e6fb93ddb02612a4eb84e5ae9d8fdaa15fce4c7c57d63555a537624b2fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40917957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083827c02404a02082451fa934364443a14603ed6c4b2d50287a1b615b1f3f96`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 May 2023 09:26:21 GMT
ARG RELEASE
# Fri, 12 May 2023 09:26:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 12 May 2023 09:26:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 12 May 2023 09:26:21 GMT
LABEL org.opencontainers.image.version=18.04
# Fri, 12 May 2023 09:26:23 GMT
ADD file:362fa5164fb227e6f3d45a41742ca485fc50dde3cfdc3fdc1f9233011d3d1b84 in / 
# Fri, 12 May 2023 09:26:24 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 00:56:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab08883ad6ed65686edc81fb213d333beda55de0937170bd1f83540ca1d8f68f`  
		Last Modified: Tue, 16 May 2023 00:54:52 GMT  
		Size: 30.4 MB (30443542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8612663af4b782213cbb53b76c256a5a24aee62f19a60124bec464be1c91d4`  
		Last Modified: Tue, 16 May 2023 01:03:01 GMT  
		Size: 10.5 MB (10474415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:51ed9e6fce6549740e033e09e11a00e143e9588b193166214f20342514d06269
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34380655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea9f9694b5f5c3f04b7d476be43e7dcfad7eb0b71b146f2e12b39e4c4f5b77f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 30 May 2023 09:26:28 GMT
ARG RELEASE
# Tue, 30 May 2023 09:26:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 30 May 2023 09:26:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 30 May 2023 09:26:28 GMT
LABEL org.opencontainers.image.version=18.04
# Tue, 30 May 2023 09:26:29 GMT
ADD file:3ed568ba86f7dcc948369fa5141ac64b558b1594643b1e8725d0e4790e4460ce in / 
# Tue, 30 May 2023 09:26:30 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:04:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23570ad9d676e13fd0b8db8546fc7cb9c1a7b4fa60ba88ebd7052142489a89b8`  
		Last Modified: Thu, 01 Jun 2023 23:18:21 GMT  
		Size: 25.4 MB (25375564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8cef30b3f52b87c898729e2bb34d291c6f7282b7618c5785073e87db7e3bb7`  
		Last Modified: Thu, 01 Jun 2023 23:18:21 GMT  
		Size: 9.0 MB (9005091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
