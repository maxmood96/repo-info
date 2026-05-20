## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:c20c05bda11f3db14ccdebdabc466244e7a7a904b77efdacd2e7ab0bdb246a83
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c7d0127b885c0e95077ef04d771430ac1f263a228a34906b3e0d34407a7c502d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.9 MB (378898367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321bfef6a28c5ebaafbdaf847031877bbc30d80969717ead6d26ff69c6baa981`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6d44b254dab2063c4226fc8a0849d5527402d24d3bea80d644a1e4ac3a47e5`  
		Last Modified: Wed, 20 May 2026 01:16:36 GMT  
		Size: 236.2 MB (236176097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0a89c4314a88896135cb743c7dc6f2edeaa7d18093c1a9a44ab9cd95fa039d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17213974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be1d383735197447d59708be5ea2f957230aa129f9bf3cb04cf54ca0aec3e58`

```dockerfile
```

-	Layers:
	-	`sha256:7d5fbfc8ed0140746e71e50b3db8d9b8032f62e79796b72a948d0cad91db30dd`  
		Last Modified: Wed, 20 May 2026 01:16:32 GMT  
		Size: 17.2 MB (17203512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12aba357160b35f53e416744f0eeaf7aa82c360b936ef6901fae551dba9610f0`  
		Last Modified: Wed, 20 May 2026 01:16:31 GMT  
		Size: 10.5 KB (10462 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b657b25501c4eba05e3ba28d2dd51a59b493012935d11628ca1bf21349ffb7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.1 MB (343081740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c5b77dfa60f59e472d65c4e519c4d251ecbc9edc50ffcaed03b9041e8e13cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:18:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:15:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6cf4508cae9439867ef520e234c0d389bafbf206c9c5e0966546716701d698c7`  
		Last Modified: Tue, 19 May 2026 22:36:48 GMT  
		Size: 47.5 MB (47488046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6871af73fc616d35749cec51e37c29aed76ddcc86d20d7f1f669b8ff2967c7e`  
		Last Modified: Tue, 19 May 2026 23:56:54 GMT  
		Size: 24.4 MB (24366903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c745eac201427a32c68c6433376345e418dca7bf01485c8f6ebcd45d9c6768fc`  
		Last Modified: Wed, 20 May 2026 01:18:34 GMT  
		Size: 65.3 MB (65335221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c30d54e413e833a421014142f9809f1abad03f09d1ea537acf6ea46589bc5b8`  
		Last Modified: Wed, 20 May 2026 02:15:50 GMT  
		Size: 205.9 MB (205891570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:904584a3919f61cfba97b83493f3b631b3a009e48fdf6e1779dca3b4b5dfd70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16976244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a097562b541af6355ad58d817743a2c6e828bfe99b1564b54e0780a0551a845`

```dockerfile
```

-	Layers:
	-	`sha256:2470db61d450d5e8b334ac97207d78029626be820f3bdf0ee398648b9f188efa`  
		Last Modified: Wed, 20 May 2026 02:15:43 GMT  
		Size: 17.0 MB (16965710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1965969ebb38841b32c34238082c541194b9eac214c307627cb1834167f51055`  
		Last Modified: Wed, 20 May 2026 02:15:43 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9461453531beec030b1883cf92d60e111dc10aaae4de0d623e85ac7898f87d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325583326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc292864bfe730df9a7b92fb14853fd491c4aab318f3b049777845cb5072c71`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:04:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:34:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:15:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a203c225dd8522bdd8715f76203677e263257613c0c04e14fd9a434bee887dba`  
		Last Modified: Wed, 20 May 2026 00:04:36 GMT  
		Size: 23.6 MB (23639255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1279ada0eefe1ba158f90c1cefb9bda61c8de2e55c4f9c92965b87f7151a892d`  
		Last Modified: Wed, 20 May 2026 01:34:53 GMT  
		Size: 62.7 MB (62740413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6302a33558dbca400d2c8d18eec519d6046916119625aeab14824af0bfc199`  
		Last Modified: Wed, 20 May 2026 02:15:39 GMT  
		Size: 193.5 MB (193461627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e54a5cc0c5ad492ef1b520ed6536a8ad25563c21e6e8d1844eaa91a87a08a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16982033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f9fbad45632049777e27a4b5cce9988bc893e19e5357021bbc607881e19a84`

```dockerfile
```

-	Layers:
	-	`sha256:0996566dc26b07790bf4cbfa56b803b640dd503c968953a56f1dc032fb49596a`  
		Last Modified: Wed, 20 May 2026 02:15:34 GMT  
		Size: 17.0 MB (16971500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c539b4c0307175c5d5f0e5dfa89bb4fc62c8a40f053ecd1c36d90ef286b1a4aa`  
		Last Modified: Wed, 20 May 2026 02:15:34 GMT  
		Size: 10.5 KB (10533 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:fb7ea5a25567fdfa855ef970b0fa771f1a58ffcc763a46f4f1e91f6c92df2a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368617432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100abc0abf216828755801095b2dcda959496502d5fda4127333fe542da812fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2882152811f66f9d033b8e9ebaa0473ab189d50d1a24186fe1ee418225e96521`  
		Last Modified: Wed, 20 May 2026 01:16:38 GMT  
		Size: 226.3 MB (226326757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a32f54f808f0b5b79bd605e05d4e44fdab27d5e3a4644f111109340f363f251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17297723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b24bb5e0b77c58ee9952aaca593703e832666d5a6baf8744636a864f044bca29`

```dockerfile
```

-	Layers:
	-	`sha256:1d32733b479581e3f76a2eed1d1bdc178e77b6cbbe9f2ece2e7c7c40e18b192d`  
		Last Modified: Wed, 20 May 2026 01:16:33 GMT  
		Size: 17.3 MB (17287169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fb6a37275b36530517a0aaa352a8e3ad372d6199ccece4c6aec314437c01273`  
		Last Modified: Wed, 20 May 2026 01:16:33 GMT  
		Size: 10.6 KB (10554 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:031a7d72def3a2137809745ccffa38b6543f4cf39884246806b423796ace6751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.7 MB (387736245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a80c6bc48ba8a0fc539f38f44c0fa666662fe80c565e3ffb01467621d3baa5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:45:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:05:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7297938c03ac6ad4e53525c3e0002337292340d300a5508ffbc391176c4868ac`  
		Last Modified: Tue, 19 May 2026 23:25:38 GMT  
		Size: 26.8 MB (26795141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6db995dae312f4650e9596da7587e265fd6b48ac92ee4cf787e012233b3a9a`  
		Last Modified: Wed, 20 May 2026 02:45:55 GMT  
		Size: 69.8 MB (69824667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75aeb0e76e4fa3105ef9199a3e7497cb44daa369da999d0374d6f497cdd6aa9a`  
		Last Modified: Wed, 20 May 2026 06:06:40 GMT  
		Size: 240.3 MB (240286883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c13da2a1b0c4c49134034e1d4c206d90053f1a4ac1e1b9d15213a8f151e51b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17183545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d51ece2c02af8c02fd6297d3f9767b764248a1cf6a5b254507a4d9d8a0ce43`

```dockerfile
```

-	Layers:
	-	`sha256:1425f7418ec0cb5c7a851fcf60bb62a8787a6825a9e20fe98ab2acbd2b341140`  
		Last Modified: Wed, 20 May 2026 06:06:35 GMT  
		Size: 17.2 MB (17173111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b3e5a93f7bd8aea2d8df62a2d01890a3062b803949d2818af4557797deb285c`  
		Last Modified: Wed, 20 May 2026 06:06:35 GMT  
		Size: 10.4 KB (10434 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d57f110de9a3876481338b598d44cfd277dbd3d160af56fdb66cd2a594a7a041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384451452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a06b9897373286f8ecb95f79a9fe02112456881a464eee20c2179a2faf79bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:28:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 06:10:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0e7e07df0234f8192ac6b8d0fa0e09c4847b899e2e0718e39e5caccda09936`  
		Last Modified: Fri, 08 May 2026 22:32:23 GMT  
		Size: 27.0 MB (27014633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227313c51a1419e3870baa3444012fd55dfddc51f3e0064592c73f0b1336a3d0`  
		Last Modified: Sat, 09 May 2026 03:29:25 GMT  
		Size: 73.0 MB (73039748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965ac950c03196998853abcfd00138afc38b3a8d8d720ffd916c9d23d9f6955`  
		Last Modified: Sat, 09 May 2026 06:12:13 GMT  
		Size: 231.3 MB (231273906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cdd12a01ee8237061946801328074af7ffe7bed76887867321b2ffada37ef417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17204871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff2ba8119efe6252ada7c66328bdaf16764b2d55e4f34dd55e4961d96af05d2`

```dockerfile
```

-	Layers:
	-	`sha256:9403efc8d3ac4540279e3fb46436a7f9f6b054b1c570b20be1b1b37da2752ea1`  
		Last Modified: Sat, 09 May 2026 06:12:07 GMT  
		Size: 17.2 MB (17194371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200114a589934afe83e45dff1548ed3effad0121107e9021891fc89f1432a444`  
		Last Modified: Sat, 09 May 2026 06:12:06 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:def3decf10759b64fceb549c7463f1e1f8c0389b939a9715611dd7f0754ea882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.5 MB (462519646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0a0f502a6f2cb4281e12b51bf975e661112e7dd6d6a7dd9bc3afd0bef7ca08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Mon, 11 May 2026 00:55:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:48:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 13 May 2026 13:25:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16def90c932096937daf06d99b8e59a8b74b84aeebf2940aac17817b2f543a80`  
		Last Modified: Fri, 08 May 2026 20:37:07 GMT  
		Size: 47.8 MB (47798394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7692e383ad230da32926d42cfa98b11eb90f51caea79109b6a826b07b59addf`  
		Last Modified: Mon, 11 May 2026 00:57:03 GMT  
		Size: 25.0 MB (24956029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04052f76d54a3689ae0d16f104df08fec9ed091da2d2a2abc27589c5c3d933e7`  
		Last Modified: Tue, 12 May 2026 00:51:38 GMT  
		Size: 66.7 MB (66663509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7b18c3a635fe2888b0e636eae8aa80e6ee1ea3df401649042b3ecc3e4966b4`  
		Last Modified: Wed, 13 May 2026 13:41:06 GMT  
		Size: 323.1 MB (323101714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ef347acea194b33be978196ac6eb4d640b55c5af20b2df44f39d31296ba87b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17275514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4179ca3320cda3f96f908e208f1e952360e7ab29959624d1f88e22b4f2cb1ad5`

```dockerfile
```

-	Layers:
	-	`sha256:4544de756b882224696e48cdc63bc577d2247874aa5e306a5f3e88818a4d5a30`  
		Last Modified: Wed, 13 May 2026 13:40:21 GMT  
		Size: 17.3 MB (17265014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e58a35be3dd4e73a6fb82b9f5ea5d22f558b5885ee7a1681dd22bc3c24d3db`  
		Last Modified: Wed, 13 May 2026 13:40:16 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3c931238e640764019311ac211c125436cfc8e46b0e5fa3d1e9e2ea18a90bd98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351503312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97658234a5436bd3bd9bdfdec03563fddcaecc46fe80222b239bcf9e812b8cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:44:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a95ac44f164c9c275ab328d3f5219a9cee0e2be081ed2ce1bb7cb8135bd49f`  
		Last Modified: Wed, 20 May 2026 00:19:10 GMT  
		Size: 26.8 MB (26804813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab366c3de62691a29444d50ed3d26e9d7524b8314a9b46521cbec555e978032`  
		Last Modified: Wed, 20 May 2026 02:06:37 GMT  
		Size: 68.6 MB (68638051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670b9b1c4f415c6933bd1559c9c20d59c3dc10986a265d1744b77a8f0cff5bf8`  
		Last Modified: Wed, 20 May 2026 02:45:35 GMT  
		Size: 206.7 MB (206680668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:32e34ab6db9e388314d8ebf7bdc7d48f90d10b93d447fbef0e8348d1af00c42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16991205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caba6feb027f6eea6feff685799493f45bcac5c4ffc20a6992dbb718aa10554d`

```dockerfile
```

-	Layers:
	-	`sha256:73388a9f6be8489ae9c9faa6ab22f3056c318cf17f48c5cb4af80093ef058324`  
		Last Modified: Wed, 20 May 2026 02:45:32 GMT  
		Size: 17.0 MB (16980745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9070406f9ce734d368d6807a8897c3805ae0faae65b982338183d40ded2459d8`  
		Last Modified: Wed, 20 May 2026 02:45:31 GMT  
		Size: 10.5 KB (10460 bytes)  
		MIME: application/vnd.in-toto+json
