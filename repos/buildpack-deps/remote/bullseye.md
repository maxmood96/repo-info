## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:401b9455ccba3aeb93a45427344ca432cc1ff07b8bbed2d5684ed7443b3561a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f31879cf369909e66e903c255c8a499bc10b5dddfb05ac80da9b59948b9630a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321446885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42e444d0ced2455cd3b480c16e1c57236edd51b48c01ae478af126da465efd9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840feb027ec25230e94a2f7f4414d50952ed3e6c6fc69a711b34ce7938a2dcdb`  
		Last Modified: Tue, 30 Sep 2025 00:10:31 GMT  
		Size: 15.8 MB (15764102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab467d29752c57d2c01fec39d489ac683e5cae8e5554713067baf3203fa856`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 54.8 MB (54756004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cc2fbde3e2936a5a869d2d3e1bcd69cf5669cd6d90107c65ac65764e213bb9`  
		Last Modified: Tue, 30 Sep 2025 09:52:52 GMT  
		Size: 197.2 MB (197170715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:525f5ef1cc8ccf9acb08cbf5d6885bfb61c2fe16a9c227269341729ed6b6da58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bc30fad7cbd1ee876896e10e11b2a6d2c174e98bdc9614f7ae452a036106d4`

```dockerfile
```

-	Layers:
	-	`sha256:3ae060958e041c7f6df2a2558432166b6540d5eab38a19d334d984ba00d1dcae`  
		Last Modified: Tue, 30 Sep 2025 22:35:07 GMT  
		Size: 15.5 MB (15462172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184338473594c2388b10f5c03f708ba00ef6a1e6789949dbc0de50d32355f8b8`  
		Last Modified: Tue, 30 Sep 2025 22:35:08 GMT  
		Size: 10.2 KB (10238 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d1bb8389f1ce483ea6134d8f82f7284b9249125f008075c9ef897d5b9d89ad0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282530343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed698357067635b1ddb89a83ddf11967d979e008e2a1f2ea06956e277c51e68`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1760918400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:680ed921e0c94a719af1d242eac2d0c1be8482153680a3940f3435ee5598303a`  
		Last Modified: Tue, 21 Oct 2025 00:20:24 GMT  
		Size: 49.0 MB (49046121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c68013a317d7d802bb25c57a724c8753caec2fc7f0e78fc13f9a38fd22ecd4`  
		Last Modified: Tue, 21 Oct 2025 02:44:25 GMT  
		Size: 14.9 MB (14879264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895fddf2807e047e5b02e5418fd04d343d3e9b5b393b2f3f0cd6704cad44b8f0`  
		Last Modified: Tue, 21 Oct 2025 04:10:49 GMT  
		Size: 50.6 MB (50628495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef331acdad14a3d1bfe859a1c645cb9f4b9526e16e3fed550eee6b86681db7`  
		Last Modified: Tue, 21 Oct 2025 06:17:35 GMT  
		Size: 168.0 MB (167976463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3368bfe50125e3bf39a5265dc0ccb9fd1b42e11bb09ee31f11cc20595deaf608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c802e9b0adbcab3d7cc2359f79d7255992840a83993df410ba77eac7e061a5f`

```dockerfile
```

-	Layers:
	-	`sha256:345b610bcc2368229c8e5fcff25890b88a7e61f829a2de5c482458c9abdb0d74`  
		Last Modified: Tue, 21 Oct 2025 07:20:07 GMT  
		Size: 15.3 MB (15261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9818b9a10921214781d18b9bbc0c05d5ef32a7135a04ba96610744d96177f36f`  
		Last Modified: Tue, 21 Oct 2025 07:20:08 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ae55ab81de1fd13c5016fc95a8492afc63251cb917e8bb80ba3d14b09ef3a22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312927377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f93d5a3eb7b96dd233bf59456519c2c2c05e5caadc83bc4fcc5a36fd547968`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed44f1c4305e990c6301b16db5ccb0849b5044d4eab021969a1274b1471f5cdc`  
		Last Modified: Tue, 30 Sep 2025 00:13:37 GMT  
		Size: 15.7 MB (15749303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06d88b67dfc22f54e531fe9bee90e889b90f5349a5ac5473af85c6967813b62`  
		Last Modified: Tue, 30 Sep 2025 01:19:29 GMT  
		Size: 54.9 MB (54854173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705d2ba96dd463edac2adb77d43c4a9b810f851ab1a5829ebe7689e44d0f7be0`  
		Last Modified: Tue, 30 Sep 2025 03:14:14 GMT  
		Size: 190.1 MB (190066487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ede147c2718c1fe531d21c2be1d22c635b5208618c093df104eced58dfe3163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15474435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7be99f772b78ed5ac225292cabf8fb8d2c7d8ee0f644d1024ee59d5ff037fd`

```dockerfile
```

-	Layers:
	-	`sha256:916e79c8752fa1fc9af6a8bf5664296a379544be446e4f0f233c4342b467e649`  
		Last Modified: Tue, 30 Sep 2025 11:45:52 GMT  
		Size: 15.5 MB (15464117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17add489d2c572081c238ecf543bed7921b3f471c571d05a2b3fb2187d9f140c`  
		Last Modified: Tue, 30 Sep 2025 11:45:53 GMT  
		Size: 10.3 KB (10318 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2cb612a26378d0aed6eb1dcafe7fbab2406a871afb1dcd53f83cecc7e1d2f07f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327087494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702282fa944f31cb5b2e33d2d238e28535adba7e51e36131d14e71a224301c3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ceabdec1cb201cbc144cbbf99606ecccc3942e0acc3ede261d7cced4e3f632e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:34 GMT  
		Size: 54.7 MB (54699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f70b590df86e9bb29cea47ff5206076a14d6ec7a2d599a47314d5c807427f8`  
		Last Modified: Tue, 30 Sep 2025 00:20:26 GMT  
		Size: 16.3 MB (16267769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eba0f07bb8b54d93c18e8046612f1ea91d973cf657c81818dae53819cabca4`  
		Last Modified: Tue, 30 Sep 2025 01:19:09 GMT  
		Size: 56.0 MB (56048318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9a76224e821b712f885d4efba8fb9713f9df95b875fdaa6a888fe9cee5bb33`  
		Last Modified: Tue, 30 Sep 2025 03:14:26 GMT  
		Size: 200.1 MB (200072162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2aa8f05ded14cfef740b6a35291cebecded1a3fb25e257b7f9f0aed79135c269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc042b1647cf93c43b398e03c522dcc0be86e69140b0205d907dbffe84f9fe0`

```dockerfile
```

-	Layers:
	-	`sha256:f65fa2943a33cd351c725a0642eaf55009b47cf37c03ef282c4c2c47271cc2d0`  
		Last Modified: Tue, 30 Sep 2025 16:36:46 GMT  
		Size: 15.5 MB (15450187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5d153f8f7fd8cd36eaf5df0cac0f814737f25ee594506aefecbf1381ebc7f0`  
		Last Modified: Tue, 30 Sep 2025 16:36:47 GMT  
		Size: 10.2 KB (10216 bytes)  
		MIME: application/vnd.in-toto+json
