## `buildpack-deps:lunar-scm`

```console
$ docker pull buildpack-deps@sha256:e3ceed08bf978f8e950b96db1d6b22ea5d217368b139dcf6762c9afe284696b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:44f8eb9cc019f857e1e3480bf134c9e875e8e60bf03412658fbcbef9105862c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81728345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ca31773c129e63d52677257f6cd307c0d0e47d5c8752c1201f68bf8e630c1c`
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
# Wed, 03 May 2023 20:07:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:08:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6c6b907db42b6f1b03645d7cd822afa676930182719410e133c9480fede45d4`  
		Last Modified: Wed, 03 May 2023 16:46:32 GMT  
		Size: 27.6 MB (27604112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db8f628eadae81eed04537247fbc6272b83d4dce338e7ca875143d8702c14c0`  
		Last Modified: Wed, 03 May 2023 20:17:07 GMT  
		Size: 9.8 MB (9781500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed7b5916395be6abd3a3f41069beb08289681b448f14afdd062a8d630050805`  
		Last Modified: Wed, 03 May 2023 20:17:24 GMT  
		Size: 44.3 MB (44342733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f27658d47ae4212f9c1edbe5e24c6d4bebdfda7ef7919619e1231de48305ba72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83229177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77800e77962fb401db2a3ed04608a462bbccfe7644e2fdb5b12fcae3d76a58c`
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
# Wed, 03 May 2023 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:04:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f8f976bcf9a33d090294b25c3fb3430a5833ce92be9f477471addb457c0dc3ac`  
		Last Modified: Wed, 03 May 2023 22:12:58 GMT  
		Size: 25.4 MB (25437887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9653ea3e4c9dbd15b264a4a6a10dddb593e3d21e899c82f1684533e0b63e3191`  
		Last Modified: Wed, 03 May 2023 22:12:56 GMT  
		Size: 9.1 MB (9103832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51bd461eaec416e884ed0c9598fa7c90d7dc6a5ce5f4cc445fcd549b5b56c38`  
		Last Modified: Wed, 03 May 2023 22:13:14 GMT  
		Size: 48.7 MB (48687458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7e9a6a6a294bfdf961a3ef386b0ad0a2794b39395d793aefd6f7d4a1801f942b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80787620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8548b6b81c08942c7b4d1a2477b17510ab3930edc68bd50e227a816d48c4af4`
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
# Wed, 03 May 2023 17:31:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eedec38ef10e1ff872f423ceae12828c5413c8183c216098c34342de77e9e5a3`  
		Last Modified: Wed, 03 May 2023 17:40:37 GMT  
		Size: 27.0 MB (27017867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccd6cc41865996a58e55a61d8d025e38c9ceac37b701e772a343eedc0099b6e`  
		Last Modified: Wed, 03 May 2023 17:40:34 GMT  
		Size: 9.6 MB (9579134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bc689890de17241df748ee35c20239945e4e35c36f83c9e737d61b2c56f96d`  
		Last Modified: Wed, 03 May 2023 17:40:50 GMT  
		Size: 44.2 MB (44190619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f31311201a45054ccc23d8d8bd7dda48bda2b27559199d5b09b1afeeed83a0af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92527049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebff396a1610b6a6fbc901a8c4bb492ec38101dc0d39b9b3ada38a05bd4fa78e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 00:04:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 00:05:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5246a498088fdea38dd591708a487dd16b5d2f571e44944585476b1383b4a22`  
		Last Modified: Wed, 03 May 2023 00:22:02 GMT  
		Size: 11.5 MB (11489391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed85444b7e5aefc964e01fdd7844636de2b2854264bda895d390390aea2cdda4`  
		Last Modified: Wed, 03 May 2023 00:22:25 GMT  
		Size: 49.0 MB (49040925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1c14a3dce9dfde2087dd06958c55cb0e10f2d36a23cf134ea42357d0e3e4ad07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79909509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd5f53fb59ebde034c7d5212ba808fa912af46cb2c41c4adb21d54ae6d253674`
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
# Wed, 03 May 2023 22:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:28:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e12ee780e94e13677b8efd3cfc5219f323ee331fab05eb1f1c59218a106122b`  
		Last Modified: Wed, 03 May 2023 22:34:25 GMT  
		Size: 26.2 MB (26236160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35b4653c27a1514d6d5fcc328744240d9a67325ba944a6e73a685a8c3aa6a88`  
		Last Modified: Wed, 03 May 2023 22:34:23 GMT  
		Size: 9.5 MB (9454421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b0a3224e7cbb9d6e6d1f3f8998601dd2fb534488293c26a3f062103de86c1f`  
		Last Modified: Wed, 03 May 2023 22:34:37 GMT  
		Size: 44.2 MB (44218928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
