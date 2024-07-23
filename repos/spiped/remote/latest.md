## `spiped:latest`

```console
$ docker pull spiped@sha256:890f2a9d0f096492177697e251595e4f9a38cb496766f9276a10f2e4d3019adf
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

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:126cc26e6dfdc483e7410ac6c49e84390618b793e9dbf9ac64f55a77ef4ef82f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38190927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93063a40ddd2e049c5ed87cec42578cfaccdb2751c5c92166d233954f808435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:53:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 02 Jul 2024 05:53:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:53:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 02 Jul 2024 05:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 05:53:46 GMT
VOLUME [/spiped]
# Tue, 02 Jul 2024 05:53:46 GMT
WORKDIR /spiped
# Tue, 02 Jul 2024 05:53:46 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:53:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:53:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bef80a63e35443eca25ce60c49e94996abd387ba46d1f06b5250c64e12c792b`  
		Last Modified: Tue, 02 Jul 2024 05:53:59 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d214b8cf5b186e7b21991508e2040ec26e149c9aaf78078d673d5232a3eec3e`  
		Last Modified: Tue, 02 Jul 2024 05:54:00 GMT  
		Size: 2.6 MB (2591982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb6932a449c375a6364cfc966328813949299edf4a394cfd938e706c52b1f8f`  
		Last Modified: Tue, 02 Jul 2024 05:54:00 GMT  
		Size: 6.5 MB (6471105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60006a98fe47cf852a0e17390b81ee3ebb0eb6795956dbf2d7d646174f8b20d6`  
		Last Modified: Tue, 02 Jul 2024 05:53:59 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ca5620b85213a1b93ddde89e569a4adbbfa8ae70ce1b99d614bbbcb5140fd`  
		Last Modified: Tue, 02 Jul 2024 05:53:59 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:888c1adf16a872e85a5d80f6b68d5dd4e5af8c3d31d69588f2997eb6e103c477
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34215257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2010507629b1489103e6a0ffca4d496175e11cfddf4e097e3f87143699d4a73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:27 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
# Tue, 02 Jul 2024 00:48:27 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:55:29 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 02 Jul 2024 03:55:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:55:35 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 02 Jul 2024 03:55:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:56:00 GMT
VOLUME [/spiped]
# Tue, 02 Jul 2024 03:56:00 GMT
WORKDIR /spiped
# Tue, 02 Jul 2024 03:56:00 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:56:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 03:56:00 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8362470aaa98ceff9facce62e9450ec35667076e9d31820bd73a26a62fc52649`  
		Last Modified: Tue, 02 Jul 2024 03:56:08 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f4c09039b9f95be7973db15ac617066647843cc4034144037daeb832e2f0c2`  
		Last Modified: Tue, 02 Jul 2024 03:56:08 GMT  
		Size: 2.2 MB (2188090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a8853e9f1c5271a67b0a489d341c8456efbf382f9f04d0f9edc3083be18356`  
		Last Modified: Tue, 02 Jul 2024 03:56:09 GMT  
		Size: 5.1 MB (5138317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41ea1c736681353f76a03c5b69038d16a614da63dc58dab5900f9dd926ecbbb`  
		Last Modified: Tue, 02 Jul 2024 03:56:08 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee8fb4d471087ff593d077bd40824679008111ecfc85bed7c66db0e8c1f7047`  
		Last Modified: Tue, 02 Jul 2024 03:56:08 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:4d4afbe3328ead5eb024bfd5755bb85dfa3e7ead661830293530ef1dcf23f4cd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31648074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e2d83dca8c3583a5588650a9f7631bc029ee4d944261087b7513e1c03d335f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:02 GMT
ADD file:f2c0623bafe70d6e2d8748c6de4eeb93699054f8d34e62c6257b940d4e24e44d in / 
# Tue, 02 Jul 2024 01:00:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:12:04 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 02 Jul 2024 04:12:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:12:08 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 02 Jul 2024 04:12:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:12:30 GMT
VOLUME [/spiped]
# Tue, 02 Jul 2024 04:12:30 GMT
WORKDIR /spiped
# Tue, 02 Jul 2024 04:12:30 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:12:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:12:31 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:60ec5feb0c17c4f910ca5d3cefbda7bcc1ca066b4482707262696f589dabdcb5`  
		Last Modified: Tue, 02 Jul 2024 01:03:20 GMT  
		Size: 24.7 MB (24718170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6814c52209e7b87b8e0ffcc649023af5344cb721789b48507b03605d2fe4dc3a`  
		Last Modified: Tue, 02 Jul 2024 04:12:45 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26d7e3d37faab9b2c680a385b43ec9d3b7c46bbb3cc69f5f20057ea42d46b71`  
		Last Modified: Tue, 02 Jul 2024 04:12:45 GMT  
		Size: 2.0 MB (2048088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9d327a5c6983b07267fb3374da94343e75ac149acb0e6d5dfe50db65109059`  
		Last Modified: Tue, 02 Jul 2024 04:12:46 GMT  
		Size: 4.9 MB (4880253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73948fa704dc50dead36d816eb07923aaa70c5d6e0b6e5ff4a00fa9b168f6eb`  
		Last Modified: Tue, 02 Jul 2024 04:12:45 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd23cd3296ac702d58fab5fb7a92d57a3464013969eafaedf4e487dd07110f8`  
		Last Modified: Tue, 02 Jul 2024 04:12:45 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:27b2197c9305312144fc82966f04b82969feb222d7d378a356e7d797dac0ad25
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37078882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5a9aa34f388c1064e5286655a38c7494c5855650490eda548f56fb69f5a543`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:37 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Tue, 02 Jul 2024 00:39:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:48:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 02 Jul 2024 03:48:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:48:21 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 02 Jul 2024 03:48:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:48:40 GMT
VOLUME [/spiped]
# Tue, 02 Jul 2024 03:48:40 GMT
WORKDIR /spiped
# Tue, 02 Jul 2024 03:48:40 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:48:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 03:48:41 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089f6ab36c174307c40f53ac8b0853bbf569fbd54a51162495ea02f672a17b62`  
		Last Modified: Tue, 02 Jul 2024 03:48:53 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280d6f5fe1acf0aff44478f421d8616d42003808794f02fb2da6b4a668a497aa`  
		Last Modified: Tue, 02 Jul 2024 03:48:53 GMT  
		Size: 2.4 MB (2439039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e083ceae67ca1faca0a69a7fa6e52d3344cfcacc7b69284d9afd79eca00571`  
		Last Modified: Tue, 02 Jul 2024 03:48:54 GMT  
		Size: 5.5 MB (5481719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c6ebec0fadcfa0d4719eede229b7eb5ef4cc2cca3c184e6cf91025ecdb2096`  
		Last Modified: Tue, 02 Jul 2024 03:48:53 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:660d5b6d5d918d4268e720265d125ac13ea0ec1a5e51593b42672c9d544887ce`  
		Last Modified: Tue, 02 Jul 2024 03:48:53 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:26c713959c9b27d2325ee3055bd20d04a068523cf1d8f2e97806b971d8d17626
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38677188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2103f7824acefa296fb99fa6724388497fe84897d2aa7d819460d02aabc8e3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 02 Jul 2024 00:38:54 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Tue, 02 Jul 2024 00:38:55 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 05:55:10 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 02 Jul 2024 05:55:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 05:55:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 02 Jul 2024 05:55:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 05:55:42 GMT
VOLUME [/spiped]
# Tue, 02 Jul 2024 05:55:42 GMT
WORKDIR /spiped
# Tue, 02 Jul 2024 05:55:43 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 02 Jul 2024 05:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 05:55:43 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d109c82e6b1b0e9fefbf8f696e9c55e513ff028a011c7c917b854cd95d292157`  
		Last Modified: Tue, 02 Jul 2024 05:56:01 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a549dea08f59971d85fcb2c9a7b7c00cffa46614ab232df749bf50a641aa87`  
		Last Modified: Tue, 02 Jul 2024 05:55:59 GMT  
		Size: 2.6 MB (2589874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c086c3e6ffc19b97658d40efc5abbd211a6290f2abfab903f03628f5410be8`  
		Last Modified: Tue, 02 Jul 2024 05:56:00 GMT  
		Size: 5.9 MB (5941477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0ebce4df2df76e3a3a00f63dbe7c1188ef443a2ea640f5c2da81cdb494b2cd`  
		Last Modified: Tue, 02 Jul 2024 05:55:58 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f431f8a815075d887ec9db0ef8e5b95e8da42cf0fa74df60a2be66f82edd2f`  
		Last Modified: Tue, 02 Jul 2024 05:55:58 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:23723f5461b0d45c874a672986442149d8e03a6a17eeff1b9956dc44af10612b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36768631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6556d322e4009893bc7c5699c5d7315113dc4eadacf4dd4734a0291f5f9ae0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:23 GMT
ADD file:9a0f0c8ed27f6f2bb89272036da4d44a63dcaf43fb03528dd2d970fbe64ccc92 in / 
# Tue, 02 Jul 2024 01:18:27 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 13:33:53 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 02 Jul 2024 13:34:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 13:34:15 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 02 Jul 2024 13:35:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 13:35:58 GMT
VOLUME [/spiped]
# Tue, 02 Jul 2024 13:36:01 GMT
WORKDIR /spiped
# Tue, 02 Jul 2024 13:36:04 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 02 Jul 2024 13:36:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 13:36:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:cbefe199012545da86e0f461f1964dea0c9bab400e37766ee5f32b967423cf0b`  
		Last Modified: Tue, 02 Jul 2024 01:29:29 GMT  
		Size: 29.1 MB (29124929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379ce90422de90fc2be1d9f30f424a117499397204636624645153156e51463f`  
		Last Modified: Tue, 02 Jul 2024 13:36:21 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a9e25f6c79bd9637e9b88fcb0dd52fcb46b78073cece110a6b28e211d26dc7`  
		Last Modified: Tue, 02 Jul 2024 13:36:22 GMT  
		Size: 1.8 MB (1838643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70480cf01341efaa56dc03474a4f3ca69819a7e1b36523e4ba525bfde2fbc9b`  
		Last Modified: Tue, 02 Jul 2024 13:36:26 GMT  
		Size: 5.8 MB (5803547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c921d4897392b78bcc3d12f23e3b6675345e8b17487c6ace6afbfa5c49d224`  
		Last Modified: Tue, 02 Jul 2024 13:36:21 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a28372ba74da9a75edb122f847ea552f569bcccb11ad6bde105baecfe0c55`  
		Last Modified: Tue, 02 Jul 2024 13:36:21 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:64e897dd3e7f4154d0bf3b9faa652fd453f3a58790b529d703467f7925e1a96d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42319076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf722eda18e584a1c87d826c92ebcc1223dca18798f0d0983a79887172efc52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:35 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Tue, 02 Jul 2024 01:17:37 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:57:07 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 02 Jul 2024 04:57:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:57:12 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 02 Jul 2024 04:57:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:57:46 GMT
VOLUME [/spiped]
# Tue, 02 Jul 2024 04:57:46 GMT
WORKDIR /spiped
# Tue, 02 Jul 2024 04:57:47 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:57:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:57:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b000cf2f4c55eee231c60d2c86db9db4b3447ccbe42c0a410dd659898feca9`  
		Last Modified: Tue, 02 Jul 2024 04:58:04 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9490eb9ba754049a82ab982f26d2200036cf6fafa2cda34a5a0f0e31e89716dc`  
		Last Modified: Tue, 02 Jul 2024 04:58:05 GMT  
		Size: 2.8 MB (2772701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e22f6dd37f21af4a36772eeec9f92f20bec12528e8e4afabb04308b0a3cdc7`  
		Last Modified: Tue, 02 Jul 2024 04:58:06 GMT  
		Size: 6.4 MB (6422531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e50d6659b422a6f024fd8bdc05124304b222930167da822c8b4eb22beada681`  
		Last Modified: Tue, 02 Jul 2024 04:58:04 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3237aada7477348c528c2b95e408c7487253f7253c32de5f297f2d615117e0`  
		Last Modified: Tue, 02 Jul 2024 04:58:04 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:1e9d3625a92a7cb984d05141db23f78c5774c4794abbd031c0fb2f4adaeae7fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35141304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47d9bde1c9f74b014ae4c5fcc04ec08bd7f8f058bee077293f2ce946c9c2554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:46 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Tue, 02 Jul 2024 00:43:47 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:48:56 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped
# Tue, 02 Jul 2024 03:48:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:49:00 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 02 Jul 2024 03:49:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:49:13 GMT
VOLUME [/spiped]
# Tue, 02 Jul 2024 03:49:13 GMT
WORKDIR /spiped
# Tue, 02 Jul 2024 03:49:14 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:49:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 03:49:14 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de82708ce3d6d3b54a8d14d99fd6c0079e2f913302b5a11bfa37f07f36e3e742`  
		Last Modified: Tue, 02 Jul 2024 03:49:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27a2bc9eaa0c1a20186a3700f3a16a38f8c920e836abdd2701bcc2c1f5ad066`  
		Last Modified: Tue, 02 Jul 2024 03:49:35 GMT  
		Size: 2.3 MB (2263277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f96231a7f8e806636a3c4cadbe3f42f4a99f8d82b984e157fee3d722b3ef90`  
		Last Modified: Tue, 02 Jul 2024 03:49:36 GMT  
		Size: 5.4 MB (5386376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731a8f19e88a5d921760e8023cee1d598022dcbc4157dc500a27c54e297d6572`  
		Last Modified: Tue, 02 Jul 2024 03:49:35 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d438bc3dded40513b0ea72780beeaa7c67df51b34b8b6600b7067da7c0cc6852`  
		Last Modified: Tue, 02 Jul 2024 03:49:35 GMT  
		Size: 340.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
