## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:5122c2b0acbdefe25910b2597800d625a1ac233f4b79b38c24130a70d43d7808
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

### `buildpack-deps:forky` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:88764078a4336681cb3346d738c92c74db24b66b66a46be9f23e5dbf4780a578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343220962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec93d5326324cc2a348b115b8e4942f89c2ec3a02a57a63ffdb5a78d4eac658a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:44:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c7cbbee3050ecd826301596e459f3fa12ca32f5ba2b65d33b56172341d2cd3ff`  
		Last Modified: Mon, 08 Dec 2025 22:17:14 GMT  
		Size: 48.5 MB (48512511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd84557bf7a7d4887bb1011af57bc292a828ae0385421a537869e26f5aaf10da`  
		Last Modified: Mon, 08 Dec 2025 23:07:35 GMT  
		Size: 27.2 MB (27173913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3215057bcdb48e2c916ff65379297925ae8e829013691d71877d63ff1c9875`  
		Last Modified: Tue, 09 Dec 2025 00:06:50 GMT  
		Size: 68.4 MB (68426643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903f4aa2e06e2057d89b3b646effc4a9009bb0a8bb22824be25bf3c33853409`  
		Last Modified: Tue, 09 Dec 2025 00:45:47 GMT  
		Size: 199.1 MB (199107895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43fba17ac357298143d17858497c3814b737d0de2c0060e41c5ab6d58f71d80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16277925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fcae7aa592341f0cab82dac4b95df37db1626bc806a572166f12a7d2f9a28d`

```dockerfile
```

-	Layers:
	-	`sha256:7e33c295cc76dc51de7e3606f161cd080fd2429daf339d2b7ceeef9ddf6dc48b`  
		Last Modified: Tue, 09 Dec 2025 02:21:45 GMT  
		Size: 16.3 MB (16267780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54172aeabf97b583bff2fb9c7464b8543599ba0ec63369c01775cbee7a91f321`  
		Last Modified: Tue, 09 Dec 2025 02:21:47 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b289c23247eca8173a62f3bb42af231a75f6ba42d034327914334cdb6c735ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291505528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b76d9f6781fb5b62b09679a7098cc8049ba630a9914b444cbfc9275ea9c3c86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1765152000'
# Tue, 09 Dec 2025 00:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:17:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:97c0e703f22fcbdd1717c90c9c81bde96e65c1c3051ad73d18fbc908c8b17e4d`  
		Last Modified: Mon, 08 Dec 2025 22:15:47 GMT  
		Size: 45.0 MB (45048041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b854bd09bce55cace36b7ecdbfa75886d833623af6ae1398f2375a0e142faf`  
		Last Modified: Tue, 09 Dec 2025 00:06:18 GMT  
		Size: 24.9 MB (24891051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86748a5099afd63ee13abe1176b7acb78164e7a321b3c6f806a0e35be9209643`  
		Last Modified: Tue, 09 Dec 2025 01:33:42 GMT  
		Size: 63.3 MB (63325446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c8a56f25509a07c5c5b7e6be4137e35c25462ed6b11fb133857e152db6c0dd`  
		Last Modified: Tue, 09 Dec 2025 02:18:21 GMT  
		Size: 158.2 MB (158240990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f5a8330c890eebfce4ee207e64b6fe046f6043fcf0a33f03d8fb4c4e2259e11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16033676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b312a3cc0f9ce05b5bd9a6b24749fbff5f51793751eaae89f27820762d2fedff`

```dockerfile
```

-	Layers:
	-	`sha256:4a542d885ec5b28f2a0cefb24e4f8fbd10a23c9de8e21348d6a7602138568c69`  
		Last Modified: Tue, 09 Dec 2025 05:20:47 GMT  
		Size: 16.0 MB (16023468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfdc9eed82951cb83c86625b638d40e98beda1bdf95c473a43bc8817dc058aa`  
		Last Modified: Tue, 09 Dec 2025 05:20:48 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6e0ebeac146a597b2d6524aad13de0558b362f968cbb5797c86ed891025c3a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.4 MB (332385925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83de09416ce3c823d638d0e9cb8631f0ae85d843797d0767f599d78f0a163a55`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:14:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:60db063fe1f6101cd454be84b0b672c499625ca27e05c40ddaf285db3af29997`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 48.6 MB (48599337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ca0bfa7c46cad923ad76830a45cbb46a0f64043f0882f050c618ba02ce26a2`  
		Last Modified: Mon, 08 Dec 2025 23:11:11 GMT  
		Size: 26.5 MB (26471794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbb44f039710af557b0ba0fa38e5cac191cdc4b476b1d20bccc4bfc817fec4e`  
		Last Modified: Tue, 09 Dec 2025 00:11:48 GMT  
		Size: 68.1 MB (68128153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb2a3a28958a248516a8d0648703eabee79edf8101ddcb153f61310f8a9f033`  
		Last Modified: Tue, 09 Dec 2025 01:15:45 GMT  
		Size: 189.2 MB (189186641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:04865a760414fa52ae4c352eeafe75ae197c22c5eed08364ff6f4d2241795f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16352553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5a0a3f39849d50e75e929d6d4513c7109fbd88f507338d8229e207cc1cf6bc`

```dockerfile
```

-	Layers:
	-	`sha256:42cf4f8d5cd2bdc8f7184bb30ca0e65986936c65fb4709ffd6afd319c167a73e`  
		Last Modified: Tue, 09 Dec 2025 05:21:04 GMT  
		Size: 16.3 MB (16342329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f39f81838abc6aaaf65b6bd8e5fa90050cb600afe19ba917197db09fcc7d7a82`  
		Last Modified: Tue, 09 Dec 2025 05:21:05 GMT  
		Size: 10.2 KB (10224 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7817df34ee7843d91e1bbf1a630f7491d6a0c659b3f5a049f0488619be426a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351145486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad7f6760853fbbadcd3f385d2bbaab9a728bb54018b5b27c508914e3fcee2c22`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:14:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:23:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:16:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ab10e575001e02de99efc833f717c00ab06eb63e6d406d2e8435c5550eb4b`  
		Last Modified: Mon, 08 Dec 2025 23:14:41 GMT  
		Size: 28.4 MB (28410871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb46e4ab022b5cb381fa5686d522dbfe46b1ccf9e09d5c6900981036d69143da`  
		Last Modified: Tue, 09 Dec 2025 00:24:34 GMT  
		Size: 70.4 MB (70379751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fa01fb7a7a4188633da6c11e400da82a80ec274ccef5a4117668b60d6b93b1`  
		Last Modified: Tue, 09 Dec 2025 01:19:40 GMT  
		Size: 202.5 MB (202480284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7da480c2cf0f651b20764e927e402b43be5d89a4177941db5c752443abe5d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16247667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fb8f00aa60453053f7f7e683e0e16328bb7c71e90dde8f0dc7b7168b909afd`

```dockerfile
```

-	Layers:
	-	`sha256:7fe85cd69fdd27f7fd9fa3c5ffcb9c2761e75f2fe1fd586ec52cb5213dfb94ca`  
		Last Modified: Tue, 09 Dec 2025 02:22:24 GMT  
		Size: 16.2 MB (16237544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1836e90ce8c9fc8e375fbfd9be87841dd7f7f86aa14f129750efe923abdeecd`  
		Last Modified: Tue, 09 Dec 2025 02:22:25 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:06da598fc830fef93b55da1e701e30655bd5e38cb8f4d723470b35f6519a056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348069384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23131226002a73ac8e35b3a88454c646efffad8d35af955596a0e95302880e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:30:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ca6b6474de59c13edb40994c0579d1471aee6a7743baa1f84bd96cf0fbd414da`  
		Last Modified: Mon, 08 Dec 2025 22:50:05 GMT  
		Size: 53.4 MB (53413786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16460d60e48e0172db82e752033b5336b64df38a32ba4e288da4b3068cc402ff`  
		Last Modified: Mon, 08 Dec 2025 23:21:53 GMT  
		Size: 28.9 MB (28864526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff96e6fb6ec2cfd3a984712824e772995b886f15a30aa9cd1af807a917dc615`  
		Last Modified: Tue, 09 Dec 2025 02:10:10 GMT  
		Size: 73.9 MB (73918725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b880315cf5eaec75e10d96ba6701919d98564258fcf9a603b0c818441829cfc8`  
		Last Modified: Tue, 09 Dec 2025 10:05:00 GMT  
		Size: 191.9 MB (191872347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:984087b97c358691a51f2c69598415113f1ae9f0291c8f2628f71c9d5a2e1039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16250875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754717f2e13092c441fa73adbb3ebd33e7867b250739833a54a0dcb75822049b`

```dockerfile
```

-	Layers:
	-	`sha256:d74fa394cc4acd86bf7024e421e524c247f362110bf7015dabbfc0ca5676f22c`  
		Last Modified: Tue, 09 Dec 2025 05:21:31 GMT  
		Size: 16.2 MB (16240698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8aa5f285a80173f31e107e00243d4fc8181db16a3c99bc304a2dc32dc70ced`  
		Last Modified: Tue, 09 Dec 2025 05:21:33 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:07a5079cd86b63163f526d7d6225e3bc814a772411687d3631b01bcc45dac4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.4 MB (455373372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48110a4c6f56c2ee341804a467245cc1209fbcd73c32238fbbb40e2732d8cdc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1765152000'
# Thu, 11 Dec 2025 08:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 06:01:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:002664050c13ca9d4571d9c24b2cd8235785825417d0a59db3d16cec4b277530`  
		Last Modified: Tue, 09 Dec 2025 01:49:57 GMT  
		Size: 46.8 MB (46840355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79762d676bf44b71b19af2f5e9bf3520032115760ca18d18b1e487b509a74b9a`  
		Last Modified: Thu, 11 Dec 2025 08:33:56 GMT  
		Size: 26.4 MB (26411155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899e9bcb2a2f2dedd16603a638381275feefb5833c5f56fd53977194d927e781`  
		Last Modified: Sun, 14 Dec 2025 08:38:25 GMT  
		Size: 72.4 MB (72429817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbf6f859df9d39b71e55095171de1ab0e019f15b8eea9901570eb9dcfea6a05`  
		Last Modified: Mon, 15 Dec 2025 06:18:31 GMT  
		Size: 309.7 MB (309692045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6363b6878b619892acb81b77cdc3d1580f1c00ac9125fc0aee4fc9b63e7d6e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c7f3ed34fa0d601c155980803788e85e0a63f8d846a87213b42cb02cada1dd`

```dockerfile
```

-	Layers:
	-	`sha256:f6aee94621a200712b5a2e2bb7d0fdfc2d2e326881cf10b0282f14767ec5e1d7`  
		Last Modified: Mon, 15 Dec 2025 08:20:51 GMT  
		Size: 16.3 MB (16321486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc60d85882b91adad72bdc91cb0c573612f41d7bf763ae4150f59945bac2479e`  
		Last Modified: Mon, 15 Dec 2025 08:20:52 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:13efc1a201f9c50c2a32cb79afef9a916c8bcb563d6b236414fb496a83ba96e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.3 MB (311328098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:255d6f685f7c6bac782f6306d903bdfd2a91844794c1e197e04cb72c4700b026`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1765152000'
# Tue, 09 Dec 2025 00:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:46:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:57:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:88e5ed2f2b5ebe4c22b20536e853aae0963f42dcc4ff80e14e14172e983096b3`  
		Last Modified: Mon, 08 Dec 2025 22:20:13 GMT  
		Size: 48.3 MB (48319837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d47897a01efebe9154a3fe179f72cecb78c93572d95a8b9465a3989d8d1df11`  
		Last Modified: Tue, 09 Dec 2025 00:11:09 GMT  
		Size: 28.3 MB (28292167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eaf6cdb14f443f0f3f48efe5aed619dde90987e70aea45fa92849adbe0c9f7`  
		Last Modified: Tue, 09 Dec 2025 01:46:48 GMT  
		Size: 69.1 MB (69141577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49aeb81a39c6d84662dbde6801bd3989c5e89b3d0bbb2d01adeba5425775ca7b`  
		Last Modified: Tue, 09 Dec 2025 02:58:52 GMT  
		Size: 165.6 MB (165574517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b0794f0c8d9a512caf901bb4190a42f0b105201368b9b61cff06d9fc19e45367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16043329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adca5714f126c1e853f9d3688f7fb4214739d2c063edfb523c768e0ea769180a`

```dockerfile
```

-	Layers:
	-	`sha256:2a766d2fff03868e77f5872899f35f27d76561c713f33dccfd877bff5ca00405`  
		Last Modified: Tue, 09 Dec 2025 05:21:59 GMT  
		Size: 16.0 MB (16033184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f17c6439001c6be6c657c528bec0eb7d7896b714dbefb63b890400f9f9cb75d2`  
		Last Modified: Tue, 09 Dec 2025 05:22:00 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
