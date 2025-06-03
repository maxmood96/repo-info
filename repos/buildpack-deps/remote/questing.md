## `buildpack-deps:questing`

```console
$ docker pull buildpack-deps@sha256:33b29783a479cfa2450e11af0568171bd845be07433124d2b6fcbadb35e79f8c
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
		Last Modified: Sun, 01 Jun 2025 05:26:34 GMT  
		Size: 29.1 MB (29106436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524a2d370386a0cd39d38026a460d26ce31a6221b6ab8aaa1f19d25d8002674a`  
		Last Modified: Tue, 03 Jun 2025 04:15:37 GMT  
		Size: 19.8 MB (19839541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65512b0923851ed2aa5a6489177af45593736a397a79a9354c144106ef1c87b9`  
		Last Modified: Tue, 03 Jun 2025 05:12:01 GMT  
		Size: 49.3 MB (49254957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b77bea228717f530ffde77903a6b41a30433f84cfb93faba05de0a2cbf8cb7`  
		Last Modified: Tue, 03 Jun 2025 06:12:18 GMT  
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
		Last Modified: Tue, 03 Jun 2025 06:12:15 GMT  
		Size: 11.7 MB (11718767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7371284e90ae9c360e3a39e72888066ad99711e3801cac07c1c33398c99df57b`  
		Last Modified: Tue, 03 Jun 2025 06:12:15 GMT  
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
		Last Modified: Sun, 01 Jun 2025 05:26:47 GMT  
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
		Last Modified: Tue, 03 Jun 2025 06:28:19 GMT  
		Size: 11.5 MB (11471208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c6cbd9af983ee48e597eed718ac1a956ec832538f3679b5dea4dc703a79542`  
		Last Modified: Tue, 03 Jun 2025 06:28:19 GMT  
		Size: 10.3 KB (10262 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:39de6c22184da5a750d869855aec341521a0aea0c2d9ccbf8d7e67bf3cc4d790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289598344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca1bf10f029da3ef42be8a1f847afedc85f9666d65d01eac583b2b681394050`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:22:25 GMT
ARG RELEASE
# Wed, 14 May 2025 04:22:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:22:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:22:25 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:22:28 GMT
ADD file:fd21715897ee52f2140290b1f7e14ee6da8c539a73b857c5fb652a047dabb640 in / 
# Wed, 14 May 2025 04:22:28 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ec022b1a79b332d6a04d4b3f21fc0806634a7ed2ad52cda89f49f10584782937`  
		Last Modified: Wed, 14 May 2025 05:17:46 GMT  
		Size: 28.3 MB (28282258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d04fa09be15353aaac96582c2c87af01ff778cd01946eec45a230b304ae9a9`  
		Last Modified: Mon, 19 May 2025 23:38:07 GMT  
		Size: 19.1 MB (19063089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d68dc674905648dc451c75f2b8a581cea021fe56ba4ace9d1d7c6c39dea882`  
		Last Modified: Tue, 20 May 2025 00:06:35 GMT  
		Size: 47.2 MB (47196388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b99adc8795ffd9c1fe05286c557face5467d2d56012d06dedc6b39a6004490a`  
		Last Modified: Tue, 20 May 2025 01:12:09 GMT  
		Size: 195.1 MB (195056609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3850ecc41fbd9177005a5f9978c470420044bffdc5121c6915fd82c5caae3d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11759548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e5b9dff5bb7b98c8bc1a3d612fcda5c220f2e75dbb2bd1d98384bfee9d22d0`

```dockerfile
```

-	Layers:
	-	`sha256:5831a4c4960c1fdf91d7a23da4c26fdd57d75b8bb8fdc1b9ee6f52fc705ee434`  
		Last Modified: Tue, 20 May 2025 01:12:05 GMT  
		Size: 11.7 MB (11749265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fd4b4868b0b1be50f26cb23ef81b885d3e4815759106791dd354c60767142e0`  
		Last Modified: Tue, 20 May 2025 01:12:04 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:71c4db03c6ab47ba088841206a84406ed22a90e77cba5d5ddba78f00385a993f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312735407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f55dd836565e2691bdb83dbdb06dfc67027f8d64e2a5648d93e74713e54a88e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:22:26 GMT
ARG RELEASE
# Wed, 14 May 2025 04:22:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:22:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:22:27 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:22:30 GMT
ADD file:d9f9e02d15868fd689bdea92a54a568a4592ed5f72cecab767af6481b0a1084f in / 
# Wed, 14 May 2025 04:22:30 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f4262ef187b79c0ab727effac47ef9ee3746639697a95792cb4e866a2dc7b223`  
		Last Modified: Wed, 14 May 2025 05:18:00 GMT  
		Size: 33.0 MB (32973841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02f2f1f81fd8e85949fe8d3c42f2ae5ba4cd7791149a420fe0bbc304b0f3929`  
		Last Modified: Mon, 19 May 2025 23:37:16 GMT  
		Size: 21.5 MB (21476675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b772f3e380312459ba542744d462839dc24d649b88002c776083f158bc8d0`  
		Last Modified: Mon, 19 May 2025 23:46:56 GMT  
		Size: 52.7 MB (52697718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ccb0bb25dffc8002297493b94e4129c38add88e65ecba604f4e0dc43327820`  
		Last Modified: Tue, 20 May 2025 00:12:54 GMT  
		Size: 205.6 MB (205587173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:64d971ff3fbf7679c6ebe75209c58f4e67ad9fa8120f6fbd225547515133c665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11677479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e490dc2b952020c7c64ad8b0599b92552175628c29e42b88f6dd0716a5a5f8b7`

```dockerfile
```

-	Layers:
	-	`sha256:143e071c0494936b627fa0cc8208c5bc50611d64ffe42e3d7e7ba780666430d5`  
		Last Modified: Tue, 20 May 2025 00:12:49 GMT  
		Size: 11.7 MB (11667245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2f733de0468dc71852668a33c36d42080ed232eb02bf8aa482bece51108a8b5`  
		Last Modified: Tue, 20 May 2025 00:12:48 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8e3079849ddfddf47797d0a9ed7c6ad6e7558db59aef515a0f58652d5657c6aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.5 MB (399466307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b916c33f6d75a63163e34499d161077b2b85e2d06e58c63235ca295e6f94fced`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:51:05 GMT
ARG RELEASE
# Wed, 14 May 2025 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:51:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:51:06 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:51:36 GMT
ADD file:0cd658103d02bf6846dbd2f13752c91538b4521bf27ad3ef8f782d20b0f83446 in / 
# Wed, 14 May 2025 04:51:39 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6b6ac20521bb58fca960ddf3a7c726f8140f436dafe253d6ed5b0749b388fa99`  
		Last Modified: Wed, 14 May 2025 05:18:07 GMT  
		Size: 29.8 MB (29759113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ca9b80989299965c9f6755f5840f8c611f6382b2f6f805aec3b88374f28e6de`  
		Last Modified: Tue, 20 May 2025 00:47:39 GMT  
		Size: 19.8 MB (19790435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672a8136e711ca2b79356e618f52f148f3de569595ab11ee67aa99bbcc3b56a7`  
		Last Modified: Tue, 20 May 2025 01:13:09 GMT  
		Size: 55.4 MB (55355863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0372ca00826f954c51e6c2e687599867d5a14faf5f50a419e59d1be7951019b`  
		Last Modified: Tue, 20 May 2025 02:28:22 GMT  
		Size: 294.6 MB (294560896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:418536b52a607c07c38758528612a42c0044005e388ce12656a2d543ac66b758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11733846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070d095de81c75e6e606910f9907fde0677d2d3eb7b1d7ddb08a4fda1ee36bd4`

```dockerfile
```

-	Layers:
	-	`sha256:e0820db28158601270a092eaf3cbc518cf76171ead02f49f47410583b83a5fe2`  
		Last Modified: Tue, 20 May 2025 02:27:44 GMT  
		Size: 11.7 MB (11723611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16500e97674bddc1589ac6f85b7fdd4b57a824dd49088cf396b5a7e301b5fa9e`  
		Last Modified: Tue, 20 May 2025 02:27:42 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:questing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0c5c598fd9c642c128671deadc09ca1c7d3998117dc90230e1308187385b8f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275890604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71677f4206481a82d9a8b0ae0b0e7671105c2220ed622acadfc5443c62a8dbde`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 04:21:47 GMT
ARG RELEASE
# Wed, 14 May 2025 04:21:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 14 May 2025 04:21:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 14 May 2025 04:21:47 GMT
LABEL org.opencontainers.image.version=25.10
# Wed, 14 May 2025 04:21:48 GMT
ADD file:b72dde882e0e50b6ae5f82f19274973d603295192777550d7c77d1932792454c in / 
# Wed, 14 May 2025 04:21:48 GMT
CMD ["/bin/bash"]
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 May 2025 22:25:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:539d1c74edf6527aa984010b302b75b04d20f8f4d72dabf815b2c1be7da9b7a6`  
		Last Modified: Wed, 14 May 2025 05:18:13 GMT  
		Size: 28.6 MB (28570819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f16c281c9509afee6a1a1681f462e9e41dda0f3eb4c5efbfbd4c15995792bdc`  
		Last Modified: Mon, 19 May 2025 23:36:59 GMT  
		Size: 21.5 MB (21455838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b859beab6f8fb64a3d38ba721371d83d8aa12a64fab424c4cab7c5ed00a770a3`  
		Last Modified: Mon, 19 May 2025 23:46:26 GMT  
		Size: 48.8 MB (48797956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41abccc10db5b8cd869c244382d80ee90e3be20f8cf9f8f4838d1170b8afd776`  
		Last Modified: Tue, 20 May 2025 00:10:37 GMT  
		Size: 177.1 MB (177065991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:questing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ec460dde8848e91ee69bc318ee46e9875ddaef102333837e141973803b9591d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11482238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0497e0c17649ebe6d222dc5725b75a38c827adb2a1e709f86aec79ac0459cc92`

```dockerfile
```

-	Layers:
	-	`sha256:6c440ee1f214e280696ada05e05ec805f0b7fe781855d0e72086fb3d05db42da`  
		Last Modified: Tue, 20 May 2025 00:10:34 GMT  
		Size: 11.5 MB (11472035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca31cd94d635667df6b15e6a7bddcfa1486d135f88659c46aab7745060db7e5`  
		Last Modified: Tue, 20 May 2025 00:10:33 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
