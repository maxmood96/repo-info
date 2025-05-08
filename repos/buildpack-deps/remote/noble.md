## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:637549b74825bf6d62421bb4848b225c000bda4319daab60a46295b7935c2dec
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
$ docker pull buildpack-deps@sha256:7a31478a762de68ba2ec7c6e1578e4d51f6405785e193ee2f827ec80516c32e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274637492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e531be26d550ad7f5354416675a328e20fcc83391f1a851332a632a5104ab1e0`
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
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
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
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eaace9b65900e696e96e472a957b7da3924a1f1e20b735931fd210783d02c2`  
		Last Modified: Thu, 08 May 2025 17:07:42 GMT  
		Size: 13.6 MB (13620461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd5c213ee5a094216a432d394a0648f5712ab727b532055e6cb5bf49c22052f`  
		Last Modified: Thu, 08 May 2025 17:09:27 GMT  
		Size: 45.3 MB (45307019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99fd84089175072bbe7e4370807913fbfdda82b46c934fd285ff892c632cb24d`  
		Last Modified: Thu, 08 May 2025 17:09:41 GMT  
		Size: 186.0 MB (185992483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6e2dbffe89268820280289acb08f8b03a5d841c0cf2b14372197694eb3b63268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11352992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f534d6c4cb539796dc17282b6f19df3e7789f29911509e26b3c53882ab9473ec`

```dockerfile
```

-	Layers:
	-	`sha256:af61b360d3a228f24faa7693809f8565d009c44d097a0044ec0bd2543fa27ccd`  
		Last Modified: Mon, 05 May 2025 17:11:59 GMT  
		Size: 11.3 MB (11342808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8713e25687c6ff487abf129cd5ad017da29cf9a9e9334a621454461edbf2f364`  
		Last Modified: Mon, 05 May 2025 17:11:58 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6b98e6c8d0f44515314e8d93367e251e79fb91151fa73fa4ded62fba987fcbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236749496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf444630467640be0e8abd327b5f84ac9117ebd83f6c89500eb645159080447`
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
ADD file:0a4f443ceea6f2d38d4cd9140cd3ff090f97e81996d29997f71a7e6267915f64 in / 
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
	-	`sha256:d5afef7cc6686ed2d24ed4bfcb591ca82e697ea35b656a63f79d222cf1271caa`  
		Last Modified: Thu, 08 May 2025 17:10:49 GMT  
		Size: 26.8 MB (26837779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44336f57998ec8ec9b6b393b0377c2fceec78d81e9802b43bbe7cc354461c26b`  
		Last Modified: Mon, 05 May 2025 16:35:26 GMT  
		Size: 12.8 MB (12779558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dae90481efbb2c007c4e2d9e63a77a0163b1886b97a45dbd574883edc830df9`  
		Last Modified: Mon, 05 May 2025 17:03:18 GMT  
		Size: 48.9 MB (48866795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444ea0fac11ed5a5a8357128aa9542f3f3cf006961eb54cfd4a1a12a57eb6954`  
		Last Modified: Mon, 05 May 2025 17:53:45 GMT  
		Size: 148.3 MB (148265364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab3c54e38115e853ac1deaf1a885cb84b7179350854ecaf117ddc43dc8870e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10702243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e8bcc3ce21b0edb53c1f6b62e5a111b3381d3acb28ca680adcdb3e78ad96b9`

```dockerfile
```

-	Layers:
	-	`sha256:72e02c9d489f1c1086ecc2d571c17d013c639c5fb790669f35c19070f66df450`  
		Last Modified: Mon, 05 May 2025 17:53:42 GMT  
		Size: 10.7 MB (10691999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c299027e16a76c66387bfba99e518166474a8eca9bc0dfb74ab4adef543c8913`  
		Last Modified: Mon, 05 May 2025 17:53:41 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cbb51add1662b8f5eae9a0c207ae7d6eee2545be7bd8ab98908ad4487bda147a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264328903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dca68ca39abd218f2ee17865e50b58cd38a81b1125b17c68c000b40e7b5b43`
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
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
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
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a0cc72f6ea7fe79563bee33bdcb1c9b244a1c5ab3c0f32fd003cd207327808`  
		Last Modified: Thu, 08 May 2025 17:46:06 GMT  
		Size: 13.5 MB (13455434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba27f6d52a24140c5d815eb929d42386c938913bb5a4a74f088a7532830817e5`  
		Last Modified: Thu, 08 May 2025 17:46:14 GMT  
		Size: 45.4 MB (45365279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f57b9408f6d3e972e57ac8fd4a37cb207661ed37d2eb274599abcdd92d865e`  
		Last Modified: Thu, 08 May 2025 17:46:22 GMT  
		Size: 176.7 MB (176661314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8082c458037db943118299501aaf32071e7fc3f2ca9dfcf8d7eefa4aa4a19afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10924480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c394556c9dbf893bab6023e8b1f38a24dd309ba6b914b61939bc082d8f154a60`

```dockerfile
```

-	Layers:
	-	`sha256:c8eff47354984d00fa1449cb78dc211648641082bb0218a96326a8f86caba1c7`  
		Last Modified: Tue, 06 May 2025 01:09:14 GMT  
		Size: 10.9 MB (10914216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406e1efd9fbb1d70d252089409f24ebbc65886984a4cf03c9c2e0bc86d3a40bc`  
		Last Modified: Tue, 06 May 2025 01:09:13 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ac8e52b5eca7c72e4bc49396f28a4ebc120ce85354360137982fdad584d9df06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290353142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab1ee2e52fea193e416bf6744b31d17151de2f08181e8d647b6592415fb3c8f`
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
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
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
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb01c615e0adf803fa55fc78bc3041600f2aa0ce1f245aedb53d467d5681ff9`  
		Last Modified: Mon, 05 May 2025 16:35:45 GMT  
		Size: 16.0 MB (15952010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c581b9092cf3087052438d5f9f23a083507d22950ca17e4d30e1c63391ceb1`  
		Last Modified: Mon, 05 May 2025 18:53:30 GMT  
		Size: 50.4 MB (50377778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964ac3ed826986d41c92d099a4cd3f502efb21192a4829235d19dd494ef32304`  
		Last Modified: Mon, 05 May 2025 22:00:14 GMT  
		Size: 189.7 MB (189682516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:03b25e9c3c966e824cc2a90cac00fde62e9fe84db1eac3b7ac5be3b251fe2fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10871710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27be9363cad0cfb1dff79075e8d21e5c195b936a8fbb32dc261dbd22346f409b`

```dockerfile
```

-	Layers:
	-	`sha256:35cd067faaf056744d60bfdd6042bbd6bfaedf705ddfbc3efa6a2b017fddfbeb`  
		Last Modified: Mon, 05 May 2025 21:59:55 GMT  
		Size: 10.9 MB (10861494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d967699c4e131bac869e7b14f5c7e6f8094ce8e38c9eae6e04cd400ac482a80`  
		Last Modified: Mon, 05 May 2025 21:59:54 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0e308ebd8690a15054383d6a41304b2ecebc22599497c5813817e90fa21d0085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330320904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d1ab009bef01bd9907f4d5dc6f0f63b919a2af91de8fab07e7b7752317bc9b`
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
ADD file:a7f5e3a8aff782c57aa8346238f9dd99048f1bf1a67260c5949ae9396a429340 in / 
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
	-	`sha256:617ff4840b8ccb0dd209aefc32c58a25fc5e72effac2d6267be2d5e4f07db22b`  
		Last Modified: Thu, 08 May 2025 17:24:33 GMT  
		Size: 30.9 MB (30943987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77fb2de0b2f49e76302577d112d09b1cc04109df7d10f98098395265b9951f9`  
		Last Modified: Mon, 05 May 2025 17:09:44 GMT  
		Size: 14.3 MB (14327598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7650db1d1e655cade0507cadb984f3019600a462599f2095a6f043393ce5e70`  
		Last Modified: Mon, 05 May 2025 21:11:38 GMT  
		Size: 53.9 MB (53862786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3cd918df539e914cc12fc5489d91619a5a9de242719070246be6d47a3b8d808`  
		Last Modified: Tue, 06 May 2025 00:48:46 GMT  
		Size: 231.2 MB (231186533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6a32aebff2b6f73d0253ce85e26542db0bb0930f00147f9a7c722bcf334056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10866147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649748d36e27a7256945de3c869bc58e1d88c97c0ae09b2d5c99a145959fb816`

```dockerfile
```

-	Layers:
	-	`sha256:2fb61942f243a95aeb8fb7dca6a2e5e87cc4c2167a32aef2ee16fd23e2504a47`  
		Last Modified: Tue, 06 May 2025 00:48:16 GMT  
		Size: 10.9 MB (10855931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c89b6c38745e67be1694bd22801e0aebaba256c56a8891891de84e7ba9dbfd7`  
		Last Modified: Tue, 06 May 2025 00:48:14 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f419ddac1b1442011c543bfca2c80c7c65b006e759af36da665c21acbc254814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253180858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176bebd2a83fb81d996a21acd780ef8273c8751057be79b6d29e1006cfbb7470`
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
ADD file:486993225aeae656f8d559f5c296f6c3164966e35f4b628d26e1da1b75592143 in / 
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
	-	`sha256:52a1750d5fddc355cdc90a83890b7d582c7f145aa5d114d9582cd010b8ead145`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 30.0 MB (29956186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01143edc1a4246e16888451bfef82ed89787f53271c5fa4fe7b59706ba37dd16`  
		Last Modified: Mon, 05 May 2025 16:35:09 GMT  
		Size: 14.9 MB (14937524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afca3d58958d5bf37f082ff662b72495788350f5d21df0853a05c5b549e9503`  
		Last Modified: Mon, 05 May 2025 17:48:55 GMT  
		Size: 46.8 MB (46773170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26892842e9eb6323fb282ed5f087eff8c11df6b1cdcec62b408fed07351d7ed`  
		Last Modified: Mon, 05 May 2025 19:44:37 GMT  
		Size: 161.5 MB (161513978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22a50037fae55090f1e91275e5d91a5de5cf6496744e46e9cbde1aa35f63cb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cfc68253429903f8d6b50745a0bde5d84b3bef279a253800c0b3a4c8c9b9f9`

```dockerfile
```

-	Layers:
	-	`sha256:ca51b35f867a61d5173dacab7af1aecf89b09b0ee1e269f66bf342a7d8a267c9`  
		Last Modified: Mon, 05 May 2025 19:44:35 GMT  
		Size: 10.7 MB (10707369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f333b71432aef8a20059817598b985f4b0be54c09ca8e0ff04889a4c2774f9b9`  
		Last Modified: Mon, 05 May 2025 19:44:34 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
