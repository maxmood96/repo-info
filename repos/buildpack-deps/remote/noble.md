## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:f7e20a42a7ca640a6695d5a67036e328150ce6298170eec3ea88015940d47376
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
$ docker pull buildpack-deps@sha256:9b1d28fd1dc2ee1645e98e4726c782406b14230e4646b3c0b7dbf181d9b3b077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277330578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71497dfbc3d6a2807c8a5f44f6de5324f12f51b5337f2d37f374a0583ca52943`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affcf24932dff649e2aba4f579c169f460375d428c50fcb251e53f98e4c30fc1`  
		Last Modified: Thu, 02 Oct 2025 04:52:18 GMT  
		Size: 16.0 MB (16023985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36dce96fa7416b8a57d7a219addbb30cf4c5868e9d6e1846e5cb7f9d6c3bb25`  
		Last Modified: Thu, 02 Oct 2025 08:26:05 GMT  
		Size: 45.4 MB (45426423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5741f81d527ab719461745569dfdba553c3d83b1da148e2bf0cb17721cca9f0e`  
		Last Modified: Thu, 02 Oct 2025 12:04:17 GMT  
		Size: 186.2 MB (186157159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cf8b3883e0ea061a68bd81991ba97232deefceb44f65e55af8dcfc45bedb9a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11742963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ea6c25341dfbfbf298d8a7f24f099788ee6b014f50bde60b9126bc6b800ed1`

```dockerfile
```

-	Layers:
	-	`sha256:ed6f5a87753f9bd0995b9d61ee6adf37f650d8851ef5ca43ace492872aa8ab04`  
		Last Modified: Thu, 02 Oct 2025 13:19:34 GMT  
		Size: 11.7 MB (11732779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80bd7e94b6370f655ddd316a4384073a79b8b1bee2174e984f98b0a57cf83b3c`  
		Last Modified: Thu, 02 Oct 2025 13:19:36 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:89c865d0c40a3839e1b69a21d7ec6d07051575621a0b7313a60080fd68ab010e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238589156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38f795bfc4bfdee0464b3dff4ff576897c0e95d6c6aae41b4f69ec728ee2321`
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
ADD file:51076814e2aa1389d29f1b4c38eee0cfbb1d321f099c50e09b19452198f65032 in / 
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
	-	`sha256:6c9f3e8be363989d138b8e3a1316487da5ee2b8384d3c6b0f9b1a8290f57caff`  
		Last Modified: Tue, 30 Sep 2025 17:07:34 GMT  
		Size: 26.9 MB (26851149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f18ea7fe9ef4178a0e236f41c554cead30170db066c48450b074df4ca534de`  
		Last Modified: Thu, 02 Oct 2025 01:11:12 GMT  
		Size: 14.6 MB (14569242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42003d15858f39d12322fbbb59f088f0569c5114141a064f9292c6ad7172be08`  
		Last Modified: Thu, 02 Oct 2025 02:14:57 GMT  
		Size: 48.9 MB (48865266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d96725f33b3d80af22c8fb820b998ab2aca559a8f124b556bacfc186a78f5f`  
		Last Modified: Thu, 02 Oct 2025 04:11:46 GMT  
		Size: 148.3 MB (148303499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07063af364430feb73fc7d25df2508ca4bb25094631b1881a593c667d885d34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11068728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475d28bb8da2571b20e9cf3e51482507687cfc3a373dded992ae850ce9022a81`

```dockerfile
```

-	Layers:
	-	`sha256:0accf2af552f1f163ed98a44ccb8878f45f44672627d43f0766296b60030087b`  
		Last Modified: Thu, 02 Oct 2025 04:19:59 GMT  
		Size: 11.1 MB (11058480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1fa7dc6767cf1a9dba5e13ec1f6fd472465b8d6e7d7f25716425932d8efd6a2`  
		Last Modified: Thu, 02 Oct 2025 04:20:00 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:403b84881d72879c3b05ad3819660c46cf6218b5e665450ccb4e28037957aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266455335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84d1ce302032a2b4605aba791b2721c9f17b46bc1922d2755017bc979db4eee`
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
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d4e5eb6699d3808078595f32cffad010cd267cf16038b9e1601e8ec9e37f7a`  
		Last Modified: Thu, 02 Oct 2025 02:14:19 GMT  
		Size: 15.7 MB (15678855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d578c8855badadeef1e8e1ad0e071290f9fbc8be7677300cee994d8861223e9`  
		Last Modified: Thu, 02 Oct 2025 02:15:01 GMT  
		Size: 45.3 MB (45274395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fdcc9509b4e64a8f6b9c68dd2bfa5eeb92196422a60639a08bc3d4a0f6cf32`  
		Last Modified: Thu, 02 Oct 2025 04:18:59 GMT  
		Size: 176.6 MB (176640510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b559f3716a83ec9bc60f7b97bc8ef20e6bc6353b4e9e6af8414f7abbc18ad1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11292512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4404e3a6b755783e3cbccd6fc2fe8cf530348816316b07c32fa95d0ecd01ff16`

```dockerfile
```

-	Layers:
	-	`sha256:8c79237d3110a3fe09dd1222bd81c25e34014ed7ffd90a1c850438c8a5d2ee75`  
		Last Modified: Thu, 02 Oct 2025 04:20:08 GMT  
		Size: 11.3 MB (11282248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2900a06836bc27bb147743afdcd536798c4287532230f6fa1350fab8767eb79f`  
		Last Modified: Thu, 02 Oct 2025 04:20:09 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:3bae3b620be00542ea7217ee1fa4bc2b082982c0ca92212d7f86d85e5b13378a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.9 MB (292929211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fa08ebd66c24e6ec93af21c5798a42a769b8dde01b20643516795a40c2a3a0`
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
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
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
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32831262c9ed2d0082fc94e452de326736750e57be1861993e55b6c43bc96061`  
		Last Modified: Thu, 02 Oct 2025 01:12:58 GMT  
		Size: 18.6 MB (18574976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54436de24358c986f80df683327e624c83c2566b8df8570538895b1d1d8d910`  
		Last Modified: Thu, 02 Oct 2025 05:01:08 GMT  
		Size: 50.3 MB (50339964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628fe7debd77f5b997cdf17446f1b206139737182d61cfc5e97862d7370abc7b`  
		Last Modified: Thu, 02 Oct 2025 13:10:19 GMT  
		Size: 189.7 MB (189710724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:19978ea10da3700df6712b0afa00c673b115a07e540e7dbfb2acec5cfc72d90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11239900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7543ee78ee4ca208d4f25b47a526f9fb6520f7c9d2c6aa1ad1380e3654536011`

```dockerfile
```

-	Layers:
	-	`sha256:94ed2bbf4083d19d1b5fe5b654932e0a7d2cad3b7eeb3fc126c1df67e7eb4694`  
		Last Modified: Thu, 02 Oct 2025 13:19:58 GMT  
		Size: 11.2 MB (11229685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59f46c38148401ceba9cacbdd98838270c49cee1d4f2a7c970011c5f91a50d9`  
		Last Modified: Thu, 02 Oct 2025 13:19:59 GMT  
		Size: 10.2 KB (10215 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1239968c904b03fb7b68308a957dfce446e4a94a0797291ff56286b48e853aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330365150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc94bf7c5e68118cb43c473166785c6bfb3ce62e9785d111aeda2f7492a3bac`
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
ADD file:58fbc6777cd47d1e58396e2c0f70255ae3bd63d0ac2ea2138ed6e5e91fdd70b1 in / 
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
	-	`sha256:fc46b4719a7bc0e446bd2b472a339bdca3990f164daf9dde3e710206f93383d0`  
		Last Modified: Tue, 16 Sep 2025 19:54:09 GMT  
		Size: 31.0 MB (30950703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef5352f27f8eaa4912970c5e40c708ff8676d4d3b32b568f91c0697ef0d269`  
		Last Modified: Wed, 17 Sep 2025 10:13:49 GMT  
		Size: 14.3 MB (14330275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c60c4f66e23d52d21fc7f3dc5c91cd17568df06d10b745951ee901f9d3229d`  
		Last Modified: Wed, 17 Sep 2025 13:34:45 GMT  
		Size: 53.9 MB (53876081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534552a1b50d5efac06d22ccd91bb1cc15d329d6c79d0df3df13529c59edd135`  
		Last Modified: Wed, 17 Sep 2025 21:11:02 GMT  
		Size: 231.2 MB (231208091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6eb8ebb4c0ec1222ba1eb51929bc7d2545017da7415508d3b12fb93bf4bed6b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11233140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5cc9af98ae1c785e3dd6eeb26fa119b12e442829bb0979a1576cf04308ba01`

```dockerfile
```

-	Layers:
	-	`sha256:6c7a8c3d7b3d82093c083c418dd4e461a602f51acd17faa6e6b54fad69897cdb`  
		Last Modified: Wed, 17 Sep 2025 22:19:54 GMT  
		Size: 11.2 MB (11222926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0b3cf219ced01ef25c40c6c51d304f8aeb08f3f7feedead53a1edb1397a4c7a`  
		Last Modified: Wed, 17 Sep 2025 22:19:55 GMT  
		Size: 10.2 KB (10214 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c8b12146a2fee34393a7fa5c38e37acc8f3c4ecfde0668b49551b88507cea261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255113356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc7bfa86db2418fd228f38c2d2f635dd936445b074c74ea56858e03ad6305b4`
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
ADD file:2df9e8bc7cd2e879b1bb1d4b43960e570cf8bf039e9c92e1b3599d2ec12b6674 in / 
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
	-	`sha256:e9a7df0c6e08fd0434347bd07ecdade7cc5d006c086084ec4347cd24546ee1a5`  
		Last Modified: Tue, 30 Sep 2025 17:14:38 GMT  
		Size: 29.9 MB (29906146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbcef77789b132db9a078a6302fcd340d67c834cc1c5a667cfffc3377db3882`  
		Last Modified: Thu, 02 Oct 2025 01:12:01 GMT  
		Size: 17.0 MB (17026854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23daf2b9224fce2c79e8979b00f4f503fe59502e9808135d3feefab2b5c4f67`  
		Last Modified: Thu, 02 Oct 2025 02:40:59 GMT  
		Size: 46.7 MB (46746859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8172dc8d735923a3e29b870bbcfd34207e80ad7c4357f498d6676c0b86bcc4f`  
		Last Modified: Thu, 02 Oct 2025 06:12:22 GMT  
		Size: 161.4 MB (161433497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:66d2f6b47ad4f77438a52dcc9d2733524623633f211c4cdafe6ee26fcef167ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11083716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e96d5b96e1bab658bfce564cd01deadda2515730f54636fcaee01530ce5e889`

```dockerfile
```

-	Layers:
	-	`sha256:12abf3ea3dc1605f1758ccc78e084f54008685d7edbc5c131b8f77a9a3aaf2a1`  
		Last Modified: Thu, 02 Oct 2025 07:20:12 GMT  
		Size: 11.1 MB (11073532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4edf4d7d0fb058b061a2e6acf82949cede80587a0f88cf493225880c2f828a00`  
		Last Modified: Thu, 02 Oct 2025 07:20:12 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
