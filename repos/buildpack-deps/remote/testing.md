## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:581288815ddcd6f5e2e57f2e2ab5cb32783e74c6b9ac570a61373fd5d5236e16
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
$ docker pull buildpack-deps@sha256:9b5784205a1c8fac24de4789208a7bbe33da50ca974dd15e9c6fad0aacb4a7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343627095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709160774b3793ca293855123892313f45342efdbeb707ec1ac3b023e1beb3e9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a5d3d8f7f036c72a68099d4e5f2152d5ebac52f060fec3d2009131f12e2ee6`  
		Last Modified: Tue, 04 Nov 2025 00:28:30 GMT  
		Size: 27.2 MB (27194469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fa7289d9c2385034e2bef8c2d8440132ab102f8472020015b0d26d75a15788`  
		Last Modified: Tue, 04 Nov 2025 04:14:50 GMT  
		Size: 68.4 MB (68443347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762ed0b206dcf709064acc85efd51762b342b9c08ca8b60ffa9148900c21a4e6`  
		Last Modified: Tue, 04 Nov 2025 14:29:12 GMT  
		Size: 199.5 MB (199507915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c53c1e86bbcc881e6c77f5dc4dc943fc8bfcca5b52224df5953f809ee7f00919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16262983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c62d7fa1601a05b4cb41f8472b97382a8cdf4793aa84be4cf034b1e6e84a20`

```dockerfile
```

-	Layers:
	-	`sha256:6959321bff2b1485f8fed332cfb657c928e35d334050ffdfe89f88608d1f386a`  
		Last Modified: Tue, 04 Nov 2025 11:21:16 GMT  
		Size: 16.3 MB (16252838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f81106108e1a1b4cfdbe2fe0181b4178c8e0584d0727847298b9e86bf757409`  
		Last Modified: Tue, 04 Nov 2025 11:21:17 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:41b4680dba08ee5a9c065f037606fa86662abe1908ccc441796e2ff95437e9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291474151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f544d724c61e5a226eccc2520a37442bf55466852471f0c151a5589301df8a81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:58:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:22:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1dd1fa3a56d87bf4dcae80a33b02589ad31d81e866bca9f061ada67db33c8854`  
		Last Modified: Tue, 18 Nov 2025 01:12:58 GMT  
		Size: 45.0 MB (45003762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6f4451a2be0f51c6d1714f46485883bd5db54f8b6d9217e249d632dee61a5d`  
		Last Modified: Tue, 18 Nov 2025 03:59:12 GMT  
		Size: 24.9 MB (24945403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e16a5a4071f52927a7f28d9d0587c256392be28c985fb8945c4f1d6790bca96`  
		Last Modified: Tue, 18 Nov 2025 05:28:19 GMT  
		Size: 63.3 MB (63308752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cbe5c11882528e8f9627e30208203a19d58c8da1755066a995908bfead1e66`  
		Last Modified: Tue, 18 Nov 2025 06:23:29 GMT  
		Size: 158.2 MB (158216234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ad7538cc80c3f08de34467d17ec74f1bb4773271874a25a8f1bdbf899fde8c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16019141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297ea6b8f073ce53515a4bc042d3c782f47c2ef46958c0b4ba568ec3c7e1495`

```dockerfile
```

-	Layers:
	-	`sha256:3bec70ab8801ea2d5ac8440779cbdca55495b13ff32f95131ae60a0e1eba656d`  
		Last Modified: Tue, 18 Nov 2025 08:21:22 GMT  
		Size: 16.0 MB (16008932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c54f300edca5a0f2d5926e6a07a200c66ad69af8df767d48c9067d6b19788e88`  
		Last Modified: Tue, 18 Nov 2025 08:21:23 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:1776c548eeabcb2088d0907306330c6d3d50067fb9ecd558925cc693ca52607d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332322565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9ef9ef61cec08b0f508e8e918e043be0928c452dd03200a8587f5ac21f2a6c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 03:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:38:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:33:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25dea15c4ffeb70e1112f1ee06dd948a8ab9dfc3b79ef239cb96080cc27ff1be`  
		Last Modified: Tue, 18 Nov 2025 01:13:47 GMT  
		Size: 48.6 MB (48591184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e989d2e0e09f298fb48c4d6ff3605064bc05169f4e2b9891ccb3261afe85988e`  
		Last Modified: Tue, 18 Nov 2025 03:25:51 GMT  
		Size: 26.4 MB (26444649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d766a3fcd99b3870f8097a1cba056eadc6327b86dc0436d4998b4bd42fba2bf`  
		Last Modified: Tue, 18 Nov 2025 05:39:16 GMT  
		Size: 68.1 MB (68117647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3638c589b2e540bc3e5e4fb95ccf8b07f498d0e3cf8da94b42f3f5e0e1da8852`  
		Last Modified: Tue, 18 Nov 2025 06:34:17 GMT  
		Size: 189.2 MB (189169085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2edd9c2f2cbc79777fa0515fd9ddf7904f4bf05fc4397f4760b7a5f7aaffb85e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16336758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c994bd8674a3370342cbb654cbbd8d0ca434aa616a449f19f55930392fed1`

```dockerfile
```

-	Layers:
	-	`sha256:99efb76c9dbf3ed90d20e15a944b03d17f1b4c5297006f6633f72bb88690d0f8`  
		Last Modified: Tue, 18 Nov 2025 08:21:37 GMT  
		Size: 16.3 MB (16326533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52e4a833dbe51979fe8c54cca62a2fe4856371b51983d64be2c8cf8d29a4a2c4`  
		Last Modified: Tue, 18 Nov 2025 08:21:38 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:097c5cc87b8af1310d5cef6954026b1466dc10e53793f76b8d91e244d58ca6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351156720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10e362c286e52b2780eeb73e9103f95b6e7a8fde6240460a1c955115f147578`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1763337600'
# Tue, 18 Nov 2025 02:56:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:09:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:19:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:898cf630ac245ec9ad865c96204520b86bb7b8760d5bd2f14bd02745e43d82f4`  
		Last Modified: Tue, 18 Nov 2025 01:13:40 GMT  
		Size: 49.8 MB (49832238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2307ec487a47570033147c5c7a8c176eb531df9120f57bf768d32ef164c1efb5`  
		Last Modified: Tue, 18 Nov 2025 02:57:08 GMT  
		Size: 28.4 MB (28443569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8afe2397c32fb7c8e88a8fb46c9042ce37ea62165c0c00b13dd2c00d1596507f`  
		Last Modified: Tue, 18 Nov 2025 04:10:32 GMT  
		Size: 70.4 MB (70405644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a19b951fe881d50c4e7f59c86893ae5fb480ecb4ae291d4f383a9576c8ccd39d`  
		Last Modified: Tue, 18 Nov 2025 05:19:57 GMT  
		Size: 202.5 MB (202475269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ee021964edf9eba055a778cab771675659cad020c02932043a8a548eb6252f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16231886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d85667c0a37ccd6ead9f6169bba180aa8577aeface412664f5a40fcc46e33bd`

```dockerfile
```

-	Layers:
	-	`sha256:2aa944b3c4eef6b5c6b94cd1757d9e2c7eb2289fe8b9380f8917fb831e800894`  
		Last Modified: Tue, 18 Nov 2025 08:21:55 GMT  
		Size: 16.2 MB (16221764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:037ecaf73e4465ab6a14d97f4b024c4e94a377470686363fd9603e0fceea6b62`  
		Last Modified: Tue, 18 Nov 2025 08:21:56 GMT  
		Size: 10.1 KB (10122 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:195e6d1c52ddfa3b13130d9b6655c3edbd51b567640951f4954badf0c26a7717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347858796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60de0eee8f87d0ba6a9368bb9864c8968d959e902bf47f582350d4bf92a57224`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 06:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 15:58:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 20:43:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9422d47ff8508a211c5181db20a5b72bab47758f9bcd0687b05752ead1b35a5a`  
		Last Modified: Tue, 04 Nov 2025 00:14:32 GMT  
		Size: 53.3 MB (53315240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aed674c331384a39236b4b411559b275037202a43d78e434b1d5c25b1e6d72`  
		Last Modified: Tue, 04 Nov 2025 06:26:53 GMT  
		Size: 28.8 MB (28798376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8defd21903bd4a9c5ce27e534598f52e2a1e6029872b40ca09576c2e165d5`  
		Last Modified: Tue, 04 Nov 2025 15:59:56 GMT  
		Size: 73.9 MB (73865276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea108f0bf025de0b233e391946942f6903fc348d3db37123cb910d4b293d8a17`  
		Last Modified: Wed, 05 Nov 2025 03:18:47 GMT  
		Size: 191.9 MB (191879904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adb09955a03e564a8d2797f08f46c172be1412c68e4ff248ab90cc97b299cdf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16237163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8c08a3ddaac7dcd06d41423a8264124e1136ee3e4c0c5784054040ff3ff72`

```dockerfile
```

-	Layers:
	-	`sha256:00561d131e31e53216d4d3a2b12bf5a329593b7e1bac25f754d7002a0e2bbe87`  
		Last Modified: Tue, 04 Nov 2025 23:20:30 GMT  
		Size: 16.2 MB (16226986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2d81cb603218b2af0a65d269196520be8fab9cd42d9fa19dc9335e9f72d02e`  
		Last Modified: Tue, 04 Nov 2025 23:20:31 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4115c41d34e472c2b5e6584f671b28e1607cba56fbe6738a7c77143499a698e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.5 MB (445494123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82a7ad3d60a866c4af1bcda7ffa05ab82235ac312da790bc5c74f14969437b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1762202650'
# Wed, 05 Nov 2025 11:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 07:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 08 Nov 2025 03:30:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:81afe9ed9d72ebbd06999820f64e36aa62bc978725062b4cc32efc39c6a99213`  
		Last Modified: Tue, 04 Nov 2025 00:13:41 GMT  
		Size: 46.8 MB (46791125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de80c58c6e8800ea08ee90fdc845007e21de17aea53e05a410b042fb2c91d58`  
		Last Modified: Wed, 05 Nov 2025 11:57:49 GMT  
		Size: 26.4 MB (26387683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba38582987e4915b52f0e092e29ae54ca12e102a825bf157a95190c5f836e50`  
		Last Modified: Thu, 06 Nov 2025 07:28:26 GMT  
		Size: 67.2 MB (67202784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bbaa85d1c7d501fec9d34d9b54416c39b19c67fb840d9f8a1abf22dfb13438`  
		Last Modified: Sat, 08 Nov 2025 14:22:40 GMT  
		Size: 305.1 MB (305112531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2f0ab91ac55a141f05a809e81d7b28ed95c221e1877c7c2c00e1aa55342362a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16310868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a6ae5a10b8073d887c3895583671ca3ee6046414c10fb34f42add1e49cf66`

```dockerfile
```

-	Layers:
	-	`sha256:ee294e4cca1bc64fce75deb66d4df267004d251a94155ab7a82d64171dacca67`  
		Last Modified: Sat, 08 Nov 2025 05:20:49 GMT  
		Size: 16.3 MB (16300691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22948fdf17087865265a2f446a5a9e7989edff5ff22f778355c7da8d9ded1b4`  
		Last Modified: Sat, 08 Nov 2025 05:20:50 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7f2ba0599577a7aed705697ad2436b5fa8a23dc5d03157963dcaf05338c56bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311460125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ed8dc529089f96f69eafc4b46af6004720130fc4aeef130700c981cd4104fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 10:00:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:50:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 17:26:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aa89048d1c3c931b297cf2d408ea7138528530c43e452af625223e71f97282b3`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 48.3 MB (48343062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd290c851a8e221175041f9832e015aa1560214f438629f7d489ba726030d3`  
		Last Modified: Tue, 04 Nov 2025 10:01:24 GMT  
		Size: 28.3 MB (28319729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc578ee5dbdb569a00fdc4f0f6cf56b364e8c2a978570ac8bfe2654c08bf3c0`  
		Last Modified: Tue, 04 Nov 2025 14:51:10 GMT  
		Size: 69.2 MB (69186605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256c6f7a44165be274215925862c2576bc84ca02e76724dbdf34b36c488dced`  
		Last Modified: Wed, 05 Nov 2025 03:18:29 GMT  
		Size: 165.6 MB (165610729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1917bc6a3e7c4a7a50f27bd35297d3ae59b592404b0f0ff6a2846a51c92a7799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16029647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df78cc2b72a24ab7c164e2d833642aff5695fcda780864d00ad17368a8c2878e`

```dockerfile
```

-	Layers:
	-	`sha256:da9938cb0940cb6fae326cf244c4224627eb78840399ecc2046ea07b2b01857a`  
		Last Modified: Tue, 04 Nov 2025 20:21:19 GMT  
		Size: 16.0 MB (16019502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff107daa3500a3397ac4155894aed0084c54eb176f45d91ece7f3d84b29e09f`  
		Last Modified: Tue, 04 Nov 2025 20:21:21 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
