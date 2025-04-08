## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:344234f4589deee18e444ede62290330a5e7d062e92e3f2c7f5e8e3e383a3572
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
$ docker pull buildpack-deps@sha256:be36f78fa8d3c2ffbddd0d22b54bda77db82f550b1b7b33c8266cdde1b461826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340992555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd83f01a34e9c731c3b39c6868bc6b330050d1560e3b5871a731e0e88bcb504`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:181ed5745a356167f17446082e0f91fa4520dec07c3cc08122f73d6e68f0ec6f`  
		Last Modified: Mon, 17 Mar 2025 22:18:17 GMT  
		Size: 45.8 MB (45764033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18890e4323b22dabb2af5cd6dd6ee47e0cbe22914fe96ed5ec5652746adc9b`  
		Last Modified: Tue, 18 Mar 2025 03:09:17 GMT  
		Size: 25.0 MB (24962637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8404f8f7fc411f8ff4d9e0e372fba1e5c10c5194b11ce9185a2da79073a4ac30`  
		Last Modified: Tue, 18 Mar 2025 05:17:45 GMT  
		Size: 65.0 MB (65008424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f582acae5b75f91304b34b72f43c840e2a5f07e436f0e9a6d41fd49ee33c575`  
		Last Modified: Tue, 18 Mar 2025 07:46:58 GMT  
		Size: 205.3 MB (205257461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5c0bfd54b425c8610523669484b34cef6466db3380f8299d9f776d4fabe2e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16629074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:703f47f04cdf10c7345a742a3c45d6dad35478346fb2e1afc54559b844caedf4`

```dockerfile
```

-	Layers:
	-	`sha256:6663ae76a8fe50b96dcb176bc8671f55e4f7d7cc82e8849e08ed61ed5998f4fd`  
		Last Modified: Tue, 18 Mar 2025 07:46:54 GMT  
		Size: 16.6 MB (16618838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3c99dd9ef20911bdc5533d10ef060a796f305689df8720a1d984e915efdaa7`  
		Last Modified: Tue, 18 Mar 2025 07:46:53 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c413dfb73d37d812e369f945fe3eb52e70877f0842219dedeb0fd693a207cfe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323207909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137e16de4776efef9b6835474162cdc668da481700a979837ab1d2f452d1cad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d0067c75852db589ec6309ccaa1c2e508a0e7bb3c58863fcadae19a1c1537e18`  
		Last Modified: Mon, 17 Mar 2025 22:21:44 GMT  
		Size: 44.0 MB (43957597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80d864355272bf90fd1144966fdc99f539dd4252af76ad0a5d7e1ee868d856d`  
		Last Modified: Tue, 18 Mar 2025 07:22:02 GMT  
		Size: 24.1 MB (24132404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef046ac7256a24a47a1208d1dca17bc5d10a76b0eec3d2cd94577b18be639d4`  
		Last Modified: Tue, 18 Mar 2025 15:31:50 GMT  
		Size: 62.5 MB (62515598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe008e013fa288b0c0b7e659668cb7168447ee9f0b8e9cec325638374c6f2f99`  
		Last Modified: Tue, 18 Mar 2025 16:21:41 GMT  
		Size: 192.6 MB (192602310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:47683ecb0dd082e9a049428056b2fb871b610561995edcece07814c2380dfac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16628641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e401e6bd59ce024e1a8d8ab60668091a9da4452faec0d6dea8f53ff544710a62`

```dockerfile
```

-	Layers:
	-	`sha256:28febfa389ce6ac3f8b59d09c13755247b148ab84f11a00d726d0c7573c21d52`  
		Last Modified: Tue, 18 Mar 2025 16:21:36 GMT  
		Size: 16.6 MB (16618405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865bfe21e029a12e7aa2e50dde7163c115f3b1158dcf0dfb3ecf684d27fe13bb`  
		Last Modified: Tue, 18 Mar 2025 16:21:36 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6ea22783b50950e7a2ea2d32639243fb3820e4ee9604d4aa1a93d17f27c76327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.7 MB (367744114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72cda23af725668f03cbb96806544a7d9497d3804ae80aeddc3ac02bec4487a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:94a031aaac55d50c4495d8888a65973ac1a320a931aa0e73e9fb6cef43e2efd2`  
		Last Modified: Mon, 17 Mar 2025 22:20:15 GMT  
		Size: 47.9 MB (47916898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab9c585ccfb21ec8756fd9ca6b5b83f6e36d0003a2342f6f55b3087ee0d0f4c`  
		Last Modified: Tue, 18 Mar 2025 04:59:39 GMT  
		Size: 25.7 MB (25697882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6d5c4d521a51c32b5544ee4fd67c57ead31e48e0d9a394edb180d78318d630`  
		Last Modified: Tue, 18 Mar 2025 13:17:35 GMT  
		Size: 67.3 MB (67330212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39170df892cae0091dd72e23ef146630d9774bb93f5036c9b209b5235788849a`  
		Last Modified: Tue, 18 Mar 2025 14:38:40 GMT  
		Size: 226.8 MB (226799122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11099e4b4b75a0a776288bbb304822a79ef319800f35dca7afb0d173a2dc4512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16943937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d01eaaf8e7f1fa3f572c06f2edf18db33ca454350ba2eeb2ed779b0b2cd3b5f`

```dockerfile
```

-	Layers:
	-	`sha256:5a56a50ab788e181b17f9061cf1bad9976fc0fa2beca64efdcfc9fe20fab8a79`  
		Last Modified: Tue, 18 Mar 2025 14:38:35 GMT  
		Size: 16.9 MB (16933681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade512987613d912dc10069ccb247b43e03ec5fbb36a41f2484279df924d1135`  
		Last Modified: Tue, 18 Mar 2025 14:38:34 GMT  
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
$ docker pull buildpack-deps@sha256:63c2343097851d188b0ec81f6a553972aba44defea19638b7dd310bcd2a9d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.3 MB (358290493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267d16b8d3b132920e1dcb021538fe92b52cebd7129474c8471ad9e38553b178`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e12542a0a53bb97cc352ca7ce416a009a12137a70b8b9c3e736be4923c559ab0`  
		Last Modified: Mon, 17 Mar 2025 22:20:29 GMT  
		Size: 47.8 MB (47750847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e581beb347f24f554e5f2cf2d1525cb47adbd2ebd171f2c46bd47fada5257b`  
		Last Modified: Tue, 18 Mar 2025 16:30:23 GMT  
		Size: 26.3 MB (26282283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f3cc7353bb84ae34c688ff3596f801439d22635390e86e17ef4a03803ec818`  
		Last Modified: Wed, 19 Mar 2025 05:27:01 GMT  
		Size: 66.5 MB (66534135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6997771a7d9e486893b103ea01f09f7c8aab4497f51e63a06d87536cd35add1`  
		Last Modified: Wed, 19 Mar 2025 13:37:46 GMT  
		Size: 217.7 MB (217723228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:50810e450fb8ccae9b440dd111e2899ee812de05ae45f3c37efe7e3bc9e9569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76c84d0e7a0ca14099125937c67fb17f3ff8b4b267336c16ff85c9cda6c74c54`

```dockerfile
```

-	Layers:
	-	`sha256:bbea06d244cee2b98ff4aa2df8e7403236d91b4bb08ab453dfe4dce71862d7df`  
		Last Modified: Wed, 19 Mar 2025 13:37:27 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7ffd04fc02922cd48be44af9a83f47200796286a0a95011d4302db1dfff74ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.6 MB (382594929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a2132dd3da3db791fab5782ff3a90f1ee636fdb78a528e0df3d6eea984eb57`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4f7ad9881f20bb4c15e9c02d5c71121438e0f80af4492bc3595dca35345480d6`  
		Last Modified: Mon, 17 Mar 2025 22:22:55 GMT  
		Size: 51.2 MB (51201856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277e01a580518b309bd39ae29e17784505bd4ae5bf702764ef69018aabfb218e`  
		Last Modified: Tue, 18 Mar 2025 00:01:23 GMT  
		Size: 27.8 MB (27793733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d1b9cddd723c4c8c3ec8dc918782516b3f18afb7b43c91515f8578d7f2ee55`  
		Last Modified: Tue, 18 Mar 2025 07:11:29 GMT  
		Size: 72.7 MB (72729373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd8a8fa31bce3f93e070ba7bb6840097bf447bf40a43360ce4dd5780bb2f7fa`  
		Last Modified: Tue, 18 Mar 2025 13:55:06 GMT  
		Size: 230.9 MB (230869967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:001d25f33df3f41f03a4ffa2b1dfa76b6a6f454fd8c2089d680019e62f6968b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16850362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd1c4e5fa2a380889aefe2f6ef3c80dec596ea8c41e5222fe70849447c9d26c`

```dockerfile
```

-	Layers:
	-	`sha256:b014d9720078f0d5e2b1d52d68a0112e9fe0fe1e54ce97978cbc4cae4e6538e0`  
		Last Modified: Tue, 18 Mar 2025 13:55:01 GMT  
		Size: 16.8 MB (16840155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08af760573c8a4f30aa596b209aa6b1363368e866d28cc5a26142191af39b8a4`  
		Last Modified: Tue, 18 Mar 2025 13:55:00 GMT  
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
$ docker pull buildpack-deps@sha256:1774c4c785a4a8ff60a1cca0f8535b5ef1f0fd4508a729d948069d5dd1bcacf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.2 MB (355204087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ecacaa9f49d89f18ee6eeaf045844d3038f3f41ead448c693c268ae782f508`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18840c5918002e02a891410ac8cb796ccc166700f997d1063ab46da46dc721f8`  
		Last Modified: Mon, 17 Mar 2025 22:42:36 GMT  
		Size: 47.6 MB (47571368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d448240a5617efe437620dbc6c199b4b34036766dc8ba22365b81ef5e32d08`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 27.4 MB (27402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e745d023c42b8954a78b55b72c865750f57f9ee36521990f6f841b155c5ea`  
		Last Modified: Tue, 18 Mar 2025 05:56:55 GMT  
		Size: 68.1 MB (68118368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a34e553468bdcb19c56bf2ff84b0dbf4cc4df8dc207ed19d676a58c343c971c`  
		Last Modified: Tue, 18 Mar 2025 09:28:30 GMT  
		Size: 212.1 MB (212111659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1600e21161f75dcd5caca8e79184ff099b5c120445f56922a862a09b0ebafd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16623516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ceba67566033ed1fc7dbdbf9f9f6f1c240f9f3aebaafb82c0b49fcc78db102`

```dockerfile
```

-	Layers:
	-	`sha256:8ee0303b501d8f7d891ad1d1201308a7050e8bf3b1e0477a5af87c56384f8fa4`  
		Last Modified: Tue, 18 Mar 2025 09:28:26 GMT  
		Size: 16.6 MB (16613340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb3791f79efa336e03d9502c4b78fd4cf75bc6170d1f6bc0f2177a188663d100`  
		Last Modified: Tue, 18 Mar 2025 09:28:26 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
