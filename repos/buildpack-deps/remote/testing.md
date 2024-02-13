## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:2b9d7ee09f795a9beb0434d09f93ec6683a6d25373c2f781e02406b20a75f84f
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2ccf6b25b8566453f5f526fbd4c3831aa06a4bcbebd9493e84e09e3b4570117e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.8 MB (409750740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca6651cb595f48fdb562484fab92a2371fd14450365d10b7516be35283aa314`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:29:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e96ba6a4df5f9a034d0f042c6ba596296abfca3f619a6c6625bec56ca08f02`  
		Last Modified: Tue, 13 Feb 2024 01:35:16 GMT  
		Size: 66.5 MB (66454282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6861838beebbc0b557a6de8a7fb09bbccaf7158cf0c2b59348823b05fdd0d3`  
		Last Modified: Tue, 13 Feb 2024 01:35:58 GMT  
		Size: 264.1 MB (264114976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8c0cc9887ce02ed395a536f49065fe63711009cee94e2d79abca0ff517ce3ad5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.0 MB (373029590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c2092ce016bdf4f1cc7ccdd8be6788c7bc03de1cf3a39edf63ff83df0cbc97`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:50:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:52:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca4176ba40503694123907b12411c085ef59844a004a61e19e8ca4ed6fdc68`  
		Last Modified: Tue, 13 Feb 2024 01:58:08 GMT  
		Size: 25.2 MB (25242967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283ca3166ffd80ea83ab111c2390bc95b099bd6fd3a16ebb965559ad02fb483f`  
		Last Modified: Tue, 13 Feb 2024 01:58:33 GMT  
		Size: 64.1 MB (64096976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d901a84a069b82728e01139c65e037a1f75e08bcc5f823a2d09e12c1eac80f8`  
		Last Modified: Tue, 13 Feb 2024 01:59:25 GMT  
		Size: 234.3 MB (234271252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:50c56853720265f8e2acd24a2ff92edfa61464b24c24fbabf21e4ea355f57a3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350795607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701bc906a4b78e2b953eda9825c63a4b1714d5d65288578da74ab395410647e0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:25:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8b8f779f6f6934c8df0f23fb560ca92edd571c516e89d73b9eb684de34c1c`  
		Last Modified: Tue, 13 Feb 2024 04:32:36 GMT  
		Size: 61.5 MB (61458710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9e89653202d76bb2d2634ea10b87a6fd514cf8ff4b054a5c0dd35be5cdb217`  
		Last Modified: Tue, 13 Feb 2024 04:33:25 GMT  
		Size: 218.0 MB (218000349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b50632c5c3c1da541f198af067944b978fc3e86d09d6e5faf31f7cd7bec9f0dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.5 MB (397477302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb739bca9cfb606e2e4198c8b388fd60e62d0ba4c857851a82f722e1fc6b0d8a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:45:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56f725cf4defa388afd50973a22d727c0eea3662f1f6927b2da7c29431eccc`  
		Last Modified: Tue, 13 Feb 2024 01:50:22 GMT  
		Size: 26.4 MB (26367599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbc13be4438f9f8d894060aed3c33f0d7346f4270baeb1a88d2666d594e5e6`  
		Last Modified: Tue, 13 Feb 2024 01:50:38 GMT  
		Size: 66.6 MB (66561866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2f96767199297b5c9b62bfca3bf8dbe64f2140a3971075286c296b044f2327`  
		Last Modified: Tue, 13 Feb 2024 01:51:12 GMT  
		Size: 252.4 MB (252353725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6bea73c06e3551fc523afbb46a8a36107fb11a2b34ef71401204332062512d23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.2 MB (406188638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ce9d00a5d17f92dea63d4f7a5cc99f96b4ba99f43b734292e757b4c9618f48`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f591e946a39d16953fde73e2ef14b2bfd79e49f9bd7d3f7f47afa1b2b5265f`  
		Last Modified: Tue, 13 Feb 2024 01:35:43 GMT  
		Size: 68.2 MB (68243501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e75a2a2fbea7b1fbd9bb0b804cd9b38871606c13ab1171e0718bc6b1bc3c64`  
		Last Modified: Tue, 13 Feb 2024 01:36:42 GMT  
		Size: 256.9 MB (256891738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c22bcdd2a316c671d589a3fe07524d1744d7ade31af60299293cbf3a5c8bae4c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.0 MB (375990697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d59a8849bed4e04ab4c47dbe072e0ceed36418b0c03df31554d8c26da99371`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:19:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141af89200b4b870fed00cbeab38968248af7ce012b97890ac09be125e872ee1`  
		Last Modified: Tue, 13 Feb 2024 04:31:59 GMT  
		Size: 65.3 MB (65254297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d879d1c67f3b1e5353b850642efde0180be4e1e5692e1198898cf9db2281efc9`  
		Last Modified: Tue, 13 Feb 2024 04:34:33 GMT  
		Size: 232.7 MB (232669218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8b34a14b0c2ae1541471d6a13d71985a6eab797c46a7e174e4223161dfdb6131
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.6 MB (420632790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90eb58e9c47c30ece9739b27b11b70332b25717bf0a3704a059b1167755ad37`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:36 GMT
ADD file:20495ab1a5b590f87307401881c4392d68c4ae3aee17cd89e2196908d9ee5c75 in / 
# Tue, 13 Feb 2024 00:41:39 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:32:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:34:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f12da478bcef0b5e264ca4e1bc3288008557f76cc25c8a87e714181c7f30ac36`  
		Last Modified: Tue, 13 Feb 2024 00:47:57 GMT  
		Size: 56.2 MB (56234839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb30d823a34f6274ec3b36fe7d62aea5946dc0fe6f3c2fbc9d8cb1574aa46cc`  
		Last Modified: Tue, 13 Feb 2024 07:39:58 GMT  
		Size: 29.0 MB (29047420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb6585507457cd34ebcb56c4a04a3a14027e38412e2f405ef1023d35c26241b`  
		Last Modified: Tue, 13 Feb 2024 07:40:19 GMT  
		Size: 72.0 MB (71960573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd44839e24d4a0018783b0ea8b4c1b977cd0f28595e199fc923d26666c81cb1`  
		Last Modified: Tue, 13 Feb 2024 07:41:09 GMT  
		Size: 263.4 MB (263389958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c310e82d82b61bec72517f6521c1516a5f0e9af4a73795236c6b8da34f02e690
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.6 MB (387584017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52adccf6519ee2b291e9647181e80778e73c8b1e060050457922decfad33a075`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:40:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1bb14fde65edf4d3cc63eb384e2aad7fa969df7a3d75e3b18a18e361903aef`  
		Last Modified: Tue, 13 Feb 2024 03:01:01 GMT  
		Size: 67.6 MB (67554101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d349cd9c4812463a9aba9a6976074c9069725e39974b26a3ac27c6ea804c53`  
		Last Modified: Tue, 13 Feb 2024 03:01:35 GMT  
		Size: 240.6 MB (240633816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
