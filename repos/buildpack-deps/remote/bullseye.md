## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:e1054277a4b79ee5e986f035f143e7b9dbd3a904aa05e146cf923ac28e2cbfc0
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
$ docker pull buildpack-deps@sha256:94af30e4fa8fc36d343d3068df7f4efca85d0689bd1c3f003eb6afa2ba8302c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.3 MB (323266908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb58058885a7ad019ca5028096650773f07325e333f8c6a76b85d150f32e1f7a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:19:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:34:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfe71fa68737bfefafea69e4a0c5b69941285043380076279a4d65e82b5973e`  
		Last Modified: Tue, 24 Feb 2026 19:19:14 GMT  
		Size: 15.8 MB (15790747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cafa00cf3a9efb63d5aec84c5357f82990b3f70ca32d8a41f639c98f03b27f20`  
		Last Modified: Tue, 24 Feb 2026 20:04:11 GMT  
		Size: 54.8 MB (54760461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61055c62b574d5a6764367e9fbc48e9e83de485bf37a6ef2da4e942dbdce75a`  
		Last Modified: Tue, 24 Feb 2026 20:35:36 GMT  
		Size: 199.0 MB (198959266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49e248b944c165c32e15618c7bf08cc82693054ab8eab04c650f5c172208167b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f10b669a7b6178a3370b045179843acf9e1856e8c3c7cb33c438afad5c3965`

```dockerfile
```

-	Layers:
	-	`sha256:2e25cfb6553f216d9e3587e6445abec3a595931a88582b17c9147163b5291256`  
		Last Modified: Tue, 24 Feb 2026 20:35:33 GMT  
		Size: 15.5 MB (15471443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd00c5558fc825957cf0e38546916b56e23566298575d53f8c982cc7930d79b6`  
		Last Modified: Tue, 24 Feb 2026 20:35:32 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:492f2ab0834ddf08a5b06e3036699d1fc369f24de758053e350ec0a2fa08c8fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283616657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8607084970a123f85c26695d9be8bc86b0746dac375a346388cd772aaabe96a5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 20:02:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:16:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dada255a3ad6614e8b2a389545f0625a8ca4a68f069cd24789cbdcf7a89bee05`  
		Last Modified: Tue, 24 Feb 2026 18:42:25 GMT  
		Size: 49.0 MB (49047560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6350b59ed962425f695241e787bf8023af23ee4d06b078f82307ec998a697a`  
		Last Modified: Tue, 24 Feb 2026 20:02:14 GMT  
		Size: 14.9 MB (14905114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b78c92b47a812d57f4809800124de840b8b33ed15c020f80d518d0739cea99e`  
		Last Modified: Tue, 24 Feb 2026 21:34:53 GMT  
		Size: 50.6 MB (50640980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cabd4cc6124d026543ef3bc942cfd6a1e8e52efae6eb953a56f43b14dd27920`  
		Last Modified: Tue, 24 Feb 2026 22:17:03 GMT  
		Size: 169.0 MB (169023003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c502ae2a327e05b0f21402a71cfbc253cbc5d3e9d181c22d34271cfacb677b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd5cea93c62d93e676d01e847a31e6e7f21529d7a2abf86042bafbf555eb0c7`

```dockerfile
```

-	Layers:
	-	`sha256:df116499ebfc93294767781e425cfff1a201013bb36981850d55923e90747527`  
		Last Modified: Tue, 24 Feb 2026 22:17:00 GMT  
		Size: 15.3 MB (15270761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900a45dcea06e1ff88689bdaff4d90d158543538c2f83447a74b1eba7989e6f5`  
		Last Modified: Tue, 24 Feb 2026 22:16:59 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:398b7c9d8db03e844c481b5786a0ae4693abe2ac7dc1fe8006765ad57e221455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314654365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70e81108587ad6d8bff4abd109cf009e9a6a1ef4a16c1b3a9298bd9094126efa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:24:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:29:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6dd0e9da832194c696500da7078d1cd12126c89f2a0283b7c424f7ffb55413`  
		Last Modified: Tue, 24 Feb 2026 19:24:15 GMT  
		Size: 15.8 MB (15774813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f5bc11f4eeb73c577f8942878489898f3a73ef826300ec26a1880e09111671`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 54.9 MB (54875024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e83f5b87fb152518aa5916bb3aa67936a7d3549b173ca944d7d97eda45e483`  
		Last Modified: Tue, 24 Feb 2026 21:29:57 GMT  
		Size: 191.7 MB (191746136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a54844e22593ab160f3a4b1921f2c15effaf74213a847988a75c94539fb8af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c675a38295f4f835f3174e814430191984730fbe458e22d70d077ec5eb8613c6`

```dockerfile
```

-	Layers:
	-	`sha256:f5903f0f87a50f5f24b5544869bc06aab1df2337957c6a41679d19751111957e`  
		Last Modified: Tue, 24 Feb 2026 21:29:49 GMT  
		Size: 15.5 MB (15473388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485222901bd3e52f111c6d7ba22eb00f07869115fa0de23402bdda6e43514996`  
		Last Modified: Tue, 24 Feb 2026 21:29:48 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cdee3c27c36c84ad0d8d5989e2387327b07b4af1c3193bb326a1669a93795944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.9 MB (328919386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00523f9bb01db304b0ef6ebed15a4adb2e0a93c566682085ba3b897134263b0d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:be7de57c5a292b6137b558f622789891088c38f02c67ce301a1559809fbe8ae2`  
		Last Modified: Tue, 24 Feb 2026 18:42:22 GMT  
		Size: 54.7 MB (54699784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0ba919300e8846f159f61d3dad9bc45f102d2250de1dac9da8674f83e4e628`  
		Last Modified: Tue, 24 Feb 2026 19:24:44 GMT  
		Size: 16.3 MB (16295541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c2152f88d25aaccd0c582b343220b4ec754827f272c5f5df677301ccd082aa`  
		Last Modified: Tue, 24 Feb 2026 19:57:01 GMT  
		Size: 56.1 MB (56059516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6625ec994fabcd7117e021e5be81d2a5a9ea5e5d29586c9171c29085646c2474`  
		Last Modified: Tue, 24 Feb 2026 20:19:35 GMT  
		Size: 201.9 MB (201864545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88bc85a43346cef8ed6e45c6dbd1d390f4827044efb962d7c77fa714f0a35bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4e5b082f3bb4c45572ef742eb11a7090fd7e2b7fd0c7f4cc9ff39a09df3a3a`

```dockerfile
```

-	Layers:
	-	`sha256:89f1082ad0ba92665d63761965989c247ec11619a99c7b1b085582303fbf092d`  
		Last Modified: Tue, 24 Feb 2026 20:19:30 GMT  
		Size: 15.5 MB (15459458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce9a5b0b4042abf1fcce1c703bdf8149dcdb9ed2fa6d413c87e0152663cc4c66`  
		Last Modified: Tue, 24 Feb 2026 20:19:30 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
