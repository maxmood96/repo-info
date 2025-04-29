## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:da4dd84dce131a7963ac68066348d3dfbde7df014c2472e74021fdac5fa996e4
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
$ docker pull buildpack-deps@sha256:e1af8d0f2be9426a0efc9d89bb1b3d0718c8082e5da6a0a6b200a25838aade62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342412589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8539e092af8ac5a336aa112210c03f0142cedf9803246333455b8051f48cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15a0811b2608aa97b4e0811060ffea557de20e605122f0c38825f47469947704`  
		Last Modified: Mon, 28 Apr 2025 21:10:19 GMT  
		Size: 47.4 MB (47428611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453de73db44edcda29182f13881db794c74b0f335096c735f5f88ffb61b994b`  
		Last Modified: Tue, 29 Apr 2025 06:01:51 GMT  
		Size: 24.5 MB (24474447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e19d072d3ad687af2af376c719bde109abef8c58cb05b32faf7ed3c425f5c84`  
		Last Modified: Tue, 29 Apr 2025 06:25:46 GMT  
		Size: 65.0 MB (64956846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72658d0155477ee6c66076c216b2d65e09afe1dbd6b141146037067d358bae5f`  
		Last Modified: Tue, 29 Apr 2025 07:12:40 GMT  
		Size: 205.6 MB (205552685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:185727ddb28f05a87aeafe67e90938ebc153545b3d3f67122d00682233c66fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16626029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1baaabc9096bab365d03cb960a7cb0866d546d92fd9e506ad0c44ee5256c5fa`

```dockerfile
```

-	Layers:
	-	`sha256:e7d08eef8fd2e33c028ec2988b485b80cde9e1e40e2d24a93bbd6ad6fb9c3d4d`  
		Last Modified: Tue, 29 Apr 2025 07:12:35 GMT  
		Size: 16.6 MB (16615776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca43c275badfc699ab31134ef4e55915d96f3d3f972f31f94cd7bd5ee823f1a`  
		Last Modified: Tue, 29 Apr 2025 07:12:35 GMT  
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
$ docker pull buildpack-deps@sha256:eac77c9892db54b705c1ce2fddeee6779ac0ba9b58448167745361bd9f6a1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6669d9b184ce01a46125c23073e51f89500c0088641c1d7eb64156ffbb19b566`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed88abda34c2c7766794d61fd8b43cac1ab4eeadc9f85398417820583a09e36d`  
		Last Modified: Tue, 29 Apr 2025 07:48:18 GMT  
		Size: 27.1 MB (27143577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fa77ab766e4eed4e829b6e08390c6a1dc6b2350ee6134f9e56b8061b308247`  
		Last Modified: Tue, 29 Apr 2025 08:30:35 GMT  
		Size: 72.5 MB (72536214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d300d0e0a443859c9d7b03f2fb73f0f13dd6195fcec9f5c4253b86e2389e2`  
		Last Modified: Tue, 29 Apr 2025 09:14:32 GMT  
		Size: 231.5 MB (231452691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f7088f0c414e7d2616fcc5fd03fd38b946c914c5505c8f62aead72caa3de4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16847298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4559f7375b27f62fa96225a7f9387a170b3cec1dc7a15388578a62f7083f1bd3`

```dockerfile
```

-	Layers:
	-	`sha256:9cf7611c957561a1a046c1473cade9fdac913e91ad743ae01a90dd9e8057ee9b`  
		Last Modified: Tue, 29 Apr 2025 09:14:23 GMT  
		Size: 16.8 MB (16837073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c6275dee09a0f14bd56a0acdb4b5fcd784cc55090c50bcd9c0ec95c658872db`  
		Last Modified: Tue, 29 Apr 2025 09:14:22 GMT  
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
