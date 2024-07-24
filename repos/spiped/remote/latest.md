## `spiped:latest`

```console
$ docker pull spiped@sha256:b1b99c4ed9404be453c9a486af208451a5afd4ca2545700d5fcb290c4f973473
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:a91b5b88c1b4beb67369e9c330e1496cd744daee5fad434809edc748d03fc4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37995583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561b03ff281146f66e0c1df57d1d972e4dacd9d82b90e6673b931c0bc63a51d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04a3ee6bb9286ef1718ea2d65215ccd30217a4d9141e91c0892a27988ff668a`  
		Last Modified: Tue, 23 Jul 2024 07:28:28 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e96dfa4385421bd0b333513120a5020d25e33ca8b183bc72b1fe8572a3005e`  
		Last Modified: Tue, 23 Jul 2024 07:28:29 GMT  
		Size: 2.4 MB (2397937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67501c20cd3d50a07b8aec28e9d761fe8f67c66bfc1681141cf2f499d3cb62f8`  
		Last Modified: Tue, 23 Jul 2024 07:28:29 GMT  
		Size: 6.5 MB (6469817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a706340bb936c15041d124988815b911e8f240e27a497337b0b14076c4a79f`  
		Last Modified: Tue, 23 Jul 2024 07:28:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ec42a8f2d8a58dd79ce90707ae13b2758b07e2d506d4eeb72773fbcd6ac2bb`  
		Last Modified: Tue, 23 Jul 2024 07:28:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:9b6588db68fbf02c37b6569b1a6cdc9a677fd8794d761709497b38caf40419c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3522295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b76b268014e43e68cb39d364efaf08fa7c15c9f2cd8782f84cb215a60a05ec4`

```dockerfile
```

-	Layers:
	-	`sha256:77cc422cdc49d4b222b341be0d30bc85bedcc31666ac1667a73a4c8e688c39e8`  
		Last Modified: Tue, 23 Jul 2024 07:28:29 GMT  
		Size: 3.5 MB (3507449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb7faf401c1735655f9c61c3bd4a88e9e1478868bc370823940561d134538bc0`  
		Last Modified: Tue, 23 Jul 2024 07:28:28 GMT  
		Size: 14.8 KB (14846 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:e23ba8ed10725fffc123326e1bf874d4af78cf070a6d48773c247019269db630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (34020062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b37d27abb3929d8501905492830da84d5ed44d02be65001beb7d7ca1a0a0c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:752589c0ca446e2e74ef0b8c412eabb01e2a8035cfec47b1d9630b9f704fbda7 in / 
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b695a3453560aacd42060f43ccf1cbd7d20412f50126ca6a469af38d3fe1e5b1`  
		Last Modified: Tue, 23 Jul 2024 00:01:19 GMT  
		Size: 26.9 MB (26887299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4ca2a8b8ba100ef238fbc2b8b7a3835fc5c06b23eda962c1bb3e4cd4ede6be`  
		Last Modified: Tue, 23 Jul 2024 16:25:20 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95fc686e4724161a11e2a8a885c622bd5c429e99dad4b583ae92797b8025e31`  
		Last Modified: Tue, 23 Jul 2024 16:25:21 GMT  
		Size: 2.0 MB (1993935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df97a25f3e9f1c0e30f62da9a9c84855d26968ca6be35dfc5cd3c1a0d7d12c`  
		Last Modified: Tue, 23 Jul 2024 16:25:21 GMT  
		Size: 5.1 MB (5137289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce31bb2a1f5235133e20dfcd1c6d545109dc2573babb88dd04f4968e4e052ac`  
		Last Modified: Tue, 23 Jul 2024 16:25:21 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e960e7d427185c19ec14acf15b7e56d284ab59db5e92cf3a371c2b9782942886`  
		Last Modified: Tue, 23 Jul 2024 16:25:21 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:4d3981c3f8062a62a8f80d6b6c2202b9b722591cdc469e5d012bda021e5a1597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3492772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc244e29336809a9b72380956692b2f632e69c0d90828b1941ddbcac62f9a6e2`

```dockerfile
```

-	Layers:
	-	`sha256:2823caa5226bbdcaef42ed91be5dc8d7ce1ee10ea3601239c8069a8c099384bd`  
		Last Modified: Tue, 23 Jul 2024 16:25:21 GMT  
		Size: 3.5 MB (3477830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d581ceb4451e896cd102c07103498a82f7ffcd1c96fa7787c267f8510584a638`  
		Last Modified: Tue, 23 Jul 2024 16:25:20 GMT  
		Size: 14.9 KB (14942 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull spiped@sha256:5faeec13d6c6fbb099704b2857470b1b790220aa4be28cb9578aacc6cefc3b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36882483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0faaa56010532211c3176bb2a9a7a68f7f94d8636fc0a8b4bc6c9f27430c3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5c4d8d704ff86051d4c0dd81f2bbaefe451d43226a8d47466dab62c46b508e`  
		Last Modified: Wed, 24 Jul 2024 08:39:06 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60370a55b75a0d7d4622d40510a9c0a78e54c6a285e743ad23051fb6cba3377`  
		Last Modified: Wed, 24 Jul 2024 08:39:07 GMT  
		Size: 2.2 MB (2244281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b141ef81200b8e13d6d7e82609485ca8c443a9111b208ab7e1500fe61337e81d`  
		Last Modified: Wed, 24 Jul 2024 08:39:07 GMT  
		Size: 5.5 MB (5480088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1321b50b7614479633681a896d681f20f51a7f97b457aef75e62f21b024ace6`  
		Last Modified: Wed, 24 Jul 2024 08:39:07 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7a51432a87dd249e6bd743577f39aa38f68a76c8e77f8d6cb6314f8073acf9`  
		Last Modified: Wed, 24 Jul 2024 08:39:07 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b519217837c6313ab98e975ade15979ace319030c1ae6d77b769410c16dcb43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3493794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25369e234615a9641a69fbfd9522f1e1b981a2460e7207649fcbbad6b3f7c2f6`

```dockerfile
```

-	Layers:
	-	`sha256:3c9335c1009ae807c5eb18a767223a1ade07f16938d879fd2472cf563e559b21`  
		Last Modified: Wed, 24 Jul 2024 08:39:07 GMT  
		Size: 3.5 MB (3478639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc4edec61cac72643f72f3144a8ee138b30c26cb0aa07165d37f82855dd3740`  
		Last Modified: Wed, 24 Jul 2024 08:39:07 GMT  
		Size: 15.2 KB (15155 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:b411e2bd771874a5c5522a5ba602a32daab68cd662c2b7435e10af0481ebc1a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38480370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9185eef7d29c995c2b7a897bb6c4a760534cf7a2df035680a2eb710b2a143974`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 14 Jun 2023 10:03:17 GMT
ADD file:9b63a9d86a51a3d56d700d09e1152578d700ba4453d852325d8eb9896534f3ba in / 
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["bash"]
# Wed, 14 Jun 2023 10:03:17 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Wed, 14 Jun 2023 10:03:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
VOLUME [/spiped]
# Wed, 14 Jun 2023 10:03:17 GMT
WORKDIR /spiped
# Wed, 14 Jun 2023 10:03:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 14 Jun 2023 10:03:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 10:03:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7fa64a47f35cb425a1275bff76c45df3b76d3ff6b07911737090b82e4f221e93`  
		Last Modified: Tue, 23 Jul 2024 03:57:51 GMT  
		Size: 30.1 MB (30144309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86559b83c8fe627d8aadbfa7cceca3c501bf695f90943a290945b00c07aae1f3`  
		Last Modified: Tue, 23 Jul 2024 06:10:57 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4ab1b2493d3b6687495d1e8c1408a6d68786a241edba3ed4ea6192ab71d60c`  
		Last Modified: Tue, 23 Jul 2024 06:10:57 GMT  
		Size: 2.4 MB (2393445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad92fcc5ea750e275a50c2b3d6160c16ed0fb41663498b51a072314f8f0dc81`  
		Last Modified: Tue, 23 Jul 2024 06:10:57 GMT  
		Size: 5.9 MB (5941076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7540a931a1558c7b81bdc9f00c85a127e18f0823d65593488e50a09a84df700`  
		Last Modified: Tue, 23 Jul 2024 06:10:57 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ab807bce315f5eff9095a30df23c139710bee0460edcdae14e64b80b634cdd`  
		Last Modified: Tue, 23 Jul 2024 06:10:57 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:1723408aac2650bde593a932505845257244f06e3f7789d45f66f3e267248e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3516185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:197caf13691fab363ba24035e78e5edf617f883d875086b83f5e1884d9b01388`

```dockerfile
```

-	Layers:
	-	`sha256:e44c2b01cacc48d0def9c5e8184c5dbf4c6ba3bc6c86a518816378364d1e1ed7`  
		Last Modified: Tue, 23 Jul 2024 06:10:57 GMT  
		Size: 3.5 MB (3501372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:549136ce57482d995212ada7e188fdcd236f799637cad575c6c90fd11c1eb1bf`  
		Last Modified: Tue, 23 Jul 2024 06:10:57 GMT  
		Size: 14.8 KB (14813 bytes)  
		MIME: application/vnd.in-toto+json

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
