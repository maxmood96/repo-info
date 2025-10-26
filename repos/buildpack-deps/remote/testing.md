## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:d02c46aa55f2bd26dda46ecfc3da2c982cd3754e6589a613b03efcd487c5bf5a
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d3d0ca3c05cbb851a8fa10c0ff66363d4835e7753aa749926eab7534d30093de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **745.7 MB (745749129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4be7b9dcf04404dd09f4c2230497fc5f2da659f3fb342072262709c2013206`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7671d30ee0069a32147537eef1beaae52a71b59148743b8ebecaf97652901808`  
		Last Modified: Tue, 21 Oct 2025 00:19:29 GMT  
		Size: 49.8 MB (49759136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c2fd0983e5dd95ff783e7a6b758ba8883a82b7e9c343a901149c14d81c6f95`  
		Last Modified: Tue, 21 Oct 2025 01:42:22 GMT  
		Size: 26.0 MB (26023893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b209652f0192a9ac0d41cdede1355372189eb2e812e9e6caeb26ec86b5ce2d9`  
		Last Modified: Tue, 21 Oct 2025 04:47:26 GMT  
		Size: 68.4 MB (68382826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131b102419d56add9676cfee379b413b99038dd941e9012af2d658e08b895bb6`  
		Last Modified: Tue, 21 Oct 2025 17:28:27 GMT  
		Size: 601.6 MB (601583274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2b5630462fb4bd06805388f8d09462669bb29e3a534faab3cad626242b7026c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16312273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e529dcce563f6ae37695e61a80e66fc94cf87aed4f221ded34c60ee51fb07536`

```dockerfile
```

-	Layers:
	-	`sha256:930c75a8e08ecc8a8f875a176842cc2b7f39ab687a0decf405d97f87ec99abee`  
		Last Modified: Tue, 21 Oct 2025 10:20:50 GMT  
		Size: 16.3 MB (16302085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e762cd4e430d68c4ac5165030adac031b95b80c08c44ca15613ace22ad32f303`  
		Last Modified: Tue, 21 Oct 2025 10:20:51 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5463b76d8886899db7739f7dbb4670213753e0980da396d1572062c3324d8917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.1 MB (677082093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45038641b04aa1733096cfe873a5b3c6d500f7ac006d3c0e77740945cb5eb00e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8d985114d6343216c46b3706ffd32abaa547ef65adf34aac773cf8677bc44aa8`  
		Last Modified: Tue, 21 Oct 2025 00:20:38 GMT  
		Size: 46.0 MB (46030435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8010abf91353efb25458a75f4596b03a8d71a09a8edd6953ba9ad16d1415cc1`  
		Last Modified: Tue, 21 Oct 2025 02:44:42 GMT  
		Size: 24.0 MB (23999710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dea2a36bd6eccf4b889c7e87442f6b3dfd31cd9edb2ccfd01a7b526586305dc`  
		Last Modified: Tue, 21 Oct 2025 04:11:18 GMT  
		Size: 63.2 MB (63238383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e3b41a5dc589adbf9ba9288cd8da305e03a79c721592900ce562593542929d`  
		Last Modified: Wed, 22 Oct 2025 05:32:29 GMT  
		Size: 543.8 MB (543813565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6129b85ea2fc95f930e375d450dc7e2cb8978e43a198b89f869d62466146304e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16070096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa31fe87dc10326494352f85a3343d5700e23c14a9b295139d9609752cac1089`

```dockerfile
```

-	Layers:
	-	`sha256:06fd42d320df9852acb30aa15979c8df2b290a47a5854966a4e813f65a9f2a66`  
		Last Modified: Tue, 21 Oct 2025 07:20:34 GMT  
		Size: 16.1 MB (16059844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17083963e7c857394f4a9f92aa0bb6ecd2d3b0447faa4c4410e556af424f2e32`  
		Last Modified: Tue, 21 Oct 2025 07:20:35 GMT  
		Size: 10.3 KB (10252 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5326245d8224f907b228d39c59828332b6a7818f5f8c535b947c520e009c2731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.4 MB (749352431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a87e58176fee775014828712af69e10b71a2bf81eabd6be3d252002e490004`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f6aed6c6f2efe803974216c59eb03806f2c41bc69dd9196f4b2f7cddd7e58f63`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 49.9 MB (49888482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11839fb5d6866dca3bea3efa274945a8c3723bf835fb6ad17497421280974470`  
		Last Modified: Tue, 21 Oct 2025 01:46:43 GMT  
		Size: 25.4 MB (25367072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f1ffac76310b47f2de8b3443ab6224819f1cad3852a8761ed742daacb7284`  
		Last Modified: Tue, 21 Oct 2025 02:35:26 GMT  
		Size: 68.1 MB (68100445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b2d5ec99679e9f82b61a4fc36c6e4d85bd59d617afec41d855e666d86ac470`  
		Last Modified: Wed, 22 Oct 2025 05:34:15 GMT  
		Size: 606.0 MB (605996432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0fc86e70324feb0f876fdfdec8cb4b8cc01755615b2cf4af4b6c73f8a59f67b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16386901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a5fb78c5fc2972745c3c314a6240130c3a4bf577b96e1788ee1f64af50d78b`

```dockerfile
```

-	Layers:
	-	`sha256:7889dd0eab0e45363ca2830d1981168b1604addcb025412414407151eb2775fe`  
		Last Modified: Tue, 21 Oct 2025 10:21:16 GMT  
		Size: 16.4 MB (16376635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:990d6e81b2df0fd5851503314aa80800b145463bb6a8fa1cdd2f1e36b7885ac6`  
		Last Modified: Tue, 21 Oct 2025 10:21:17 GMT  
		Size: 10.3 KB (10266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:61692ef457e189dc3e623bb1739506d127eab13fed72646be24e791ac0000aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **746.1 MB (746099241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a5c00afaf8ae69b8e887778fe392d341c181634ae98a1d5eb55c68054dbdee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bef87153a80d12c20903cc117b0638354009942edbd8ed3d2109a962622491ad`  
		Last Modified: Tue, 21 Oct 2025 00:21:54 GMT  
		Size: 51.1 MB (51134403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f73306b9394ed7f30a96e0fbcfc141cdabfb83109d8e85bdac496e2c9cdcf3`  
		Last Modified: Tue, 21 Oct 2025 01:53:28 GMT  
		Size: 27.2 MB (27249811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14863f4c3dd93b3b95799707d9b3e3233bf54ad0b102e7174f6505ae2c62640f`  
		Last Modified: Tue, 21 Oct 2025 02:36:23 GMT  
		Size: 70.3 MB (70309820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd9d36fe79a5cee6154ac882457957ba549425a650e2968611830fc52d72fbd`  
		Last Modified: Wed, 22 Oct 2025 05:34:05 GMT  
		Size: 597.4 MB (597405207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a1a279a9e897f788177493aecb1b6fe2c083adaf3f9644a28244420190926876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16282030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb6fc6dfb181b6bb350596e1cc61df2a853b863802714d4f1948c089ed5355d`

```dockerfile
```

-	Layers:
	-	`sha256:611793a90d92d2acd64b0078808a2e4ce6cf15d3cde7c5bf8a3847e2857de02c`  
		Last Modified: Tue, 21 Oct 2025 10:21:30 GMT  
		Size: 16.3 MB (16271864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d75748a6f60567ab6de3a34979989301c0f0679a5ac75e21902731642738368`  
		Last Modified: Tue, 21 Oct 2025 10:21:31 GMT  
		Size: 10.2 KB (10166 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eeb80dfa570df5103bc2a7b85f9a690ad4b6c744dc30b02ce29ef590273d0070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 MB (695251351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bf5991df99734dd2aa0275806d8f2b7ebf4d0b5c4376f42a9519bcc71286d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e7d4356e03351899ba9f4be32ba46e679bea4702bcfe72d9b6fe6e31094e1e6b`  
		Last Modified: Tue, 21 Oct 2025 00:20:47 GMT  
		Size: 54.9 MB (54875797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bcc30631d4ebf74056ea48897550384c1481cf43eaade92e3921cc0643a2bf`  
		Last Modified: Tue, 21 Oct 2025 07:44:17 GMT  
		Size: 27.5 MB (27478769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87a04ce21422586329cf59f62b4efbec13228e3bd60b2f1a900885826778f60`  
		Last Modified: Tue, 21 Oct 2025 17:32:33 GMT  
		Size: 73.7 MB (73699578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13b1c6fe96ded03ba62f142f974448ef1505ea0e5587fd6b8f1fa54f975800a`  
		Last Modified: Wed, 22 Oct 2025 05:33:52 GMT  
		Size: 539.2 MB (539197207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:141f814470e48d31e9249a52c07b1bf1caa3e7bebcb4cbc6835c9e3fc5e35875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16286458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bfb5c9761228f7c1801c3b0ead80a4ef0c82ec5afff4b682dd33c0ad35a8cf`

```dockerfile
```

-	Layers:
	-	`sha256:0d8be0934b536e4fec97e376c6f1ec8c6e7eb2f30ae3a15af5329ad32160f62c`  
		Last Modified: Wed, 22 Oct 2025 01:20:37 GMT  
		Size: 16.3 MB (16276238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c70e2f0e166b68604dcb0242bf8b8d2122923e7128a9dd63a033ef3cd02eeb5`  
		Last Modified: Wed, 22 Oct 2025 01:20:38 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:881bd26a38de150a5f93cc4f04d5fa860656993bd526845a3153b9abac2729ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1075336072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a6c85816df80e69b4df12979be107f3483b44a956ed93a4c28271a3d1321e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:900b76287341e8d31ab6f7e93e1704f0b3f8f921cc26e9b52c61d9ca744682fb`  
		Last Modified: Tue, 21 Oct 2025 00:21:40 GMT  
		Size: 48.0 MB (48011809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b707e625b2b66ed8212d08094e38d3d8ad6190ee6fb155233b24c4272dcc4f`  
		Last Modified: Wed, 22 Oct 2025 18:02:35 GMT  
		Size: 25.4 MB (25350235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289a49d4334af2a7114772c1c1dd72325f16c273184dbfad686587605e372ef`  
		Last Modified: Fri, 24 Oct 2025 21:19:28 GMT  
		Size: 67.2 MB (67210026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ca0b0305876a7f03a9d7ed90e068976b7df67da5099d5ef60772e031aff991`  
		Last Modified: Sun, 26 Oct 2025 11:11:24 GMT  
		Size: 934.8 MB (934764002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc5582737b758a7ca027b23d73b91d6b8085aa1aa930b1bc5055711e6d1b9dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16359069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78d8bfea2b3b24547501faa400fe1e02855ac7b08cf4892e11caea83d772fe0`

```dockerfile
```

-	Layers:
	-	`sha256:c205615429681f7dc6a8fc0dfd286e2972fe9ac84766242db2da18d4ffe171a0`  
		Last Modified: Sun, 26 Oct 2025 13:20:42 GMT  
		Size: 16.3 MB (16348849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840791d14c4b53ca708f9343f83b23aedcd8b91d640a47a003866552b0514d5e`  
		Last Modified: Sun, 26 Oct 2025 13:20:43 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a5f4ac1e99941781e12e150565494b91910b625af3b3d46f9242963ccba20528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.3 MB (648325650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1b37e122033c6adbffe3c4778b8f47117d2e5b534cf4fe0c8d6daeecb530e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4c17c2477a00887cc596493d4aa463fcafb677435d66760d41166feb0acd2773`  
		Last Modified: Tue, 21 Oct 2025 00:22:26 GMT  
		Size: 49.6 MB (49620788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fe8a7e87d33de6f27420b538e4d4def300139279c514e15386689dae092d6`  
		Last Modified: Tue, 21 Oct 2025 12:37:54 GMT  
		Size: 27.2 MB (27216829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2021b48125f7f538d074d5cee67536afd71a173bb0f5407bc24672bc22a16e47`  
		Last Modified: Tue, 21 Oct 2025 23:22:56 GMT  
		Size: 69.2 MB (69196789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a26c0835e294ae417ca3df33e1fb25eadafddd60be660cdd26ceb285160fb`  
		Last Modified: Wed, 22 Oct 2025 08:26:50 GMT  
		Size: 502.3 MB (502291244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:29eba0ccbc970c3cef69153ab79c7b70ae03678005c544e3bea21502b56824d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16078924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8c1d95a38adeb2e5a54304f0b49aadf1afafcaf1f9e7f5216e959a58a8a470`

```dockerfile
```

-	Layers:
	-	`sha256:245f5cc3e8309757c34f15bb5aff14e256f626bfe94b881bb089cb7265b4e7ce`  
		Last Modified: Wed, 22 Oct 2025 07:20:50 GMT  
		Size: 16.1 MB (16068736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e655ecf7fa57153ca4f07c971ac0d1bf7c10b84b2dcbebc450e8137b7cf259`  
		Last Modified: Wed, 22 Oct 2025 07:20:51 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json
