## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:23edd117a48bdfe0b384de0d7fae693759fb50344e3e14a0a34e3c52e724b856
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bbac5eab6797110a4db28088a3907299f8f110eec4bd9618880e5a93635f3c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351505646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e43074bc048d073ad874f02bd4f0b346028127abb116b8b7ad758c2f267768`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:23:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7b208148f3abde07a5ac47cf579ac1ed4c9312d2ae485addb285765d8008fe12`  
		Last Modified: Tue, 07 Apr 2026 00:11:41 GMT  
		Size: 48.7 MB (48710648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7ca04ba629f5f7cdd4aa096cba4636e37f730219647da205f4cb7f89dea8d6`  
		Last Modified: Tue, 07 Apr 2026 01:47:20 GMT  
		Size: 27.0 MB (27007442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43a2cd4602dbe5429677edb66576aa077582075ca4c152b9b2df5ab5ea932b1`  
		Last Modified: Tue, 07 Apr 2026 02:43:39 GMT  
		Size: 77.2 MB (77203046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5226a7018d358491ba1d25598f22425e7cd299b57f36d3697b6b79ce6bff01`  
		Last Modified: Tue, 07 Apr 2026 03:24:11 GMT  
		Size: 198.6 MB (198584510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:66f71f24433100c9b4df8df3fd1cb7a405d1007f56de25ed78910d640e3e96ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16871307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e34b44e75587e3284d14baf8bc13e4489804c51e6b21d74b7de1b512a1181b`

```dockerfile
```

-	Layers:
	-	`sha256:4fa67d32a1a6482d6f1950347bc9d0cd684fdf99f36b83ac5f7b56d9e969601e`  
		Last Modified: Tue, 07 Apr 2026 03:24:07 GMT  
		Size: 16.9 MB (16861174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de62cdd2f1d87a5c55922987bda63a1ae092eafbc3660ea1278863718f7f787`  
		Last Modified: Tue, 07 Apr 2026 03:24:06 GMT  
		Size: 10.1 KB (10133 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2c9e82ce021ffc43fb191993b9b3c17a3664359973b562f930c63476d8033005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296618857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9831c23c249888d4967748260ba64f9fa12472dd3df028c8ddf846817d839a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:49:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:28:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d57b8f402ed3b2e5154e90fbc7b01b4f8d5c01264728a34f6ab1adc5ba51c506`  
		Last Modified: Tue, 07 Apr 2026 00:59:34 GMT  
		Size: 45.6 MB (45637964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc68b29d82a1982370d6e1b760ed4153b5652ff3b2c9443c5f434615b7c9d54`  
		Last Modified: Tue, 07 Apr 2026 02:01:52 GMT  
		Size: 24.7 MB (24691180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed91bb88c2729723f2560e1a93ed99ad38f92fe7ac00db1c9fda86e8a9585cd7`  
		Last Modified: Tue, 07 Apr 2026 03:49:53 GMT  
		Size: 71.8 MB (71757835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05dfed87a84ba0a47c1d54e7ac18241ecea09d5fdafb4aaaba008fee97cc078`  
		Last Modified: Tue, 07 Apr 2026 04:29:12 GMT  
		Size: 154.5 MB (154531878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7c653f08b241ceb7423c568e7b1c1e31d2415fc64963fca729f022d6902aee6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16626457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34f3069a238ae2ef9498c59e043461322146e2c78c1788abc7883876d8c700d`

```dockerfile
```

-	Layers:
	-	`sha256:92c4e8656af27d3f3d706d184c40ce47486d093a9c913cc9d7088a88831f09cf`  
		Last Modified: Tue, 07 Apr 2026 04:29:09 GMT  
		Size: 16.6 MB (16616260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ffe2ccead48d7ab5dd21f7b7473f1f8e67eac3250628cd83ae1c15257d01ba8`  
		Last Modified: Tue, 07 Apr 2026 04:29:08 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c0bae3b2732ae70b8d0136bf00529c3cd1ecec8ad3a2f7e7f65e44ccd6ec0d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339517369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b47a7e86b127ceced2e6b08d5f794d45348f2e3226b84ac1c535d02060d06b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:50:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:53:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:35:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ac9c76c00b1b19d9057c64eebc87efd57976d9d3d4373752703081335cbb1900`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 48.7 MB (48744945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82fc2e1b0c8b2b1d04da85219313625f50f9cb567044095b396e8e551b7fb8e`  
		Last Modified: Tue, 07 Apr 2026 01:50:20 GMT  
		Size: 26.3 MB (26299257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d915e03ded5c2c7c26b7a49eca7961b13f6f8992577033ae02b2fd04da5a207`  
		Last Modified: Tue, 07 Apr 2026 02:54:02 GMT  
		Size: 76.4 MB (76444966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904f88d7626de1f9b9102cc5c127ba28dabf860b55637e7c4796be16b7d4999f`  
		Last Modified: Tue, 07 Apr 2026 03:36:03 GMT  
		Size: 188.0 MB (188028201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:04b723af97ef49e71fa2d1615ca59593d84d12cc48507071648fc5cc22bb76b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16953773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b27f42385a70d34eefa71b96ef6206eef75cfe852c9a30d241e7b1dd9e773f`

```dockerfile
```

-	Layers:
	-	`sha256:91ecbca02a458f33a8fc374c2275ad077536a2f5c0256b57f4c61d5c1d947fbb`  
		Last Modified: Tue, 07 Apr 2026 03:36:00 GMT  
		Size: 16.9 MB (16943560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958e3093e6a0dbafa5a28dc90dd1c2b29dd011afff3dae147312126dc5b1c2c6`  
		Last Modified: Tue, 07 Apr 2026 03:35:59 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5b5e2ff338c1d962a606acc37c77cdcc8ed52240119c2432efbaaac52a8467f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359097363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fa319444fe783fcdfc4ef6c8e95e5edca41c9ff62369c12741b5777e2525b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:46:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:41:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:19:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c9bb2730bc0ff710016a40d05d0bbd6ab5db1f6ed39dbb5569902bdddb97cb`  
		Last Modified: Tue, 07 Apr 2026 01:46:36 GMT  
		Size: 28.3 MB (28287053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61d37ae8d9569041f72a5d94976af076721a00ef2857d8844925e31d049b859`  
		Last Modified: Tue, 07 Apr 2026 02:41:38 GMT  
		Size: 79.3 MB (79338598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f118897ad1cad22ffbc07eea21e56c9dba3b363c220c4464bc468f0a8ca57`  
		Last Modified: Tue, 07 Apr 2026 03:20:26 GMT  
		Size: 201.5 MB (201478001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:404f5ba49f9f83d56221fb27fe93f99874d8d49645a551cee354c4c8fad2d14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16840346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d574dbaf89cdece4e7639c1619f2343892105df4dcbbf6385373e3372ed8b3e`

```dockerfile
```

-	Layers:
	-	`sha256:6d9cd8bf765f1501d02a3a65b3da8023e2e905676753e0c3fa68c8056094d8c1`  
		Last Modified: Tue, 07 Apr 2026 03:20:22 GMT  
		Size: 16.8 MB (16830235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27a2e8d90b3967baa2c7dda33c2a3f6daa8384395974fc330119e74c774414ee`  
		Last Modified: Tue, 07 Apr 2026 03:20:22 GMT  
		Size: 10.1 KB (10111 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5b4928f1105718f64d49f9260f5415c04f48e2848e6adaebb1d31210d3388a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.4 MB (359422699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c2e9ea180a08bf5af2e4619f028260b45ac483c7c14e33810a4ad0457f2dfb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 04:22:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:53:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:12:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8091a6b5ece83586bfb56b6975e0b2d9bc01c78d84b526c5c6e82463bb755232`  
		Last Modified: Tue, 07 Apr 2026 00:11:11 GMT  
		Size: 54.0 MB (54001950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3485868c65e901d140674210bf2ba257ab5ac6120dded36f6536c4e9c5178623`  
		Last Modified: Tue, 07 Apr 2026 04:23:16 GMT  
		Size: 29.4 MB (29412504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03748ec5472f740753f922099fd48a5c13afbc87f15362a543b090bfa949e6b`  
		Last Modified: Tue, 07 Apr 2026 09:54:16 GMT  
		Size: 83.8 MB (83763893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025c0f95360ce011930b4e5c1251aeb95e6c660c0d7b16f1d863f0eafd278973`  
		Last Modified: Tue, 07 Apr 2026 18:13:31 GMT  
		Size: 192.2 MB (192244352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:345757d37078fa63d220123f94d68fcc0541df3ef22d308f0be804723aa7bbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16822158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe77bf335dce5b86cbe64059d459156489df4421f9757460e78556650f452e1`

```dockerfile
```

-	Layers:
	-	`sha256:7a35b258e2d74022d399695e9b9af36615073df88ac09d4559ae159c991d8e89`  
		Last Modified: Tue, 07 Apr 2026 18:13:27 GMT  
		Size: 16.8 MB (16811993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c538a50620f49b50785bc27c82f4b203287063a9d8351a4dda04b7fbee4425c9`  
		Last Modified: Tue, 07 Apr 2026 18:13:26 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9e9527fad919a5683e5bed2111af55fb006fbb41a3a3888fe9aed7701b874aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.7 MB (468695189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6092a153d9a8284bd1b9ce035258f18967661bafe1b12143f28fa3920b1c09`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:30:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 18 Mar 2026 05:05:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 21 Mar 2026 12:24:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:841ba95affedab9f4249c4c606ebf4cc415dddd1f44cb3edeed8f5199c8d1168`  
		Last Modified: Mon, 16 Mar 2026 21:58:56 GMT  
		Size: 46.8 MB (46778346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550401bf99e797417727d38582b31e96ea6704ee9ebdabb221407d77e3831412`  
		Last Modified: Mon, 16 Mar 2026 22:32:13 GMT  
		Size: 26.6 MB (26605431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdaf4a15ff63babbdd5aa39bbde071d09f4e73afdb49d2a8a0f3a168053ba41`  
		Last Modified: Wed, 18 Mar 2026 05:09:48 GMT  
		Size: 75.5 MB (75472808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebf6e45766220ec35d578176627583919db350cbb7288ae90a2b6d66bdabb17`  
		Last Modified: Sat, 21 Mar 2026 12:40:08 GMT  
		Size: 319.8 MB (319838604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f44ca11a069a9ccc4f78b9058a9d3617dd8312d0f4ed16d5ab36fa9e4d0718e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16890604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb13d2071ef738f8387e2e186646266cf16024c71c90c111433c27a9c9821a5`

```dockerfile
```

-	Layers:
	-	`sha256:00cd2a8295eeec95bc30d93ffa9233cf59dd77630b17be58352a72729a1b0926`  
		Last Modified: Sat, 21 Mar 2026 12:39:21 GMT  
		Size: 16.9 MB (16880439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb0e623af96ebc530be224814442a6214d6db570c43bd16c68765b55c99b5f3`  
		Last Modified: Sat, 21 Mar 2026 12:39:16 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b0992a25762c699266b7f8e25dd5d74e20bd5de191980b636503983777c5244e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.1 MB (324061037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d03c7ebdbd2ecab99fedcb63e3ced5b6517b08ec94c339e0be655e56da0fed1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 03:05:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 06:00:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f4e3a27ede4ed598ceeca73aae5842ded1c7c01f18c06d6c08d11ba5ee2f57e`  
		Last Modified: Tue, 07 Apr 2026 00:12:04 GMT  
		Size: 48.4 MB (48425378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3603919d864d726efd51563d3638c0f58e2671f83ef3d775155f64a94b910d45`  
		Last Modified: Tue, 07 Apr 2026 03:05:17 GMT  
		Size: 26.8 MB (26795763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae2afc6f5b4c5dd73680a5531235390e280e79ddf6ea03c9527bb4f35951d71`  
		Last Modified: Tue, 07 Apr 2026 04:55:17 GMT  
		Size: 77.7 MB (77717531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad6cb06f53e66da0009e766994bcd14606d4553c79c26dbff4c59333828f219`  
		Last Modified: Tue, 07 Apr 2026 06:01:09 GMT  
		Size: 171.1 MB (171122365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:434b7d8c4eda503143b939c4a4b3f7013d4c581f167b402a8b0ed71964cf6356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16626229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a226e17b86fda26d07c1a446dbd8b9238a6956fe89cebc3cd0c22129e675e87`

```dockerfile
```

-	Layers:
	-	`sha256:a6bb1ad1279f9fbac1e02b5de48e1000cf7d126dae9bb8a40f15bbfbba8f37dc`  
		Last Modified: Tue, 07 Apr 2026 06:01:05 GMT  
		Size: 16.6 MB (16616097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534a1d3fe41475e38271409594c13a7de2a7dffdcddf1ac6f2e1dfd53319ee8b`  
		Last Modified: Tue, 07 Apr 2026 06:01:04 GMT  
		Size: 10.1 KB (10132 bytes)  
		MIME: application/vnd.in-toto+json
