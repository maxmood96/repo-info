## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:b700549649e6925f68221f86a7a1131374ec4b848f0da66e6d043925d7aa3232
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
$ docker pull buildpack-deps@sha256:45629870e0be13b15b5e2fe723e8ff520126b5dd5c3c04536450cc11ed06d44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358491179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bd1346e88eb4447372a751bc46ba6bd3b71019b445280d0deff872baf5ca6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:42:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 08:19:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c764a369daed85f9b52e15146ccfcd0c76380aeab0914a25d45d32d7e95e4f6b`  
		Last Modified: Wed, 22 Apr 2026 01:42:57 GMT  
		Size: 28.3 MB (28284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7091ca31d67d63360b5bd63eedb35bca55f65b3881e95a9b699db1be7692a36f`  
		Last Modified: Wed, 22 Apr 2026 05:03:09 GMT  
		Size: 79.1 MB (79124028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6374f9717c7e64116279c1c65c129c06bb2b93e2fae6a78205ac879df6a4dc49`  
		Last Modified: Wed, 22 Apr 2026 08:20:29 GMT  
		Size: 201.1 MB (201099731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b3dd0b122d9e89c8b279fc48440877177a7bd90e8308d66cc711dc44eb80525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16853464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcbe68c4ca8317484716bb722926422bdef6628e4c9d9a5991a9dbced6a2adf`

```dockerfile
```

-	Layers:
	-	`sha256:eeb81ade24a69114f61583315bcfb5fc8b58d36d1576a7385574fded6d760563`  
		Last Modified: Wed, 22 Apr 2026 08:20:25 GMT  
		Size: 16.8 MB (16843341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b0c828c8a344174d817cd87eed54b680582866dced4640b9292c6e58b98c902`  
		Last Modified: Wed, 22 Apr 2026 08:20:24 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c7e4c0f8744f905d738eb3cdd7d29fd3a458915b2f0d3c46e1e1aa6bf541a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 MB (358721242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1529f5f70a40d2b33ddf9d096712295526b21bba1446fbd0dfa538bf8e80c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 03:39:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 12:13:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acf335ca95a581f78a61de78111418bda596ddf71257299393203995ee7ea4f`  
		Last Modified: Wed, 22 Apr 2026 00:15:35 GMT  
		Size: 54.0 MB (53983935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d29dcef074d70bcd1e851f17e286abd94e829b11cf89631a079de7a5d724304`  
		Last Modified: Wed, 22 Apr 2026 03:39:43 GMT  
		Size: 29.4 MB (29406037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd57b32a5dc3e8581a7c19ba8dc6ae535a2865291f197fe5f63b9c08c56a590`  
		Last Modified: Wed, 22 Apr 2026 09:38:28 GMT  
		Size: 83.5 MB (83450223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb7b4d6eb6936014d95321bb4d4d17ce4d3d96685a198208daec0938daf7004`  
		Last Modified: Wed, 22 Apr 2026 12:14:42 GMT  
		Size: 191.9 MB (191881047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d8d3126009ed37eb8db9596af3980c42fc21b7c5669b20fc5c718bb113e059a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16836757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95df67720613607f875cdaa155960d24b1ecb03481ddd5a0a5eed9614116f422`

```dockerfile
```

-	Layers:
	-	`sha256:991dcd03267bb488c3bdb8188708a861db730e4a868fe3fd821de3cd35a2ae2b`  
		Last Modified: Wed, 22 Apr 2026 12:14:38 GMT  
		Size: 16.8 MB (16826580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e7192e85925f3e15bd71b7342bedfc18434291451d5762a12d448e7f4eedc6`  
		Last Modified: Wed, 22 Apr 2026 12:14:37 GMT  
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
$ docker pull buildpack-deps@sha256:d158abe384082127d7debb95ed6184dfb421a9be5380155be414beefe2dffdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323525945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652cd9f81980875f00a737810bc6cae1ef810d02a1b18a693b8225687613afb5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:20:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a1060191b9434ca828b6395f3c2782a999320b4babb35dd20cb17592437fdf4a`  
		Last Modified: Wed, 22 Apr 2026 00:15:37 GMT  
		Size: 48.4 MB (48407607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca628a02ce8552e3ffa145824b47810287e1d695728e354379828ee1a246028c`  
		Last Modified: Wed, 22 Apr 2026 02:32:22 GMT  
		Size: 26.8 MB (26781237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4284620042de7e700765e6cf3d08ae5e2f2bfa319c3f4a48a20ef1a1a7fa7b15`  
		Last Modified: Wed, 22 Apr 2026 04:21:17 GMT  
		Size: 77.5 MB (77487748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ec35d7f52cdc224d8205bf3ea020409c177f179d218b3ff9a5391d71dbd84f`  
		Last Modified: Wed, 22 Apr 2026 05:14:46 GMT  
		Size: 170.8 MB (170849353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc92e3aec97bfac28a1f3715c066d7e95b2ec07278d271c64b76b93248858e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16637539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f7c17f32d377b1b6eec0638583b46d8d080cfb28923e7dea119217a508d7c2`

```dockerfile
```

-	Layers:
	-	`sha256:8a670490aa62f32cae3d4544c960a079f498512b238aa9afb3bc9d081e727b87`  
		Last Modified: Wed, 22 Apr 2026 05:14:42 GMT  
		Size: 16.6 MB (16627394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac5399a45ee65ee5e566f72a0574dddf32fd5c5e3414731c5bf68a0f8edfd20`  
		Last Modified: Wed, 22 Apr 2026 05:14:42 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
