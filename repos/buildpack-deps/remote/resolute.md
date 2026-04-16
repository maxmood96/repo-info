## `buildpack-deps:resolute`

```console
$ docker pull buildpack-deps@sha256:a9bddbefb775335810ae68efe4f707cc105556d775966e99014f160e63f022ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2781098695003f5cb7468fc4e480ec1190f419154a24da7e6ecbac54986d3b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290403563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb16e81be41dd97de2b9deeed70e9269c56b9c20651a0efe91aab43bcf9cda6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4430.tar --tag 26.04
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:43:09 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4430.tar
# Wed, 15 Apr 2026 20:25:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 22:14:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5f528443f34699bfec0f2308065cd6e3542906dc651e44adcbc224911a068119`  
		Last Modified: Mon, 13 Apr 2026 04:42:47 GMT  
		Size: 41.5 MB (41456182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7db96ef8a1ff29f593a12f085ddc564d16b3924f6213bb6c978b9dbe40b304`  
		Last Modified: Mon, 13 Apr 2026 04:42:50 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c119d0c66c27f7d34953d535ece957fc04cc295f72889f2b773ff2b7ce656f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:13 GMT  
		Size: 22.5 MB (22470928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e0b629e25426934d573e59d216b907cd4ca93f9451c2a889cadc5f7f1ce8c3`  
		Last Modified: Wed, 15 Apr 2026 21:27:36 GMT  
		Size: 49.4 MB (49425688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391af822daa406c82ba77fe9fe00a2b8f102f1baf042c9ed8974c29f815eaa24`  
		Last Modified: Wed, 15 Apr 2026 22:14:45 GMT  
		Size: 177.1 MB (177050373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81faf60066cd581cd6864c2354ec913cce7fdf860683e38d6c90744fb9420fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13152942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25e2603e061362380f5802e428ab5a0ed1f42271b6dbd88c25f66741fdbc4a3`

```dockerfile
```

-	Layers:
	-	`sha256:979b288ec041a7b55b134a6c885daf42791b3d975b7bc268d6ffa5ca470f03db`  
		Last Modified: Wed, 15 Apr 2026 22:14:41 GMT  
		Size: 13.1 MB (13142474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d912bbc2b075c4cf4e1bdfc4de9a9ec946a684b39f79ee1f6738fe0ce26179`  
		Last Modified: Wed, 15 Apr 2026 22:14:40 GMT  
		Size: 10.5 KB (10468 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f4aa3e7d9f768f038248f54a5011036ae4c9047413bea1657a64358bb58c2771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243598992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b4bdce48c7badb2e0ba700479f44e1a5ee5787e06bb876fd4ecc718b1b3de8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:21 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4467.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:22 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4467.tar
# Wed, 15 Apr 2026 20:16:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 22:20:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ad4da938cf0c0570f3f7d460c11d9db8ebf696978ae9b30e56bbbce569cbf516`  
		Last Modified: Mon, 13 Apr 2026 04:43:18 GMT  
		Size: 38.6 MB (38638847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86038324bc4115f9a18bd6bdea151513582b60ca3c9de1a881935f1beab04dcb`  
		Last Modified: Mon, 13 Apr 2026 04:43:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29851844ca92a399541c3a7a70f5c076de781b7bf6acd8369d547689815e304`  
		Last Modified: Wed, 15 Apr 2026 20:16:55 GMT  
		Size: 20.0 MB (20001894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ee8fd48bf93f1544ca6dc0eb0f51d4f4047c2986dbc7bb3dd7236a88ed8649`  
		Last Modified: Wed, 15 Apr 2026 21:32:49 GMT  
		Size: 52.2 MB (52248555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f191c24dcb87c59ed5b71bb79750e447e6145d1fb605164006685ef4358a995e`  
		Last Modified: Wed, 15 Apr 2026 22:21:11 GMT  
		Size: 132.7 MB (132709289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d7ae20ab238b845a1a7bdbbf86221a74d726c54407115b89c499ad8b82634b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12893895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:859c5d8f196c1a6c1f3ac8ba1b5069f8cfd75fe83b1576d03a4151f601bbe931`

```dockerfile
```

-	Layers:
	-	`sha256:826a30e8b080da4c7c2fb65834b70264982c5baa4fd010e7e0c4d600cefb6272`  
		Last Modified: Wed, 15 Apr 2026 22:21:08 GMT  
		Size: 12.9 MB (12883363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edcc884afbb5fc40638911ec358a4707c2124055a7297a80168f414532be8828`  
		Last Modified: Wed, 15 Apr 2026 22:21:07 GMT  
		Size: 10.5 KB (10532 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6ba54f0465fbf92e2401d35d3e44f1511255a51b57555fcb17f29eff4db624cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279278079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6101a09ea397aba4a8dc45a7654c67ba69375f906b6bde300624a4d10ac9910`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4512.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:27 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4512.tar
# Wed, 15 Apr 2026 20:24:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 21:36:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 22:25:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86973008df0f4d84f186cd417b697dd89ad0500783a74fbdf846af4e31defe9d`  
		Last Modified: Mon, 13 Apr 2026 04:42:57 GMT  
		Size: 40.7 MB (40683787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1d2ed58370ae479dbd99563da5d88c6adecad662d756c0dbce31ca40162b95`  
		Last Modified: Mon, 13 Apr 2026 04:43:00 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9312fd14283f97d0c5f184b060bf26f1bb507d6cfd80927c5d04bbd3cf5d9d`  
		Last Modified: Wed, 15 Apr 2026 20:24:43 GMT  
		Size: 22.4 MB (22362393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ec7c74949ed1d1147300d1277cb82b4bc3f8ceec48ec61ca2e9f0457e0449d`  
		Last Modified: Wed, 15 Apr 2026 21:36:31 GMT  
		Size: 49.0 MB (49021170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56219c4cec7fd1f2afca4e084137c0dc951500bc4fe076563bd2198e1b7753a`  
		Last Modified: Wed, 15 Apr 2026 22:25:48 GMT  
		Size: 167.2 MB (167210340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b6140a4ce72555df63831e33dac81c95dc0484048f62c711be055154d87a590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13207191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bab14bc37a4f57b352a5981e099fa45daf890502b2d149b4d48cdbbaba2c890`

```dockerfile
```

-	Layers:
	-	`sha256:f2f898213a2cb91421d3027738509355ee15179daf24068961423bf5cfb0eb28`  
		Last Modified: Wed, 15 Apr 2026 22:25:45 GMT  
		Size: 13.2 MB (13196643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec8e84242c459fba6939a3c9b2ff0335841aaa17cee118e8757d62ac739df7f`  
		Last Modified: Wed, 15 Apr 2026 22:25:44 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:342458fa0c60f37563b6169e7a00105f25c59f54a391a242a00f3f34e9469c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291790033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97703e1756f5fbe4c57f8ca38e2213be8c29169ebb5dd0d69cd827428e1e1ec9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.4420.tar --tag 26.04
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.control_data.4420.tar
# Tue, 07 Apr 2026 04:25:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:58:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 18:19:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0db7ebb2f8444a7effc07cc060085d3ebb0c3b962818809de2885138fa645def`  
		Last Modified: Sat, 04 Apr 2026 05:27:38 GMT  
		Size: 46.7 MB (46739906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250b37d4175277ba214b7494c79a05938f8c42cb3deff8c57b2eb4d7951bfbc`  
		Last Modified: Sat, 04 Apr 2026 05:27:40 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c404c821f83acd9c9ffb53162181be6e1ceab2de93b8b1a7f8de617f8c0383`  
		Last Modified: Tue, 07 Apr 2026 04:25:28 GMT  
		Size: 22.0 MB (21990388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d483f13091e34784b72a22ab7d97877821d8d9ed739fc2a369fd01b53e3d1b46`  
		Last Modified: Tue, 07 Apr 2026 09:59:00 GMT  
		Size: 55.5 MB (55466530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5fa9ec176f2ffb02251e164fea2460109a8c5b60bb5e2e51db647f2a2aba0d`  
		Last Modified: Tue, 07 Apr 2026 18:21:17 GMT  
		Size: 167.6 MB (167592818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0b2ba1f616b63e3810313a6cc465ae81aeac232089fb29f43c494f22404372f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13128776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c5ac5976d65e3ce6dab7bb72ac8f53995566461b56703d2d6ef11190a1c4b0`

```dockerfile
```

-	Layers:
	-	`sha256:0353dfa0fa4419bb02a406c556920d2a2a3212166cf8c212fbd0f7fb3c88cd1a`  
		Last Modified: Tue, 07 Apr 2026 18:21:13 GMT  
		Size: 13.1 MB (13118277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c703cbbf84c8e2baed0117a5c81b512359b8fbec52d608327013482305e624`  
		Last Modified: Tue, 07 Apr 2026 18:21:12 GMT  
		Size: 10.5 KB (10499 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8e6e98016e39f194e2f4031c6b189558b7327c68354746c9f8e6e5c1927e71a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265385198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bf34e101e4ba58a709fdc3f2bdbdd174d80713caba0dbc4ee24163d24fe4d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.4487.tar --tag 26.04
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci config
# Mon, 13 Apr 2026 03:44:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-472e35e483a575a4515eb13f3fffa1eb/images/.temp_layer.control_data.4487.tar
# Wed, 15 Apr 2026 20:43:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 15 Apr 2026 23:51:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 16 Apr 2026 00:58:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a7f3c6c466d8b59f9a103cde6bc7628a0057e9d800bfdd5f06ee656d07ed9a7`  
		Last Modified: Mon, 13 Apr 2026 04:43:37 GMT  
		Size: 41.1 MB (41145053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79f07b4f43f880fa2a19a5b25906c31b8fa10386bda422165111b0fa1f377c5`  
		Last Modified: Mon, 13 Apr 2026 04:43:39 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8ce8e664329b3e5cce2e99d01feecb396d0a720b4aadb5f84e0007779982f2`  
		Last Modified: Wed, 15 Apr 2026 20:44:03 GMT  
		Size: 22.6 MB (22597584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff452ea2b8aa8fc6b12e19cebad9c32d2a9859675517d9ef48fdedde178002d2`  
		Last Modified: Wed, 15 Apr 2026 23:51:38 GMT  
		Size: 50.6 MB (50592778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f359fa9f45405621a0d25dc9edd7a8eccf60bb88f6ffc95ddb2605602328fb`  
		Last Modified: Thu, 16 Apr 2026 00:59:52 GMT  
		Size: 151.0 MB (151049396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2de2bcb5c405c906ea1a39826ac7aa36a4dc31801c1fe20c5aa5d1c97e196e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12937288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f1f8147ce8690a62f98edae463d103c1af1b2a1075348429efe39d99c89898`

```dockerfile
```

-	Layers:
	-	`sha256:d9c27f791418d23ce8130771b44e2e4250a466390b7308dee45c0d9a15f29b6e`  
		Last Modified: Thu, 16 Apr 2026 00:59:49 GMT  
		Size: 12.9 MB (12926820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d07f63ec0e1a3bc7473dfcd57af59cb68170d83638d4245781d90a078b14f6e3`  
		Last Modified: Thu, 16 Apr 2026 00:59:49 GMT  
		Size: 10.5 KB (10468 bytes)  
		MIME: application/vnd.in-toto+json
