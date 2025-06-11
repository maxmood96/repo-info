## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:d6a4703022b5f3c4e6cc019049623013bf99ce205754d0361fc7cd9faf4d54d2
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

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4c37ab5f6f0d007c4d897ee58ae3abd40dbdf6ad8d18d9b347cf32e072b57607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348280090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c522cf17983894d1505acdd50b51a182ead422c80814c354c596bfab0fad3222`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b8862a18fa961ebfbac8484877dd4894e96ee88177d8c4f1f54d9727262b7d`  
		Last Modified: Wed, 11 Jun 2025 02:16:04 GMT  
		Size: 211.4 MB (211370316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b9ebdffc84c0206c2d56fa9e8a6ec4f2cd6774fdc9608fcc9d46d60b1aad8cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15870235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f79c0db0ba720b5c6cea4deb2b6516677a61f324ca5f11b65549013b9e13712`

```dockerfile
```

-	Layers:
	-	`sha256:371bdc74953f795e311219675fbfe5f20fbb7b8c80b55a85e1dce912d6676e92`  
		Last Modified: Wed, 11 Jun 2025 03:40:59 GMT  
		Size: 15.9 MB (15859695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603adcae870f0f52f8a9f19a807afb3a48b375868fbdf6d794f8b53cee7019a6`  
		Last Modified: Wed, 11 Jun 2025 03:41:00 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7a5f5d5039bd60e648a8b6e8d0dfb9c43fcdbb8c91f78f3205eceff98b5dbabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315358804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd9045c2e60c097b73c0e0136687d1b949f7f02a2e0a8df728966dff055e5fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe4bc1cbdee9e4aabbc6c58a2156f300e4c3158cfb501698b1878215892a8763`  
		Last Modified: Wed, 11 Jun 2025 00:30:31 GMT  
		Size: 46.0 MB (46026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7973a0421a43933f783f2da8c4e6210bbcb63636694bdb47f5939d46f0cd8e74`  
		Last Modified: Wed, 11 Jun 2025 03:12:54 GMT  
		Size: 22.7 MB (22694196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd263284be736a4785fb0c489cf441580757a05d8cb52c26f07ba8f071d621a`  
		Last Modified: Wed, 11 Jun 2025 06:33:53 GMT  
		Size: 62.0 MB (61997905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30652400d271bd60054de74fdb5974778115084d744807cfc209f10e782a415`  
		Last Modified: Wed, 11 Jun 2025 09:06:12 GMT  
		Size: 184.6 MB (184640116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a897de0e263d4427d57a4bcbfb08889d9caa3e1009ed8ae25ab6e62f96e19480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15667295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d556df461cd7762d7b8d764f52a9eb5a16d35d22eee79d131e624dd54bdba0a`

```dockerfile
```

-	Layers:
	-	`sha256:1cbddb955efcc29dadaf1e87fff2385553d9e0ffffc3b4473734c87def181de7`  
		Last Modified: Wed, 11 Jun 2025 10:19:46 GMT  
		Size: 15.7 MB (15656687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9b1dc53af3e8fffa0ce89524d9c4066bcda2fb554b6ce9b165d3d81a2b4c3d`  
		Last Modified: Wed, 11 Jun 2025 10:19:47 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9c243b46e16cc9cb1342a1fa2d02c53fcdf8bb41dba2b2898de4187e23e53f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301081485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f58e948c34be82583637797a8c73b934ada980253d812c71ee2f3f448818a1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22ee2db9f8d2ea3317ceb36f4b9bc7895f6cb8402903d639c8083eaec948450`  
		Last Modified: Tue, 03 Jun 2025 13:39:41 GMT  
		Size: 175.3 MB (175297793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b1d1114409904339b77f03fe17f51f442cae1566dd1cf5583bcd54a67d3d4a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15380853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4ed2c189e23875a60cffa8209bca9e84c36c94173a58da7c77e3243c6dcba8`

```dockerfile
```

-	Layers:
	-	`sha256:808d1e809273834e64dfb121128a3dd5bbf4dc22fc65c910ac1e72813aeaea71`  
		Last Modified: Wed, 04 Jun 2025 01:01:36 GMT  
		Size: 15.4 MB (15370246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cff77529fee4fbd5ac4ded48d5d8c6112936e878eb09a20409c0c6cfbb265c5`  
		Last Modified: Wed, 04 Jun 2025 01:01:37 GMT  
		Size: 10.6 KB (10607 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:5d40f778450ed9fb38ca416211e7eceb70fc27806a73dc9a73ef4367c0e7c4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (339003122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468b393ee822135d3f2b4d67d5eddacb49d88924e43872bc6c38a6970f85b756`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ee5cb7152015437e4a9b3066ae9e25a26a3bef6617d0b7f25368511c2d954`  
		Last Modified: Tue, 03 Jun 2025 13:30:35 GMT  
		Size: 202.8 MB (202762554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0daf6b46bbfebe757741bd05cc776f6e095c5c0e8c7753c001d19094adb51a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15606926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74b61220a13020baeac1c42b5f0e150b79409ceff2df7dcedc5346ac5138fbe`

```dockerfile
```

-	Layers:
	-	`sha256:1436c6c53e53573c8ded110c42e9c7ba3287edd5916c1f3a90c39ac670d4b4fa`  
		Last Modified: Wed, 04 Jun 2025 01:01:48 GMT  
		Size: 15.6 MB (15596294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e051828ff9adeb0ee869b3eda258ca32683d20e21634aa07b5eda70aecf121b9`  
		Last Modified: Wed, 04 Jun 2025 01:01:49 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:285fa6e3884288e09c641ebdc0e72d8074b3cd3bfab9f230e6ef99a713c4c170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350858779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bcac04c68189372f41e6075edc2c44ea0ea7847848a850e6e6acc0e79f933cd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75453a9e8c0ecda25b39aaabe16c9694b0bdb799dbc4bb61d1d0aee7d8b70850`  
		Last Modified: Wed, 11 Jun 2025 02:15:24 GMT  
		Size: 210.3 MB (210300359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bf79d385367f4aee09b6b8bce9eff60cb57c1f5867972142d4fd1a9788a622aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15848434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dec6d1f58713334dd32ffd6ddb3d32f30490a01a4eaffd9c76d165e5a815c0f`

```dockerfile
```

-	Layers:
	-	`sha256:8d194db5f800eac5ee0678dbf5d0ad5b40b2d327bb8926f2a192079f3fbf689e`  
		Last Modified: Wed, 11 Jun 2025 04:20:17 GMT  
		Size: 15.8 MB (15837921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb24e1a49b1e73e90ce809bfcee8af1a8ec465daeac07556db81d1e1b5834d5f`  
		Last Modified: Wed, 11 Jun 2025 04:20:19 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e0f70ab73f63480340d9d5820844d4cd8f3e9bc5e188745183c6487bab997931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325627426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bcafd8c201cfe722ca7ac29333a7ae2dfb4191f4d4d31808f939a632987512`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc05e2d1c7537a7663041b66446ee4a24f98e673290839931cdaf3c0b93f56`  
		Last Modified: Tue, 03 Jun 2025 14:36:17 GMT  
		Size: 23.6 MB (23598613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fef5bce771d4c7090ec3bddacaa83a3ac07da89649b62764c8f0bb14e3e0ed`  
		Last Modified: Tue, 03 Jun 2025 14:36:20 GMT  
		Size: 63.3 MB (63308472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a53a9cb668f2a062fa360e20d3af717b100c5754bc85acaaaaf399e65052b90`  
		Last Modified: Tue, 03 Jun 2025 20:14:04 GMT  
		Size: 190.0 MB (189950588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:687ccb0d4c1a7b86f4a050d72923b32bf8a25544358a35b353bfbbd020daff3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eabebaba4108077fce2f173e30a959caacc1562e8b09afbf95331ac9ba46242`

```dockerfile
```

-	Layers:
	-	`sha256:925e39a40f6044a70bde75f91942ae8b5eaeec4786049bc3d0c05ad5882179a8`  
		Last Modified: Wed, 04 Jun 2025 01:02:11 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:56d5948fe69cea597e07abe88c61ebada0f5fa939f74a7c2b4165f5285d06bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362244766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950dd672646b8d013146b2f2486c2e76791897d4638d24b9db67a95aa8d33d17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5288618fea79e9a348995382235e6bee52819db4047a345ffaeaddd2b82e06`  
		Last Modified: Tue, 03 Jun 2025 13:37:01 GMT  
		Size: 214.4 MB (214416172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ebead102bba3522d00ea878bc9b3aab1d5b01fb685f957e823a0b13860400cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15554857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847793f31f62669b63aac29ea807f9f5915892ad1c0fdae8be0a2292aa20f815`

```dockerfile
```

-	Layers:
	-	`sha256:107a1b2da7e7fdc5bc1ce3a2a945360bdd2907016a8ab58d96ab01d163de860d`  
		Last Modified: Wed, 04 Jun 2025 01:02:15 GMT  
		Size: 15.5 MB (15544279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4396b6bfce8a4b2505b3026a08fad8c04f0ff91477965f9a8afad0629c3ca9fc`  
		Last Modified: Wed, 04 Jun 2025 01:02:16 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:938ef91f8c9ce50baec3cf84cbeca228c74cc370f100d0c5fdfa5ec4748cdc7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318062426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a6b4dfa702bdd456daf5488c44f90ce890f9ba6015932f1b5ca7908ec1deca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3151505c70d8a7022bb518bbfce9c7488d1dd6ab624e1d96b883eb0654da7562`  
		Last Modified: Tue, 03 Jun 2025 13:37:22 GMT  
		Size: 183.4 MB (183405201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:879484f5fad57595029490b29734b9d4691ac28cf536aca6a4e455bef191104c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15388812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3f989fe38a92800cfb6f10910598a46c3d01d41b7fa89216663a9db9a08a96`

```dockerfile
```

-	Layers:
	-	`sha256:2be90c0eb0d094f07bf76cc3c34cbecd9795e27ec2de02ec2224013317a450c2`  
		Last Modified: Wed, 04 Jun 2025 01:02:26 GMT  
		Size: 15.4 MB (15378272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f1226446678e9fe4c7d58080765ed7a4f74aca9d9252331b26eee074aeea15c`  
		Last Modified: Wed, 04 Jun 2025 01:02:27 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json
