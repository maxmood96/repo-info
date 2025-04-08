## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:466d21da69ae86c9d2b89e419f85ba9200081ae988e25bba60a3c9bb6af3bd91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:714d65d6dcb146264c5c754dc0638647d965935f788b758435d54d6b126a16c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.4 MB (380415444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a9a29f68461753943f832688217121cc3ed2477296d6b3c40ccbdfc49b1a7c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b43386f4a8eea1a35e7c4f34a0bb12426fd9b88216af22d7c3ee489419eb1bab`  
		Last Modified: Tue, 08 Apr 2025 00:23:13 GMT  
		Size: 47.5 MB (47545414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf061a9daba97c5d47244462ed42ef128857bde7ddf55699ef7e9fdc7b5705bb`  
		Last Modified: Tue, 08 Apr 2025 01:24:30 GMT  
		Size: 26.3 MB (26341855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8361b4078dfed2d0b312e243d8a8dda81b0432bf8ba1990bef58417d90eec6`  
		Last Modified: Tue, 08 Apr 2025 02:14:25 GMT  
		Size: 67.2 MB (67236723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf868a513350d48322b2a7d35490456ed2a0a824a19d9cd421eeda7bed1e7ef5`  
		Last Modified: Tue, 08 Apr 2025 03:17:06 GMT  
		Size: 239.3 MB (239291452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a0471f5f2abd3e51593cb1da3dc9dbae0ce2fa905fac04435ff809c242d23352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16855169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0292e712826ea79a7b24bd27b1f9d1b513b4443946d2ff4193bd6362c4cf21`

```dockerfile
```

-	Layers:
	-	`sha256:4d66e63870ca0c65058bb34b0ff7d4c934883a1346b86e982246b389923ecb94`  
		Last Modified: Tue, 08 Apr 2025 03:17:03 GMT  
		Size: 16.8 MB (16844976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6f8640f87963453e62d912d6c680caf129431632baef09b6fe78f583e6d6a5`  
		Last Modified: Tue, 08 Apr 2025 03:17:03 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:62f4ed8859f74593c2598cb5eed3fc0cd8aa72da0decf4d0955a9bd689d11867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354855768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0f1d470dabb961ab3be75325fe59c65dd8956b16c7ec53758404077d6d25dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:43d6e898d3a5beca16572b1a502b9433116891c583ecdbd0b66dccfd8af9e4fe`  
		Last Modified: Mon, 17 Mar 2025 22:21:05 GMT  
		Size: 45.7 MB (45737144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a0e893b154d7d5e322d742da1db8537753d0cf777b8cb73ca869670a0c807`  
		Last Modified: Tue, 18 Mar 2025 03:08:29 GMT  
		Size: 25.0 MB (24957496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86725112f5149cb61d854be49fdee119e7f61817be65303ade6d8bf0230a955`  
		Last Modified: Tue, 18 Mar 2025 05:18:53 GMT  
		Size: 64.8 MB (64765151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcb91fae58b88ab15ec7eb1f6d2556f75c522489cd5f3e67ebfd4f77bf37b15`  
		Last Modified: Tue, 18 Mar 2025 07:49:51 GMT  
		Size: 219.4 MB (219395977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69c1cf90b09348bc84d410e7a4349ef7163aaea8d2eae347e433ac9d4d249e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16627740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb51bb9bef7ad012118a6bc655f203bdca1c4db54455aa0c1b51c44c1b561e20`

```dockerfile
```

-	Layers:
	-	`sha256:f1414f287c46637f387cdfeff64c89bcddf22bc691d326dce9d76543175fde94`  
		Last Modified: Tue, 18 Mar 2025 07:49:46 GMT  
		Size: 16.6 MB (16617487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d384facb581646127c4149eede13b21772556c46072588d83605971e8cc55d`  
		Last Modified: Tue, 18 Mar 2025 07:49:45 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e948d41d8b98ec96e6fc5b01528a92385fc16ae7ef1928643f31bc40734cfb8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337106367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9ce7b04b9f7c54bd2b8c8eade952d2c559e4e5f2d39bf908c719a65ae61010`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:344116a397737c11dc2811d8baccf64c6e4150467542a11a0c5572ed1b6038c9`  
		Last Modified: Mon, 17 Mar 2025 22:21:24 GMT  
		Size: 43.9 MB (43934171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d1689e965c6a71d99b5f45c9a0e5483f83d9ca9f7db740f0b984c85e463e9c`  
		Last Modified: Tue, 18 Mar 2025 07:20:09 GMT  
		Size: 24.1 MB (24112343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6fc84037c86bb908f0e3c32b087f23cd1e04e67f611071e98457da630f4516`  
		Last Modified: Tue, 18 Mar 2025 15:33:45 GMT  
		Size: 62.3 MB (62298292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8b87c4a86f2cb48e9858bcef73a84d77e45d831a8049f1cb22daba38ab7ab`  
		Last Modified: Tue, 18 Mar 2025 16:32:56 GMT  
		Size: 206.8 MB (206761561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dfd2bb67461a38e80d403c70791fa34d4c35b6e15ed1bd9705280a5515a22f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16627319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84c1dec110d31b554e1785a4893a4fe91c6a4d20159afbe93d2dcedbc61b249`

```dockerfile
```

-	Layers:
	-	`sha256:00033bd3f9687cb4bdda9bdee459ce0d7a09b7f780557ba42dc95fab475f03b7`  
		Last Modified: Tue, 18 Mar 2025 16:32:51 GMT  
		Size: 16.6 MB (16617066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b6b6aa28af7b9f05f9a92ba3ae8b34a403033f96fd2fc8a7eae6db09cfe8462`  
		Last Modified: Tue, 18 Mar 2025 16:32:50 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f4e980f09d897376a0a5d5fd4af883334dca4fef4eabfccb3211751f246aa1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.1 MB (381086194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfc0b529ca4d96e75b234c54952b78954b2e83da03312643666817df4f00375`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f094fa2db11dac08419411aeaf2d9c561365872610ec591de05f23f2fadff3bd`  
		Last Modified: Mon, 17 Mar 2025 22:19:09 GMT  
		Size: 47.9 MB (47886359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84822f7d47020ba3b073f3f8ebb18e27a90b8e25a519c2b492131234a060ca6`  
		Last Modified: Tue, 18 Mar 2025 04:59:07 GMT  
		Size: 25.7 MB (25690430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcae46c8b749bfef6c1f2eaab2853deec3a02eb1815b00768b45dd741aa09214`  
		Last Modified: Tue, 18 Mar 2025 13:19:59 GMT  
		Size: 67.1 MB (67130545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93125d8cac1d8e5c7abb72bf5a7b7da662240c4c79d866d42fc2c723652ecb94`  
		Last Modified: Tue, 18 Mar 2025 14:41:44 GMT  
		Size: 240.4 MB (240378860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:198c4c1f1926d7edb81ec4c6d692f51532bce6bfd27f308a40d786bb97288afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16942603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb13d1a762bdaaf453a6edf58da962b5ba01cbf687b1dd8658b6596489139cb`

```dockerfile
```

-	Layers:
	-	`sha256:29fffe57dd60e26e6b68a6e4708d983bf8e0368989b8e3f8d5c5578ff215ad27`  
		Last Modified: Tue, 18 Mar 2025 14:41:39 GMT  
		Size: 16.9 MB (16932330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d121131108e502b8d85aa2964409f96f7fe652210bdd0eec9b6014a890db363`  
		Last Modified: Tue, 18 Mar 2025 14:41:38 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cf96560d178aae269f9e8150f69cd59ab2423257a2ffd07f805caa7b3b9c6fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 MB (389154773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bd71f51c8795bf647b32846691455f33295c323a42fa6fac0f59364bd5f69c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:091329a1d6a6197a5d3e206472c088a0858ef7008c0ef0caa690ee6550acc80d`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 48.9 MB (48867484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fe46607c901c693e43f5e041d9582f12c310a5a19737459269da4c901faa70`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 27.5 MB (27452280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcbd919650c8b320058909af3123af41da829ccab581f2651d0f6c59ad671d6`  
		Last Modified: Tue, 08 Apr 2025 02:13:58 GMT  
		Size: 69.2 MB (69163782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93795169e388ccd2bcfe8b4098615c124794951fbb9b521242b019448eb853a`  
		Last Modified: Tue, 08 Apr 2025 03:17:19 GMT  
		Size: 243.7 MB (243671227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6fdaef49a461317312e5026da4791c60508a8195b2432e42972e69e49856dcdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16824670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d7c260917542deef0a5c2f29f3e5193d4797418609e99063e02bb091f94472`

```dockerfile
```

-	Layers:
	-	`sha256:7b4c13980ec3d178648fd09b65a120062ceab784e023337821f85cfd151e422e`  
		Last Modified: Tue, 08 Apr 2025 03:17:14 GMT  
		Size: 16.8 MB (16814500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389a68e36b8a92fc40320311f07361c4167d70857a7c6763ebfebef1d273dfc6`  
		Last Modified: Tue, 08 Apr 2025 03:17:13 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e89526ac236ac350359c7b332fb104038e7225c6964bb9e6dbbc2801ec19d42e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.1 MB (372078206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495a9cbf46335fa6687522282cc87b58c206a0e1e00de0a7b35d910575011cbc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:46069a6fb0408c39827d84c4f957cdacbea0859425bc5cee1431cc570428f262`  
		Last Modified: Mon, 17 Mar 2025 22:19:48 GMT  
		Size: 47.7 MB (47726922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8024e8bce62fef1bb0a0244ed9a2bd73704dfdd7237b2039638682f562d4721e`  
		Last Modified: Tue, 18 Mar 2025 16:27:50 GMT  
		Size: 26.3 MB (26278793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52953f47d605c459697759af84e7c1a91c6045ad23c5d6ccb67b71684026bb6f`  
		Last Modified: Wed, 19 Mar 2025 05:44:52 GMT  
		Size: 66.2 MB (66242506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d81c1d06fd4ff3af42d1362fa9d0c2dd450468d04884561d60956ccbd9612a`  
		Last Modified: Wed, 19 Mar 2025 10:40:44 GMT  
		Size: 231.8 MB (231829985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:55db8b8b2abccf40c0b39e0efac8ead86c9459fe43987293f09dfeec4a273139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c771ff1948b074f0ac843742edebe2494f8e5e59b02b1fdbce4574cbffeb65`

```dockerfile
```

-	Layers:
	-	`sha256:1c10a8ee0eb4aa94ea3c51aee056eb45441b1987fee7aca02a0f1aa6f00f13a5`  
		Last Modified: Wed, 19 Mar 2025 10:40:23 GMT  
		Size: 10.0 KB (10026 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:993ec975a109f3c7be9e15a87f733689f6721706ba61cc766bf3781609e8ee5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.2 MB (397237514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5113331d563073d42f994aa99c913cdac631ad36ebf83bda2e1997e61a8b7f3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:895a5f19953067f7b5f8d8697fd370f37def792e6b968ea95a15dd11594bc1a6`  
		Last Modified: Mon, 17 Mar 2025 22:20:07 GMT  
		Size: 51.2 MB (51162729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aeaa0f265ddf4206f6d845d5494e3733ac72919e3d0329859f2ce1f44f19c11`  
		Last Modified: Mon, 17 Mar 2025 23:57:42 GMT  
		Size: 27.8 MB (27773366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f105bd00bb4fe66e0c28648fd8c55c5c78baf7508cbe6b000b0ec61ceebf10`  
		Last Modified: Tue, 18 Mar 2025 07:15:25 GMT  
		Size: 72.4 MB (72444096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a07cc02047648edde215f40ec250120d1433488e72d57feec3961ebf2d69ff9`  
		Last Modified: Tue, 18 Mar 2025 13:59:36 GMT  
		Size: 245.9 MB (245857323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:00fd825a9319edd4a142fa16b216d3eaa6ff350ef78ef7c12f3f62b7fedaf12f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16849071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9644987a568c1ac9e3992ef79186bcf789fe2dec5e482ec298f15fe04f6d263`

```dockerfile
```

-	Layers:
	-	`sha256:7898ead0467b4f1c77b11a027da5f91fd9b76185f69d857fe89072c480640953`  
		Last Modified: Tue, 18 Mar 2025 13:59:23 GMT  
		Size: 16.8 MB (16838846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:209f01a6348252a5049893c867d38c99b0a979258304618df2b382a8eb634395`  
		Last Modified: Tue, 18 Mar 2025 13:59:22 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:38eb0c50dbb46ac02d82917b8a6f738b4290af6090318a393f581c6e917094db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (363999107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f3cfb7a8578e4dd14f259392f5a37657235dbd750ad501a1bef2274bdf50ad`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1742169600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d25d70cc33acfbb261e54e41a50ee310f48343b555ff5a724ee79cad7214fbf`  
		Last Modified: Mon, 17 Mar 2025 22:51:24 GMT  
		Size: 47.5 MB (47548830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74e201480524a9e7f1671230b2cae3b456d6d6a91a8a4a2b07140f308c08518`  
		Last Modified: Tue, 18 Mar 2025 02:48:54 GMT  
		Size: 27.4 MB (27392489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe56110fe210f7a220bd33778fbc68a1d3b26729f0b2ea2d7d03b68e494f18f4`  
		Last Modified: Tue, 18 Mar 2025 05:57:55 GMT  
		Size: 68.1 MB (68123437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd8b3af6b24d8432ec9aae2bd7e9960e1b60e218148a064934b4b04013ac747`  
		Last Modified: Tue, 18 Mar 2025 09:31:15 GMT  
		Size: 220.9 MB (220934351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b802ca56533c24e3881b900584b15f35d29e4cc92afa86153808612f7bb4cb12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16642720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e7c86e6c699a8231da500f81de12e53ca8d8b91fd57408af020e234c21317b3`

```dockerfile
```

-	Layers:
	-	`sha256:83e8d45bf449f2d1dc038e07b8870e8e82786cf8f0af6f7e112258fd7098f74b`  
		Last Modified: Tue, 18 Mar 2025 09:31:12 GMT  
		Size: 16.6 MB (16632528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0305de3b679c464394923e2421f8f14c3bd20b4807d3818b988b43cc2bed0e5`  
		Last Modified: Tue, 18 Mar 2025 09:31:11 GMT  
		Size: 10.2 KB (10192 bytes)  
		MIME: application/vnd.in-toto+json
