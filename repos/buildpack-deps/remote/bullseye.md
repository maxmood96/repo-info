## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:73a18e0bd58bfe7c20b1ddc85989be6cb09cb988fe5582bdc977f95a9e4ceb6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7ce51cd47bb5143b23e8f783f7ef2edaf63da681f76bb8be4dbd45260196184e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321480200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788c444f2bc228f47a93af171a19f35e63d169184e67535afeb72f6b028d0053`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfa9ab09db8d94503213f634b29be3505174979f2e0c6e3fd46c2acc0716c25`  
		Last Modified: Tue, 21 Oct 2025 04:46:42 GMT  
		Size: 15.8 MB (15764056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e663cb3204c49ebc21b005f5976ee62e4f00b632aaa8000dbe6db86d9cde2a1`  
		Last Modified: Tue, 21 Oct 2025 04:47:30 GMT  
		Size: 54.8 MB (54755162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bafbf91825be17f2ceae6674de95a31e6f8a5a24c7cb95ae123d19de9c63e61`  
		Last Modified: Tue, 21 Oct 2025 10:22:52 GMT  
		Size: 197.2 MB (197204867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8950328426cf0fe12cf13e61b374abd02ef0f18b5030ab9aca31b7bc50836fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca3bf382cbc54fb9b1bfebbebbc1305ef93cdb1352c30b19d2abba786c7a5c5`

```dockerfile
```

-	Layers:
	-	`sha256:4369395cdab0f08f1a15d4786818ef3f8a00b3a7c597924908d9f09736946c0d`  
		Last Modified: Tue, 21 Oct 2025 10:20:09 GMT  
		Size: 15.5 MB (15462172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d5202b7e62ec66fcd3b38be1afa81f454fe45289f4858f17c048bc549c1fdc6`  
		Last Modified: Tue, 21 Oct 2025 10:20:10 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d1bb8389f1ce483ea6134d8f82f7284b9249125f008075c9ef897d5b9d89ad0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282530343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed698357067635b1ddb89a83ddf11967d979e008e2a1f2ea06956e277c51e68`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef331acdad14a3d1bfe859a1c645cb9f4b9526e16e3fed550eee6b86681db7`  
		Last Modified: Tue, 21 Oct 2025 06:17:35 GMT  
		Size: 168.0 MB (167976463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3368bfe50125e3bf39a5265dc0ccb9fd1b42e11bb09ee31f11cc20595deaf608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c802e9b0adbcab3d7cc2359f79d7255992840a83993df410ba77eac7e061a5f`

```dockerfile
```

-	Layers:
	-	`sha256:345b610bcc2368229c8e5fcff25890b88a7e61f829a2de5c482458c9abdb0d74`  
		Last Modified: Tue, 21 Oct 2025 07:20:07 GMT  
		Size: 15.3 MB (15261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9818b9a10921214781d18b9bbc0c05d5ef32a7135a04ba96610744d96177f36f`  
		Last Modified: Tue, 21 Oct 2025 07:20:08 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:54ebfe1e7996e94da1d4fcf99542eda3abe3216dd7aca95d5843a250a941f0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312964938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba618fb19e6cb39818578d826dc80728612abdaedade8bd90d7f60315252918`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f7bdca064e682157394f36dabd112bc9831aff9743216b035e2ccccf704cc3`  
		Last Modified: Tue, 21 Oct 2025 01:46:24 GMT  
		Size: 15.7 MB (15749510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc7a49f7691cb1ac5f0f40edbe6f4beec62021b4fd2544c431d8f694b4b4647`  
		Last Modified: Tue, 21 Oct 2025 02:35:21 GMT  
		Size: 54.9 MB (54860806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452b809e62b80ba90b1a217898e5cf7675ff6aac67b2967e58600172590649e`  
		Last Modified: Tue, 21 Oct 2025 04:14:12 GMT  
		Size: 190.1 MB (190097178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:03f0a9618331ca3a038682775295f52576c7e9bdef415e924d0a7a2566480109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15474435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0810bfb1346b9b7e2ef3a3d812a5b7fa812be9adeb5bfc03f59f733acc2234bd`

```dockerfile
```

-	Layers:
	-	`sha256:9b80d3c8a1930319785f0c4ba2dcf853a05d01d83c4b7a41507fba4e5c4f6cce`  
		Last Modified: Tue, 21 Oct 2025 10:20:31 GMT  
		Size: 15.5 MB (15464117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fc5746d3f13db63ff0f8c4db60f8e0b4c57c0f7df1d3840f3d48bfb140c2bfe`  
		Last Modified: Tue, 21 Oct 2025 10:20:32 GMT  
		Size: 10.3 KB (10318 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:daa992d47bbaa113804921dd87ee03aeb7e638d22a8c17171e3c2fb880ede885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327119404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfb82a6dae874533f7a02d6c3dc640fa9b8c6e0b5b52bdb6eeaca4297d49c95`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c453fe6b4c7a680d5464137a3450d263e01a7ec4d491659295432d36b0198bbc`  
		Last Modified: Tue, 21 Oct 2025 01:53:19 GMT  
		Size: 16.3 MB (16267847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96adc169c4af311ffba07fa68db5821d6b9b00d285e00f44dad87eff52496658`  
		Last Modified: Tue, 21 Oct 2025 02:35:42 GMT  
		Size: 56.0 MB (56048779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd845a5707f187f6670f0831bc55034f6333f3aa3eede705f688f3c3342392e`  
		Last Modified: Tue, 21 Oct 2025 04:14:36 GMT  
		Size: 200.1 MB (200103484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:10c22580082533dc9aa08cdc2f285c856e43a4a7a86edfced0f6c9378b161e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a004e4cdb6ca8ff0fdcdaf93496da3b8793b261f7c052d6ddec45d71c77f0089`

```dockerfile
```

-	Layers:
	-	`sha256:1d27735d40116266fc0859770940e133e42b3e280b9948290cca0120e11c9aa3`  
		Last Modified: Tue, 21 Oct 2025 10:20:42 GMT  
		Size: 15.5 MB (15450187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78d480c4be0c90211ab15cd8616afa30720758bf64759a06b1032efc2622a44a`  
		Last Modified: Tue, 21 Oct 2025 10:20:43 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json
