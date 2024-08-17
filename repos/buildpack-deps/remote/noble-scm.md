## `buildpack-deps:noble-scm`

```console
$ docker pull buildpack-deps@sha256:f2b37d40945143f8689f0501cf78aba559e6578de28b25a0b2cf018a102c8f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:noble-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7cca663125706539abaff96a7d22357007092215aee78e08316021ff7e5ae9e8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89648628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1145143d9069dbb8bdfdc88150b49b7e6a63b0813dab5fd0da1f1aded0f85620`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2b3981cac065674916a0b4e8d1b5d7eb49d9863a79ec47ba37336c70496ac8ab`  
		Last Modified: Fri, 07 Jun 2024 20:58:31 GMT  
		Size: 30.6 MB (30566626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88b5e33190acf28dfb7f13b5906a424ba9bae4ea993f48bf0335c34b3525c9`  
		Last Modified: Mon, 17 Jun 2024 23:14:19 GMT  
		Size: 13.6 MB (13610093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72ee9d28d3323b69c1e98217df15ce99add4d7029330c19edf34afb08d0f6ec`  
		Last Modified: Mon, 17 Jun 2024 23:14:33 GMT  
		Size: 45.5 MB (45471909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5123e18b23283e983435188b0efad6a2bf55810a9c8e88df1ba1315a7444f2dc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89468708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd91127d1bd2cc71e111ddd276b455226127a0fbcef23a11d5cb2f87709501d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:56:56 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:56:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:56:56 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:57:05 GMT
ADD file:b748f7f0dae18a5c9b75daf9f538536d4e2ef86d0765531567a4dfe83eb96ff0 in / 
# Fri, 07 Jun 2024 11:57:06 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:17:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f8d8d41dba086e9a9d743fe5b990924057d2470da76cc6ffdc8e6e7bd5aaeee`  
		Last Modified: Sun, 09 Jun 2024 02:03:28 GMT  
		Size: 27.7 MB (27688462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3542190a7a76ed477fea330a487588cd93a8a0d1a7d7edabc78ba8db3b4b4243`  
		Last Modified: Mon, 17 Jun 2024 23:22:52 GMT  
		Size: 12.8 MB (12767209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a3d83d18813ec3c59260e725e09e29242f2cc5cf4e44e224657d25db8a16c3`  
		Last Modified: Mon, 17 Jun 2024 23:23:08 GMT  
		Size: 49.0 MB (49013037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d477af5db35ff44f214f92b84de818dd3f03a0f70c7d55e35b9dd545853ff67f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88785094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e775b4006c238856702c6adaf6bf2c6669302a6aa934b083054d6e0dc514be4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:19:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3c95e61d1355f5aace462c7753a3798609ae289bd54e5eba7c974757972cb33`  
		Last Modified: Sun, 09 Jun 2024 02:03:31 GMT  
		Size: 29.9 MB (29907980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9daf10a4c85f4e13c3dd399854dcf26021fb061d3779d0fc8b6f68d09ee17b68`  
		Last Modified: Mon, 17 Jun 2024 23:23:47 GMT  
		Size: 13.4 MB (13446966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609a6ad39dd54642e8c65403c8463121f544eaa46734a9398e92504cfc9b58b`  
		Last Modified: Mon, 17 Jun 2024 23:24:00 GMT  
		Size: 45.4 MB (45430148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cd44cea5713601b9d67059c57e116e28b331fadcddb64dffd60f12cedfc40923
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.3 MB (102339819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295ecb5a3e55316f1ba417d43ce139c5137df9033cf99f943ab4dd924ecbb00d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Sat, 17 Aug 2024 00:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Sat, 17 Aug 2024 00:40:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb5c4ccf8117e814932a8d9e3dab429a8f90482e5881d43fa8b5af0f7888c82`  
		Last Modified: Sat, 17 Aug 2024 00:47:53 GMT  
		Size: 16.0 MB (15998331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b02f58c3bb9b5e807e488d763aebfd412e5c890fe7395af264f03013905316d`  
		Last Modified: Sat, 17 Aug 2024 00:48:14 GMT  
		Size: 50.7 MB (50713751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:noble-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b5e817c6055ba102aedf7daa16c007aa70e27821ff653e39f3541ad249ec340d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92793545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4887a2fe2a1ed08dfbb5a70d4130f2d0aa6d26478ccf9e13890eff22d6363f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
CMD ["/bin/bash"]
# Mon, 17 Jun 2024 23:02:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Mon, 17 Jun 2024 23:03:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a92fbd042f28db16ac0b86e8841e492b886d701356ad15137dd1c8c01886aed5`  
		Last Modified: Sun, 09 Jun 2024 02:03:37 GMT  
		Size: 30.7 MB (30691272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce3e53cba658c999f4ce16677ecd64270b0b0449f58cf7d49accf717676df09`  
		Last Modified: Mon, 17 Jun 2024 23:07:30 GMT  
		Size: 15.0 MB (14983870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1284840252b1ffa18ebffcad2e64de45bf1abd606a36285969141c9abcb94772`  
		Last Modified: Mon, 17 Jun 2024 23:07:43 GMT  
		Size: 47.1 MB (47118403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
