## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:7cb445d6a87c640ff533b6b93c4cbd7387884c18c1e43b6848d2088be9cc19da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3c21085ee3b8cd7ff77928238b59b954e21993f8a2bc5537f28915091cb4aaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333677567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8d987413bfc2f6c795be7f0047bce9544e5bb8012a0bd8c042a6cf150cb105`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2aa53e779a14a678b6be0553334055853528ebc9774eaa3e69e5fd71326114f8`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 49.0 MB (48967949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f505e1c0337e142d28ab6c58fa7e5bf319287c629af695b520d6eb278c386eca`  
		Last Modified: Tue, 08 Apr 2025 01:24:25 GMT  
		Size: 25.3 MB (25273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68956bba4f38c9a7df8163b678a6e5da9925d8244f2276ad427d279ae2fff2d5`  
		Last Modified: Tue, 08 Apr 2025 02:14:00 GMT  
		Size: 67.6 MB (67597538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8af4b1ab5b0693130d71f7f83f140c6e34c26e50a70b9a8f741f0bd2d812b24`  
		Last Modified: Tue, 08 Apr 2025 03:17:13 GMT  
		Size: 191.8 MB (191838666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fb1b4baa9a847ba9783216c6afaa1de26268176c801fcb6519713a68c7eafb02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15983799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b2c8036b0e5baa5de52fa36e53320186f58b857348b021d26811b0c013d0f4`

```dockerfile
```

-	Layers:
	-	`sha256:9b025afbf075800309b5afe0e6c348eba979b91d213427f46985841c29c3c002`  
		Last Modified: Tue, 08 Apr 2025 03:17:10 GMT  
		Size: 16.0 MB (15973624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1695c288f5fc50e5f59d17687d4fdfea942925c435d7793ed04851914a7fbb2e`  
		Last Modified: Tue, 08 Apr 2025 03:17:09 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f3ef7789c6cfb6d656271f1f3913517b92fdea4c84fd176b40d6a647e7458709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298840827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b4c6f56808fe2707855f6f6704f5ad107c48c9a8a29ff00ad9603eef1a6115`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7a67f90f752f0b4c3cbc55e5cc36457c9464d60f34b4c1a8cb2a06c06cfda363`  
		Last Modified: Tue, 08 Apr 2025 00:23:29 GMT  
		Size: 47.2 MB (47203396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5a07c09d53242d965ab755e1358498dc94eabdef8c99be65a21d5b9eea16d2`  
		Last Modified: Tue, 08 Apr 2025 05:12:45 GMT  
		Size: 24.0 MB (24031511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b89d4498cb31b4e330ac0bf8f8366b90ab05c82f7ed154f09e19faaaf575be5`  
		Last Modified: Tue, 08 Apr 2025 08:38:45 GMT  
		Size: 65.2 MB (65171140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d7c6f0bb4f71c1091fd068fd25ba7ce3f4049fbef51a6e276a07e702980826`  
		Last Modified: Tue, 08 Apr 2025 10:17:56 GMT  
		Size: 162.4 MB (162434780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dcc394f9fa3b7e6aaabc4cff89a2444eb4d6bd4c057944963dd08c2d62aa0f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15753829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86af81686e0bc0b5c2e9f5e54cf819ccf660d28ba2df6963bcadc903b74c841`

```dockerfile
```

-	Layers:
	-	`sha256:53832a1c8fcf66d268404bad52cf24e8495fceb7442ac0c79bb824cd99ce2bf6`  
		Last Modified: Tue, 08 Apr 2025 10:17:52 GMT  
		Size: 15.7 MB (15743593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7de7c76ddc8b11f4e7fe0e0d68c90d29125ab4a9950ca29b4d67368e2c9641`  
		Last Modified: Tue, 08 Apr 2025 10:17:51 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:711f111feba55965759930e293bbaccd17e4c99f4022a65ad530010ff1b69e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282106775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a557b530430fa44d68cd8eb6b06fe39480febbe3fb0d8f9c9525903a7ac0f1da`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9e1d1d502e5470a18b1778621dae87bc08126015f4514c8d42f4923e5bbe3526`  
		Last Modified: Tue, 08 Apr 2025 00:24:51 GMT  
		Size: 45.5 MB (45459990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aef4244a5aaa0829da0ede8fd328ccc49be5178ede43a05010a5169a12ac0dc`  
		Last Modified: Tue, 08 Apr 2025 07:39:15 GMT  
		Size: 23.3 MB (23303278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f877aab82202905af0b48ebd21bac544815a1b4a8d0acbea3e524330c43db1`  
		Last Modified: Tue, 08 Apr 2025 17:31:40 GMT  
		Size: 62.7 MB (62685699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9a8ea1c1c01e2b63b22955cd81cd4dcae1eb5e85234e59435db4d4b05d4afe`  
		Last Modified: Tue, 08 Apr 2025 20:38:41 GMT  
		Size: 150.7 MB (150657808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8373ebb6c61c00638299f3b9e860b66b8f5f94164279c45741306da8d4183f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15753154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59fce0863d975a3bbd12d05972fb96b3299a0ca80436ca3ca138281008042cf`

```dockerfile
```

-	Layers:
	-	`sha256:501880dc9a2a67767e653a07bacf4740cfc433342246d972a7f50252d3287bbb`  
		Last Modified: Tue, 08 Apr 2025 20:38:38 GMT  
		Size: 15.7 MB (15742918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f53b64d6ef570e739c6c4e68612f10330afb93c075109e2f1e215793f4b8370`  
		Last Modified: Tue, 08 Apr 2025 20:38:37 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2f8ff4b49fa5c610db3602a998a5d18b531bdb290f11ee74a1eea05c84eafaa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323521500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed7dd8306207d6afbab2f528fb2c0f882912891b82bc5e0a76724c80a87f74e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:09d775ffe2e3a261e25d75c66999fe50b8109b656ae312ea92d80a3277b69b88`  
		Last Modified: Tue, 08 Apr 2025 00:24:23 GMT  
		Size: 49.4 MB (49356840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd26d5bca0f15f13ec1e165536514cafcf57ff3d2c87ab2850f356915ddeb3aa`  
		Last Modified: Tue, 08 Apr 2025 06:04:11 GMT  
		Size: 24.7 MB (24668055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435258a53ca79e7f70aa94751fa20a91cc1653438c309c299182c4de6da3bdd2`  
		Last Modified: Tue, 08 Apr 2025 12:19:28 GMT  
		Size: 67.5 MB (67456662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5269e15ea2b98519a186e5da41778f5a8789812e5cc63300c963712c58f1070d`  
		Last Modified: Tue, 08 Apr 2025 15:56:09 GMT  
		Size: 182.0 MB (182039943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5fa936bc650a908e3a7d28440709992c2bbc2d875ce18495114bfdac235ffec6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16068030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e30888d4c9645f49eab0f5d4c8c61eb2cc4c19665e81887d47c361c63c714f`

```dockerfile
```

-	Layers:
	-	`sha256:3546f1d5423577861b9c8d65d9561cb8ed4a44fc418fe0caf0852d57de9cc0dd`  
		Last Modified: Tue, 08 Apr 2025 15:56:05 GMT  
		Size: 16.1 MB (16057774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5429809f159c9b2f3536292e72a42443254348cef294a768cdb89c8b1aa6d4c`  
		Last Modified: Tue, 08 Apr 2025 15:56:05 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:080905ca60a3a7f70abefdd18f7ee883cb922ec9f998bb7c787669d594aaabe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.8 MB (341839309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb66ebbb533743c464cc75e09dbbc85f5ba24838aa4551901a199cf1bf2231e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0f0bbaf0e5a890ab90a12e5df307c321a3344fa0accfb31dc895fe008c16f85`  
		Last Modified: Tue, 08 Apr 2025 00:23:19 GMT  
		Size: 50.5 MB (50476501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686927d82bc30ed67f20e1ddfb9d146b7acb12e90c947c73db07541c131a8cd5`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 26.3 MB (26298358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f78585b0ae6a95bc4b41ccaf9f3cb3acfdcca008d5b11330a5414a8ef1b7691`  
		Last Modified: Tue, 08 Apr 2025 02:13:58 GMT  
		Size: 69.6 MB (69606736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cb477a3e1e6cbf7cda845e80af93f5fbf0e1b5ec36716ecb888c727a8f62f7`  
		Last Modified: Tue, 08 Apr 2025 03:17:07 GMT  
		Size: 195.5 MB (195457714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4b0c774eaa86faa4bf9945baa52a1774846107f76f371fcfa6ca4c55cea8ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15954253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd41d067ac29b5304f4cd3b0d8b46673dcaf10dc7969f2eac0339bc7fb28644`

```dockerfile
```

-	Layers:
	-	`sha256:7e73b77264a67fc7f5d21b6f93d27dac363ba9e343af985a3f04e6b71c4b0bb3`  
		Last Modified: Tue, 08 Apr 2025 03:17:03 GMT  
		Size: 15.9 MB (15944100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96df7144794fa9df725edb6c977a4adeb91fb81d0a52313e797eda2ee4f871f8`  
		Last Modified: Tue, 08 Apr 2025 03:17:02 GMT  
		Size: 10.2 KB (10153 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4c65548d782c5b1e4f88335c601516fe69766bfe4f82f4eedcecb1d216d29be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.6 MB (317619019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9de9ccd26ba1ce28ff0824cfbdaaab482d4a546422d9e0f7d654487cdc18e5f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e47ff6f8c72dd6db533d94619301df4fe359af27c4bdf16e11f5c32ee9c26e9`  
		Last Modified: Tue, 08 Apr 2025 00:23:50 GMT  
		Size: 49.3 MB (49276857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e51d673a637240b96d7c17ea9519652624afebf48f4c69f85cde5bf9564505c`  
		Last Modified: Tue, 08 Apr 2025 16:33:23 GMT  
		Size: 25.3 MB (25333380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6496631413be1b4af7658f44458c20e2e7b199a13d97fee3752f289b6ea176`  
		Last Modified: Wed, 09 Apr 2025 00:41:38 GMT  
		Size: 66.7 MB (66660148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302580e4720bdf5a5f07eb563d36aa09e4f8373c453cd1e3b5ebc33b2413f9a4`  
		Last Modified: Wed, 09 Apr 2025 08:05:46 GMT  
		Size: 176.3 MB (176348634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ef83848c6fc3d0a1e06b5f8eb8600f844c21e8b3bdde2742cbcc7aa0870be5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5d37b4cdc08fcf5dd75c727247b0721b78346692f8ddfb2c6ae66a98c84a57`

```dockerfile
```

-	Layers:
	-	`sha256:c9a0dd0e14a4d6d7821db479f0c7ad824277bd62a9e32fd712ff23a67e056f45`  
		Last Modified: Wed, 09 Apr 2025 08:05:30 GMT  
		Size: 10.0 KB (10008 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:73b2e87ede3065be870e7acbebcd036537fffca75dfb7741ff953e4e4749e253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.8 MB (337811704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8327400492ea809af343f73f4ca8453bdb1363733c8ec9329623472ffac1b759`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:24038d07494a40a6e0f9bb4cfa800b5c396d2199d38fdbd9a4d93a09f5534ac0`  
		Last Modified: Tue, 08 Apr 2025 00:24:22 GMT  
		Size: 52.8 MB (52784300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db81c823da47f6b320f39ca946071003941c644715aa03b5cfb4494f3617d2b`  
		Last Modified: Tue, 08 Apr 2025 04:31:07 GMT  
		Size: 26.6 MB (26637683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40825775c0fc5d49e80018df1342d3a42c3a0c76661dcf0b4bcd002c52dbd16`  
		Last Modified: Tue, 08 Apr 2025 08:39:20 GMT  
		Size: 72.8 MB (72824486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c053a5a828f5b66493294d4d96a6b7cccd7af658022410d6c2652d3fd9954`  
		Last Modified: Tue, 08 Apr 2025 15:37:50 GMT  
		Size: 185.6 MB (185565235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a595e9ea94f570aa3f2818b50dc2165d9d3dd6acc38d476897dea14a1d67120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15974501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cbed792df20fde3522d92e4a91a43f08dd819223b90f826ba93e08edd104552`

```dockerfile
```

-	Layers:
	-	`sha256:b8d5a191f5fd343e2b3bcabec8f90ba46562db988e7c587f086cd371c6398529`  
		Last Modified: Tue, 08 Apr 2025 15:37:39 GMT  
		Size: 16.0 MB (15964294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018aea02d181efc2628012de782477840dbfd1a7b37f851fdfbb02eafc6e4aed`  
		Last Modified: Tue, 08 Apr 2025 15:37:38 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3da470e49fb3d718624786853e9479d108eb55d1c1005c48700a31fa6cf3b4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407193297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc3e1b00d269f7d215923ef9041ab573cd1776255c8436c46daacea95257e82`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9c53dca7ad1a1783f586e5e01ac8c6a23808333e74dea8e73cb813fed1a625b5`  
		Last Modified: Tue, 08 Apr 2025 00:25:11 GMT  
		Size: 47.5 MB (47479327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffe0734c1595d1fe0c36013a6078b10a14e39d1128a06575271e9a043d41f2a`  
		Last Modified: Tue, 08 Apr 2025 01:22:05 GMT  
		Size: 24.6 MB (24613675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6508389986649aabcea20a16ac597e9453899e4f0fcdc57dab93e6abf5afec42`  
		Last Modified: Tue, 08 Apr 2025 02:18:53 GMT  
		Size: 66.5 MB (66491536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b633bfaf2a01aecf4a4abe1b4c4797e0af7e52b6d2e95f4b209b40c7e74ec5e`  
		Last Modified: Tue, 08 Apr 2025 03:35:15 GMT  
		Size: 268.6 MB (268608759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38e02e636af7c14c9fe120abd9e05bce1fb8b71ff81e2d21058cefbbf3ba4dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16040272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5d6f65b2fc0efebac95ffd4b10b0d0022912384dc0b558fceb5e41a058e00b`

```dockerfile
```

-	Layers:
	-	`sha256:e09e6ad20eb81175e6f41b35a60cd540a478532e36e928e87b8494d438db1783`  
		Last Modified: Tue, 08 Apr 2025 03:34:41 GMT  
		Size: 16.0 MB (16030064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49586466212da1f47db1733df8734603b23e88fdba70738b8e7edc345eb3de8f`  
		Last Modified: Tue, 08 Apr 2025 03:34:39 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fff22072ecb3fc36c80d99a06e0fd9bddc5b9113028bce3bc41df401a6f84bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305488157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33827ca008c24eb99cc992f0e99d6ebd59ad2b75e007a635b61ec2c8f7525aa2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1743984000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4724dabe4aa05329c356a033beb752bf4d3d8e15762c4c9025e18f8b74f6a65`  
		Last Modified: Tue, 08 Apr 2025 00:24:40 GMT  
		Size: 49.0 MB (49047465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70d32a5e527bdaaef0ef8d058290901aa64df97cc259e7f2fd2e845c51227b`  
		Last Modified: Tue, 08 Apr 2025 03:45:05 GMT  
		Size: 26.5 MB (26460166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d56a7d1628e664d6ddfb9ea04b13051b1461c586b96d98f706033c1d083c89e`  
		Last Modified: Tue, 08 Apr 2025 06:53:42 GMT  
		Size: 68.2 MB (68214289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0110a4d42dbd737f4c32b27e1fd610de3473e03b7f565b427510ce244b6981c`  
		Last Modified: Tue, 08 Apr 2025 10:06:28 GMT  
		Size: 161.8 MB (161766237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9fe0103a27bbca5bfa997c01a24576da5ca3d8afd2183333bc0b85cc52ce9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15749951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8383e798db63e5ada1494ace90e0526b032c1e34ffa8ac4884aacc73f0d9036f`

```dockerfile
```

-	Layers:
	-	`sha256:8296f6248b77255afad0519e75cc438f8ad59e6f6e2b131ff01fe2163562f0b4`  
		Last Modified: Tue, 08 Apr 2025 10:06:25 GMT  
		Size: 15.7 MB (15739775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d8e69f54828b913715b9ee388c212b18759be0a7d98a3e84a955e3e4b14cea5`  
		Last Modified: Tue, 08 Apr 2025 10:06:25 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
