## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:16eb0c0701494ae3707545d7dacd61f599175928112c92e71298d58b094cc95e
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

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:93dfadb4a9675634ed66ea064cd8e5adfcef90e61e436d9d6a3e25e1213dd76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378380292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c627e1a79701aee469df8355da2d959be77c94d201be0c69fc5de17a5957e46c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f8c8542523ef5c08ca9bd5ab7d7265d12930a45ccc7c8364e909fde03c894479`  
		Last Modified: Mon, 28 Apr 2025 21:08:35 GMT  
		Size: 49.2 MB (49248239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8723664ae2848fca92e9c796c763cdd28a6906becf75b0bfcfbb3c85be887d97`  
		Last Modified: Mon, 28 Apr 2025 21:56:17 GMT  
		Size: 25.7 MB (25744486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c56640361c19abf9b8129978ab6e07a598a9c0bf24f8542fd21b2672ca8881`  
		Last Modified: Mon, 28 Apr 2025 22:15:52 GMT  
		Size: 67.3 MB (67279216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202e99ce079b3a2d8c739815170f5b4566262430a6cd1ce2a9e2df2283f6eaf`  
		Last Modified: Mon, 28 Apr 2025 23:12:37 GMT  
		Size: 236.1 MB (236108351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6e20f2c3e9983b9d2abdd7ce33db5195ad16558747f977bdadadd40aef098d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16855306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81513547fb01b8590e52277380c341ed058ef333d3745adf967432acdea61e1a`

```dockerfile
```

-	Layers:
	-	`sha256:77317babf1c5d317de847068c1772d30d08a27ee8ab4c8b9a3d690b691879c0c`  
		Last Modified: Mon, 28 Apr 2025 23:12:33 GMT  
		Size: 16.8 MB (16845113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf60dbf8bd99ec2477ee4a2f5cb3c094457f2d7aa4c472b646df1ed28406eb0`  
		Last Modified: Mon, 28 Apr 2025 23:12:33 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

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

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:acd18a23761b2ba759047a9639493abd3133fb8840d3d1a5325e2cc382fac510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.5 MB (326510504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee067c8901b41f8180ad540673b3f936cac2f372576c211dd09be032798e1088`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7f935b3012df284a962222bcccf691a593747f69aa524b90eccdcf9bed048a7f`  
		Last Modified: Tue, 08 Apr 2025 00:26:28 GMT  
		Size: 44.0 MB (43962830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625705c4ef1fc9cf5c68338bdc47ec99f95384a22547d22ce9113fa1a4477154`  
		Last Modified: Tue, 08 Apr 2025 07:39:55 GMT  
		Size: 24.2 MB (24201775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9372173581cf51eee4c98494ac2b0977a2019e7d1175018467ee54556552146`  
		Last Modified: Tue, 08 Apr 2025 17:32:38 GMT  
		Size: 62.4 MB (62443135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0909fa1746eafd75a02b3f777f993a483ee288d5c6fb3cf4f0eb5137881b2f9`  
		Last Modified: Tue, 08 Apr 2025 20:41:13 GMT  
		Size: 195.9 MB (195902764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0af023aebe2cdaed2592878fe1b8be11f2ed3b1f96fd281e0429421e81302c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16624820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4745433c96c40901bb40f7e03c715f6a1761ab0f0a31f52e13db020b741d0acf`

```dockerfile
```

-	Layers:
	-	`sha256:bb22749e3e3bb549750cd7951720193fc99dfc8e3d8071e9e785f5ee920f4efa`  
		Last Modified: Tue, 08 Apr 2025 20:41:09 GMT  
		Size: 16.6 MB (16614567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42cc4efb6c17da1ff554923b24cfdc3969d46b7ac94c171781d5fa19e665626c`  
		Last Modified: Tue, 08 Apr 2025 20:41:08 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm64 variant v8

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

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ae088e225a35d818f2c8ed3e63991c4fbcb89f84b13c24564e2116337d701793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.0 MB (386962053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e040913ae81a4ea9eadae6fab8500534c57e478d784e4c94298c343f665036`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ed5e8397bb7752a7889fc6f59947b41ffcc3d3218435299a473ce5a254d892f0`  
		Last Modified: Mon, 28 Apr 2025 21:08:18 GMT  
		Size: 50.7 MB (50743157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec898d3c3ebd3311a66f69a4e126ef0cd8c4ca8f645a36cd5ded8a3f3b5c9e6e`  
		Last Modified: Mon, 28 Apr 2025 21:54:00 GMT  
		Size: 26.8 MB (26775040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08677a88d449eb952fa6d6174cbea68fd7c8c35b56d3c18db1886165ce9a008f`  
		Last Modified: Mon, 28 Apr 2025 22:15:25 GMT  
		Size: 69.2 MB (69194967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51ddb23b16933aca5f8d640c1b7ffed7363c5660f00cfb6cfd99181a7efbb48`  
		Last Modified: Mon, 28 Apr 2025 23:12:51 GMT  
		Size: 240.2 MB (240248889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b443d8f03ba8095215f0476bb47fbcba0020ebd9018c3f73aac450829119d2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cffa8758b43005979dbecf91b8c4584fc7f2d3e8c110c5267b69f267e7787c3`

```dockerfile
```

-	Layers:
	-	`sha256:c60168dc35fcd711d2b0fc3fe920f4388a96702b80e4190b7f52dfcc50bc5163`  
		Last Modified: Mon, 28 Apr 2025 23:12:43 GMT  
		Size: 16.8 MB (16815291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143211df77393cba5086c97314e3b23dfe26fff9d42799370f4d4128fbfe4228`  
		Last Modified: Mon, 28 Apr 2025 23:12:42 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b54d9783ab29d4f9057feeff1ca8f4f28175793d256378c739dc5702d509317a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361499012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8ef2917ec4904884c2e263c757d4785a0bc96d3bd5c5b60c1769b181a4160e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:574fdf9455a60a8eef233edb482713c5b89d1180e8a134426313714c5369a364`  
		Last Modified: Tue, 08 Apr 2025 00:25:55 GMT  
		Size: 47.8 MB (47767083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6009983b77d9776ab3b7d6cb770b45be9311a22590aa9a6de0b4730c3af4ac0e`  
		Last Modified: Tue, 08 Apr 2025 16:35:37 GMT  
		Size: 26.4 MB (26374545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158fbc6d91957d6cf889428383a76b4e5c13eb0a5c4926eedd8db6d97f12ff95`  
		Last Modified: Wed, 09 Apr 2025 00:44:49 GMT  
		Size: 66.4 MB (66404142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5882aa6977e957c0ab082f4d91b403228e49bddaf278f99de19523c5774269d`  
		Last Modified: Wed, 09 Apr 2025 08:17:16 GMT  
		Size: 221.0 MB (220953242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f6a504c2604a3d3e4d1c659c9a6ace145f1a92510cd56079ebc86744b08970b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8324643b37928a6585976b03b9f679869cbf66837f1819cd6010caa5159698b`

```dockerfile
```

-	Layers:
	-	`sha256:ce62fdc4816efdb58a082161e279bd7c805e7c9554620b646d85fe5d06268250`  
		Last Modified: Wed, 09 Apr 2025 08:16:56 GMT  
		Size: 10.0 KB (10025 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:393513935bedd7da2a8c899320d99320b25f7a22d84a2e082c62deeae9182ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.6 MB (386649538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fede2257b7c4d6b1048bdfa7486048021589f5020a490408e9f5f730239c58e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1743984000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2152bfaf5665d7c627f661d81f1ebb038ec9b798a3becef3f95f6ec6dfa2adf5`  
		Last Modified: Tue, 08 Apr 2025 00:27:27 GMT  
		Size: 51.2 MB (51205085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0924c3716841f5effee584d0edc58283639e6ed70d2000758424dcc55e8232c`  
		Last Modified: Tue, 08 Apr 2025 04:32:21 GMT  
		Size: 27.8 MB (27841786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdd195c05796e75d6c49a1674778ee5cf1851af8875fdfe4f94f09464edecba`  
		Last Modified: Tue, 08 Apr 2025 08:41:06 GMT  
		Size: 72.5 MB (72521437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed60a4a8e4d31a64d53d6596823232758a096808d0740b0de35324f97176c0`  
		Last Modified: Tue, 08 Apr 2025 15:42:35 GMT  
		Size: 235.1 MB (235081230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3d9b214e250071896515def22a04aa0d1c9977eafa13839da53e5f1c11580053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16846540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14d605b064795ead2bb637d890c74a6493b194c6c18b4bcd05f4cc050df957e`

```dockerfile
```

-	Layers:
	-	`sha256:5d49b8808d6a3702cb944f129b5b49d393e4f516958bf87d1d8b9ec34bb21357`  
		Last Modified: Tue, 08 Apr 2025 15:42:26 GMT  
		Size: 16.8 MB (16836315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41327328a2fbb37a28a4860578a43b9c07b2dbb6dfc50d339fc10ad03c8c880`  
		Last Modified: Tue, 08 Apr 2025 15:42:25 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6854d82d77e914b12de74676853f6277183f304acd645ea0081230f6cc46e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351239514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8994ed8a97ada24df9dc0e0d58ba50a5af2a8b618484e74912d69d385db68016`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2dfe09dce90ef60478379ac93bf4db4640c14411109c4ddd5060ffa49cdfa1`  
		Last Modified: Tue, 29 Apr 2025 00:02:32 GMT  
		Size: 26.9 MB (26932582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683df7242435f0ea9a0034ffcad35c09ebe0ed400dc39d5de0e749bf3bf141b1`  
		Last Modified: Tue, 29 Apr 2025 03:00:34 GMT  
		Size: 68.3 MB (68302009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e7c0cdf1713513bf973e01f68c8257ca3e8331172aebc82594e488fa6c4f4`  
		Last Modified: Tue, 29 Apr 2025 05:37:42 GMT  
		Size: 206.7 MB (206688277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98b0859ce3f551b889c4078ac3e5e24428f5bb60edfa192c866f5063a84e8301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16641018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7851ee9beefc063fbd046683349a8276da0dbdf84c1c8249095f7f9be56733cb`

```dockerfile
```

-	Layers:
	-	`sha256:c9d77e9d8706a2a507f5eb0b3501dd4c4646c58c31b661b14fec7e02afb37610`  
		Last Modified: Tue, 29 Apr 2025 05:37:39 GMT  
		Size: 16.6 MB (16630825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cdf14adabd0769365b999a4997a4ccd829c0c98f97de700b04f1d8713a835f`  
		Last Modified: Tue, 29 Apr 2025 05:37:38 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
