## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:ed7ce2d2de459b55b1dd81a09a7c798f3c6adeef834e290cefa1f904b09e64fb
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
$ docker pull buildpack-deps@sha256:0357130b032ae0c854db1dc21229137704ae206a83f05daf23ffc95712eecf93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (367984491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a39104e33d7cad4c9c9d85b3127205c321bf8353351b6730a4181a98e58027`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:1dbb9219e4db2c44c251f0ada692f495f60d7f7206c6921c094608440df579c0 in / 
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
	-	`sha256:2d932a6262bf92703e4c318877f26c9f5817456038e35b8c537685fc2b40a29a`  
		Last Modified: Thu, 17 Oct 2024 00:26:49 GMT  
		Size: 53.2 MB (53238741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f31efba20d2de2a38e9be5393dc31cf8ee1b44853ff5d87cddb66164a6614`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 20.6 MB (20643097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6a86195a6ac634586ab2d95656285880bf44bc989315a1a390e89fab37bcb2`  
		Last Modified: Sat, 19 Oct 2024 02:06:34 GMT  
		Size: 66.2 MB (66236156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62683c6ad6022c8249b2258dcace69634541663e2eceb81fb4c1c2e36d49de26`  
		Last Modified: Sat, 19 Oct 2024 02:53:50 GMT  
		Size: 227.9 MB (227866497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:49b2368a3f95d6e910307e3c9f69f87deb7c2d3354b778e2874705c3bb4d5ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16507570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0df43ec87be3e27a39b4d13c738ef559f245755c425d593b205930559792820`

```dockerfile
```

-	Layers:
	-	`sha256:92f3ef1413b81322d8f5ea466d1cc9afec312eb414214d83c7c9cba360fa6bf1`  
		Last Modified: Sat, 19 Oct 2024 02:53:47 GMT  
		Size: 16.5 MB (16497377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63ee48f91490aa5f9944f1624c3f85bbc3f0562946751903e3d5c114b1e114b1`  
		Last Modified: Sat, 19 Oct 2024 02:53:47 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; arm variant v5

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

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; arm variant v7

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

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; arm64 variant v8

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

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ee56890ed8d6f91cba4394aa3f5083c5123400202ab7d096522a85a831f612f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.6 MB (372586202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcecdf46d089364cbde632cfb8e3b506ec37ff689e40ba870fd8b365626314c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:4d5beb040f172554a949bc99442605b682a56e62c519e97a7b25948e06a423c7 in / 
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
	-	`sha256:33d5fa78ce89fa0c095775872e03741607d5e662aede62fa388ef8ad810ffa10`  
		Last Modified: Thu, 17 Oct 2024 00:45:54 GMT  
		Size: 54.1 MB (54077458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5c3ffdc80062869321bb7433b1adb7b34816c3fba871dc68884bdb4115b512`  
		Last Modified: Sat, 19 Oct 2024 00:55:05 GMT  
		Size: 21.8 MB (21754592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86cb3c57ae9f50b2cf4f508d0c23399cc9692dfc7336323d593f363cb71e400`  
		Last Modified: Sat, 19 Oct 2024 02:06:45 GMT  
		Size: 68.0 MB (68040402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9067ce74b0ad44714f9fcdde6e1e80ccc5ea632bd70cc38760f160485b65493`  
		Last Modified: Sat, 19 Oct 2024 02:53:44 GMT  
		Size: 228.7 MB (228713750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2795e01efc42f3f6e6dec027b25de27f203b53cb39ba0bf807d31e1d8fda2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16477955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8734bfa35aa50645b7863013835b368e0353dcea699cb346e1e1c5a7d046a558`

```dockerfile
```

-	Layers:
	-	`sha256:f840f39bb756f2de1a67ce2157b37a9f49eb73423510632741ce767af0764190`  
		Last Modified: Sat, 19 Oct 2024 02:53:39 GMT  
		Size: 16.5 MB (16467785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de718ffef3484dc52d3236b9e93a9bbcfb9884f51c7d9cde604bc6d4b99c1d2`  
		Last Modified: Sat, 19 Oct 2024 02:53:38 GMT  
		Size: 10.2 KB (10170 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie` - linux; mips64le

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

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; ppc64le

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

### `buildpack-deps:trixie` - unknown; unknown

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

### `buildpack-deps:trixie` - linux; s390x

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

### `buildpack-deps:trixie` - unknown; unknown

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
