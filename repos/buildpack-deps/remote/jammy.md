## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:8dd223ff1e9e1e061e2929ac47109af0c845eb793c36f3259fd3186ba7603d55
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
$ docker pull buildpack-deps@sha256:918cd44b94e364f615df59823fab68b732a2c0fba5c66ed6e10aa98b4125b3ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249078314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e929bacd45f9dc82a9014e9db22356bfd42d8d1a2008556d80ccb5b6e387407`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882c2cc2b3487f954b121776f38449e97c30ef32043eb9907c13c525178e473`  
		Last Modified: Thu, 02 Oct 2025 04:52:17 GMT  
		Size: 7.1 MB (7106046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7eae3ce667e15aacdd991f13045b9040930a5ccb6f865a903a8cd4b8e17a3a`  
		Last Modified: Thu, 02 Oct 2025 08:26:19 GMT  
		Size: 39.5 MB (39487111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642c4d829b2dec61d6d5b281c8a8f5543751a6bf6c6434e135cd0e983b969ae1`  
		Last Modified: Thu, 02 Oct 2025 13:20:23 GMT  
		Size: 172.9 MB (172948339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5617f905ab66cc5ae34ecd2a591960970888b0c3ac33c01671e2b318ee7863bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11849737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8ccf7441bfa74e65b1275cc87966a663b947c49ee6a8549314a62fac57ab20`

```dockerfile
```

-	Layers:
	-	`sha256:2cbcff97f3264ad1cdb3c915ba9c7a0fca15bacbd80303b027cbf833ff0aba1b`  
		Last Modified: Thu, 02 Oct 2025 13:19:22 GMT  
		Size: 11.8 MB (11839534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d604c51f8ed0f8844a86bd2c35b1475a61da71d2670b84c8c17521c3412e79b6`  
		Last Modified: Thu, 02 Oct 2025 13:19:24 GMT  
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
$ docker pull buildpack-deps@sha256:df0d3c4e27aa9ccb9c465acbcbe150b647140abbce4ba74500d2aba4db4327a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269817857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0b3cfa4b15656ea13c6cb31ce0f7ed4e3b19d32ad5c04c7eeed195e2da8d26`
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
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
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
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85815504a72bcb6a041dc9c6719b247fec1e21041f41b6f9131d482de517db9`  
		Last Modified: Thu, 02 Oct 2025 01:11:05 GMT  
		Size: 8.2 MB (8184433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5327de806c5a472e2179a5a497c8fd14d1352f950e28cee0d7d2c2cba9df9dca`  
		Last Modified: Thu, 02 Oct 2025 04:59:10 GMT  
		Size: 43.8 MB (43759999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f781e978d124a5f6fc12ceabde8787b4203fcbdcc4c5eb6c92e85b513c73b78`  
		Last Modified: Thu, 02 Oct 2025 12:59:04 GMT  
		Size: 183.4 MB (183426636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:798090b0a293f3579fd8e8797768a6b8f176c85a16b555c4376afe29a259871d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11809133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ea3c4a24a585c5b029e1b46305a2f7ad00f273802311c1bd5c9b39a727bd18`

```dockerfile
```

-	Layers:
	-	`sha256:170c1b81da2d4c3b2214adfd60475e5c4b648d668112194a8af32a5fdd235714`  
		Last Modified: Thu, 02 Oct 2025 13:19:54 GMT  
		Size: 11.8 MB (11798899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29a5e86b5b7c3f38d27d9d42de95b1b6a35c32501f630644b9cc1d3df7c3d77f`  
		Last Modified: Thu, 02 Oct 2025 13:19:56 GMT  
		Size: 10.2 KB (10234 bytes)  
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
