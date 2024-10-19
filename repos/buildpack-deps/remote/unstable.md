## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:d668f255f8b7986d465dff2f90136efde590f3371baf8523a19381423cbf2588
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e8a9bfddf607e07c59acad6b37e74a677f55b222264fff4086481b94f103248e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.6 MB (368573290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608313d91b8bea5bfdaa7ae32f69dd84b19a7f528219c5ce18cd67955c1d10e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a14dadd8caa2d3d30409f89a0e500fab2dca15c8214c05e428a7ac38fbb7b22`  
		Last Modified: Sat, 19 Oct 2024 00:54:54 GMT  
		Size: 20.6 MB (20558732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b881a2f1232350ec7e4aefdf5b77bf5210861f5960ef5f73da8c0d1966802d8`  
		Last Modified: Sat, 19 Oct 2024 02:06:29 GMT  
		Size: 66.5 MB (66470763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86943b23dc3779237d892368b9a4c4fc090241e0fbaaada00b55b3055d2b3bc9`  
		Last Modified: Sat, 19 Oct 2024 02:53:08 GMT  
		Size: 228.3 MB (228271921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:406de61fc1deaa52ed02dda2f9335e5a3add1c139b419573cf5ce61aa0e5df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16623042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996b9f714262ed15f13040714584face383fd4a6b534fb51a47c89f857d30b03`

```dockerfile
```

-	Layers:
	-	`sha256:912cf800b3ff32bb074626dd668053449112fc6e0bda6515290514d72472b67f`  
		Last Modified: Sat, 19 Oct 2024 02:53:05 GMT  
		Size: 16.6 MB (16612866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccba7f94f8614c179b40098212350a18928af7d09ff485a475fb59ede87a07e`  
		Last Modified: Sat, 19 Oct 2024 02:53:05 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:81d8c0d6447b858edb105c6f0d36c43e69aec3fc28802fcbaf946a89dea28cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.9 MB (336917228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7412bb66380aa2cacb805f58d47eae5dade33c2b198a03442dbb0692588ea268`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4907cc8268897b865af11c617e0b6df9243de9b6a7c9d42c7a265f1e626be0e8`  
		Last Modified: Sat, 19 Oct 2024 00:55:48 GMT  
		Size: 19.6 MB (19568622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66f2bedc6e003c8fcb6ddc00648906d674fc1d4c5b2e82a6680469e7f789b52`  
		Last Modified: Sat, 19 Oct 2024 02:56:49 GMT  
		Size: 64.0 MB (63986649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04edaf6ae2335470c9d8311b7a345d75de126b2f02dd715d304da44c5f64abba`  
		Last Modified: Sat, 19 Oct 2024 03:57:16 GMT  
		Size: 203.2 MB (203214369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd85f413c3b3ed859c238623e26cf465b4f4c9b855f6586be56a4abe6b21da2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16415618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88332ab0b27baf8b09d361fdf44444b685330ce1bf18524e66aea9097f48efc`

```dockerfile
```

-	Layers:
	-	`sha256:03176e842056c7148acc1c01266fdb48b6ed4fed10209dc5fb56678c7787b544`  
		Last Modified: Sat, 19 Oct 2024 03:57:12 GMT  
		Size: 16.4 MB (16405370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d9eb51d09371e1da56b276c69c0d0527b03d56aa50549c1257d44d3f09b05fc`  
		Last Modified: Sat, 19 Oct 2024 03:57:11 GMT  
		Size: 10.2 KB (10248 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:515c123d32c6aa7255a21ad574f394666fb16d3c565f24fa15b43dbcbb1182c9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318104301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036ee1ccf0154b3ec16d5f2b9555c44031d50cb756335a8bc0da6d1f3ad98246`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 03:04:18 GMT
ADD file:bf9375f2b0e5c66c0a1840e13cfa8b3f0aa55934d9c92c13e479c8cf7909e923 in / 
# Thu, 17 Oct 2024 03:04:19 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 03:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:31:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 03:34:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cf1d8a933c6efa9a7129c6faf202eeab8feff677f32fbc0037a3ab76003edcf8`  
		Last Modified: Thu, 17 Oct 2024 03:09:00 GMT  
		Size: 47.7 MB (47691399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbd60cc121d929130eeee92fc8225e4ed5482cd36b62a951095ebafb943c0a1`  
		Last Modified: Thu, 17 Oct 2024 03:38:59 GMT  
		Size: 18.9 MB (18896921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32490c623445d27e949376c8158021571cd8530fc358794dc7642b8bade85da`  
		Last Modified: Thu, 17 Oct 2024 03:39:18 GMT  
		Size: 61.5 MB (61463673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeb9fde67196f11fd2b11fdc769e780383d757a9acd06f324a681d5a67d9f62`  
		Last Modified: Thu, 17 Oct 2024 03:39:55 GMT  
		Size: 190.1 MB (190052308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a5bff4e6897ef7ce3d60f235ece06477a670c718938744616f5c5be5f3cc0dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362218506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4617705cb588626ef2ee3fd18d59a3c8c267abb961000229b9cada35dd22a8fc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b80bac00a06288366529b5187b9485c685d4f46018bcb866049abf9f952247d`  
		Last Modified: Sat, 19 Oct 2024 01:11:43 GMT  
		Size: 20.2 MB (20196615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19663fa8e0a57915a50484edf1e2599200b05cd9b029d04f6246f46e4ebd7b8`  
		Last Modified: Sat, 19 Oct 2024 05:19:11 GMT  
		Size: 66.6 MB (66554364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a1930b82ab676514849567fb2f84c77abe6dd46e00fdaf27bdffdd5e50852c`  
		Last Modified: Sat, 19 Oct 2024 06:19:49 GMT  
		Size: 221.8 MB (221838042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aee10b071d72be87195fdd239fc32f4bc897cf5365082395c39d748923726e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16719540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce06ab8b69758fa40926415c0cc6e0fc487417847973ce13cf61898b34595a31`

```dockerfile
```

-	Layers:
	-	`sha256:0c705747a331f205ed3932bd8aebffa27283a5197af7462eb8b34649f08b2b6b`  
		Last Modified: Sat, 19 Oct 2024 06:19:44 GMT  
		Size: 16.7 MB (16709272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88f34d6a5ad6f6573131d992417c533e6d9e3aa6754dd91f84650909955ea149`  
		Last Modified: Sat, 19 Oct 2024 06:19:43 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2586af5cbad80ef32c8987ed795e71f33f008118127d124c39f84dbed46b6b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.2 MB (373211235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c837d757dc27783ca87e9a16ccfd7676c7adbd00fed98d27616d3f6a128eb548`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778d1412c3e0a18773ad9511a1dfd5c117b0ffdc0c988451759a39e13c6a3c9a`  
		Last Modified: Sat, 19 Oct 2024 00:54:56 GMT  
		Size: 21.7 MB (21665152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c29126a4a4aef17404bd71b479313e117a2f9ea628fcde52f725427fcf1c14fc`  
		Last Modified: Sat, 19 Oct 2024 02:06:42 GMT  
		Size: 68.3 MB (68288819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4c0958eccba088614505337cf12f450adb63c3426aaabbf6f2e56318550eb2`  
		Last Modified: Sat, 19 Oct 2024 02:53:33 GMT  
		Size: 229.1 MB (229139287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:72362d081c1bb8ae447bdca140fe2a9ff70d2754d3d9517a7dc02825a86b3101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16593424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb16d25ce0b74d32d0f00b676aa5ed31860af3eb2f992e62cff99c66b2f57b9`

```dockerfile
```

-	Layers:
	-	`sha256:3cc7643878c4a97b1d4c557d239ab4a5318d6bdb4f9efec20c5580b6184e9a7a`  
		Last Modified: Sat, 19 Oct 2024 02:53:28 GMT  
		Size: 16.6 MB (16583270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b43d99e8ed8a3e4a6aedcdab18d8a594b76680efaf4b6f36e723a7d3040ced62`  
		Last Modified: Sat, 19 Oct 2024 02:53:28 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7aed501446d1d4aff5e4e665344ff39c2bb23697f79269ade9d17d43c74bc637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346369313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d558ca969f15110f47b12e6e5f8ac0b3c2bc1d5aef4bccd85c13c7d012683040`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35efd481e6347988498fa292e64d8b2f0d728f327f48bccb1d2c2bf371f2f1e1`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 20.9 MB (20887623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d42e894e27bd8661997e28ccc989f4b18c73e3892449a02653f995d796aea`  
		Last Modified: Sat, 19 Oct 2024 02:11:09 GMT  
		Size: 65.3 MB (65280292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5494e53db7cb17f11f8f3553b0b8f89e494429f535472ab40c3dc0a4a53a958b`  
		Last Modified: Sat, 19 Oct 2024 03:09:12 GMT  
		Size: 208.0 MB (208043499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0c7f47bdc09a05b6d948bb27b33411f3b5a300b2c8d1c54d84eebe0c13592d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52a53cd41b52a2ffac4c7c5eff91689862f82eab42ecf464a1ad8ccafa36f61`

```dockerfile
```

-	Layers:
	-	`sha256:c6c4c3b65b2f2ee5188b595c005cab57e11fa88adc238818500a0f9d289bb37a`  
		Last Modified: Sat, 19 Oct 2024 03:08:54 GMT  
		Size: 10.0 KB (10021 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6e1614575430aae725ce4d1ca72a021b64b14a73524639c6866a13aba370b80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.0 MB (378020992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972288b37cca39db49db1bfbe29a851813a8543f0a7f4c72ce65531923b42a8b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f3cdfb0755564cd3c4456a7fa23e621d79e4f8f43bd8107c734f66d381334`  
		Last Modified: Sat, 19 Oct 2024 00:57:49 GMT  
		Size: 21.9 MB (21944061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fc954d509992bc0347fcedb989b7696ca6b5029587c5a3cacd05686fe99e03`  
		Last Modified: Sat, 19 Oct 2024 04:08:51 GMT  
		Size: 71.9 MB (71893560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e8fc7c4002604d4ecd95f73b88e6577ffdafa0c5d8add4adfe85a32b924574`  
		Last Modified: Sat, 19 Oct 2024 05:20:49 GMT  
		Size: 227.0 MB (227006547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5a372eadfc10bc82dad638f92376f112fff82b71cd161e5b05c835e3e4d7423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16621262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46ae6569046be118b2021b37e251e01f3d851d6b370fb2e380a09f956b1c437`

```dockerfile
```

-	Layers:
	-	`sha256:4b845df74b1833d65eff42db4f1e60c04ccfa5b2e99372f560c60ba8e33d6eff`  
		Last Modified: Sat, 19 Oct 2024 05:20:41 GMT  
		Size: 16.6 MB (16611042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:080d4475f5f734ac76d094f5229cb78e77712607292807a5e1b8fba7c54e82aa`  
		Last Modified: Sat, 19 Oct 2024 05:20:40 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9170b718174b1a2155dc6f1f30be5d257ea77bfb5cfd20c8b882eb76bd970ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.9 MB (449863543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578f59755f82ae837d05d043953beeddcd5bed8e73b690b8f7d707e36ed9644e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de12fa48532c87115805a1e3efbbdd980575096676ddd00868f642d72782b610`  
		Last Modified: Sat, 19 Oct 2024 01:03:17 GMT  
		Size: 20.0 MB (20023981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c05579e9b49f41a2b6960286d8ab9b1d090127915ab4b5f2c9ec35e3db7815`  
		Last Modified: Sat, 19 Oct 2024 03:48:10 GMT  
		Size: 65.8 MB (65756980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1c1438a38b6b5f19898954943b519c13357a75b5de527c10fdfa839a2bf9bb`  
		Last Modified: Sat, 19 Oct 2024 05:19:52 GMT  
		Size: 312.5 MB (312519897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d4efa39a2089a0bae14fc598dc2be9721c56cf31ca6d013b630959dd86d0a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16684099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c950fcfad2f9ac619e283071159fabbe0d2519f685c971de572607a5a2ab72c`

```dockerfile
```

-	Layers:
	-	`sha256:c00879de8cdfbb4f86a8411d81ebbb57bfefc3b7b5517bb5e81cdec0f5d57951`  
		Last Modified: Sat, 19 Oct 2024 05:19:13 GMT  
		Size: 16.7 MB (16673879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7759997ee312035b99e28a615c8b12688bb5567df93ee0be4e659c908478b864`  
		Last Modified: Sat, 19 Oct 2024 05:19:10 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:03ae369846cbc99feaec0d7a675c3f1cb296806fe18be3ea3f2b2fcd60ecb688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343811634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2955362ae47bf0486452d86b59e314d1f8357dca737a96af3e6f917fc1c7969`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD file:2f1a819570e851a9bce2342f32c7927abdb02af08d5e469e6f5d41a193235bb2 in / 
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79590eb16acf1f35f7a00e8c30e7daf7ed5d8bc9d65ff782665704f532af0ac0`  
		Last Modified: Thu, 17 Oct 2024 01:50:44 GMT  
		Size: 52.9 MB (52851981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf56c8e1a853602c0af0f40a2561d6ca90c547c99b9bdd2c5349a88e1f5cc1a`  
		Last Modified: Sat, 19 Oct 2024 00:58:05 GMT  
		Size: 21.6 MB (21639639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a7102bce19ae53b519fb58ec97dd26aadbdffdfec95cd2613f51b842e60866`  
		Last Modified: Sat, 19 Oct 2024 03:47:42 GMT  
		Size: 67.6 MB (67567932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006e2316904bd5e5d8b5be83f2d3c16ffc8b744bd23f895fab2465c751a090a2`  
		Last Modified: Sat, 19 Oct 2024 05:06:51 GMT  
		Size: 201.8 MB (201752082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ba7e3ba1bbeac3a6078f008e5ee17b68529098e3909600dfbe90edb605f54c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16414228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc84b27183ff88f33658ac103e14e91bb216a76083e15c060fef435fa42bfad`

```dockerfile
```

-	Layers:
	-	`sha256:1ee265a8788e328e9fef94039d90ab4df6d624dfc385d1e5faa95efe0c935af1`  
		Last Modified: Sat, 19 Oct 2024 05:06:49 GMT  
		Size: 16.4 MB (16404040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:306d2621686c7e09b57487558deeb4f574d7074bcde002751c60c8186e07ee0b`  
		Last Modified: Sat, 19 Oct 2024 05:06:48 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json
