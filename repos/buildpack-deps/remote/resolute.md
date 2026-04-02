## `buildpack-deps:resolute`

```console
$ docker pull buildpack-deps@sha256:63282b5aab5fc6ae133bb9c2555cacd4eaa70f6895169395d2eb4af3205e5cc0
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
$ docker pull buildpack-deps@sha256:0d665fce41fe83ec8438afd8ae17f524e5e95925d7573fe047bf2b23228b2ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280746236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305094f186e578732c7964700186f181d4e7a888d2f89b19478fd595eaa42b15`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4425.tar --tag 26.04
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:01:06 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4425.tar
# Wed, 01 Apr 2026 20:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 20:25:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 21:05:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a028660a7b4f1b5217ef1f9e71530c04bb548e81d05a91dba1c14a136299f534`  
		Last Modified: Wed, 01 Apr 2026 05:09:39 GMT  
		Size: 41.6 MB (41551910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f09f0d240e7d8cf10637b0dc107589f18f90d5d58b7a8d5d83253e788969e0`  
		Last Modified: Wed, 01 Apr 2026 05:09:42 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5838583e0357c92d847bf5b230796d38f2e305482cb640ea0a33a08f78ea86`  
		Last Modified: Wed, 01 Apr 2026 20:05:47 GMT  
		Size: 19.5 MB (19519626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aad78dbbb1b4a2f8c87c89a6791e12c480f16cea67b016135dd6bd5d3a88a49`  
		Last Modified: Wed, 01 Apr 2026 20:25:41 GMT  
		Size: 49.3 MB (49335730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755aa868750e818f1610ce84afff1037d5dbe0a2dac44dfb9bec2d8726ca62aa`  
		Last Modified: Wed, 01 Apr 2026 21:06:10 GMT  
		Size: 170.3 MB (170338583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3fd28739d910b8dd195dc2c0be355bfb3c154eac0b564338b3a2c780a10b42da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13156162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7042add587791b4fdf2e20403f0a9440025e23de1b353a56fc73051c15ec940c`

```dockerfile
```

-	Layers:
	-	`sha256:f8bcac6a61ece11186c6e58a014768c83694fbea56bd4e2d12a3e33df373e821`  
		Last Modified: Wed, 01 Apr 2026 21:06:07 GMT  
		Size: 13.1 MB (13145695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:616f797a86fecf6a8f9f4b934df25254723115ba66d37dc303d1f436d7817696`  
		Last Modified: Wed, 01 Apr 2026 21:06:06 GMT  
		Size: 10.5 KB (10467 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e74e5e8d3206f2861bf8a8e568816dd47d64c714e98c38984914f4277deaa86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (235003830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f45d402e0a562135d1a0cc99798aab85b36c1732174d33bf29a8e8230584d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:04:09 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4460.tar --tag 26.04
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:10 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4460.tar
# Wed, 01 Apr 2026 20:07:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 21:04:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 21:09:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b87bc5e9902cacc98659b7db3fea909a8ae8c0e207125762ba9f55078ffef605`  
		Last Modified: Wed, 01 Apr 2026 05:10:11 GMT  
		Size: 38.6 MB (38647549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90488af8b50823555c030ac051af6efa635ef247e7d4c3d8c7e9910c3755891f`  
		Last Modified: Wed, 01 Apr 2026 05:10:13 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46104cf503adc45c0cd7985b491e2cefa21745aaf0863b165b0c724dbbdff0c4`  
		Last Modified: Wed, 01 Apr 2026 20:07:52 GMT  
		Size: 17.8 MB (17808270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4ea4930a6195b97f68d78754dc69ebc0455b3bcfa054b2fc8af384b723a19d`  
		Last Modified: Wed, 01 Apr 2026 21:05:04 GMT  
		Size: 52.2 MB (52238536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22325ee2b59641dbeb94595a377815f1ea62f64538944af0137dcf899449a03a`  
		Last Modified: Wed, 01 Apr 2026 21:09:33 GMT  
		Size: 126.3 MB (126309084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2c248748d41f6cc4c348942f76a2413c11605a525b7835cf02fd63442d727840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12897116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b16e82d10a56f263bdffe04fcadbe6a48064b217b7657f1200109772d5cbc16`

```dockerfile
```

-	Layers:
	-	`sha256:9463a5302d2f527b2a585d47023dd1c34425f2b4655cc29613f162396788e4e6`  
		Last Modified: Wed, 01 Apr 2026 21:09:30 GMT  
		Size: 12.9 MB (12886584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58ee3d284543d7e6bd0a5786487438d58f7d539968c8e94786923b04f786251`  
		Last Modified: Wed, 01 Apr 2026 21:09:29 GMT  
		Size: 10.5 KB (10532 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:98821c403a6a13c77f0d396ac53e758fd568073661bd7d650fa6b057fc89340e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269341955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71b1ff933d54adeaf83234ab99b3dd3db6942b065873c0b2e9f0052c27980bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4502.tar --tag 26.04
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:03:15 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4502.tar
# Wed, 01 Apr 2026 20:05:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 20:22:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 21:05:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e01771b74c5a1f96dc758c147c06fb46daa8f6142de3935a5b8ad25c5f395a90`  
		Last Modified: Wed, 01 Apr 2026 05:09:50 GMT  
		Size: 40.7 MB (40734995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59caf9e43b45d2a51ce8729f055a065c5081c6e9a3b145ea8f9b573f05936182`  
		Last Modified: Wed, 01 Apr 2026 05:09:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e62c4f1f39ef342f5f9676dfc2e62081ae01b9edd9b110549359bbe5b9e84e`  
		Last Modified: Wed, 01 Apr 2026 20:05:55 GMT  
		Size: 19.1 MB (19054561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055aab8025099ee9b09763af46fd5b27f267ab43871bc2781622ae80cb7c05bc`  
		Last Modified: Wed, 01 Apr 2026 20:23:05 GMT  
		Size: 48.9 MB (48931282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe9c80d98a2e12d49b934deb0d13d743a59964240de996803e5de50136f7595`  
		Last Modified: Wed, 01 Apr 2026 21:06:15 GMT  
		Size: 160.6 MB (160620729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e15a3757e520ac95d2391d2a34e97b2c73b2a4d6c247d40dc24093c4dc3993bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 MB (13210412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd517e304c2bac95b5212afa1ad2888874011f97cc19875a0718c6f3d7ade7c`

```dockerfile
```

-	Layers:
	-	`sha256:53f2ca6e33c6ae92b7cb7fe11a812c546b1eb6517a87ae988fa992228b17ed9a`  
		Last Modified: Wed, 01 Apr 2026 21:06:06 GMT  
		Size: 13.2 MB (13199864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7501f9ac8078ca5a5198f8ce6ede9b9a89c5c5f1c202afc850720c3c605a2dbf`  
		Last Modified: Wed, 01 Apr 2026 21:06:05 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f9a6913a5eb047c470991b3e5351850b530671289ae132534a320b0cf3ae88c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291682065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:295c37c949abfbc204af809321cab790b69949d1a7dea32b0b1e0f3682215181`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4409.tar --tag 26.04
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:11 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:12 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4409.tar
# Wed, 01 Apr 2026 20:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 21:04:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 21:50:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d29a67913207c73576260dcfc2f317ce8f370d2e6036a15cea1d4c50619f9e0`  
		Last Modified: Wed, 01 Apr 2026 05:10:00 GMT  
		Size: 46.7 MB (46747843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632d8b198f2e7d6fc57ec36af12b5218cd6b2fdd0af240c60203b87363f9d140`  
		Last Modified: Wed, 01 Apr 2026 05:10:03 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a322216276af0165efcb8f7a01337a87030ed5621a502f99fe12e03f8972fa4`  
		Last Modified: Wed, 01 Apr 2026 20:17:58 GMT  
		Size: 22.0 MB (21990398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a2c5552f053a3780c21ce21bded89102bfaa1105d46a7f7882266f0e249ee8`  
		Last Modified: Wed, 01 Apr 2026 21:05:23 GMT  
		Size: 55.5 MB (55466658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9323b5741461094b8bb23a4a05f49a332e7e6078367bdd1fe102d2870a516142`  
		Last Modified: Wed, 01 Apr 2026 21:51:32 GMT  
		Size: 167.5 MB (167476776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a966631e5eb542c92184d87fc3901d707c659a8350eb133dec827ef7ef626750
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13128777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb094b0a0cf590e4cc71bd93240efd584784446afa6296aae558cb2f6b16b7d`

```dockerfile
```

-	Layers:
	-	`sha256:792cfe07907ad3c213ade66eede1d2a6173ebd3d4fb2a9045ab54373b17402a2`  
		Last Modified: Wed, 01 Apr 2026 21:51:29 GMT  
		Size: 13.1 MB (13118277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a6590b026f2161477fe33c698d4a91b3590e60e503cd8029b5de248c6da999`  
		Last Modified: Wed, 01 Apr 2026 21:51:28 GMT  
		Size: 10.5 KB (10500 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6554c52b5f4277176b82d0c5ce6b767342a605e2d9c31e0ca2b78943ad3777e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256819511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446c4f82dc1d4f0b6591b9050abcbee3434143c593db428839c02860560dbd3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.4471.tar --tag 26.04
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci config
# Wed, 01 Apr 2026 04:04:25 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-2190cb971fd0e5f37eb1b492cbc3c1e3/images/.temp_layer.control_data.4471.tar
# Wed, 01 Apr 2026 20:14:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 21:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 01 Apr 2026 22:56:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ec23a920706567555cbde8fd1a678eb0fc884335da074568e17a20e5c82930e`  
		Last Modified: Wed, 01 Apr 2026 05:10:32 GMT  
		Size: 41.1 MB (41118651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bdc07369a1ddaa6de066f70a0f9a108bb5825b1bd40d6d4f6597f005bc34d7`  
		Last Modified: Wed, 01 Apr 2026 05:10:34 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc25a5beb15342c7e309bfdccb5203cbe47007ad1730733e60115e0d560df0a`  
		Last Modified: Wed, 01 Apr 2026 20:14:27 GMT  
		Size: 20.0 MB (19996422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f20af229b32ffcb9695bb539922395be1300bc8e6174369841b1e5bf19564d`  
		Last Modified: Wed, 01 Apr 2026 21:08:49 GMT  
		Size: 50.6 MB (50591078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4673d0aa02cbcde50236eb751e2e1289774879aef7a41e72ade977f4dd49c8`  
		Last Modified: Wed, 01 Apr 2026 22:59:31 GMT  
		Size: 145.1 MB (145112971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:41bf411ecea1f5fb6e1d68447b75a1cc535bbdb0d7e58b70e020dc49be38c425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.9 MB (12940509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e809ed87067028e62356bc88337c653dc6ca1e991c7de5d200c1ffbae908966`

```dockerfile
```

-	Layers:
	-	`sha256:db097cbefe0b37e3555cb3142b95226b572d3105f08cb969576eaaa6661a2fe0`  
		Last Modified: Wed, 01 Apr 2026 22:59:17 GMT  
		Size: 12.9 MB (12930041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf209bfa899e3a574e84e232402644c326d475193dba0207e86840ba7bbd6cb`  
		Last Modified: Wed, 01 Apr 2026 22:59:06 GMT  
		Size: 10.5 KB (10468 bytes)  
		MIME: application/vnd.in-toto+json
