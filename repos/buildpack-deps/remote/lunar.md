## `buildpack-deps:lunar`

```console
$ docker pull buildpack-deps@sha256:9a73313ee0d60b24e7e4adc31947f0f1f674d647c712e02176d81e99e09060df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:79dc8da90ace8f7d431268d6f3611f3d07434d6250c06e890e0f443527abf346
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276174659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fefca31db7be23c6f72d99fe917da1f1c8cefbd3eb18ff7640a7b61b1af97f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:02:17 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:02:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:02:18 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:02:19 GMT
ADD file:9627edfd854222fb9117755e0e89c54a01ba3477dffb8137693b12c586d970b8 in / 
# Tue, 28 Nov 2023 09:02:19 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:13:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 01:49:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:efcc827fbbb39a149bce1b1b0951eccfa438d1d84153744033dd253856da8a08`  
		Last Modified: Sat, 02 Dec 2023 04:29:07 GMT  
		Size: 27.7 MB (27663335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89be6e41d0da2e13b8aacdf92ea3bbe1ea4a92027ac0f38f8feb44bd4e21f56e`  
		Last Modified: Sat, 02 Dec 2023 04:29:05 GMT  
		Size: 13.7 MB (13749136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85be60323243d50ff84a27aaaa0df4eefed88ee280702196c9c10dd343b874f`  
		Last Modified: Wed, 17 Jan 2024 02:06:45 GMT  
		Size: 44.9 MB (44909916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d4635121cc7cdcded4f3d34817781c7371d3466d91ccf559787f15a4d45299`  
		Last Modified: Wed, 17 Jan 2024 02:07:19 GMT  
		Size: 189.9 MB (189852272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:32de6b65e45e9dcff0d5cce8c548a96814fe1b31de4961ac8e81ae981774b857
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238160700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da185f927d61a64e20b051550d49d31a544c2bf1f0395626f8463709a487540d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:13:30 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:13:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:13:30 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:13:34 GMT
ADD file:26fed032754dce7b61f687e0c3d6d657971aca74602c12de619a784c993bdd72 in / 
# Tue, 28 Nov 2023 09:13:34 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:38:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:04:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:08:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25e5040c4e77c352ec740991a280f8ab040dc8abd1365fa7de40d33e0779de89`  
		Last Modified: Sat, 02 Dec 2023 06:50:30 GMT  
		Size: 25.4 MB (25444267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf1c2703d701a964af5dfeaec665c54c0e3ed4f7c0be876bcba4a45d0f378d7`  
		Last Modified: Sat, 02 Dec 2023 06:50:28 GMT  
		Size: 12.7 MB (12666407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279c9533161aee6d0356a2ca5c47dbbeb138abfe88c1d7333e653142e2728ddb`  
		Last Modified: Wed, 17 Jan 2024 02:27:05 GMT  
		Size: 49.1 MB (49102733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ea41ab118f7490d877c92fa7aa67d822a097f77561ebbb1cc252ed10021bea`  
		Last Modified: Wed, 17 Jan 2024 02:27:43 GMT  
		Size: 150.9 MB (150947293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:992f23af5f0537bccef4b418eb6a0bc84914bb0858ca7457969e0cc78faf39be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265501280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a22d58d4c4e2cb8f3673fbcd2cae505b8714e38e93f1809b610d9d1e7b337b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:09:50 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:09:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:09:50 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:09:53 GMT
ADD file:6859e1ffc351c0e88484a54fa40a0e572765d4c34180b05901ea0adab3a5928b in / 
# Tue, 28 Nov 2023 09:09:53 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 05:17:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:41:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 02:44:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:80dcd200a7d0fef40eb1ea39ad236dd61328907d6d0f7ecf0c894346d77bb1ff`  
		Last Modified: Sat, 02 Dec 2023 05:28:30 GMT  
		Size: 27.0 MB (27020145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b39e5dfff806e4ea2d441b57002854ca0e0258e64be7afea72f21a9564ef51`  
		Last Modified: Sat, 02 Dec 2023 05:28:28 GMT  
		Size: 13.3 MB (13340925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de05f11c8976c8450e479e0b91573ee36e8c69a6bf22bb6d7e06beae4c0d687a`  
		Last Modified: Wed, 17 Jan 2024 03:07:46 GMT  
		Size: 44.7 MB (44729962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4976c361862a189f8e20de881883bd69f42b6ad632274e2f846db695a31feb22`  
		Last Modified: Wed, 17 Jan 2024 03:08:27 GMT  
		Size: 180.4 MB (180410248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f4f8f1e44daef9ab397199b3fad02fc5cf7feed445051e7a5bbd89fad48fef7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301574442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53837da1a8142f8c4fa3e5da457964dd4d898f229fd3b17455dcec6ce349f29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:18:09 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:18:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:18:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:18:10 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:18:12 GMT
ADD file:6b3f0585aa120c4ab6a2a030727088bedc6e7d88a01d65c847d77f311637589f in / 
# Tue, 28 Nov 2023 09:18:13 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 04:32:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:04:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:10:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9d7985dd9abca9e449ef51d53fea4f59b7587f7d6678b26f8a59f74f654005e`  
		Last Modified: Sat, 02 Dec 2023 04:50:19 GMT  
		Size: 31.9 MB (31898961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d6c482e153eb90eb945c1192b46b13d00b5c8dbcef601e120cf3bbd98c3d35`  
		Last Modified: Sat, 02 Dec 2023 04:50:17 GMT  
		Size: 15.8 MB (15846082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8699c7700c9a38cad4d88fa911a6ce092f070751612dc230b1bcd5d2bc4eab0c`  
		Last Modified: Wed, 17 Jan 2024 03:31:20 GMT  
		Size: 49.7 MB (49697703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3501a560acb823f3a02ec2a5a22eb9e5b113d3c119680b0bb863de68148e67`  
		Last Modified: Wed, 17 Jan 2024 03:31:59 GMT  
		Size: 204.1 MB (204131696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac997a53931bcf78fef716c9da1da5049cdd949e6d0c4330609d79a06cf462b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246699303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52743969732af906143b0fc143afbe75673fdad5437d53ed275049f818ea6a52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Nov 2023 09:17:26 GMT
ARG RELEASE
# Tue, 28 Nov 2023 09:17:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 09:17:26 GMT
LABEL org.opencontainers.image.version=23.04
# Tue, 28 Nov 2023 09:17:28 GMT
ADD file:34e95cddd67480da1b7990b0957bd24393bc65dc923e9af86031a3b55ee0d3c8 in / 
# Tue, 28 Nov 2023 09:17:28 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 06:05:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:45:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:48:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:df880fede659201a3fc93d6b2a4fcd158b4a03c1fb5cba7faea86e5702e20e7f`  
		Last Modified: Sat, 02 Dec 2023 06:14:56 GMT  
		Size: 26.2 MB (26236315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080872d7ee22dc0c228c4f2e15d9751b0bbc8a570f79cf7978062ef8daf3ba1b`  
		Last Modified: Sat, 02 Dec 2023 06:14:53 GMT  
		Size: 14.0 MB (14009218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3238ce9aa9a722d31365ebc139f0c1ccc9926fd84de44b115764e89083b8eb7`  
		Last Modified: Wed, 17 Jan 2024 04:08:09 GMT  
		Size: 44.8 MB (44775022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0615d547505e5ab97e2685b8ae9e9b82d13e44f5d47568b86bc69f5e523465e9`  
		Last Modified: Wed, 17 Jan 2024 04:08:35 GMT  
		Size: 161.7 MB (161678748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
