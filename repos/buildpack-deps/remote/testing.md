## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:4ac6498b5548f8d54e233f24a0959550a9ee1d848a47f88e85673f19841c5d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5bf0a8ab539a3061a177f582f83bdf81716c93e9e8e358594b1fa383d37945eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.6 MB (473577214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf40329d2a502d3632fa0677a3849e8588de21636fafc34ab4e7b544478008f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:05:18 GMT
ADD file:ec1a9a704ae13b142c48069368561119760ccdf3d65d854c426d0dc9c39e60fb in / 
# Fri, 11 Dec 2020 02:05:18 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 16:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:55:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 16:56:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:57:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e4991c356405721fc787980835bdbf5c529ae12379346a771feb34407c522bd6`  
		Last Modified: Fri, 11 Dec 2020 02:11:29 GMT  
		Size: 53.1 MB (53113553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31d9601ffb01bb76b4b0f063798a4d1ee0fd755c12d07c76aebee06efabb9ba`  
		Last Modified: Thu, 17 Dec 2020 17:23:45 GMT  
		Size: 7.9 MB (7908261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba58616c17ab814aac1a7b782186b5ce1114f80b807ec7635a3895fecec549`  
		Last Modified: Thu, 17 Dec 2020 17:23:46 GMT  
		Size: 10.6 MB (10648148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4e78a0ed9f63a0a28e8e8e899d253ff1658a5536db81e8636b4fe46a4dc490`  
		Last Modified: Thu, 17 Dec 2020 17:24:13 GMT  
		Size: 53.8 MB (53849812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362f2ecb577bfb822fd0936355d49b56df36cd774d1da27cff5164edb77c1a2e`  
		Last Modified: Thu, 17 Dec 2020 17:25:45 GMT  
		Size: 348.1 MB (348057440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7c1b4f5adcc0a6a06b80c182cb1098f6f8198d3a762d7d9bc96ca71a699bb540
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302384589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfcc33cc62602e4c18e75fa0f531ebffb3ced2ab94410974540d2c95e3f63f9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:50:29 GMT
ADD file:d4da31b3c934d9b6c8328e7951f06cec1babe1f9674a7a3ee2e87670575ff01c in / 
# Tue, 12 Jan 2021 00:50:30 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:24:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:27:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f9810833d48e3d19cbfbfb8871ba282d104d5bcfae1b19c0c003f9811dbe7c4c`  
		Last Modified: Tue, 12 Jan 2021 00:58:53 GMT  
		Size: 51.5 MB (51487444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d257fe5697f52f59aa0dbdede36db8adf4c0796905b3388832de43ac1e4ab97d`  
		Last Modified: Tue, 12 Jan 2021 01:41:45 GMT  
		Size: 7.5 MB (7527914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59bb7c72bcd7ff3df84ab37209a928574816146c37f0808619c4b5a6dde4a1`  
		Last Modified: Tue, 12 Jan 2021 01:41:45 GMT  
		Size: 10.3 MB (10335674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2064b7463d16bbcc2e8bc6d085c083e4e8d5bf88ac7a254843dc12449eaec623`  
		Last Modified: Tue, 12 Jan 2021 01:42:15 GMT  
		Size: 51.5 MB (51549893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b96292ec002aa2f69335d7a934c50886b11e8eb437c505481d1998923ea7c74`  
		Last Modified: Tue, 12 Jan 2021 01:43:14 GMT  
		Size: 181.5 MB (181483664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:351a5c6c0582ba30067abe0d39793326686b8dd7b1c068f8b30138b9820e6b09
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289712622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74eb074d50a54cda9cf29fdf1b2d4f12ca7cc8dcb8796c62a60105c1246ed89e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Jan 2021 23:59:52 GMT
ADD file:ad9ce4dd05291eba636daae5f0b9de510927734ac26dcca6940d93e88b5c5330 in / 
# Mon, 11 Jan 2021 23:59:54 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:11:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:11:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:12:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4ecb0a075e68a9a1a4b7394123b05b2811afa9bc0a23170e2e6c42d5ee19a7ac`  
		Last Modified: Tue, 12 Jan 2021 00:09:56 GMT  
		Size: 49.2 MB (49159573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dea32ec53c55b5a19d9fb093241be9ba6e2fe2fd55963111e57d39b0973f01c`  
		Last Modified: Tue, 12 Jan 2021 01:27:54 GMT  
		Size: 7.3 MB (7265094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b285ad78deb9119d75d41a2decc62fd9676078225d860eec32d20835fa7fb`  
		Last Modified: Tue, 12 Jan 2021 01:27:54 GMT  
		Size: 10.0 MB (9975049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e47a7484b9800c33e8812962a70ed0114c8572b070a16230fbfcd1c09b7a60`  
		Last Modified: Tue, 12 Jan 2021 01:28:31 GMT  
		Size: 49.6 MB (49587245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ef31ae7211e144bec0e79d33cfcb609d9bac6a1f0368146ce60b1ccee3bcf4`  
		Last Modified: Tue, 12 Jan 2021 01:29:36 GMT  
		Size: 173.7 MB (173725661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e6758e27ebe539eebfdb1e7af27b00380dbb1dfd1e73f29b46053e0901feadd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (321037802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d55ce6157b804eafe2dc59cb7c43de411e9837f0e00c349f8af4ce6e77bb6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:39:49 GMT
ADD file:0700c58361c6ae34d399d7ca2a5a6f509980a496c07d319f7455d86b483e7f25 in / 
# Tue, 12 Jan 2021 00:39:56 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:20:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:20:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:22:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1e62204d5e176f9e5ef453b346203f7bda9e22ed810a0a4e2c14548d7cc3afe`  
		Last Modified: Tue, 12 Jan 2021 00:50:17 GMT  
		Size: 52.4 MB (52428437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f37b86a934fe39fb5aebaff30977af7d0075b2eeb06b1b794582ae2566dff1`  
		Last Modified: Tue, 12 Jan 2021 01:36:53 GMT  
		Size: 7.8 MB (7840062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0908ecaa573834d3855dd61a0aabaf6565245ab200624d87774802a93f1b2dea`  
		Last Modified: Tue, 12 Jan 2021 01:36:54 GMT  
		Size: 10.7 MB (10654799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8b5a3d04882a1f9723afda0d32fb1325ffa21fe435e1088c0b1736b2ba28cc`  
		Last Modified: Tue, 12 Jan 2021 01:37:17 GMT  
		Size: 54.0 MB (53962123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae5592b7d4b54a1ed855e77b1f5d140002a31dde11ef835179bd01efe8dac5ae`  
		Last Modified: Tue, 12 Jan 2021 01:38:14 GMT  
		Size: 196.2 MB (196152381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:325d23ffdb7414599f6ac964476c3c1bdf11811fbee52cd473af0e74cc37538c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.1 MB (335111425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b83e1843dd69df65aa3c6b374f5f180e6654728ace2ee23c00a5887548c9e31`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:02:21 GMT
ADD file:b10b66385eba9f330914811c1ea9830c75a7d222442b3076a102c918588f96cc in / 
# Fri, 11 Dec 2020 02:02:22 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:06:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:06:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:06:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:08:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5cec9c367337182f351780e9e280bde357c303f0ca43358fc7dcbe63a9420fb1`  
		Last Modified: Fri, 11 Dec 2020 02:08:35 GMT  
		Size: 54.2 MB (54157004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bfed47518c0a507801e5cbe565f2d9072a66d37097eb93c108be072d452bcc7`  
		Last Modified: Thu, 17 Dec 2020 08:22:55 GMT  
		Size: 8.1 MB (8082025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c73ad66a61af03c90dfc68fd0342e7c31aede5c056cec3bb18195e6c3af97ff`  
		Last Modified: Thu, 17 Dec 2020 08:22:55 GMT  
		Size: 11.0 MB (11031118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b17636990e83105666693f7637b7aeb56bbcfc13e62b0eac8d8e8a78c158b8`  
		Last Modified: Thu, 17 Dec 2020 08:23:33 GMT  
		Size: 55.1 MB (55144761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93bce259fdca42d889bac8a282a3f05d40d562e9d840ce71381d67156e623e21`  
		Last Modified: Thu, 17 Dec 2020 08:25:10 GMT  
		Size: 206.7 MB (206696517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b063004b1efd19a5038d2d567b1840356deb2c1155c8abcf31ee753211bdf35c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308195143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e6a906b1b929635c1387f58cf4c1c2b20bbbad9efe2319acffadfe33dd15cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 01:15:12 GMT
ADD file:171276d9060030f06df201450c4356d6449f4c6a905d02db7f2371f7ed26b34d in / 
# Tue, 12 Jan 2021 01:15:13 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:45:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:49:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cdc62d8dca2f8e7c324fa9f4efc40193ada4c98be9ca6b3f1388ad903e4bd5d9`  
		Last Modified: Tue, 12 Jan 2021 01:20:56 GMT  
		Size: 52.3 MB (52264790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60b87fc90acd9bd7359cfb81de768ce7f4cdc0821db3ed523142fe855433832`  
		Last Modified: Tue, 12 Jan 2021 01:58:49 GMT  
		Size: 7.5 MB (7492735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6084ef3498948096f602b4aac1a0fb7a2dbaa7d5d751897ddec139d2cebb08f`  
		Last Modified: Tue, 12 Jan 2021 01:58:51 GMT  
		Size: 10.7 MB (10657326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d002bf71507be6bd90480c0b53df54edfde519a712016ceb3e562397e7259f42`  
		Last Modified: Tue, 12 Jan 2021 01:59:44 GMT  
		Size: 52.6 MB (52588286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c881ad6b44a52f076da88203cb158447a4f1cfe756338cf1be55d7cb50552b1a`  
		Last Modified: Tue, 12 Jan 2021 02:01:56 GMT  
		Size: 185.2 MB (185192006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b2b21bd2f597465c03101c62646325ba64499ec6f02f0ed8ea57fce10034cd6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.4 MB (471371421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03b47d0cee4c98be6ea83641ecda0b90b1a7a1c12bd9396d295ac288619595e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:31:53 GMT
ADD file:9583240ab6aa83a5f964dedeba18905486e879b1839d8329fc20f91cfccdd8d1 in / 
# Fri, 11 Dec 2020 03:32:06 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 11:15:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:17:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 11:20:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:32:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:018083dcdb1846644d37fb03ece4c9beb51dcb25f9851d01fc02f63c6fb143cc`  
		Last Modified: Fri, 11 Dec 2020 03:40:16 GMT  
		Size: 57.1 MB (57079148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0f8189a228fc57571454349d96c296688da37380e9b69091c6bee4d5f29315`  
		Last Modified: Thu, 17 Dec 2020 13:31:15 GMT  
		Size: 8.4 MB (8363474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765c21425572bad2d7f45674f0aca68f65a0064c986d32df2a8bfa1a71486b9f`  
		Last Modified: Thu, 17 Dec 2020 13:31:15 GMT  
		Size: 11.4 MB (11421266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8b746c36884ebbc3753c6b143c63c5253980af55ae64b0699e6254c39ef8cac`  
		Last Modified: Thu, 17 Dec 2020 13:32:37 GMT  
		Size: 58.1 MB (58121475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42418b22b1d1f07d78a5b2361984048835818c9ef994dcb308995e0bc5a95654`  
		Last Modified: Thu, 17 Dec 2020 13:36:57 GMT  
		Size: 336.4 MB (336386058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:443d285bc1ffb143cdb4b1f698b51a2ab9f6dcc68c57089a020df0b847c5109d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302859732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae125b81f2ed5d4c83d1accaeba68360a41f2748e68d64c705ad1e9c657cd0b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:41 GMT
ADD file:5007beabc318acc6a33d879e231105324ef7801fb709d3d69813b180e883d64f in / 
# Tue, 12 Jan 2021 00:41:44 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 02:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:07:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 02:07:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 02:09:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f1b527eede6bdcb4cce85e897c3a92fbf04bb476403758d3b535dbf6e388d192`  
		Last Modified: Tue, 12 Jan 2021 00:45:27 GMT  
		Size: 52.1 MB (52107904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f7f4dc3450e7b31e01a1746ba85df290d5b698d495c8ab448923393956e52c`  
		Last Modified: Tue, 12 Jan 2021 02:16:42 GMT  
		Size: 7.6 MB (7649499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945c37e35656a95430c56e2a6bb0a416252a37130eca65d1f3beee38efee696e`  
		Last Modified: Tue, 12 Jan 2021 02:16:42 GMT  
		Size: 10.5 MB (10525963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7df15c7e29c90193fbc5bf8d91410b9860ebc7c3975d2951c83c543f5cef88`  
		Last Modified: Tue, 12 Jan 2021 02:17:45 GMT  
		Size: 53.3 MB (53327354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c3bff3ba098dec8b91e286ffc94a19d9311b5981a74dae3dd90763f8dbe259`  
		Last Modified: Tue, 12 Jan 2021 02:19:06 GMT  
		Size: 179.2 MB (179249012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
