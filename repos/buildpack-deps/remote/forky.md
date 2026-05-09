## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:8452d49feda53468a23efad92014953fa70cb76e8e515bb5d0a231e41eb8b3e3
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
$ docker pull buildpack-deps@sha256:b2e4f35d12ff9914fa1fc759869db47a22b132ee9b5ec07c40b652009cbeb6d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351779342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a15dbf0b5aab1caf1b537eeece4ab378864f1ff8cb3b3b63c80c6e843c8055e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:17:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd9ff4ed5fe9d40159f9f23c065d56cc6738732b6aa6aa03dbabd14807df17`  
		Last Modified: Fri, 08 May 2026 19:40:58 GMT  
		Size: 26.9 MB (26931106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5e74373817d223614205755063bd680dbeaabd9413354b6512787e7493e72c`  
		Last Modified: Fri, 08 May 2026 20:26:46 GMT  
		Size: 76.9 MB (76922259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb66be309074c477a0a1f030f5b10d6b9dbbe225332db63d2983ea2c1d5c32ce`  
		Last Modified: Fri, 08 May 2026 21:18:26 GMT  
		Size: 199.3 MB (199303934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:428b6448e0bf3e5fd14bcfa1bc1a36aee87763da540bac809cb14d62824d91aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16898493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6083cd6c6f385345cdf20fbe54713d58fea6fee0cb6f9f9caf75240c1db798fd`

```dockerfile
```

-	Layers:
	-	`sha256:965db8d9c015d6836478f467fbcc0dd6d7e1004f4a421bc2e6120248e9d8951c`  
		Last Modified: Fri, 08 May 2026 21:18:22 GMT  
		Size: 16.9 MB (16888348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb4ff2924203fb178aac9d4d016aa740c3119924d40943be0425bf3f2a9ef80`  
		Last Modified: Fri, 08 May 2026 21:18:21 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8337ebf420294c77a972e8924c9a2e422fba35e54e7eede52c8a48a5f3a2d98f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296765189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66526c5dc00a94f342880a3276c76005b405058468ed328a334d9e3fffa44a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:13:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1d504d75b0bac1a71363cc538d085e2c22d8b451c5112cd1892dea705c788f73`  
		Last Modified: Fri, 08 May 2026 18:37:09 GMT  
		Size: 45.6 MB (45559652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9e557f096b0076a9b942cb90588ca852b5e2621c1b8f7db68c5da56f1d563`  
		Last Modified: Fri, 08 May 2026 19:44:57 GMT  
		Size: 24.6 MB (24627884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7656597f355ff486609cac9b41999af529a6b55f6a5cc1c7888048b9d1f921c0`  
		Last Modified: Fri, 08 May 2026 21:35:23 GMT  
		Size: 71.5 MB (71469593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61818bb10df73ecba30a1abc183d3bd1acaa758ce9db35be6d4baeb9f649e651`  
		Last Modified: Fri, 08 May 2026 22:13:44 GMT  
		Size: 155.1 MB (155108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b986b875ba48d981c092c2703e27e6d51e55bfbf852ca567cc6ab7346b1e2844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16656948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5317171d74f5e2821b763d0655bbddef1d4eeef4dafa597315951bfa7e547b3`

```dockerfile
```

-	Layers:
	-	`sha256:40a9934055fbaa665701e5401cd7e78783044fe637a48c7807b8aa3db3d4bbbd`  
		Last Modified: Fri, 08 May 2026 22:13:36 GMT  
		Size: 16.6 MB (16646740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bb9323bc683b4013f135f615e1b80eb57322f5b48ce7cdd34c615f3fefa1d24`  
		Last Modified: Fri, 08 May 2026 22:13:35 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a84d6b8add2c1452dbc8eabda80d819046a3547607e3c75ac0f8aafcff690efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.2 MB (340176758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a769579aa1f36721d25e87af295e070f5fba784856144e4f441e024d1b6e0bd3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:17:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1cc0aceec664d055c261d350fe983921369e3615a68574b4c33a17a625489`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 26.2 MB (26215967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a7c71d7585d5a3c2cd0c50f396ae3fc659aeb54277293c1791833880128752`  
		Last Modified: Fri, 08 May 2026 20:32:45 GMT  
		Size: 76.1 MB (76091566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4b47adc5cc914f8b034215f54aaad951919607184236550b3f083385c26a85`  
		Last Modified: Fri, 08 May 2026 21:18:17 GMT  
		Size: 189.2 MB (189209474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f6d8a62b3117d75b71a76ff545c33898df82eeb74f261ee91f9db972577a3ee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16980323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65563962da8355014c65fd91d92fbfc0900f29bb3dd02db7d61e76f013565fdc`

```dockerfile
```

-	Layers:
	-	`sha256:7dfde42929b3d1e6ba7fbf8b0c3a4623dfcf4606f97e8252adce941c5f8de2b0`  
		Last Modified: Fri, 08 May 2026 21:18:13 GMT  
		Size: 17.0 MB (16970098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25549f0552caaf1eb19ce932054a77849ad2d971eeab01fb93c8bb20d9f129c6`  
		Last Modified: Fri, 08 May 2026 21:18:12 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c31fe29b00dc922dffc2bbc16001a1352ff2368010991b558b83b352ef8daadc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.6 MB (359571834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3279ab377986dd373000ded115fd3401775f45c142f9b11cf4d24d142fbbf09c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:43:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 02:26:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce975e5bc9e5b821fdbe31dcc55ec740aee98d254347a49a09e2157accffc9e`  
		Last Modified: Fri, 08 May 2026 19:44:04 GMT  
		Size: 28.2 MB (28247335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accb2ad2fb3504d5babe277108227672c99e7f6267841ebac568eabee2b26666`  
		Last Modified: Fri, 08 May 2026 23:05:47 GMT  
		Size: 79.1 MB (79136938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5abe1d44b299f4e09d2bf140506659fc0ee63be96b7abf41855720eb36aafd`  
		Last Modified: Sat, 09 May 2026 02:27:19 GMT  
		Size: 202.3 MB (202263340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:160b5dff5dab7c41823d5174f4d743caf1a1969978c8e814dc8d6df9840395f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16868341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16d0fafd21d603d4bf8b42e0cace1b4efa91ab78f22a0b0971930d845693c81`

```dockerfile
```

-	Layers:
	-	`sha256:576f0fac92d3e345fd56903bfed96788762bf58b49d44404de74e6a13ebfc9b2`  
		Last Modified: Sat, 09 May 2026 02:27:14 GMT  
		Size: 16.9 MB (16858218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f35c492004f881d2aa15783cc4f6345b70b872b544f86d211af60da5ac570bb`  
		Last Modified: Sat, 09 May 2026 02:27:13 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7b2afedd7591603a8c178060bd7d150d3bf8b4aa141e109fd88fe353ad84f034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359774257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71955057f71c409c5950d511bac1a770b66c3f3f5b29beadc453eaacf1e34c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 22:31:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:27:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 06:07:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b0beeba61b823ca3e14a339f1111ae37331fca42dd43aff18c04950bc3c9921a`  
		Last Modified: Fri, 08 May 2026 19:44:35 GMT  
		Size: 53.9 MB (53926974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f3b32fb543eab144095fd22346cb5e6a9d20cf9a632717c0a11d280547f7a`  
		Last Modified: Fri, 08 May 2026 22:31:29 GMT  
		Size: 29.3 MB (29268977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9ada7fcdf049694ac82397db78a7b39cd1a082adab6683f0a1f738caf441a6`  
		Last Modified: Sat, 09 May 2026 03:28:12 GMT  
		Size: 83.4 MB (83429867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f3f0c4592a4837f08de3d29c9955226b64fcb919010f6f2f4f9801eb563ff8`  
		Last Modified: Sat, 09 May 2026 06:08:29 GMT  
		Size: 193.1 MB (193148439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:78872704172cd68395ac66218fa1504f13bd2c7e5220d42f8a190f48b4d05569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16849480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474b6f9eb8af22789b940ea226482ceed088f7a618eaf56870361261469670df`

```dockerfile
```

-	Layers:
	-	`sha256:a1d2adf2588e2bfbb655df5a4fb9bae0c4287477f6ca8e25f097b241fb11152f`  
		Last Modified: Sat, 09 May 2026 06:08:25 GMT  
		Size: 16.8 MB (16839303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:273b5754a46ef42054243bbbd400837f1815c06472901eb2346628ce3b842809`  
		Last Modified: Sat, 09 May 2026 06:08:25 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a5b9d83fb84e75e1a08ce057b8c2b4e74c8ea3422472bd6bea9f56aebd1e06c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.9 MB (473867714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b0f8dc234a7f1e70c567070cfd5b0ab247f8d6bcec72933d0d937b4e050783`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1776729600'
# Thu, 23 Apr 2026 16:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 25 Apr 2026 23:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 26 Apr 2026 15:38:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:04fb0dd36a6b62569331264b3dc244d1f567b4ad68c8c1b27f9d22978f421544`  
		Last Modified: Wed, 22 Apr 2026 02:14:57 GMT  
		Size: 46.8 MB (46771523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67bcef726e432bfd28120bec18ce459483cfe5851a88769e35186b7e9186e99`  
		Last Modified: Thu, 23 Apr 2026 16:16:58 GMT  
		Size: 26.6 MB (26575473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c088d66fe4b03f57a1b249457eed3a1d678ec813dfb34d56e5a011edc2f10bf`  
		Last Modified: Sat, 25 Apr 2026 23:10:22 GMT  
		Size: 75.3 MB (75303599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191bfb4f01e7bbaec3a82bd0f2b71b5dbc24af9931fcda8d2ea34e49447bb3f9`  
		Last Modified: Sun, 26 Apr 2026 15:54:27 GMT  
		Size: 325.2 MB (325217119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87d449306bd3a2094ce87a922c390becffed48695020fab39b4d67c33a332789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16933038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a75301ee2cb5419478a7c4c04f421460085ec86c106350ee04074315b07922`

```dockerfile
```

-	Layers:
	-	`sha256:0a3076d28294a40e325f65d0fcb9a0eb8ba36096270746c9181e2c673bd2481a`  
		Last Modified: Sun, 26 Apr 2026 15:53:43 GMT  
		Size: 16.9 MB (16922861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a8d59d0c6feee030755805e1c958091266934f86208462e330ae53dcf28c8ba`  
		Last Modified: Sun, 26 Apr 2026 15:53:38 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8bf1e488b7b03ac94574bf40723e7af8903becbfb0e29fbd0e576613984c62b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.6 MB (324587119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760d495d650f848496e45264e3ec903145975155f1d4acf445cd03f2ffe7d1d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 20:53:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:33:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 00:14:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba3092798c7b7e427c9591ec4f0d9efaf8a9b59416038e46d07c57fb149b38ce`  
		Last Modified: Fri, 08 May 2026 18:27:50 GMT  
		Size: 48.4 MB (48373532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea40167dce774b75145b31dc946ba69ba4700a809db349b4a3bb2a9ef77497a1`  
		Last Modified: Fri, 08 May 2026 20:53:38 GMT  
		Size: 26.7 MB (26717627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30067cce4acd56b3088a56a702bef852ed218d3ff66dd3e1c87034bbff2dedb1`  
		Last Modified: Fri, 08 May 2026 22:33:58 GMT  
		Size: 77.5 MB (77468385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d618be169b1ce1927882989a819c625b3e61e2d624fdb9428a9b097acee27133`  
		Last Modified: Sat, 09 May 2026 00:15:36 GMT  
		Size: 172.0 MB (172027575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4813b8201e3f0b2e6d7bff6f2b0da99392c08a65595fc20abe2e50841c8e6912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16653463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:901700305b58c754c8ef3fa577fab017992739f4e18187be9826e194f607a077`

```dockerfile
```

-	Layers:
	-	`sha256:817356d58566b3b559f4fb0b26a819538b5ebe0c8c179adba76660c6931e51b1`  
		Last Modified: Sat, 09 May 2026 00:15:32 GMT  
		Size: 16.6 MB (16643318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaa7fc4b3c944bbb64ff0572c2ada578ce023f0db69324c935b8a77b56fadcd0`  
		Last Modified: Sat, 09 May 2026 00:15:32 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
