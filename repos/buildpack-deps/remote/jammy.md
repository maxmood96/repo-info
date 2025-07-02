## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:43ba74f05af4ebfb1ef07553668a45754b6f36e89ef65946b35b7f9c37b42939
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

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5d4011b61505d673a5350c9f2ad53747ea92d9d0491082932d364afd6958f82b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (249046275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3cc43003aeef75235ad5392fd52e005118705e2721cadad8722be062033206`
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
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e87101798c1c992d7c441a146a64a4a76a20702382a0e0ad72a873e291446`  
		Last Modified: Wed, 02 Jul 2025 03:09:59 GMT  
		Size: 7.1 MB (7103261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a1aa76818dce63f07dd58dd5d43f128f03c6e179946ade2073fc935ecfd682`  
		Last Modified: Wed, 02 Jul 2025 04:11:46 GMT  
		Size: 39.5 MB (39485981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e869816fab3c2d9c5f91c219b2a3dd7f517ff81251a7f6ad17ec0593e3d0a1`  
		Last Modified: Wed, 02 Jul 2025 07:21:22 GMT  
		Size: 172.9 MB (172921347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0f2d4a4458d62bbca2e380eac4150684c0f08c1a7ca69edf857c4d6e0c563821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11849589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfed42c3d5d803a5f5c43faea9d1b7317fd66c600787a3d1ea1fddb13a9e0b38`

```dockerfile
```

-	Layers:
	-	`sha256:b299ac9832063d5a633eb540d4bcf8c87876a763bd498f5653c03d14b54753d3`  
		Last Modified: Wed, 02 Jul 2025 07:19:23 GMT  
		Size: 11.8 MB (11839386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2171e1db7eabed5a642736b6544a8201282ea7331ac8ec935b6122abfa356a53`  
		Last Modified: Wed, 02 Jul 2025 07:19:24 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f58417aeb5b3505ded346b977fed0e854fa92a58b85750a8d2b8668a5469fe29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216270592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88652a2de31b72e698adf8cfec89b493025940353232c558a94a3d5362e9099a`
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
ADD file:a68d8d0994670732edac30efcee96eec3850856e5c33c1c7fee7fdc59173ac3d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f35c50ead1843adba7d4d13281d31bc17c201a55b8bd1a3961e1bcfd131b762d`  
		Last Modified: Tue, 03 Jun 2025 13:42:56 GMT  
		Size: 26.6 MB (26640475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade18f0cb153eb0e80505edf909a0b5fb573468108f73d59398826c27dd2252`  
		Last Modified: Tue, 03 Jun 2025 17:26:26 GMT  
		Size: 7.0 MB (7007661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edfc049546e2833bbae11371047122a90cc58851d9baf3c81cf215428e6784f`  
		Last Modified: Tue, 03 Jun 2025 17:26:31 GMT  
		Size: 42.2 MB (42244551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fbecdf9700ff0462af026066061a3df6eea7ceb45bfa67d8188c3e205ef534`  
		Last Modified: Tue, 03 Jun 2025 17:26:41 GMT  
		Size: 140.4 MB (140377905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88d8801bcfccaf49e89d9083905e5f288defe0fd150e5786230e2ccfc7d2fe2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11349506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0ec8c77d8ca9c4c53c7d539485a2e0007148e7e4d1ea008e5c0da5ef8182d0`

```dockerfile
```

-	Layers:
	-	`sha256:ac2d479d35cd1c65d782b704ed23a0bc4beadad73d2244361a07830e190894a1`  
		Last Modified: Tue, 03 Jun 2025 17:26:28 GMT  
		Size: 11.3 MB (11339244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aef2607ad17512e05a3167158fb3ae5515b193996702957b93643bb0596f3073`  
		Last Modified: Tue, 03 Jun 2025 17:26:29 GMT  
		Size: 10.3 KB (10262 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:aec1b680d949f2cb2e4669026e49c3ef31ba4d1cd2faffeb001f5016b190ae7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240175696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cea38b67f8bd061df7b289ce3fc7e95fef068013d2051316d35d38335ddcbb`
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
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc8f9e3619942200ecbccd8a285496c9f5f75c9e60a1de3a2f4dc84b79a25af`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 7.0 MB (7049073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b94abd03e0d697b3738e4aeb08f56794e94f092a06971fd222b20f05caa82e9`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 39.4 MB (39379660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2043013db3e8402d36496875235c8e43609da353e2e145cef4efe41f699a7a79`  
		Last Modified: Tue, 03 Jun 2025 13:48:16 GMT  
		Size: 166.4 MB (166391382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:21b13177d777d903873ad42612142857737af04e9f68241bcf2821eb5364b8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11555970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023c09542b303dd1fb21a8d7a6cba268da86cbddb44ac70c581291ff4f217df4`

```dockerfile
```

-	Layers:
	-	`sha256:854d2dd9a9cb5011d27d32aee469d8a2d77c66ce32bf233337e51ac293cd4dfe`  
		Last Modified: Tue, 03 Jun 2025 17:26:32 GMT  
		Size: 11.5 MB (11545688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a852918860656a383374ac53c03a3d83d13b94a0c30793dc50797e89ce5825`  
		Last Modified: Tue, 03 Jun 2025 17:26:35 GMT  
		Size: 10.3 KB (10282 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bc455b3a9d1c94783765eaafb2c9f7b58c5a01a376e9ce36567ac9120430aed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269786200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07452b26a0bb0ffa04c694cf1de265e4517494346250b4f394002c865fee4c35`
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
ADD file:ff7ae346164d0b3da702390fb0f6f4187ba164036794a6081fdf0f9817b59053 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b728b0b1adf8a1b191ffc8bfd1fbfbb2bc25a989db32698511ae9a36f8b82a7`  
		Last Modified: Tue, 03 Jun 2025 13:34:58 GMT  
		Size: 34.4 MB (34440357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f199bc4ad98d2856395093db736f7cee937c730bb3d218bbf267319ae0f77073`  
		Last Modified: Tue, 03 Jun 2025 15:23:17 GMT  
		Size: 8.2 MB (8181061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fe8682996947e855124ba09e9d7bfe031082f75873ffcf2ed2f161528cde5c`  
		Last Modified: Tue, 03 Jun 2025 17:26:48 GMT  
		Size: 43.8 MB (43767012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf61fe4fec6eb498ebe7dc523e903e6f15cddcaed669e7fccaf204ebeae05a`  
		Last Modified: Tue, 03 Jun 2025 17:26:58 GMT  
		Size: 183.4 MB (183397770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f3f4ae0bac48cfe9f1af7225dc56e85f5eab0982a8b57df02e8ed08f0e4239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11519617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4548e86c41f252fd26e13308fba87c80336d59aaf3070451b24fa9528424d4`

```dockerfile
```

-	Layers:
	-	`sha256:9371b58ce372e0ee467cd3e795b78ed8832d8be60f7fc7579f6f7ac980c4844e`  
		Last Modified: Tue, 03 Jun 2025 17:26:41 GMT  
		Size: 11.5 MB (11509382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0398582b96a24edc0974bcc91eafbacf982bcf7a7aa88d7ce5cffa243ed946aa`  
		Last Modified: Tue, 03 Jun 2025 17:26:43 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:279659f23eda9679fc5aa0f125e9e3b3e103a82f6fece15c978ad09fb4caae94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274249205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2bf7049b8ee25947887ea6cd31b1c6b5d49c80d3ef34ddc5be104b33e65c7a`
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
ADD file:805054292411bfacf95662e1995adf90eef5abc97c604865fe65b213d7b41a1d in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:37769df37bf710dfefa24b110325d4a7bc5e0c1af364d18ad2da15a09b327dde`  
		Last Modified: Tue, 03 Jun 2025 13:32:31 GMT  
		Size: 27.0 MB (27038448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03983569ea2a2387b0d1cda89603d34e38695b0e017dd4a2109d9c8e42ba2191`  
		Last Modified: Tue, 03 Jun 2025 17:26:49 GMT  
		Size: 7.1 MB (7116346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c4b08e359be6039c2b07034529ff7d022b17172f9e2ec0b66f13835b25c218`  
		Last Modified: Tue, 03 Jun 2025 17:26:56 GMT  
		Size: 42.3 MB (42302827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b61c22557490022aaf6e06bf129465ff1561873f2194661561267f9af1a02a`  
		Last Modified: Tue, 03 Jun 2025 17:27:23 GMT  
		Size: 197.8 MB (197791584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adbb1c8f6fbd13b6e3e8227b8d1d7c15e94730e4a35da857ae4112ddc085773a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11500625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c468886959098f1d11ad1b13c7652c4825f85a0443e5e0fc24c253f386dfb3`

```dockerfile
```

-	Layers:
	-	`sha256:7ee340d0e466c9bcf8e33ea73693d7de347247bb809a9cf86a64d849deecf577`  
		Last Modified: Tue, 03 Jun 2025 17:26:48 GMT  
		Size: 11.5 MB (11490390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fffcbe3e754232944f98b64afa26ba86e0bc6761be167f286a49db2b9cbc0a2`  
		Last Modified: Tue, 03 Jun 2025 17:26:51 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:87aec182a3916dd3e7d9d5791562a5b21a04997910d031b103f19cae6d99e191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223036474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af778d8752c852ea5f36996c5d06e9a7ba0e697828690d9369c2ca511196e4d8`
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
ADD file:f153a831e3d8b37cf290a0e64d208348b0231dc123ac8127decb555f982fe306 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cfa1809998a055f097abf4f27759694a126f64b86912d130052f49642e2be80b`  
		Last Modified: Tue, 03 Jun 2025 13:35:34 GMT  
		Size: 28.0 MB (28000600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d72f21f5960e611ba62223730c2365f458813d47dda4f15dd2001615e7599f`  
		Last Modified: Tue, 03 Jun 2025 15:23:17 GMT  
		Size: 7.0 MB (7014114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2065174a163a6718c68496123e0640ad969ccc9010c78f9bee48547a2aeff9`  
		Last Modified: Tue, 03 Jun 2025 17:27:01 GMT  
		Size: 39.4 MB (39433827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5315ec1b80ed4ad35833b129997fab3ed9770d529eb57240358009895391b2e`  
		Last Modified: Tue, 03 Jun 2025 17:27:22 GMT  
		Size: 148.6 MB (148587933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e0cf54d68cd94c11d7119f026f1883ef632b0455ae3ac6aaa22a7737d02df982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11374113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934e34c65639c6afa9abafdf36ca756e220c441e1eda297ce9b5ddb6e1503a02`

```dockerfile
```

-	Layers:
	-	`sha256:80dbc6195fff0b503e78fcffd04847686409738e816fcb5156a4e055c475aa8d`  
		Last Modified: Tue, 03 Jun 2025 17:26:53 GMT  
		Size: 11.4 MB (11363912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb41e97cd2d512b47f0cdda40de711da480f865e1b102a13a15fee6d6186fc53`  
		Last Modified: Tue, 03 Jun 2025 17:26:57 GMT  
		Size: 10.2 KB (10201 bytes)  
		MIME: application/vnd.in-toto+json
