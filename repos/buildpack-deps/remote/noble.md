## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:483a31eacca0c4ad239557127ec4eb160f7257fa87c206347282ed4349044441
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
$ docker pull buildpack-deps@sha256:4d60f6396c965ce3e14839688a7f9ffbf4a3bb3474c107a32eb93c471e2f9c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274719485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c701dae3972ae9bbb6e2a76840757112de5852b28b0840a4df082118f2de875e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552e7b3a08fae7407ef8f950501569fa3360f18e39d873ac1921a71da14d6b9b`  
		Last Modified: Tue, 12 Aug 2025 17:23:50 GMT  
		Size: 13.6 MB (13624915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec44ced3262f32d17fffdfe945832c470db55a37feb68b59642a3f9a3231052`  
		Last Modified: Tue, 12 Aug 2025 17:52:59 GMT  
		Size: 45.3 MB (45334169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23596ba5595e37d7dc075422533dcb8ef1639f10d66e1bfceff4152e2ebb5649`  
		Last Modified: Tue, 12 Aug 2025 19:49:04 GMT  
		Size: 186.0 MB (186037186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:13a084a5a5b9c019d5358d9a397e737f84c4f9413857dd18540955334454f525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11742953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9467b84bf0b0bab12575a47824ab1c78feb121b7a5be44a01379207cd4264dba`

```dockerfile
```

-	Layers:
	-	`sha256:8141d048ed71fde8b6f6cc7730599a704b8a3f2ec0f987d7240cc0657fa801cb`  
		Last Modified: Tue, 12 Aug 2025 19:19:55 GMT  
		Size: 11.7 MB (11732769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb60e34f385e57b054f7fc19869b76c8c4440963de8c13c9bf11c482934e360b`  
		Last Modified: Tue, 12 Aug 2025 19:19:56 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:76549b5161e59e19460bca67cf0f6d3beb17fe2170045cf99607c16dda347482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.8 MB (236773418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2e6890fe99c903a1e56f7e79345d3b42288cbc426f162a4bf72f13aefa37f0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:3d0bcbe19ab589b9febc888a3f1e7d731d2ffc32ab216f5a65461d73e6542ece in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5775aaee0b6caf578e138eda76ce3385180e0796b81e02b9edf4909084017d62`  
		Last Modified: Wed, 30 Jul 2025 10:35:13 GMT  
		Size: 26.9 MB (26851072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65c1e6e8d6e49b6a21d80ed5f0be8e0d1a70f1b210b7897fc9211050ac4c5c8`  
		Last Modified: Tue, 12 Aug 2025 17:23:42 GMT  
		Size: 12.8 MB (12783741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cac8e4708375aa6f5d07f8ef10b4800e53bea0eb06d38c5a50ff5e29e615b40`  
		Last Modified: Tue, 12 Aug 2025 17:53:45 GMT  
		Size: 48.9 MB (48865761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e891a9f3290c9d4186962d1d1360d0c12b6a66194797dff87522a7c5ef65933a`  
		Last Modified: Tue, 12 Aug 2025 20:20:21 GMT  
		Size: 148.3 MB (148272844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e01f244b0525ba49f0bb13cc126c75eb745fc43d8ca57114d63de5636e1c939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11068714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bab0919ddc28a8e10e9e72303d240652fc055a30b5c2de94b5aa2e0d1dfa6ad`

```dockerfile
```

-	Layers:
	-	`sha256:1fe324c7d17afeffa3cd4fdef6853b20e4fd17146ffd3a87d672a7dec9bbb054`  
		Last Modified: Tue, 12 Aug 2025 19:20:06 GMT  
		Size: 11.1 MB (11058470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17666df453180dc6f9b4bc930f91090c181342fdbf51abb8a660ed2b23a15ac6`  
		Last Modified: Tue, 12 Aug 2025 19:20:07 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4829e281333b49307dc893b94a6b4ece8e1c1008b52cab5ad9bb76243b782715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264339896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae1f55d5b19c565318ca8d70417ec48ac5ee10aef352791ccad8a10dd169ad4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c62336d0e960694fc4c54a90b27a6f2b9c96cb37051a77fbecbb178ecc98f5e`  
		Last Modified: Tue, 12 Aug 2025 17:25:03 GMT  
		Size: 13.5 MB (13460243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d53f5c7ed7267d74464b4e4f125c9dbc3eb9af21fbce0239d84fdfcebc2202`  
		Last Modified: Tue, 12 Aug 2025 22:15:10 GMT  
		Size: 45.3 MB (45309839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a020f179f522e247341c336ca75bf1ae333e2dae20b3215f7709799578074e5`  
		Last Modified: Wed, 13 Aug 2025 14:10:41 GMT  
		Size: 176.7 MB (176709437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d1ce09dac11968c7a84c929257917144997215c7fe10985516e98b7345a861e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11292502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da09e5a6b888de432e98a2a4e16b472394000e95c5b8f56cab64d0a9a34304c6`

```dockerfile
```

-	Layers:
	-	`sha256:ab93779128ad0d367fd29f710a7b8b2a38bcb19fc47f8dfbeb8c3b8a27f1bf6b`  
		Last Modified: Wed, 13 Aug 2025 07:20:42 GMT  
		Size: 11.3 MB (11282238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f1315dc3f40c3ccc1976eac5688a674984ca334da9f31d61cc73d0a65c689ec`  
		Last Modified: Wed, 13 Aug 2025 07:20:43 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3c468f9c8699492eefd3a9cbf6c4ca5aa408e0d36a5a3f506a08d05342f29be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290404810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208e97f023be35c2337f0f8a6f8d2d5717117dbcfe0b7020a5a48ff9c89035fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b91bea16983599d5d56d392195728b21b204304ef105b59dafe3b14bc2e91a`  
		Last Modified: Wed, 13 Aug 2025 01:33:53 GMT  
		Size: 16.0 MB (15952898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a6357eea713cc04260ca2c4fa5696476b2c45f5be7f4b503c35f59c93cb47`  
		Last Modified: Tue, 12 Aug 2025 23:16:44 GMT  
		Size: 50.4 MB (50438809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a341ef6816561311f134b4c189d7762ca31f20bbb5a16933fbad72493bfcd2`  
		Last Modified: Wed, 13 Aug 2025 14:10:45 GMT  
		Size: 189.7 MB (189683453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e7bff2f99c726d471c65cebd3efc5487b123a0797382cb096d56e22d0edea29e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11239891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ea6fb36a8789d443f86a8bfbb651e7ac599fbd9061af4e70e48aec5f75100a`

```dockerfile
```

-	Layers:
	-	`sha256:2020b679f6c2170e9c61b62f55ab0709753c9aea3ed9b27e671ddbd5c5cf77e3`  
		Last Modified: Wed, 13 Aug 2025 13:19:47 GMT  
		Size: 11.2 MB (11229675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9508daf45dbe9cf6e76169af3b6384d99a3cefd3a416cc91673a9d0fee704183`  
		Last Modified: Wed, 13 Aug 2025 13:19:48 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8503c429694c8f7a823e090e9662d44c22eed80413a4a53325734f290c371987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330317588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1b9ce1d465b0beb9c09a3b988d241ba8aa97a199c32bca82d3a990c391a347`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:07f3c32dd2b7f6af0f399701257442794654b72aa96759b98cb033a715461739 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b12e9b07091787c99b29dd2be63680c86c47e8be60a46566329007fb82cee41d`  
		Last Modified: Tue, 12 Aug 2025 17:05:53 GMT  
		Size: 31.0 MB (30951577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1c92de88b6f5d1841d526c8e8cec306e3c3db1b6e524a3c75f65fcb249b90a`  
		Last Modified: Tue, 12 Aug 2025 17:28:45 GMT  
		Size: 14.3 MB (14330521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579503ee6a75e1b1dec33beb0c62ca25886472c2c599aa8c9feb1c5f4cd595df`  
		Last Modified: Wed, 13 Aug 2025 06:30:08 GMT  
		Size: 53.8 MB (53814402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99000d6f664967a4ab9d2081faccdbb58593a3831c8b5f1f7dc30498562fc4c`  
		Last Modified: Wed, 13 Aug 2025 06:30:15 GMT  
		Size: 231.2 MB (231221088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:12185ba0c6b590c82253351e14b8765ba9b8db23c77d2cfeb241d1a23b69b2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c684bd31bfae6462897f929ecc505d3b85c053b28932805723c6d42e83ba299`

```dockerfile
```

-	Layers:
	-	`sha256:7994d26d0483ef9761d7a09bc2b49a80b315b7e4d7625cd8f383b0ef2a3b8d66`  
		Last Modified: Wed, 13 Aug 2025 04:19:51 GMT  
		Size: 11.2 MB (11222916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef93a9b1cc0aa25e50f4e08dce4842e0a7fbd10f5cf4301bfdf1cb7139413c32`  
		Last Modified: Wed, 13 Aug 2025 04:19:51 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a2b166d02b7d1402395625c507cb995e9a47bc6a95ed6dc5e5d124ae26f15593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253056909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c368b429882b1d1c982f90ca3a0eb5b477599cfaab207d78a14c1cf10b39e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 22 May 2024 20:42:04 GMT
ARG RELEASE
# Wed, 22 May 2024 20:42:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 22 May 2024 20:42:04 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 22 May 2024 20:42:04 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Wed, 22 May 2024 20:42:04 GMT
CMD ["/bin/bash"]
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 May 2024 20:42:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84400ce3eef4778a70239f864f38527e70fcb56dce37d1f0c2653c9024fbac19`  
		Last Modified: Tue, 12 Aug 2025 17:24:38 GMT  
		Size: 14.9 MB (14938064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8260bd25ec32d149d214450e2a8a1337ac9ec9a14f5e5180359a9b1f3a85d9a`  
		Last Modified: Wed, 13 Aug 2025 14:10:48 GMT  
		Size: 46.7 MB (46742761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888c43c5bd98d5f4f660f718dc32c10aefe4c33856e8da9c6a5a84192da06068`  
		Last Modified: Wed, 13 Aug 2025 14:10:56 GMT  
		Size: 161.4 MB (161443404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a12526acc8a27b1627fdc30068c908c3b6fe6c2a9671b3d5eb64cdf0115848e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11083706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9edc7263eef8eabfb2a95de21db7162f4c5323f374966edd7790e2759b0b34`

```dockerfile
```

-	Layers:
	-	`sha256:eb84b4a0661d92b9b7e853fd783b3b13ac56ef1add40f4109022e2a5ede045c3`  
		Last Modified: Tue, 12 Aug 2025 22:20:01 GMT  
		Size: 11.1 MB (11073522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4da7ccf5164692c478e93f75c346de1f2277c62feb670cf5ee0128b03e543fdf`  
		Last Modified: Tue, 12 Aug 2025 22:20:02 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
