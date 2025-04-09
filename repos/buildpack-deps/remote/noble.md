## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:37b42d7e24e38b2fa695773fad96fcc2fc6d1d5fb4136ed26779281a8606bcf6
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
$ docker pull buildpack-deps@sha256:8c394bd23f182ad487b90acd485cf846a50a5f2c252634f8cd1cb1912318d24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274589093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229c4aa002ce4788e92e41b4ccfda9b43d6fb67297305e489990657efec148a7`
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
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
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
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69309ca3d9d60664f532872b9e1059b60a35b8bcd9da011efbec14de1397debb`  
		Last Modified: Wed, 09 Apr 2025 01:11:36 GMT  
		Size: 13.6 MB (13620217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9c07a4a3cd036ac7c92fc3ace1538882a1927198a7a271a4ed8154cb5a6610`  
		Last Modified: Wed, 09 Apr 2025 02:11:56 GMT  
		Size: 45.3 MB (45310427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343902907140cf223c434c8c6ff8c44ca01a2c64718bf30e43550d42efdd7664`  
		Last Modified: Wed, 09 Apr 2025 03:11:47 GMT  
		Size: 185.9 MB (185940797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:572cf16ff845a86d96dfadb9b19f95fec8b890478195fbf8991761cbe502be24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11352980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c96f8156d04904ac84a7766d6439f7ade7d87e4da5429cc0e6b91178b3e3b6`

```dockerfile
```

-	Layers:
	-	`sha256:01fac514d80c68ddca1930fe5fb3ca3ee8d1066a200d6e120eb043b37da4b1a2`  
		Last Modified: Wed, 09 Apr 2025 03:11:45 GMT  
		Size: 11.3 MB (11342796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f388f779a1665078ed515003b8fd243137c2fc977ad2e128a25c4fd7fcfed7`  
		Last Modified: Wed, 09 Apr 2025 03:11:44 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c112912ff2efb995d1ad20f91900e5ddc963be6bf99bb162bed0132a9ce3ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236665774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed61a6021a4e39645cdea88adedc73f087887b79431a905895c273d39ff1065`
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
ADD file:0c96eee5fced5e61820b5d18bd668a362ad0e5b3fc04c115f9023e8c295e7000 in / 
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
	-	`sha256:34560582cc6246fb88c88648a1db5ef09d8b65d143991211ba2abe7378aee811`  
		Last Modified: Tue, 08 Apr 2025 11:53:53 GMT  
		Size: 26.8 MB (26837532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61ae8c309ecd2f4c2830c9d05cde6b1ec98b1230dc3ccc9ec8e2f33256e2c3a`  
		Last Modified: Wed, 09 Apr 2025 11:34:51 GMT  
		Size: 12.8 MB (12779568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b800cf45f3970426537a7cc29d993e5d491f2825c492b5e484a4000db5300da`  
		Last Modified: Wed, 09 Apr 2025 12:19:53 GMT  
		Size: 48.9 MB (48866715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251553e68d8bc4b745d4d8b31d95982e49edd42e58eea53d0598f4c21f8cd52a`  
		Last Modified: Wed, 09 Apr 2025 13:23:09 GMT  
		Size: 148.2 MB (148181959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:19d80dbfa4c1df6efe5a71e2ec674846ee112a32810db99155b60d471f75a189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10702231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2da825e2c5c4df88b869f1b6d60b690ed171668cd76540dae2064be0afa4b2`

```dockerfile
```

-	Layers:
	-	`sha256:0d53550d904e68c6f54cb0254f45cbf196b71b019c35613d8166931339ae918c`  
		Last Modified: Wed, 09 Apr 2025 13:23:05 GMT  
		Size: 10.7 MB (10691987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c526d6de59da037549f9fcc14e419045157d72c6ee8c98514c99720798964a1`  
		Last Modified: Wed, 09 Apr 2025 13:23:04 GMT  
		Size: 10.2 KB (10244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2c6b1a58e492bb9a47160cacd347d60ee6ffd9943b91ee02e8e9a6ef5b84464e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267319864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c08849ed55e172a675511112c2162cdf2ed1e0d55ec8e5b7f29b1c42c1cd94b`
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
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e873299a39c8bb8cb3b5d978575339de6ade976cca414b5727de8d362ef599f2`  
		Last Modified: Tue, 04 Feb 2025 09:03:21 GMT  
		Size: 13.4 MB (13447918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94ea46ec0243a993d7c367da2602e0a5008adad8e66c3b027175cdc919418bf`  
		Last Modified: Tue, 04 Feb 2025 19:05:48 GMT  
		Size: 47.7 MB (47732701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1a6fdf4c84ab05014514daab209ab340e6a23ddbcfa591380a07f0fa77e247`  
		Last Modified: Wed, 05 Feb 2025 01:53:00 GMT  
		Size: 177.2 MB (177245647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:804e3d87410f925c0a5a35315bdcdeb5688e8419532c1332ba991684eb953058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10929069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0fb44f3945084d3ac354133e3f6ffb57f10ce3cc0ee648d0469a1ab150f572`

```dockerfile
```

-	Layers:
	-	`sha256:c3b40c8bff9fa4ed8aec00534cb79f33a2af63ae628a15e0d20bf9106593a5b8`  
		Last Modified: Wed, 05 Feb 2025 01:52:57 GMT  
		Size: 10.9 MB (10918805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07a196ab7620ae4f5e60f8ce810b0c4aeb5125d3cf8af61beb9e8dca5d0db349`  
		Last Modified: Wed, 05 Feb 2025 01:52:56 GMT  
		Size: 10.3 KB (10264 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ba0cff6a49efef511a9598f1b2dc103aa37b98f85e34d05eaaf5d3ad377b874b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290236762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314f4488b85c140313baf0826957568b87ee532cdf1a10b6ce59e3b2012c50b6`
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
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
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
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f1c8bb3d99b4917c8ba06f9646b55d42ffc7d868b7d8010468bba3dabffc300`  
		Last Modified: Wed, 09 Apr 2025 04:29:36 GMT  
		Size: 16.0 MB (15951765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c952ba13ea9a62012e20c05b5d9dd20b6885153704ecbf859c6fc8f1f3da578`  
		Last Modified: Wed, 09 Apr 2025 07:37:17 GMT  
		Size: 50.4 MB (50371987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed45ef3a762654d57c134c2a6e509ad295269c882c0cf33eea02c64a716c277`  
		Last Modified: Wed, 09 Apr 2025 13:35:21 GMT  
		Size: 189.6 MB (189572143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a3161f0c7003e00c691c7eca30e0d27478d8229f73f84aecbda9f6bde7e36db9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10871698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58faa668b775948c2aaadd510963da7be31040333668a1e1a19526865c49f7e`

```dockerfile
```

-	Layers:
	-	`sha256:09a710e0b5f244bd0d94f9c3698cd828eaf8764bf038dba6e97bc6683f87e00b`  
		Last Modified: Wed, 09 Apr 2025 13:35:14 GMT  
		Size: 10.9 MB (10861482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0502e5fafa93d5c07b824c53bb0cd4f16e2d0325936f7e3793fe6020f498c9e1`  
		Last Modified: Wed, 09 Apr 2025 13:35:13 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:676b3f1507da964a2c7eb588b5c235e4023842aaf1d6866ec0dae5c132c5da7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330114264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea29db35bc970de1dd6f9958a1e5c21e2220a7911d0b29464bef2be5a2569dce`
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
ADD file:ef7c97f5dd8d665aae899afe52c54f7acaf71fa51e9d7f26e13ed6073141c666 in / 
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
	-	`sha256:ba2f284f7444fb0b78fa804d74c44dee4b397610267539e4a6e9c41ae41e06a1`  
		Last Modified: Tue, 08 Apr 2025 11:54:06 GMT  
		Size: 30.9 MB (30943202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5f313a1c6dbd13467e879d320aa46ad9e7a8abb607e47f5fcd4fe19d104810`  
		Last Modified: Wed, 09 Apr 2025 05:18:21 GMT  
		Size: 14.3 MB (14327361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb39271530bef5884da7d90dd3fff241bde4855d8423132d8efa1eadcc6ee74`  
		Last Modified: Wed, 09 Apr 2025 08:41:09 GMT  
		Size: 53.8 MB (53804467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19e9c693ea89b16c002fac41b7ac2c578b3c352e101baed7e938bafca673cc`  
		Last Modified: Wed, 09 Apr 2025 11:03:21 GMT  
		Size: 231.0 MB (231039234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:360501222ce4bd505067ee02a16478b7bb66a8408c482eea16d23774fe19c77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10866135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b093544fa15c4cd6b57f8efabf02ff44ceb07227a9e0393bf11946a37d13a387`

```dockerfile
```

-	Layers:
	-	`sha256:c3d1e73354ab6b8fccd60cc6c60972358eb15da230a3509b4eb7db236244b2fe`  
		Last Modified: Wed, 09 Apr 2025 11:02:51 GMT  
		Size: 10.9 MB (10855919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c229081c057cba80ce4b38529d021a237577b4aca196200fc0ebe1582e6da3`  
		Last Modified: Wed, 09 Apr 2025 11:02:49 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e6826c79d541d74a4599d3a6c91d20a681e2d667aadde712aaae847707269737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253043609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a659ba108f9f6542140e2023eca59129735bb49ac9617050a9dace3e93e73`
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
ADD file:8f287f40ca940c9bd87c8706751f5f1c5bbd0a83fd75f7d938832b226fdb936d in / 
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
	-	`sha256:e5722f32c6281fa87f1e5f7ebe307864b50aa95a116496a205ce47478bc9b52c`  
		Last Modified: Tue, 08 Apr 2025 11:54:12 GMT  
		Size: 30.0 MB (29956206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704885473e9016559440f7dd673fed8248fa9c173ce47190caab5bc5ba71e91`  
		Last Modified: Wed, 09 Apr 2025 04:12:34 GMT  
		Size: 14.9 MB (14937511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13864cd5d972733632aa5cddaa489533b9cfbdc5130cf29bbcf6bffbc8be43d1`  
		Last Modified: Wed, 09 Apr 2025 07:09:02 GMT  
		Size: 46.7 MB (46744434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5799e14a2be51a84cf3a372fcf4ae550e0489cabd88a06516e784b25d3241ba`  
		Last Modified: Wed, 09 Apr 2025 10:35:11 GMT  
		Size: 161.4 MB (161405458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d4960681971cacc7c6526eae97f888d49f666dcf9aa79655fb71eb58a8282ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10717541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b2f69964f48b491112a147e3162b41df0233514dc4d44c38f41efcf01eae3f`

```dockerfile
```

-	Layers:
	-	`sha256:c897aab525fac01261f87891b6f4e06c6854fbf3451f5020bfa0206825b53126`  
		Last Modified: Wed, 09 Apr 2025 10:35:08 GMT  
		Size: 10.7 MB (10707357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d34c8920a20b75c3293bd825d506f406d9c88bc92635bcb55c7edc7d99ed280`  
		Last Modified: Wed, 09 Apr 2025 10:35:08 GMT  
		Size: 10.2 KB (10184 bytes)  
		MIME: application/vnd.in-toto+json
