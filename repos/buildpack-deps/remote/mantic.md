## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:e5ea05fbee2bd3be8a636f5233a11d0f4e48c7066bfb0e7dd0fb7a4f528dea5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3e626a20692ed77279609abdafcad66c7476203cea1c6db137e008a18bb866e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.2 MB (286212063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e061eedef8677a47750ae0e3bf0c544f807a567c8da27ed6af706931e3132b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:05:34 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:05:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:05:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:05:34 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:05:35 GMT
ADD file:e12b21146377229efd13935eb949a5d74cf2b246efc163ed315734630be3958c in / 
# Tue, 16 Apr 2024 12:05:35 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:27:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:28:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:33:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d8fffc499ea6c8c41da994c0d9d485a884eacc48cbaae54af0e8248add34a72d`  
		Last Modified: Tue, 16 Apr 2024 19:37:42 GMT  
		Size: 28.0 MB (28037251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de3bf0c3305a1be64e9984b6f9a9fc997b6eddeda43eca40198080956a3e44b`  
		Last Modified: Thu, 25 Apr 2024 21:44:37 GMT  
		Size: 9.9 MB (9911592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd7f61866536d2a2c137f7939338579779b27e557caff274e1598d18d0de9bc`  
		Last Modified: Thu, 25 Apr 2024 21:44:53 GMT  
		Size: 44.8 MB (44767442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ebc0d0d7f3387d0c22b38f7d64c9e615514e3b8d4cb9244becffbb969cf7ff`  
		Last Modified: Thu, 25 Apr 2024 21:45:27 GMT  
		Size: 203.5 MB (203495778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:38ec33a865bd2d98bd71d1904bb7fa522cc5f6dbc52e065dc6b1d804669c071c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.6 MB (251570263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8236b27288a05fb3b91c26fca9cd337cbb1246e4422cf1c2c6130722096f3759`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:08:51 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:08:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:08:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:08:51 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:08:54 GMT
ADD file:f07b1f2c0ba7dbff20c2f89af95625b7160c10dd0b56c8ce400479098ff75d9e in / 
# Tue, 16 Apr 2024 12:08:54 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:56:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:07:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e89c6209d73c95b4a561524bab8b142d958224c65b38f1815b271bf45a6b6993`  
		Last Modified: Thu, 25 Apr 2024 21:21:18 GMT  
		Size: 25.7 MB (25687521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d611f98574fca5102b33ccd28e2f963e80c8c8e988af15477d729f0bcf6b9f`  
		Last Modified: Thu, 25 Apr 2024 21:21:13 GMT  
		Size: 9.2 MB (9152067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673fdb7ddba1f1fbfd83c45e0c9da9c1e40a8e8c94119cc3775822ab677e287`  
		Last Modified: Thu, 25 Apr 2024 21:21:35 GMT  
		Size: 49.0 MB (48950214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8052f4f6f60aa7b6eaf2a76f1e38ca8d8b430f83defba84ed144d831f38c25`  
		Last Modified: Thu, 25 Apr 2024 21:22:07 GMT  
		Size: 167.8 MB (167780461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9a3640231d503821e2c6a5da0188ac7bf1cf3007bd824ab909aaccdd8773e222
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278033925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59229c4f31385dbdb1ebd95e2d43a2a346c2a4357ac6299ffc4564aa484be29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:36:32 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:36:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:36:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:36:32 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:36:36 GMT
ADD file:2a859c5d715743469a5a33d7b6038db94be34745cff1d5f681ed1d3d0e5931a6 in / 
# Tue, 16 Apr 2024 12:36:36 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:23:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:25:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:33:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9f940a958fa1db38437a7b5c1c0ed37e0c5942712bdd8f2b76b3389807d1ffd6`  
		Last Modified: Thu, 25 Apr 2024 13:46:30 GMT  
		Size: 27.4 MB (27379628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67d18d62fa954ee78994d922bbd009c6e5a86cf5622f267d40eff6d0e20d7a5`  
		Last Modified: Thu, 25 Apr 2024 21:46:46 GMT  
		Size: 9.7 MB (9664678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bee0d85689fcb88d4edc1a4a568dd0c83256cd6df41453994ed58fa7b4e17f`  
		Last Modified: Thu, 25 Apr 2024 21:47:00 GMT  
		Size: 44.7 MB (44677946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f80c1f8fb52f7ab333456e3bb0485fecad800cfff0082408b4424cca4b0a3dd`  
		Last Modified: Thu, 25 Apr 2024 21:47:27 GMT  
		Size: 196.3 MB (196311673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cd4fadf1be30331d776e1c0bca51d8f3eb84c269e05f8482b29332931e8b7c97
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300858916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a29d9971d8be44fb65d9fc57e243af484322b74bc313188a441b0381015ecd8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:36:34 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:36:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:36:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:36:35 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:36:42 GMT
ADD file:d101590827db35fb306467a12041319349f48362c5708f20a992cacfa084f678 in / 
# Tue, 16 Apr 2024 12:36:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:38:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:40:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 21:50:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48003274bf9d81034d8159e3fecf795a0d28af11431c0dac90ec318b737dba7f`  
		Last Modified: Thu, 25 Apr 2024 22:06:33 GMT  
		Size: 32.4 MB (32350551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a96571a4483e69c613086a3247b75c7f4157a94d51eaa2b35b852337ec5cba3`  
		Last Modified: Thu, 25 Apr 2024 22:06:27 GMT  
		Size: 11.6 MB (11585701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e03369684bdfa11e2d1e5cd9d25cdda8608261828650129c36480834337b220`  
		Last Modified: Thu, 25 Apr 2024 22:06:50 GMT  
		Size: 49.6 MB (49561538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b527830ba02a4c6f389d5507ef2b815ae774ee62ff3aa25d06fa2a03bf7d2a`  
		Last Modified: Thu, 25 Apr 2024 22:07:30 GMT  
		Size: 207.4 MB (207361126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ea5804d173f43218f5fc93c48419f3b0e55a9d278cf71acff0759173b7553bd2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263826958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a845b1361884122c0f22a6c1ac02b88c9686392981a809d6900bfdcb3131da7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 12:37:06 GMT
ARG RELEASE
# Tue, 16 Apr 2024 12:37:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 16 Apr 2024 12:37:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 16 Apr 2024 12:37:06 GMT
LABEL org.opencontainers.image.version=23.10
# Tue, 16 Apr 2024 12:37:12 GMT
ADD file:bcaae6745c5074969da19bc7c697ea513ed4123bd3a263300b0dd2d86c419d62 in / 
# Tue, 16 Apr 2024 12:37:12 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 20:31:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:34:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 25 Apr 2024 20:43:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:383198d5df8d4ba96d57ebcdf24f767bc0cb4db9ae335a6ef7de76bd893b3bd8`  
		Last Modified: Thu, 25 Apr 2024 20:59:14 GMT  
		Size: 27.9 MB (27890823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8514db07371eaaa86882f69cfd0b0771cda74b8001732c14e7daaa5b5e82488d`  
		Last Modified: Thu, 25 Apr 2024 20:59:12 GMT  
		Size: 9.8 MB (9758799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d49389615718d3f50c34097e37fac7a07970f9115ee870e86179365588676f`  
		Last Modified: Thu, 25 Apr 2024 20:59:32 GMT  
		Size: 45.3 MB (45253931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abeb5a9da7acfadec275252d7976efeb7c9dc4ecedd5470e0b0c59dd0dcd0b94`  
		Last Modified: Thu, 25 Apr 2024 21:00:04 GMT  
		Size: 180.9 MB (180923405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
