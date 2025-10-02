## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:8502e6f7aa02a0d9f841b1f6d28182f91d89d3e2eaadd8407f195fef07ee172c
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
$ docker pull buildpack-deps@sha256:e7cacba24084cd459c248a57ea733c45131417fbe775648a859cc0f73dcd50e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249066787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e6f0d302822653c5be3126d2ed2e495c02d294362ddf25777d8c9e3756ab0b`
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
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
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
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3856fb40e8823986f0d2b16e4bb928a603347223ee232458482a4a5a7b70b7`  
		Last Modified: Tue, 02 Sep 2025 00:12:14 GMT  
		Size: 39.5 MB (39487201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7b65e6fafecd199cb99814a4d4bc3298d0c486580723cf34f8b5c6f8a0d4f1`  
		Last Modified: Tue, 02 Sep 2025 04:27:02 GMT  
		Size: 172.9 MB (172936373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f53ce0bb9585214f1d5623af56ce5cd98b5a36407f19caafb028803274b989b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11849737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d36242650dfaae2e599113f88ad7e1b7dc534f7c2380f6ef5362be3004c00ba`

```dockerfile
```

-	Layers:
	-	`sha256:03dde242051f62edb4122dd6706db600872a4b4f5ffeb79b3f73b9d44a42f3d6`  
		Last Modified: Tue, 02 Sep 2025 04:19:26 GMT  
		Size: 11.8 MB (11839534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903790ec039fa1638d35cc2535769906f7b78d86f608c1775f6c19f2e9962e18`  
		Last Modified: Tue, 02 Sep 2025 04:19:27 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7eb93b11daa070f382d7df80b476c2ccb8574059a17359f85d94ce4f94789968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216304557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f83776214790ec525778325a67f93d2cabc4355445f7e4c54e7e045c822044`
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
ADD file:7939f961de8cf091ed251aa1d8e432c16ec7506130ed39a1db4028efdad8fbfe in / 
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
	-	`sha256:33392950d914bf1e16e980fc0bbcec6367a2d2b8ecbd726dc5fc65b4c96ce79f`  
		Last Modified: Wed, 01 Oct 2025 18:17:15 GMT  
		Size: 26.6 MB (26643435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9171b5af741a0ace05e08730bfd3e3d15b256638bd578879f8bec957a53865fb`  
		Last Modified: Thu, 02 Oct 2025 01:11:04 GMT  
		Size: 7.0 MB (7009648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ad66e157af2e652af3caa8bd7ad08a7179d484f1b6882961c023ec58b25c05`  
		Last Modified: Thu, 02 Oct 2025 02:15:10 GMT  
		Size: 42.3 MB (42251833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc1c1e1992afaa509dc30af347e97bfdebd21ae628d6cd521610fce094a016a`  
		Last Modified: Thu, 02 Oct 2025 03:15:29 GMT  
		Size: 140.4 MB (140399641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85e5b18eb88b0a6ddf31419d380f88cc5ba758bff1f2c814aaba9494822baf83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11639010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0f725b607d6ec9643c9ec33beff67792219ffb7108ed28af721070b485b174`

```dockerfile
```

-	Layers:
	-	`sha256:c6bdcb6a0e66ed02dc9cc5b674a3c02828c0a8027a71fa66faf1904936e726ee`  
		Last Modified: Thu, 02 Oct 2025 04:19:29 GMT  
		Size: 11.6 MB (11628743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35c15b95e151662a15017d82d5f4bb80080c870416a0afc651409d866a13ecd9`  
		Last Modified: Thu, 02 Oct 2025 04:19:30 GMT  
		Size: 10.3 KB (10267 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:44c2f46848c663928c415c5d2e35ff1ad70cbcafb3d99e5f8d7c42c1e7fd366c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240307569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee2e53c5e8862a3c48228908c67d299afc6a7b1a7d10fc32668d364d0a11e84`
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
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
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
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544fbec883712e8b92ee5a8fb96accd816f1bd25c1cb91370bc6a156f3923503`  
		Last Modified: Thu, 02 Oct 2025 01:11:19 GMT  
		Size: 7.1 MB (7052114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0761247749305bde9fb9bf7bfca381206a20dfde11549ca1ba13996d4f60209`  
		Last Modified: Thu, 02 Oct 2025 02:14:20 GMT  
		Size: 39.4 MB (39382496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f102a21bd825cefeb6deddc85f1175ff8130d1152c51de56574bb1547df50b99`  
		Last Modified: Thu, 02 Oct 2025 07:04:05 GMT  
		Size: 166.5 MB (166489852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aa14d36d5769132101311afaf3b9f1e5704dd32e35e520fe2adc13f2bc279090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11845484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7ed20d4b67c2098b46d9200e79c219ce9ed3924bd87605a75745b092835536`

```dockerfile
```

-	Layers:
	-	`sha256:e88ee97493633e311374c268071c6d49e2fb94b7a37de3123092387dd72ead58`  
		Last Modified: Thu, 02 Oct 2025 04:19:38 GMT  
		Size: 11.8 MB (11835201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f051a24045152e0f248406946409e56739ec49e945558207fe6b3dee1c32025`  
		Last Modified: Thu, 02 Oct 2025 04:19:39 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9da2e71c24894dd4033744e45e3f45ba74542f840a6236937ec6778608b8c6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269810357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d94c1c57cd02a7588175aa693292c6e4508d700d08ecfcf9ea31b335cd0c5b1`
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
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
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
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f77bc9e4ab6e5fb5af578f087cd1cd7d1b42df4ce3edcb7205e77fa641e55`  
		Last Modified: Tue, 02 Sep 2025 00:12:15 GMT  
		Size: 8.2 MB (8184933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06d2fcee6246a83413eafcec3d64fbc5be759a0ab354df9c761fc5007cd6746`  
		Last Modified: Tue, 02 Sep 2025 05:24:06 GMT  
		Size: 43.8 MB (43760164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d7edd685c2fbf1e8c5842486db95ff4f30daa5e21dd95de3d6225c6713da2`  
		Last Modified: Tue, 02 Sep 2025 12:59:57 GMT  
		Size: 183.4 MB (183422036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:262a5e75fb936afc2b4ee2a65aa32eef50c7b0342c175459bcaf80291daa04a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11809134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1abf7099d882108279c2743145dd8f2837f88cf0185b4b52195274af404783a`

```dockerfile
```

-	Layers:
	-	`sha256:01be9f109ca4d96721e38a1c3fe39eae3f9e767a300a20738fe86112cd433013`  
		Last Modified: Tue, 02 Sep 2025 10:19:42 GMT  
		Size: 11.8 MB (11798899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee325842ac73bfdd9274469a370832361eafed0c075c7c7eded94cba2d6823a3`  
		Last Modified: Tue, 02 Sep 2025 10:19:43 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d3eb51e56b23c29e0ce757036e8977d6999274921a0b5df06dbf0356ea0b2c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274271627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749978808b69a5adda08dcc435e7e1e24a0972ffa5d1114fa3e677f23fa70943`
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
ADD file:c50534025103b387d6edca09570ec78d030f9514a469228d4d2c12ddbc059678 in / 
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
	-	`sha256:d152ae8117dc009abe5def1b70dd1fee217a52c100ea2406284b82890b29223e`  
		Last Modified: Wed, 03 Sep 2025 03:52:06 GMT  
		Size: 27.0 MB (27042655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2827b5fd296164594bbbb195caef81b70a3799001441c64ed9d1c44305d6ade1`  
		Last Modified: Wed, 03 Sep 2025 16:00:58 GMT  
		Size: 7.1 MB (7118262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d419b3a38152e2f0763a6d96e4ff0628be5a7d8f45e983beaa5a6c0de269436`  
		Last Modified: Fri, 05 Sep 2025 14:52:58 GMT  
		Size: 42.3 MB (42306095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4999d61c1b02d6f421a974c6da842284899d931ec3045b0b24144822f6ec2fdc`  
		Last Modified: Mon, 08 Sep 2025 05:07:51 GMT  
		Size: 197.8 MB (197804615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ae372fd90afe6fbc348421a75d76280e193d39e6a69caa018b2e71bb2f4451c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11790118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fdd676aae356e41f615c758a0023c553d1af7b6a61f5c00bb3598a4d67f4637`

```dockerfile
```

-	Layers:
	-	`sha256:f2e9a1c0049a778e9df597c6fbcf23390fc892a6ea8fbacd15c1554c1c072af7`  
		Last Modified: Mon, 08 Sep 2025 07:19:50 GMT  
		Size: 11.8 MB (11779883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8160ac5de07605bb42d3035963fa50b6bab2f43ba4e8919def56968647c10ac`  
		Last Modified: Mon, 08 Sep 2025 07:19:51 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c69b5d5fbd877f2fac179cfe0409185bd76253760d265d0214af3ba160db48a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223043383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cbf14cc437f5cbdffb686a6380a8ae8de819ba596fd95afd806c7f2e8978645`
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
ADD file:14014318483b695859df2bd7cf65af4796bff1435b6a558937389c62e3df6cfa in / 
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
	-	`sha256:e4a5a322dd65d010805129ca793d5d5e6b07872cbc2f41d566a84091b39c794e`  
		Last Modified: Thu, 02 Oct 2025 00:25:04 GMT  
		Size: 28.0 MB (28003413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c17dd0c731fba631ccfc3aeb70e205e57d15badc6b26edc465d60bb61dd3c1e`  
		Last Modified: Thu, 02 Oct 2025 01:11:00 GMT  
		Size: 7.0 MB (7018299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7a6b2fe5670a7425cebb606528db0b3bc0b822a68bc9de4e677f95e0e8f766`  
		Last Modified: Thu, 02 Oct 2025 02:39:57 GMT  
		Size: 39.4 MB (39419587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d630b2433a25ba77d2bb9ef27aec5d4d9c82f9a684fb6ed4b5b7f84d25c60b61`  
		Last Modified: Thu, 02 Oct 2025 05:16:28 GMT  
		Size: 148.6 MB (148602084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ffc42d77146e6af712fcfa048f96667c0aa6f9ba7b660a2dd08b0445fa9370b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11663614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304b15f5473942b2c71c8faa8d6d872b5cdd3b4c4eec9d8bbbdd3a45e7a02dbd`

```dockerfile
```

-	Layers:
	-	`sha256:98b49df647d089a1ee2725a19749c796d26e525143bb223c08d522c35f096db8`  
		Last Modified: Thu, 02 Oct 2025 07:19:56 GMT  
		Size: 11.7 MB (11653411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98bca31d894837eb5238c0859ff10c3ec18555ec3d4a9d396c01cfb5ed69b161`  
		Last Modified: Thu, 02 Oct 2025 07:19:57 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
