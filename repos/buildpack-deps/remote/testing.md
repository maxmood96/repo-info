## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:9efd42ceba6876de1bf7a54cd80cdfe2e4b4a47d4af85d0c10b7e159ad58db51
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
$ docker pull buildpack-deps@sha256:3c6c3044d9e1004e8c25b4697e63cb0c5cf0c0ff6a48e3f95ecd6b2ccdc4bca7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.4 MB (344421481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e881f9a76c38ab0d010c9ef9493facfb2824d31ce0aa658f1299bab3d1a36309`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ec645b8b1764e458ae4d21700842e441d914fd80d6e0135fa393952e129298fd`  
		Last Modified: Tue, 08 Apr 2025 00:25:30 GMT  
		Size: 45.8 MB (45786687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9068871a08a0535e32e79d1a45670b225b99f46bbc4e55433b3bc2d040fea9`  
		Last Modified: Tue, 08 Apr 2025 05:13:28 GMT  
		Size: 25.0 MB (25013942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8929ef57738cef401ed1f8ab43e4013b674116ce7a1c298b5e5cdf5147046731`  
		Last Modified: Tue, 08 Apr 2025 08:39:49 GMT  
		Size: 64.9 MB (64929330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47437fa0fb70489a1ba7f83c667f44710a761fc6e4b8952ef12d7012416b75c7`  
		Last Modified: Tue, 08 Apr 2025 10:20:47 GMT  
		Size: 208.7 MB (208691522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ac4e4eb3e329dfe0ebbdad0f957dfb61cdf5b2f7e829acca856476c397964262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16625249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce63fc072119f7dfa180e0852ba8f4e90c4e2fc8770686793757597181c3fe1d`

```dockerfile
```

-	Layers:
	-	`sha256:9cbacd0e4a962aa765ef2c3c69b1fac386c69ab9df3fc30d4c0921f9c6c3f6f6`  
		Last Modified: Tue, 08 Apr 2025 10:20:42 GMT  
		Size: 16.6 MB (16614996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d835ffc59dda7490d9b617b9b221cac39f284c5fc8055fa17d85f35961b47cf`  
		Last Modified: Tue, 08 Apr 2025 10:20:41 GMT  
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
$ docker pull buildpack-deps@sha256:737411357f64f5e11876d92b26a8bc846626513f7a011c72acfa948e87e2aff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.7 MB (370693125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d163d2201c50354755e068a9acc2c14ee54906b73d887d53579e54079cae7f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:60dbfae895846be1589b057802d5cd4dd276320555a3dce75612dc628209cb7e`  
		Last Modified: Tue, 08 Apr 2025 00:25:57 GMT  
		Size: 47.9 MB (47922433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb7cce4b3d3d4958fcc2ffe1fbbf0181efd0f5febf1b3b140f3c5fb190e3e83`  
		Last Modified: Tue, 08 Apr 2025 06:04:42 GMT  
		Size: 25.7 MB (25728139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bcad993240040602e9e9d51c79d2c2f69a2ce32db81787fed4ac65abcc1c07`  
		Last Modified: Tue, 08 Apr 2025 12:20:12 GMT  
		Size: 67.2 MB (67242386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8c2c604cdcfd0a1b9c0e89d68ad7dd4b320b921221d5283d2acb7fa3c7d135`  
		Last Modified: Tue, 08 Apr 2025 15:58:14 GMT  
		Size: 229.8 MB (229800167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:38af7862b35d0ca779d8ee9c297c9301810aa5cfce236d36c7af8fbe977552eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16940112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb9cf3e29f2b7caf1a080c5172961d18ca3a8b39558f13a1bbaee4c44aa76fb`

```dockerfile
```

-	Layers:
	-	`sha256:151242ea49c9a74da045f7cf8ac595b504521e8fdeef1f029859a2ecaaeec909`  
		Last Modified: Tue, 08 Apr 2025 15:58:10 GMT  
		Size: 16.9 MB (16929839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9786737c038dbb29da8ad330ddc8caebe48e64e000fed5bfa87001d02af4a25b`  
		Last Modified: Tue, 08 Apr 2025 15:58:10 GMT  
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
$ docker pull buildpack-deps@sha256:ececbc723723564108b58b995b1ce145ef6c68e851f6658988a238c0eef556a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.3 MB (353256466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3407c132d03e8dd4d77d6246f8c4c8fa6bae1ef718baf1084f3505e7bef725b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:19a5a2e5eb505d0c1814e6d65469ecbbf0abf7cbe214ddd85cb24c5fb088dc02`  
		Last Modified: Tue, 08 Apr 2025 00:27:13 GMT  
		Size: 47.6 MB (47577872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a838b52d3c41c71c15b487ddc0ce4cada3e3fb6a44e40511f7176fd1633521`  
		Last Modified: Tue, 08 Apr 2025 03:45:39 GMT  
		Size: 27.6 MB (27569332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c84145d0b040e4691b868f5a57cc79bd3be75960c21092b456873daf06064e`  
		Last Modified: Tue, 08 Apr 2025 06:54:37 GMT  
		Size: 68.2 MB (68220800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae90e503cb7c6551494f69bf640179b9dea08ebdb147ebabea23fddc2e51dcc`  
		Last Modified: Tue, 08 Apr 2025 10:09:55 GMT  
		Size: 209.9 MB (209888462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:79771ef4ed3cdd03c8ad046d829c3851a6fafb041f53514ac437d592687bd5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16640238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bb4bd81e0d8e2861ee7e9a62920447a1ede2ebb4dc4a716cab7047ff008060`

```dockerfile
```

-	Layers:
	-	`sha256:f70782f14275880a925625d3423895296b657cab2bb70f0b4c7672076ba2b1f7`  
		Last Modified: Tue, 08 Apr 2025 10:09:52 GMT  
		Size: 16.6 MB (16630045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f564865823d10db81631c22f4c2d4fee6bbfa4998d5ed922aa837e0aa01de8`  
		Last Modified: Tue, 08 Apr 2025 10:09:51 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
