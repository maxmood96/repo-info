## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:d516c7b6c59e085de9a1c25a361f1a2c7f23dc0aae9ffe64b3211000e25d7ec9
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7cbe3791c734ad4570773a958b63e1371d045a3aff24011c5716ccfadeb65a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368973816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7703f03776d03820bc730c7ba4a1357b289a3c1e5cd0d41bab150afffe8d752`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa039132691ce2d5258743dd8ecefd941d85955a38506ba77c3fb6d2f554298`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 66.5 MB (66531021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c24554062853c5674b963d550e30ca0a757e9eb981889481f056f908bfb85e`  
		Last Modified: Tue, 12 Nov 2024 03:59:20 GMT  
		Size: 228.6 MB (228618122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fde6ad638d3489c2565f8fd9372ea5a582fde062402076e49c07d546cbce9f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16694153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1b4e4371b4516fbe01c132347fd12fc0e48c4c84d419d3f4d87a1585cddc59`

```dockerfile
```

-	Layers:
	-	`sha256:ecac10a1f2388f1010f072658b62094485c4427f64b84a05b42df2b85a715e3d`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 16.7 MB (16683960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5443e4fb350c11c56dd93b8946e2d787d3ec950b1cf9ba87f19e87f295b7e40`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e17c334b0b7edff201bf3dad7371e01081435d00f0903e32d9992994448af3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.4 MB (336404250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fdb6b544d03da28fac795acce46b3e40d93b1c044db57624dc9f947b15ea72`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:010709d78fdc05933a72549f7cb322633ad7dbe3d97bfcbda0aa10337118fb24 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f9250cc0718983393b852e9ddb20839b610fbab7fa648abee09b726c74343ff5`  
		Last Modified: Thu, 17 Oct 2024 00:59:25 GMT  
		Size: 50.1 MB (50146097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5571697784adcbe29d963579310eec564ff21e0a1805050b884b9a866946b3`  
		Last Modified: Sat, 19 Oct 2024 00:56:34 GMT  
		Size: 19.6 MB (19643438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e345c83b2739677a81bb65e8b14bcf4b74047ea7c75729f3715016f0c7c8e4f7`  
		Last Modified: Sat, 19 Oct 2024 02:57:55 GMT  
		Size: 63.7 MB (63732701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba13208d3d98c2c044903d623250746a9f82f21615d81cd9320324e88d2c5986`  
		Last Modified: Sat, 19 Oct 2024 03:59:38 GMT  
		Size: 202.9 MB (202882014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:437a0ad697104270ed2624404f330a281828ed64330de5e5f077617b72e030c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16300149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739965cf82b4ed3119927e3b6ebcef8fe79729c4c10a648883933bb70809bff7`

```dockerfile
```

-	Layers:
	-	`sha256:08cfe0ef62790cb5ea5c20d9b2ee6d533f0d8460704a3f9e3d5748f2db0c94f0`  
		Last Modified: Sat, 19 Oct 2024 03:59:34 GMT  
		Size: 16.3 MB (16289884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c3c169dcf3a7b48256e3352f5d250a328a498218a7b95d90059a1d80c1978c`  
		Last Modified: Sat, 19 Oct 2024 03:59:33 GMT  
		Size: 10.3 KB (10265 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:43decaa0c198ea49c25e0579b8e4459dd1eccbb162c2f3b3cf60c5f105c30532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.8 MB (317793004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e5bbbfe2db111d7c0a74257c7e0efd4390af8f93f7a297fced39742d6fee01`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcca10ec23fe707cc08f7ab790838065704861f60c0f678095482cc25ef593`  
		Last Modified: Sat, 19 Oct 2024 06:40:45 GMT  
		Size: 61.2 MB (61228559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b8715cfc77ca9de75ae3a4c97787dddb260f81e6774113adb34eeb4df9fbab`  
		Last Modified: Sat, 19 Oct 2024 08:15:21 GMT  
		Size: 189.9 MB (189933594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:201e31e97b8198b5b73245292db7ee57ccbcbff11baedb28f3c8716c3712a460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16305861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e54ca52b2d36a1153fe982f6c91426c036c1c8752aefa37315bbb6ae468eca`

```dockerfile
```

-	Layers:
	-	`sha256:db8b42ad1f6e5f980314f108470f162b14dd14f2b57c0eb4a15526b533e7ffc4`  
		Last Modified: Sat, 19 Oct 2024 08:15:17 GMT  
		Size: 16.3 MB (16295596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dd62a0b90c1f4d9670edefd460b2729d71461a06b59b621e01e0e5c090f59f`  
		Last Modified: Sat, 19 Oct 2024 08:15:16 GMT  
		Size: 10.3 KB (10265 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4ae9574eaaaa819eee22d771b30ecfd1b6a61732dfedf09f4d626004b7756023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361701064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbbe0de592c14b77f79d5364ba45b6b102a8f12377baa10181a3daeae528fa0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125c1d7d6d0668d3d31049e15ed26c5f15741a45a407eab00423ec50972be12`  
		Last Modified: Sat, 19 Oct 2024 05:20:09 GMT  
		Size: 66.3 MB (66298697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd09379a59f4bf2683bfc63736559fb02ca078899a46853d3dbb50955d6ce02`  
		Last Modified: Sat, 19 Oct 2024 06:21:51 GMT  
		Size: 221.4 MB (221420169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5e44adae95a33c8855a957d37239c524418aa044cf210b118df590bc5c617ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16604076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d6fdab1445139470616a1ba7e76135d8184f2d94c3e977392d6f83c93cee3c`

```dockerfile
```

-	Layers:
	-	`sha256:49838c80534b422aa73f107fe50cea0e08b56cb8df4bed441762f4c6fc8da938`  
		Last Modified: Sat, 19 Oct 2024 06:21:46 GMT  
		Size: 16.6 MB (16593791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130ddeaced8e30940ccc1ba76f5f1b1037cbac31ce7fb4fea621f464b45b9969`  
		Last Modified: Sat, 19 Oct 2024 06:21:45 GMT  
		Size: 10.3 KB (10285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:13a5f075e4b03beecdfe160afa42b8b6109f2e26e8e33707314cef4940012410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374066765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bc8c18b13cac0f90dc06c003982716d8f2c3d57540c4dd475cd2bf2aeb0768`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c207d20a70d18f9e95ac6b10fd58bbc5d2a036845c50cdab8e2fa983066a990`  
		Last Modified: Tue, 12 Nov 2024 03:14:35 GMT  
		Size: 68.3 MB (68343373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2790a8863dae4d5397c7a550a69104b8b23dcb717967ee6e4eaadfbb1e2b031a`  
		Last Modified: Tue, 12 Nov 2024 04:00:28 GMT  
		Size: 229.9 MB (229905775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ca9a1ae52fdac26a890763e00bccfb82d42e7c8eb0f3b6d31f79942c3f9a34e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16663809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:283d90ebc233386f9ee9c40e4a432225230f776486c2e00d3fd2ad23d5160970`

```dockerfile
```

-	Layers:
	-	`sha256:d3892b08125fc65dd00ec24cf04745b40b69e5b08348457ba04c1bdb60167dbf`  
		Last Modified: Tue, 12 Nov 2024 04:00:24 GMT  
		Size: 16.7 MB (16653639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ebaf548cb0955edc73a8e3008964cb55db8614f1c4e3ca7733ffebe47caccf`  
		Last Modified: Tue, 12 Nov 2024 04:00:23 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2d79e8b7e96fe38d9e45a4d282bd0f95d67001a444552087bd3cc32f25d08084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345787888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56875b7a504b29b2bb3123f42f536d1f78dc908550e86383f2d6486887d1a44`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64eacd2dd173c3ffb6f366cf5087686edf0379bf94a7576a971e2b52513c8882`  
		Last Modified: Sat, 19 Oct 2024 03:18:15 GMT  
		Size: 207.6 MB (207636776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:25e904418fdd672b948405e1f14bcb5c092286565f8ea58f426a76778aedf70f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce2990a7740c1ee661056d1286c412d9aa033ccfad23335960773e59e4582da`

```dockerfile
```

-	Layers:
	-	`sha256:529b4851b6d08464af5c7c7f70b64a67057dc822143fa9cdf853e9719b9b0d5f`  
		Last Modified: Sat, 19 Oct 2024 03:17:55 GMT  
		Size: 10.0 KB (10038 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fb2d0b8252543fd9aac6afd2358f8c036517399d15ab671d2c26238bf25b8817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.7 MB (378675496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2934ca0774acb5c953ccff3f166b5c11443c95326cb52e98f91e9aa4cb675ae2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c73c116650c722a140d5e98dc4d5b306e6daaa1f611e7f00699c828890445`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 23.3 MB (23314858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888fc73ea70716bfd3afc5289dca8e001895bc72345d7defb80ef4274358afe4`  
		Last Modified: Sat, 19 Oct 2024 04:10:18 GMT  
		Size: 71.6 MB (71620992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e85c4c362f2752b90470a2e9c73e4b582008ca3b0314740e6a4e1c756cc08f0`  
		Last Modified: Sat, 19 Oct 2024 05:24:17 GMT  
		Size: 226.6 MB (226613001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bb68d7efafd7d984c6f1b48c59077419faf23c6d84bc1bacccfda22722f3d873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16505785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07402716cde3edbdad9c0a69eaa180c73b700706e17afbcf700e741832b7c2d3`

```dockerfile
```

-	Layers:
	-	`sha256:4b95db3e2321004c462504333af6b67a31f8bf670842e66a4656832a64ce8ec1`  
		Last Modified: Sat, 19 Oct 2024 05:24:10 GMT  
		Size: 16.5 MB (16495548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c87f6f72bd68371ce1cee3cc527c15b062c2dba5a32da15805811213cc92cc`  
		Last Modified: Sat, 19 Oct 2024 05:24:09 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:64db136082af530566b7ed8329ddad4bb6bc67827f9ed7e770fb7c7d363aaa30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343151504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b638beec4f55aadeb0294811090591f2020966a01e0943d5ce76f0a912864f80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc2aa2fcdc4addb1b596c3dbc6f3699d60107644fd49f54f3050356c21437c`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 67.3 MB (67332572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc706768a06fa9cf16504e13939b12c91809de8a89473cc7b793fbce1b5adb60`  
		Last Modified: Sat, 19 Oct 2024 05:09:06 GMT  
		Size: 201.4 MB (201353900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8964bba7c715a5e8f0de47782dfc27bfae53b34e72337817658a05402ea8c5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16298751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de39e96e1289fd9ad90558f1d9bc9ba89833a4dc736aa81a7d1eec6e72ae985a`

```dockerfile
```

-	Layers:
	-	`sha256:2e89bddb8da9917b83fcd1c1c9cd13cb701e559da0f070b1b66e91712318f5db`  
		Last Modified: Sat, 19 Oct 2024 05:09:03 GMT  
		Size: 16.3 MB (16288548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d292472b39d06e2e9473e3ce69b1cd5133a331271d388009a134a30414dbc91`  
		Last Modified: Sat, 19 Oct 2024 05:09:02 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
