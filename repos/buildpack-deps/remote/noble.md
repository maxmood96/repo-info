## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:903734dc0de2d5e495742464e67a6095e02aa4f85b2b81de77e41522ff4de355
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

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5561b50f25463ce1200816ca53c210fb0db4b20a593cf0614581e52ea9d54ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274958185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c9f2a2c2e015224763655c971869c43630846711200e7090c120fb5655617d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:47:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:23:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87036178ad86a6ffffd0bfbc6472da5aebf31ed69c5b3f17251ddb308c41f20`  
		Last Modified: Tue, 07 Apr 2026 01:47:22 GMT  
		Size: 13.6 MB (13631344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eaef83111d329f083aafe369304809b4c6d4f05a8d9cabbe3c275dee19dc18`  
		Last Modified: Tue, 07 Apr 2026 02:43:40 GMT  
		Size: 45.3 MB (45336372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeb295bafe1977685bbd91469b0396a2fc30c33e59e422adf4f0a7798fb47ca`  
		Last Modified: Tue, 07 Apr 2026 03:24:15 GMT  
		Size: 186.3 MB (186257010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8dec490e2907451802132b559994deda5998959a5b7db7b028ec964862dea6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11743898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307f388ca3892d742ed8b27fad485b142fde3747b5f668ec551300186a220fd8`

```dockerfile
```

-	Layers:
	-	`sha256:ef16ec90c5245c347fc9216aab69fc13940340ef491163b411a56a6eabf5f403`  
		Last Modified: Tue, 07 Apr 2026 03:24:12 GMT  
		Size: 11.7 MB (11733757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad9a389e51f498e6ad992f68a84622c92efcbcbaaf6227fd29e0a3a9766df2ea`  
		Last Modified: Tue, 07 Apr 2026 03:24:11 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fe014d272ab960bbc09b96cac68b82a161a77ad559b62084cb5c0ccac42e1f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237196277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4891415d38d3f4fedf90627faf73d452d9a806271cb67276bae829dc8b521fa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:14:30 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:14:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:14:31 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:14:34 GMT
ADD file:68e3febb1e8418fa8ce83073bfbf6ec7236d81e7c8781177d7295e5adce34436 in / 
# Fri, 03 Apr 2026 15:14:34 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:02:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:28:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d7d21bc3f0364f0d98c41b0bcda87b8f2bfbf1688f75f6322ed679752a149163`  
		Last Modified: Fri, 03 Apr 2026 15:56:43 GMT  
		Size: 26.9 MB (26858365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0da5755f16317e3ae70ab41f8cfd9bfaf9ebcfc807f501bfdf9301feb5834d`  
		Last Modified: Tue, 07 Apr 2026 02:02:19 GMT  
		Size: 12.8 MB (12788637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c02927550b435a954ad1bc7a94f1e70f5a5ffb07a1e0b6927f1936cd876cef`  
		Last Modified: Tue, 07 Apr 2026 03:50:05 GMT  
		Size: 48.9 MB (48875041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ad3979a99f5b79083f1eeed3eb3f696ecf61f7e9802a39f1c20497b2266aa5`  
		Last Modified: Tue, 07 Apr 2026 04:29:08 GMT  
		Size: 148.7 MB (148674234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98bed19891374282c48e79145485c2ae8e245da40d8114bd9763601b8a6e5daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11069641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc0bafb79a4d352117c93b47459498833319387a1669ac965b5c54ce43b2cc70`

```dockerfile
```

-	Layers:
	-	`sha256:e72106ba6ce3228dbda1692ce28a62d5434995abce0cf194b56153a8c15430f3`  
		Last Modified: Tue, 07 Apr 2026 04:29:05 GMT  
		Size: 11.1 MB (11059436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308edae2bb2c56763c200dfbb0dd8565430a6e6a02e9a0f341a4d82df6f29dd0`  
		Last Modified: Tue, 07 Apr 2026 04:29:05 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d2aaf8b159b5dde58f86ce3c167614cfc7174d58c8b205ad5bfd07d4d1fb766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264436673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72b41c4c38e447c5e397ef105f42c66c69617d636a9a24302657f9554ac8b5b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:50:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:54:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:35:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250898647707f5617f944580836cdb26a429f5b2583cfefd84515874dcc57a45`  
		Last Modified: Tue, 07 Apr 2026 01:50:30 GMT  
		Size: 13.5 MB (13466018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759b38b74bc437a0488655af47936530d492f5f32fd7af8351b6fd1460780a14`  
		Last Modified: Tue, 07 Apr 2026 02:54:16 GMT  
		Size: 45.3 MB (45273450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcce924facf9831b0bdd2ab4e1aee9d28f6463522982602732ff593c6273cfb`  
		Last Modified: Tue, 07 Apr 2026 03:36:22 GMT  
		Size: 176.8 MB (176823130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7420ae2e7ea0d208219df9d1bfd8646bd9567690932ee1ccdb20c220b916c11e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11293443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac58e4adb79de9756105dc2bd75ed88007e9dbe5c226bcfdf52a0e0e5e861789`

```dockerfile
```

-	Layers:
	-	`sha256:06a81c95c771314273c39fe63e57071b0c8296ef8454bcd706ecae65a4c5d9b3`  
		Last Modified: Tue, 07 Apr 2026 03:36:18 GMT  
		Size: 11.3 MB (11283222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7dece0607a1cde2c72bde065e7e9478015280c5474c4f0a9f069bdb17bae2d`  
		Last Modified: Tue, 07 Apr 2026 03:36:18 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:158b2d73a9daf0f28a351c5ef00d9143a43be265ea06b3e63158279ee0ae5072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.6 MB (290585297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af302b4108635e789ee5fa89726ade73d515b950807ed773f4fe6b247d316af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 04:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:19:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f8c8315ff69e0ade5c27a5f32668c5ece93dfdbd029e67d7b478a2a133a289`  
		Last Modified: Tue, 07 Apr 2026 04:25:12 GMT  
		Size: 16.0 MB (15960385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81007fb33e08eb5e24180ed20968c7c036bc484af1aeddba776ca581f9b36b3`  
		Last Modified: Tue, 07 Apr 2026 09:57:04 GMT  
		Size: 50.4 MB (50442746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60e33eb65e6664ea80a740fd5ea7a0e61f057eceb72d77865e819460a2116c2`  
		Last Modified: Tue, 07 Apr 2026 18:20:34 GMT  
		Size: 189.9 MB (189868832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:693da657281d60a0782a5654c3a1c93f9efd438ed338a750cea92436c3bf2bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11240830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ba31636484ec70b8c922205a9e65dd7dcceee7deb799d5414e7922569b2e47`

```dockerfile
```

-	Layers:
	-	`sha256:d657cb68d60c4678e449540e83364ae3ad8b30840f638194ca714cd6d918a2b0`  
		Last Modified: Tue, 07 Apr 2026 18:20:30 GMT  
		Size: 11.2 MB (11230657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7968b58c32833427f23731fb6ed05d67142204631f0dcaae799989cd26fa1e43`  
		Last Modified: Tue, 07 Apr 2026 18:20:29 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:57211708d88d1fb70802dee0537ebba0e50e0591ef017dcdac7ec03c5aa6d886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.2 MB (333213589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af76303392bd34470299580ee0fab89438542d76b96e250378ecb16e2aea333f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:35:32 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:35:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:35:33 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:36:09 GMT
ADD file:59e78909d1b1cd9a524f68d8ff44bb077ea09f4f39da5e046d635b48da9d33bf in / 
# Fri, 03 Apr 2026 15:36:13 GMT
CMD ["/bin/bash"]
# Thu, 09 Apr 2026 01:53:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 03:05:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 09:22:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:23ef52cbd4674ce4f8269086177a6a1fc3abbc052567212551b8169743067808`  
		Last Modified: Fri, 03 Apr 2026 15:56:59 GMT  
		Size: 31.0 MB (30963791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f90ac4813ec6bbeb96b9ca1324f326cb79250eaeb56ecd108a3a0d03888dc3`  
		Last Modified: Thu, 09 Apr 2026 01:54:59 GMT  
		Size: 16.4 MB (16443158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c23f88fd80cd62b142ca8ede0942ed13340c22bab3bade167a2b7ad9289ef`  
		Last Modified: Sat, 11 Apr 2026 03:07:53 GMT  
		Size: 53.9 MB (53885657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b62fab9059d0499d273d3e42bb7ec3422929a7b1f1b6fbad790d8b1f43038c`  
		Last Modified: Sun, 12 Apr 2026 09:33:03 GMT  
		Size: 231.9 MB (231920983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:84222859bdb249942d68768dee91e7e043c1d13964466dfd3ce770fa85efdda4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11234059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b80d339274eae533a41403fcfde7fcfc7d654b26397b67b8839b80e706d0c18`

```dockerfile
```

-	Layers:
	-	`sha256:d6013d4bd401a6b85c86e8e0f67080abf0acd06319af0e0d44b3244382768064`  
		Last Modified: Sun, 12 Apr 2026 09:32:31 GMT  
		Size: 11.2 MB (11223886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e165e9a2f5dfcd385763fc5d20dd78e34e38ed21335bd3c085a29c0fad2e82e4`  
		Last Modified: Sun, 12 Apr 2026 09:32:28 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:324521c4d982b148689964ef9f9f688163ed4fb1ba645eba0dc486b9314170d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253389100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cf10e270a865f3f10edaaed82b735e41c7e3f53b0acdc580db8f8e5e114a69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:12:46 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:12:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:12:46 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:12:48 GMT
ADD file:31d45a66208318e1066130bac8975f44dea6e7e93cbfb2d29b0888e686bb10d5 in / 
# Fri, 03 Apr 2026 15:12:48 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 03:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 06:02:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:248eeda3355e38b5891b7f407370b5faea53785cd947438684bf34a757d0f83c`  
		Last Modified: Fri, 03 Apr 2026 15:57:06 GMT  
		Size: 29.9 MB (29911843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cbc7b0e0dfda4f493fc8f104984fbea17a2f5d7d1345c3463d92d4acdb49dc8`  
		Last Modified: Tue, 07 Apr 2026 03:06:17 GMT  
		Size: 14.9 MB (14943206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd585f62eae2a6c89da020ab0ed29d752cd73be02dae049a068a3e8979f2970`  
		Last Modified: Tue, 07 Apr 2026 04:56:16 GMT  
		Size: 46.8 MB (46822779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f146ecbee78b54c569ae277d8690eb285aab5e8dfb4c4bcecdb764b34a189e64`  
		Last Modified: Tue, 07 Apr 2026 06:03:24 GMT  
		Size: 161.7 MB (161711272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db6f948d9e0f01a80f15f30692baf768df4e3ffb9b610a6cba92deee3a905423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11084633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d44d20c69b7d2b642d9f91da501ce45456309d758bee2b1e50f91607346601`

```dockerfile
```

-	Layers:
	-	`sha256:6925868d9b65142db5b38e0d433b7f255d02db2b7d3a391e21bfc0e77149604f`  
		Last Modified: Tue, 07 Apr 2026 06:03:21 GMT  
		Size: 11.1 MB (11074492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3637776c5d4ee3ee500d7ed9fd45b7364c8c56d67462074a1c460ff4267e4ff`  
		Last Modified: Tue, 07 Apr 2026 06:03:21 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json
