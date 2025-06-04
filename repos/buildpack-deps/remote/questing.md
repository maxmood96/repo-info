## `buildpack-deps:questing`

```console
$ docker pull buildpack-deps@sha256:4e802835c6307f2a9588f90a5a944774e667c0f9862e5e9099243c7cb690b7c4
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

### `buildpack-deps:questing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:736a4d1954e32084f7b2b72fc676e93dea37abf6329900171c45db066d8b26c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306219231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5c47afea0c29f3e6d3a3dcdd1f4de77a843bb5226306768fab928884531c4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:05cc544084bb3fa6b9d35c9616e72a64a3e4639021957070a288f64f014f1b24 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15d8b49a304e2f84c28f203b3109aac57a5f04130d8a13ab89db6528a8bc2e3d`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 29.1 MB (29106436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524a2d370386a0cd39d38026a460d26ce31a6221b6ab8aaa1f19d25d8002674a`  
		Last Modified: Tue, 03 Jun 2025 14:19:26 GMT  
		Size: 19.8 MB (19839541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65512b0923851ed2aa5a6489177af45593736a397a79a9354c144106ef1c87b9`  
		Last Modified: Tue, 03 Jun 2025 14:19:26 GMT  
		Size: 49.3 MB (49254957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b77bea228717f530ffde77903a6b41a30433f84cfb93faba05de0a2cbf8cb7`  
		Last Modified: Tue, 03 Jun 2025 14:19:40 GMT  
		Size: 208.0 MB (208018297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5c27472f2314a76367d0b7e516910d15ed190f312427929ad65c3cf3cd5829c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11728970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6a67bccb6fd978ba034a61aec986135c54e1f8f253d2e4036ed5930d91eb03`

```dockerfile
```

-	Layers:
	-	`sha256:c3424d3ab00f00e9b80d92cd7c3a5004d4157400dce4ec8a6f2f00a82197d138`  
		Last Modified: Tue, 03 Jun 2025 16:19:39 GMT  
		Size: 11.7 MB (11718767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7371284e90ae9c360e3a39e72888066ad99711e3801cac07c1c33398c99df57b`  
		Last Modified: Tue, 03 Jun 2025 16:19:40 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9e0ffdc7120484e9e7c032f25cc7675a53574167636da4acdcc7200615baf140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256148881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233316ce8e1d92038dfb5f7f6301198842b19e4e4d225f71a12f787e0322287c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:64488fb6b3ce2ee2840e65c2ff29f801f160033b9aa156736e9515d881ca5bd4 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ae13f6240d71b4e49221ea0402dea6bd07e09d94c8c5c453ccf627c165d648e`  
		Last Modified: Tue, 03 Jun 2025 13:48:35 GMT  
		Size: 26.9 MB (26913307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53874f6a00ca89fc01eaa92fabcc2ef180611cda1ffaa63785cc0f2f13acd225`  
		Last Modified: Tue, 03 Jun 2025 04:19:48 GMT  
		Size: 17.9 MB (17859666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b98d9371863e08ef17358bdbe165e029982ab1846faf3e5d299c8111ded84a`  
		Last Modified: Tue, 03 Jun 2025 05:15:31 GMT  
		Size: 50.4 MB (50445387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517c4e38653bb4469e0858402f96a2718f271f5359d49d185100e1b2b8d4437d`  
		Last Modified: Tue, 03 Jun 2025 06:28:23 GMT  
		Size: 160.9 MB (160930521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:19fefffe7ee05488241219a1a67dc7b2e66bf7380957e804bd1b6977906ae8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11481470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a0eaa48a50c9d5c4369108ac4b829d03d33c0ab12aa1f67b03105d895e12e9`

```dockerfile
```

-	Layers:
	-	`sha256:93d0489fe39251cb3863e8c0d00113a7740e109382cd0f93b515478e8df57f1f`  
		Last Modified: Tue, 03 Jun 2025 16:19:50 GMT  
		Size: 11.5 MB (11471208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c6cbd9af983ee48e597eed718ac1a956ec832538f3679b5dea4dc703a79542`  
		Last Modified: Tue, 03 Jun 2025 16:19:51 GMT  
		Size: 10.3 KB (10262 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:285da0e8c87e2ab5b08bfc8d051e8eb20c571017585391409ad7e5894a2e6ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292797970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed54b7d68582e70447a55b5b1fc50cf05e2d91edec16cfc71103b6bb05e2f32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:e7d95872fd9b2265d0ef9932a3a613bcac89a6887fad274039f57708e8466742 in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f553ab7f5e64c9213adb141dbb943fcf439b06bda49c21d9637656e0e1033744`  
		Last Modified: Tue, 03 Jun 2025 13:34:04 GMT  
		Size: 28.3 MB (28284813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb9e72daec54872584552e76e8bb0b85cb4e28ed8bcaeb98ea9fe184f899e81`  
		Last Modified: Wed, 04 Jun 2025 11:30:08 GMT  
		Size: 19.1 MB (19146322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0758ecb86e4624ed6dc39005328cde6fad108972adac3ce2501336c4b8f2b1b7`  
		Last Modified: Wed, 04 Jun 2025 11:30:23 GMT  
		Size: 47.2 MB (47232127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd27e769783a146aba60c2da7baba9e7693b18bdb89f501f9a00f8d647a9da3b`  
		Last Modified: Tue, 03 Jun 2025 11:48:48 GMT  
		Size: 198.1 MB (198134708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9e34edf7a1fbcd85b3ff1c448351ec325316accf300117bba47b89065540bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11801563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b1d57d2a191d2cbb0b11c3d8307248b76a298725a66502f3fe2b48266eafa`

```dockerfile
```

-	Layers:
	-	`sha256:b1ebc07837317398b120b8e3e05ec89bbabcf910ead6334eb1a929566ae69c25`  
		Last Modified: Tue, 03 Jun 2025 16:20:00 GMT  
		Size: 11.8 MB (11791280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a71e1de6de0629b532a9bb5a934eed3f0fee001204195c5aa4e35b63688664f`  
		Last Modified: Tue, 03 Jun 2025 16:20:01 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f412d2bbc4947873422fb17a30499a829d3f6d9565526f2026dd7a0fcf90304a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.9 MB (315882691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb1c6b69560ddc329e7fcbd03b3be9daffe8aba64a363125409fd93f41a9562`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:13d7a96466458c3909b82b8ab831f9a568057a566ffa930b3df35fc558dd9a4b in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4a6626be4dde51767d2f322fcce23eea122e82b08f99962b3dc7ac890938cdd0`  
		Last Modified: Tue, 03 Jun 2025 19:03:01 GMT  
		Size: 32.9 MB (32921224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a6a2b121e6a335d78f4905325ed4812e495517ab4b9b91b7eba68099bfbc10`  
		Last Modified: Wed, 04 Jun 2025 11:29:59 GMT  
		Size: 21.6 MB (21613543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68617ded14083d61c71972a6be342cb6d6131d50e46aac3ccf0aeb996dc205e`  
		Last Modified: Tue, 03 Jun 2025 06:36:16 GMT  
		Size: 52.8 MB (52825113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366a2492d0c450cf2db721a2d7509bd5eaa5a334faebe1e1fd45f92a1e815736`  
		Last Modified: Tue, 03 Jun 2025 10:33:08 GMT  
		Size: 208.5 MB (208522811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2fa718cc9e80a7ec45c02efe6c1ec7a91ac6806ac42b0b24b075bb3a6b4b53cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11719502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d50c0782c7e3aa0255035d8b6a60d88b619e39d93b623bed6ce080d9122a76`

```dockerfile
```

-	Layers:
	-	`sha256:e6806c6f1c9fb9ead4a1980943d99ce0ea145c87f9e8c0393456b39f9450a6b4`  
		Last Modified: Tue, 03 Jun 2025 16:20:12 GMT  
		Size: 11.7 MB (11709268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e29f2608376a7f0d3b5b01c0b8c78da3f49bdc69169f58f277d62a8dbdc93641`  
		Last Modified: Tue, 03 Jun 2025 16:20:13 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5ee74724211c1c9a0432362ac5ac1df1d336f7890e202b84a6a06ecfaa67c0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 MB (397346749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ff2998dbdfc33145a8cd7d68b9cd83b3fa9a859ab1463a69a39d1dd4e6fb03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:475cb427dc9b3f71c87aace60b2f0254e77ed7334f39a111cf1f81f084f9be5c in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0fd1b4bb8c78bc11e2f7f6980b3c09ccc4285cd9434ab4a9dc84c8d9fdde9bcf`  
		Last Modified: Tue, 03 Jun 2025 13:40:25 GMT  
		Size: 29.8 MB (29810224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3272e38fcc5d5a6755eed30786ac2e51eff0bdabb6a709c35c7df389fa75604b`  
		Last Modified: Wed, 04 Jun 2025 11:29:38 GMT  
		Size: 19.8 MB (19781909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2208078e1ca0e3367cee9ec52fb7c96f0601608397decd71bfeb83a245da263`  
		Last Modified: Wed, 04 Jun 2025 11:29:55 GMT  
		Size: 55.5 MB (55485491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9968972f42aef35e5d3832d7b6492f9c569a098fd6369c9774612acda0f3dd9`  
		Last Modified: Wed, 04 Jun 2025 11:30:13 GMT  
		Size: 292.3 MB (292269125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23d35ef1579a0e4dc68cecb70177f3f6a56758e4ed3c339e6ed23f0be226414f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11766808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc0bc1207a30e309788c22e9741d496e97db84615a6d62d7be2ed2f87b2bb33f`

```dockerfile
```

-	Layers:
	-	`sha256:b249495965a6e11c5a6ee076df97f1949ab4f74a741e6eeac42bca1a9cf43396`  
		Last Modified: Tue, 03 Jun 2025 16:20:24 GMT  
		Size: 11.8 MB (11756573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173552f9ee68f8507e0d12b522cdfbc9c81ef1bdfcd683c9114ec8d95bb2eed8`  
		Last Modified: Tue, 03 Jun 2025 16:20:25 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:87e0e93784a58a30c9c98326d0b039ad15242862b39903b7e784c65a10c68288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276095352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf26835194e03873f5cf37465ef2e6efd82afed36d9f980461005e37a2f3256`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 19 May 2025 22:25:54 GMT
ARG RELEASE
# Mon, 19 May 2025 22:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 19 May 2025 22:25:54 GMT
LABEL org.opencontainers.image.version=25.10
# Mon, 19 May 2025 22:25:54 GMT
ADD file:8419b0c54ced109f1a86ac0df8febd2313936943cc6f5e51f8cc6789fed40a0c in / 
# Mon, 19 May 2025 22:25:54 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f83117ffdbeb353c4d64f37cd0b900511b0f13104632ef537330017b9342f673`  
		Last Modified: Tue, 03 Jun 2025 19:04:02 GMT  
		Size: 28.5 MB (28523638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb9c85ce7fb406691ad8c01800f1b0cbedcb1b2a1f99617eed4b5888d15dda3`  
		Last Modified: Tue, 03 Jun 2025 04:18:52 GMT  
		Size: 21.8 MB (21756689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd56e409834b5f6151e5d905d4c560b677cb9078c1db432899e4888c9c1b37ab`  
		Last Modified: Tue, 03 Jun 2025 05:19:34 GMT  
		Size: 48.8 MB (48813365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cdde0e2528d88de949325865241c0b81da541883bd1ff658df91b34316e19`  
		Last Modified: Tue, 03 Jun 2025 07:07:11 GMT  
		Size: 177.0 MB (177001660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bba54c83133c0b424b060b8f6ef0324ae9256a89483821b3cca812a154cc68a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11514982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22920c86df927c41779b251eec145c2c428b8f61cac19f1472c8927ef34740cc`

```dockerfile
```

-	Layers:
	-	`sha256:90523a53cbaddd805fe0d89b6c9715e22830586ee97334f723e8b3074b9a4990`  
		Last Modified: Tue, 03 Jun 2025 16:20:38 GMT  
		Size: 11.5 MB (11504779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a7cb78a560706a6dcfb05ba7deb830d40b4975946122018a2397cb76c0839bd`  
		Last Modified: Tue, 03 Jun 2025 16:20:38 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
