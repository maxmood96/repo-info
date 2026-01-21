## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:48db12716df6987b308b5c8e15f85c34674ba39c78e1db306f4af1faf13bc6d8
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
$ docker pull buildpack-deps@sha256:aa5431a773d555e22667fb3891c814199265e5a80bdc1c60901834d07de8ecb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249082625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f005275be25e9926e62c0b7cc7086c98b4a8752af7ed87749166c62b944ae54b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:05:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f818244d3a9533436026768f3a47a0258ba1d5300c359e89da8f5c6906ba04a`  
		Last Modified: Thu, 15 Jan 2026 22:10:42 GMT  
		Size: 7.1 MB (7103894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c050793ebe1bdac76f856d4222c4fb1916ed15b69ba2ee9bf59e871325a5d397`  
		Last Modified: Thu, 15 Jan 2026 23:06:06 GMT  
		Size: 39.5 MB (39487196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951e4fb0755ef7be8f216802c86c1f17d5249508dafd17e604c1cf68ba65ee88`  
		Last Modified: Fri, 16 Jan 2026 02:22:10 GMT  
		Size: 173.0 MB (172954868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7e83562a6814c5010f0acac21df33bfdd6611c8e4c6cc165861caf17f6274040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.9 MB (11850521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9343e5424092e2502a63bc2a55019f7eec17d39f616dd9966f504182e4bba91`

```dockerfile
```

-	Layers:
	-	`sha256:cc60635fcb17a59afc8ed7626fec31291d197cc8025c4ff9aa733364e81d4d98`  
		Last Modified: Fri, 16 Jan 2026 02:20:27 GMT  
		Size: 11.8 MB (11840362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea20d277459e8ec2380d40eba8a31442a40f00237f5052ccfbec0b628e91c81`  
		Last Modified: Fri, 16 Jan 2026 02:20:28 GMT  
		Size: 10.2 KB (10159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fa242ac3d6eb4363b083378c925b5e3280cf8d590b58e8140f4fd796765bab6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216312187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0c4a06bf5aa6c90b181facbdcbea3f0b6d91e3bcce63b65f47e6e920718d67`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:02:38 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:02:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:02:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:02:38 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:02:42 GMT
ADD file:c6e8dc9cf610f17d4ed912b48dc43aef299146d67e62f2248ccd0e2cca210a77 in / 
# Fri, 09 Jan 2026 07:02:42 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:34:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:27:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:83d1a597d0ed11bf60c1ab8ef65516448b87de3790f14ee8336174b7f9a56d82`  
		Last Modified: Thu, 15 Jan 2026 02:42:29 GMT  
		Size: 26.6 MB (26643402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dc5444244ff1596a0134006b703a83ce3593e82ef40de9773c242916a3730c`  
		Last Modified: Thu, 15 Jan 2026 22:06:43 GMT  
		Size: 7.0 MB (7007642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9845ca4390db4dd4dbb8032870be7cf0b7d049882dc35d954db1fcaaa5d59c`  
		Last Modified: Thu, 15 Jan 2026 22:34:51 GMT  
		Size: 42.3 MB (42252883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f5fa55d9613d03a56e4d24185e82f921966634864db206773c8c50c679f72b`  
		Last Modified: Thu, 15 Jan 2026 23:28:16 GMT  
		Size: 140.4 MB (140408260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2cb2d68b1173e4091a5fc8cdbb2d219a4147445c0a6de36c393f0a96658551e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11639795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b408a462e09e95e8580bee4dc42dca0b3e6f926918c5a86d9a265dc0da86c76`

```dockerfile
```

-	Layers:
	-	`sha256:c24e150687405842460b142ad70be43adb5cfb4e4df5e307360501706b3966f9`  
		Last Modified: Fri, 16 Jan 2026 02:20:46 GMT  
		Size: 11.6 MB (11629571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e6b49b46eaa842007a7fa581d55b6829f67024582b3db75a03349af2c59b14`  
		Last Modified: Thu, 15 Jan 2026 23:28:13 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7169b14eaa70f5a51e2a4bd0b8d2cabc4605c884f81cfd5c42c5d627c4d41e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240338576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c4a99e651f54a245c26e2b31333f73f84329b569d2c594c72fc31cc7e06739`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:12:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:56:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786d4bf33c2933fa12f0a1a6196c7fc894058df3d74975169eb5b36ee78c0c4`  
		Last Modified: Thu, 15 Jan 2026 22:10:38 GMT  
		Size: 7.1 MB (7055052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c44d1c89d729b03a8ac870059f95ee87fed030d46cf377f199d042d42709b94`  
		Last Modified: Thu, 15 Jan 2026 23:12:45 GMT  
		Size: 39.4 MB (39382123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc12f497d3715f922a46bf106228162b2ee9d07f7e2624633cb52e095b0b5cb`  
		Last Modified: Thu, 15 Jan 2026 23:56:54 GMT  
		Size: 166.5 MB (166517904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1e0ce540fea1d53522cb331661b0e87764069746630677abddcd08416f8640c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11846269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cc33df931f6ca1b3e77809336617d474efe920dbf75ae78ac49f2842bfa030`

```dockerfile
```

-	Layers:
	-	`sha256:de0a76f3792506f4e4e91a588a3e7f7e321b7704ba54a104033b7862e374b99b`  
		Last Modified: Thu, 15 Jan 2026 23:56:51 GMT  
		Size: 11.8 MB (11836029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec269ac0feb344879c69e66cee9672bd4a4097efbda7a1ee8bb1debde3ccf61`  
		Last Modified: Thu, 15 Jan 2026 23:56:51 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:798de4abe96066253dbc1c0e2876f0c3e515caa23922b483ad220d1b60e730e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269815791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007271a4a7e82445876cef756034c92579c8eea96e941df84d21e21839f9702e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 00:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 16 Jan 2026 04:18:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Thu, 15 Jan 2026 21:43:22 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e324a7d0fe63304b6bce6644333cbfb5521335136aae9f84610301209810a7`  
		Last Modified: Thu, 15 Jan 2026 22:07:18 GMT  
		Size: 8.2 MB (8182022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93fc9e94f4c507f858d8897154ad632528d5ac46926c7bae35c65fea43cd3d6`  
		Last Modified: Fri, 16 Jan 2026 00:26:36 GMT  
		Size: 43.8 MB (43761375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381298fffa33a8387089ec8dc06e6b24ce1ac6465cfa50af4dc7b92942e4226e`  
		Last Modified: Fri, 16 Jan 2026 08:09:14 GMT  
		Size: 183.4 MB (183425432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:023c7f7c6d6867cd960e625f14713b9c254ae54fefe6b66327984eccae6fef11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11809919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0279b95df33d9de6305fc8916cafa474f074774a8de36deffc771c93ec755552`

```dockerfile
```

-	Layers:
	-	`sha256:4d12fc5fc50e9c8af3c5b7dc59148cb4f02f3b3f0de09092c3e58880b5100718`  
		Last Modified: Fri, 16 Jan 2026 05:20:01 GMT  
		Size: 11.8 MB (11799727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2259d5dd623e6ced5b0aa7a4c66a12c546016dfb3999b5b81ea900ca85b0cad3`  
		Last Modified: Fri, 16 Jan 2026 04:19:51 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:46a58a255ebc09a773f0ba2106b104a7157a57aa86e3ba5541669012b1ee6108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274272061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1d5a386ca4316e44597d8b4a5b47a1b930a2546249c8bfaafa7d51282430e6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:49:58 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:49:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:49:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:49:59 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:50:36 GMT
ADD file:16753c6442cb9871940bcae347672f49a6a001793657c89f4fff53584922f035 in / 
# Mon, 13 Oct 2025 17:50:39 GMT
CMD ["/bin/bash"]
# Sat, 15 Nov 2025 13:00:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Nov 2025 18:38:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 15 Nov 2025 23:05:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5284c23c7e2d64db45a1d6cd39e83038698f86052acddf8ba9fa989a1c5ca270`  
		Last Modified: Wed, 14 Jan 2026 14:47:16 GMT  
		Size: 27.0 MB (27042158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7443a254ed640b3e9cc4214e379249f0da2318389406feff1663a907d6beb399`  
		Last Modified: Sat, 15 Nov 2025 13:01:14 GMT  
		Size: 7.1 MB (7118011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb21c499deddbc9d2b2ad93e65920f2ffe6a7bce1d8a8f3bcc857acda40161a7`  
		Last Modified: Mon, 19 Jan 2026 08:55:13 GMT  
		Size: 42.3 MB (42305748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f7cced600f8d6f7406cf88fe979fb4c95a4d3d0d6aab2822c74306d06dcbe3`  
		Last Modified: Sat, 15 Nov 2025 23:15:01 GMT  
		Size: 197.8 MB (197806144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e305b632d893d900799c174b6330c5ec8a5ed67cb9f61eead0c91746d90dc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11790091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:645ee963023dcfd9aafa4faa06ff3405b4b1dd82ec57786d49270ceae98a5f38`

```dockerfile
```

-	Layers:
	-	`sha256:e81e761de2eab0f908a9f4a7b132b4f0dcde3cbd30e6722d994b88d573a0d906`  
		Last Modified: Fri, 16 Jan 2026 02:21:21 GMT  
		Size: 11.8 MB (11779899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc6b7045e773ec5c914a00794bd39c68d01bd17627ed4a6b0b8b084456ecafa5`  
		Last Modified: Fri, 16 Jan 2026 02:21:22 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:147e23c8ee7a5e4c4a5a887301e2ae63c35d7b079e0222f4ef9700c5f6b35a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223040714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1c6bc8b4802f8edb9cd70079021cb3b945475c59824f071059ff5cbe56a60f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:05:09 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:05:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:05:09 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:05:11 GMT
ADD file:03078bbac5343c8831dae57f317f9a6ced24a6c8b7192435e81027780f524a3a in / 
# Fri, 09 Jan 2026 07:05:11 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:06:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:33:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a0be7aa393c334078596b27f39dc3946551a30dd1cad58fe06cce6be05b244b2`  
		Last Modified: Fri, 09 Jan 2026 07:36:31 GMT  
		Size: 28.0 MB (28003138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b03f4e15777f635f53d1749caba8e1a02c7da7a8061d6e0e9d546b43523c253`  
		Last Modified: Thu, 15 Jan 2026 22:06:31 GMT  
		Size: 7.0 MB (7014411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa324ebe96b646080245b57f86cd4f0b097a7f68956ef2876329c1801d2eeae6`  
		Last Modified: Thu, 15 Jan 2026 22:46:03 GMT  
		Size: 39.4 MB (39420034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1b99ce3d8e61377718bf01dfb7703456dcc67e6926b3fd5da578ed2b3e721d`  
		Last Modified: Thu, 15 Jan 2026 23:34:30 GMT  
		Size: 148.6 MB (148603131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6ab2614f594ff9f6ab26164384eb5755b1a4937271a9d9de4f704458c39aae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11664399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049ff27e07734d587a18ba761fbbc8587d6b5d121eee1abbb230f5bd01b26eeb`

```dockerfile
```

-	Layers:
	-	`sha256:62945c6cdada4cfbbbfbe6ca8912e0b193914a5f3417aa28844e414290c88304`  
		Last Modified: Thu, 15 Jan 2026 23:34:26 GMT  
		Size: 11.7 MB (11654239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:569cf2516022ef9a5083e9f2d5137a94bc3e82a773acdd7588cad40d2b5868cb`  
		Last Modified: Fri, 16 Jan 2026 02:21:34 GMT  
		Size: 10.2 KB (10160 bytes)  
		MIME: application/vnd.in-toto+json
