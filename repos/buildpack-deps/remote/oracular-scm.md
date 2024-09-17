## `buildpack-deps:oracular-scm`

```console
$ docker pull buildpack-deps@sha256:e7a8f3c1918856b8dbbe6d6aca20652a01512da2c6aed6b46cc95f20872cfcf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:oracular-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1dbfd363c7265b73108465a8d3d29f0f9f581cb47beaad4ea0b3401cc66bad85
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97162065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11d235b4586dfae5f82c5113a4bcc2c2f300aec0770c713922eb195365e78a0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:58 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:58 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:00 GMT
ADD file:e0e1920c83dbb04acc51e3cea2d1100f9149baca28e8f9ca859721b92a00c661 in / 
# Fri, 13 Sep 2024 03:45:00 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:48:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:48:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8cdc21141b65ce4bcb1fda37d4d022dae065e029a30e7bf520c22f0a695a9634`  
		Last Modified: Tue, 17 Sep 2024 00:53:01 GMT  
		Size: 35.0 MB (35037517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b855f4b2872c5cc776792754e4a57964c452aaaa6fa69c1a8bc9ed3d1bf6ee`  
		Last Modified: Tue, 17 Sep 2024 00:52:59 GMT  
		Size: 15.3 MB (15307006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ebac33bb0b35e8874ec506bbc4ce286511296d30234e78372cf6cdb13cbb27`  
		Last Modified: Tue, 17 Sep 2024 00:53:16 GMT  
		Size: 46.8 MB (46817542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:12a47b46a874c599524492f8c571093df7d2524b0181552b851ecab6e85524d5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (97975273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417cccdaf24873a75e31ece8146224d802f454a148b4956fb9e14499f69a4052`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:07 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:07 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:10 GMT
ADD file:e9634ff8178ea06d2cd7dedd0f077e5501a6c0fdbb296cb0b7ef7d735c18ae9e in / 
# Fri, 13 Sep 2024 03:45:10 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:37:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:73a40ba9ed63d001697167ff54866082cbd3c39d46006a3791839b927eee00fd`  
		Last Modified: Tue, 17 Sep 2024 01:43:38 GMT  
		Size: 34.2 MB (34207534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b32b30620024d46a4a7a9d575c13217912a0ca5bf54c541a018d59bfd5b65a`  
		Last Modified: Tue, 17 Sep 2024 01:43:36 GMT  
		Size: 14.0 MB (13995288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc0b48238e77689d32490011b9eec7f8b42e661b5baadc8728d31db963ce0cb`  
		Last Modified: Tue, 17 Sep 2024 01:43:53 GMT  
		Size: 49.8 MB (49772451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:373b593b8fcc2bc70185776e5973a9dd7b5c0bfeb3249d6ea4471469f317f930
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96695398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57475d81c6eeec3edc4a5d1a241ba02add703605758ade1eb02d30ca7ac7593`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:45 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:45 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:47 GMT
ADD file:09509f4e7d531b71ff20f83a8fdb1fd7fafd2621a6c0d5cf35bee26ddf03028a in / 
# Fri, 13 Sep 2024 03:45:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6f192fbb9b2ab30739ebcfa04665d365d4fb63abf3e4c9a796803829bfaec560`  
		Last Modified: Tue, 17 Sep 2024 01:30:27 GMT  
		Size: 34.8 MB (34848776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea80fce0de88a3884c083b79a6bd7d132b5e10d46af1dd280165763a27986b3b`  
		Last Modified: Tue, 17 Sep 2024 01:30:24 GMT  
		Size: 15.1 MB (15080016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e6b6483c3ac4e3d3df1b1381200ba57b3548bddcc959674a665f97651815fd`  
		Last Modified: Tue, 17 Sep 2024 01:30:40 GMT  
		Size: 46.8 MB (46766606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d6c7636a492027cadedc80b2be66033e88bcb71afbfb869d1399a6e8bed8e49a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.0 MB (109044474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9076d4d7af26071c76e0e56979ffaf8e0a166374403bcb86b9496ffdfb4237e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:45:23 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:45:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:45:23 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:45:27 GMT
ADD file:5e35a64fdad21cdf96e70998641a823422343cb6ea2010b118d6476fab494360 in / 
# Fri, 13 Sep 2024 03:45:27 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:46:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 00:47:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4888f88bee4723604514eb67de9747f97c48812938a294f52e966dcad4b9cce1`  
		Last Modified: Tue, 17 Sep 2024 00:54:26 GMT  
		Size: 39.7 MB (39707210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2258f534636942cc44347387dfeec93cb3a51718f6b960d8eb5b1db05d18bc53`  
		Last Modified: Tue, 17 Sep 2024 00:54:21 GMT  
		Size: 17.2 MB (17182432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d032b3cccdd32b4010c1af161c1a432b31b8a95216f55327e02c652bd9616d31`  
		Last Modified: Tue, 17 Sep 2024 00:54:43 GMT  
		Size: 52.2 MB (52154832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8e27480fb5658d17fcad2c1b7a265bc681a9957eb3fb549267852b8893976201
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109327069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11b0a5e81034dc297b460e20a85d5365a9774cc36218611effdb2c1134b6e47`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 04:00:09 GMT
ARG RELEASE
# Fri, 13 Sep 2024 04:00:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 04:00:09 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 04:00:42 GMT
ADD file:fe1b6caff13e4673435edd0393d6a3f32627418ddd1d4f581d953510f87f8aa9 in / 
# Fri, 13 Sep 2024 04:00:44 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 02:21:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 02:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:adf60c3ca2ea943019774faf982dba804d10a64bd1a899c7b02591ef2bacbd23`  
		Last Modified: Tue, 17 Sep 2024 02:42:56 GMT  
		Size: 38.5 MB (38532888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d94ca004400cea4a3b19ceb645b60b2f4123c2ce8d0e9a3e087262598d72363`  
		Last Modified: Tue, 17 Sep 2024 02:42:44 GMT  
		Size: 15.8 MB (15825384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10db76789a2225592ba3f2c14ad9b00436b5d8aa72d91ad76d779dbdb33026fb`  
		Last Modified: Tue, 17 Sep 2024 02:43:56 GMT  
		Size: 55.0 MB (54968797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oracular-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:932d5e55c820ee37ded13972b2005a7d5a8b347daccda453bb92a0e6d55376fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99700636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d535f4dfc10d95fa40a20365b6ac144cf64260f38800c57559d0cd38ac0d61ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Sep 2024 03:44:47 GMT
ARG RELEASE
# Fri, 13 Sep 2024 03:44:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 13 Sep 2024 03:44:47 GMT
LABEL org.opencontainers.image.version=24.10
# Fri, 13 Sep 2024 03:44:49 GMT
ADD file:132837a4612be4355076a48f870207884955b63b76fd44ac020d79b2730a5f74 in / 
# Fri, 13 Sep 2024 03:44:49 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean
# Tue, 17 Sep 2024 01:25:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:34da9758d8d5a006f82493f0be0750682e1e1be81fd54054249dbca37bbc2bc9`  
		Last Modified: Tue, 17 Sep 2024 01:29:53 GMT  
		Size: 34.6 MB (34602418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9992b219704ef108ccf2d8abde848bab6670645ac4a1d49f612d8e821da3bb`  
		Last Modified: Tue, 17 Sep 2024 01:29:50 GMT  
		Size: 16.9 MB (16870086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3709c28ea82a54374ee542db4b1e24030f79925aa8d7be6969a213a51299ee8c`  
		Last Modified: Tue, 17 Sep 2024 01:30:07 GMT  
		Size: 48.2 MB (48228132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
