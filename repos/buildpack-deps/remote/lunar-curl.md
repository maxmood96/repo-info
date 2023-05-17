## `buildpack-deps:lunar-curl`

```console
$ docker pull buildpack-deps@sha256:7dec9364c175fbd161081254595121e6a6608716cacb9b92c1cd14877f53a816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ea91eb9a4009fba19c23257ec219cf3fc27c901abab9db4a73213b3628b321b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41363822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d037ac62638b983d77bde73312dc69285d0621df34f0d51db8b57f5aee39ef9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:41 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:41 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:43 GMT
ADD file:6652bceb064b5b28324fcb2db853ca272d29914a5b10e6c33ef0fd824018efa0 in / 
# Thu, 20 Apr 2023 18:20:43 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:32:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6c6b907db42b6f1b03645d7cd822afa676930182719410e133c9480fede45d4`  
		Last Modified: Wed, 03 May 2023 16:46:32 GMT  
		Size: 27.6 MB (27604112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878f85888a90c2a34e30a0c0a9b5fa2d5ec19c9a0971bfdc5c58bad2d07f8c1f`  
		Last Modified: Wed, 17 May 2023 00:42:36 GMT  
		Size: 13.8 MB (13759710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ecddd17e251f28a5bed2fc91a6c52bf5645892ce008796685fea21d8c80f6daf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38112093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2bf17730153d7693068e114ab5b1d93cc51fda6901596d2883cb29f3434266b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:52 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:52 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:55 GMT
ADD file:61209c58d1b634acf67890d77ce3b799ba77b810241b26943e2a3e9b59328216 in / 
# Thu, 20 Apr 2023 18:20:55 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8f976bcf9a33d090294b25c3fb3430a5833ce92be9f477471addb457c0dc3ac`  
		Last Modified: Wed, 03 May 2023 22:12:58 GMT  
		Size: 25.4 MB (25437887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839eae4aef603ba497d98c83948abc648ed6b000c1d03761b5a774a82f143027`  
		Last Modified: Wed, 17 May 2023 00:26:45 GMT  
		Size: 12.7 MB (12674206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c9552b6fbcd8a1c888d1cac9bd51fc3896f0935acd3313d0ce405b202d4a2134
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40367403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbeeee865ec4f1a0a232360e8e370f6387b154cb14ba2ef0a60d6a0caa90a8f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:23:18 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:23:19 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:23:26 GMT
ADD file:c9e694041e535b8a119a8dd2c03795193f66cbbcceb27694bfdae2411765e386 in / 
# Thu, 20 Apr 2023 18:23:27 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:49:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eedec38ef10e1ff872f423ceae12828c5413c8183c216098c34342de77e9e5a3`  
		Last Modified: Wed, 03 May 2023 17:40:37 GMT  
		Size: 27.0 MB (27017867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b19b0b741f1c54f6a360843f1321028128af5d283a1d8f0f5f66bf8beece0a`  
		Last Modified: Tue, 16 May 2023 23:58:57 GMT  
		Size: 13.3 MB (13349536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bd4afbaedbdabdfe562fe4bb6b755dc3f19036a578380191e9f6ca1c9d1f0a58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47849304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f7c5ac74000bb956e9fa96be7a4c87db2073b0a142b8cb92f596db372ab5bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:20:26 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:20:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:20:26 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:20:29 GMT
ADD file:8d28b8fff20cf3ef8af5805d942e8aa5d19026e5ee01beb77e5863eb33637893 in / 
# Thu, 20 Apr 2023 18:20:30 GMT
CMD ["/bin/bash"]
# Wed, 17 May 2023 00:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cff954998e64505d58ea7cf2bf1a248c9fdc2287c6f6c0f41d3268aa8df574bb`  
		Last Modified: Wed, 03 May 2023 23:42:18 GMT  
		Size: 32.0 MB (31996798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27aa53d052871f8af1d008e844405fcfee71156e0db99a5f455da388792a32a6`  
		Last Modified: Wed, 17 May 2023 00:52:48 GMT  
		Size: 15.9 MB (15852506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:20c98320ebce78be25ddbcd248443efae34cb51df3e705952abfd968a2551d9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40253760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbaf57c1f79c81f69edeaf28891628e442417d848ba856d40bba55d169ce01de`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Apr 2023 18:21:08 GMT
ARG RELEASE
# Thu, 20 Apr 2023 18:21:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 20 Apr 2023 18:21:08 GMT
LABEL org.opencontainers.image.version=23.04
# Thu, 20 Apr 2023 18:21:10 GMT
ADD file:96d7710293ddafe0813d47d0fbeae45dc31a20c6115c489702cab4d2352d48bd in / 
# Thu, 20 Apr 2023 18:21:10 GMT
CMD ["/bin/bash"]
# Tue, 16 May 2023 23:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e12ee780e94e13677b8efd3cfc5219f323ee331fab05eb1f1c59218a106122b`  
		Last Modified: Wed, 03 May 2023 22:34:25 GMT  
		Size: 26.2 MB (26236160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc738121c9813521fa4a0fca88e02cb1f66ef200380dff38dd077ab483e2c4b`  
		Last Modified: Tue, 16 May 2023 23:57:26 GMT  
		Size: 14.0 MB (14017600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
