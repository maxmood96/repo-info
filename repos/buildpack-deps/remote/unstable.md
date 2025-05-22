## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:894e809a892ac759854001a8a65536d0c9ac30ba9135eb83a76bbafec210bf25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:60949139e0404aa4e8bfbc72a5f4026b4eefc2a9099ca8f8f5c125d1650f3925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334454470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af567b7e90c831565925eb290b259d59001da957c00379fe23e75b75e6a871a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:21c8f2db1ca60de292da0e982c4bd4b81bfe468b8d652fac5b9003ceedf12013`  
		Last Modified: Wed, 21 May 2025 22:28:04 GMT  
		Size: 49.3 MB (49250549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d79457730a0db09039cff8714fa8c41f073c5bed3529b5417fcd2b8736c7b`  
		Last Modified: Wed, 21 May 2025 23:20:43 GMT  
		Size: 25.6 MB (25585150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedcbbec8ebb5599a6f3f7c58410495e59f3b554270ce0b5227dc68965286c92`  
		Last Modified: Wed, 21 May 2025 23:38:03 GMT  
		Size: 68.0 MB (68019464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7711fab4f4cd78e37eb5166cfeb7e6fb24a203796a4d199054e65a9c5fa0a2`  
		Last Modified: Thu, 22 May 2025 00:12:55 GMT  
		Size: 191.6 MB (191599307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4db6756cbf50482faba9db27bbd3999b7f566da0fd71f580241c2510eb03b75d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16049858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc28e67fc91f379b1d590df8190920f2e8bbff9407ea95cfbbd87bee40f8713a`

```dockerfile
```

-	Layers:
	-	`sha256:d65c99024ef76abc888a6f914255895aedebe20c062c8af8bdfb7f236a355f36`  
		Last Modified: Thu, 22 May 2025 00:12:52 GMT  
		Size: 16.0 MB (16039682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0015a70b41f6c592e48535c74ac6324b55201d696043dd425ebf1d44ac0ddea9`  
		Last Modified: Thu, 22 May 2025 00:12:51 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e2ce147d66563cd957a7bea7f2c44a9a57806614f60d71d406903f3aee121d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299581596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46dc05a231df9fc57ca66e57cf5cb1046f2d1ad8b1df464f1716cac8119f656`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f211461130ff11866a85e649352ceeb2f6ebc110118114f92b30349c5de358f`  
		Last Modified: Wed, 21 May 2025 22:28:23 GMT  
		Size: 47.4 MB (47442893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390184f3e2aece3a9d3a8380bf315948d0d62ca40bd766f23543d583f330b82a`  
		Last Modified: Thu, 22 May 2025 01:14:31 GMT  
		Size: 24.3 MB (24323529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa73818847f3cc7d5638e8f2c0e6dbb5c84e00109279fe366152e8bc162b55cf`  
		Last Modified: Thu, 22 May 2025 04:45:28 GMT  
		Size: 65.6 MB (65632076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95f812ac725e3e7e3203b2f256cf7109c6b5d2fb3bdaacc2268860449d43e52`  
		Last Modified: Thu, 22 May 2025 06:38:09 GMT  
		Size: 162.2 MB (162183098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cc9d7294b52bee5a4bad8f78dd03007ef080351e2857ca507d74650c3b97198b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15818350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c10ed02a2b086127e1a15b09c4f5de7248c8319793b74cab06135b9be3d0e41b`

```dockerfile
```

-	Layers:
	-	`sha256:61d46a3be03c8fe3bd5cf06eef018905c6b810d9faf6b85ac72cf8f7a6c0faf1`  
		Last Modified: Thu, 22 May 2025 06:38:05 GMT  
		Size: 15.8 MB (15808114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291a464884fe965103bd1a3e48bdb492f888b833156909ce169564a9609a5391`  
		Last Modified: Thu, 22 May 2025 06:38:04 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0fe91b2823abb0059a74610002e78de36fff2981413de126df43567c1f96216e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282872835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c27078cf432387030e543a6c4b29f2e246520a5bbe0d431aed77f872c7384d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:766cbe9ca16b5ae7e32cf18657be459754ce87056cceebf6831ed9c18fd8a62b`  
		Last Modified: Wed, 21 May 2025 22:29:51 GMT  
		Size: 45.7 MB (45698630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e723f972fd882067b040659dac6bf0007c9489588821ca8240ce91487131`  
		Last Modified: Thu, 22 May 2025 02:29:17 GMT  
		Size: 23.6 MB (23589756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe087ac4a0ee4d60e25cc222cddf59cdeeee34ea48ec3d3c1cbcb898be35e05f`  
		Last Modified: Thu, 22 May 2025 12:13:22 GMT  
		Size: 63.0 MB (63013467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa29825fcc6086962844c477c67d2b74406b6d95d3b6b775eb5b504d858d2e`  
		Last Modified: Thu, 22 May 2025 15:36:21 GMT  
		Size: 150.6 MB (150570982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2d30bf7dddc3d1e9a64703611fc405d9d51713931df116f1e8778195e1704c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15817508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a435871beab3ae31c3971b511f1f5d1e4b4ff432a2c62151b4c8d7dee8578326`

```dockerfile
```

-	Layers:
	-	`sha256:9658b68acbc3b469f28b117f78e338d308ce70a79917d12d64040ab2b3b6e4d8`  
		Last Modified: Thu, 22 May 2025 15:36:18 GMT  
		Size: 15.8 MB (15807272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a82fc9b3cfddbd5e14da74bce9c1343864292b382f6439f5abed64036844bbb`  
		Last Modified: Thu, 22 May 2025 15:36:17 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:08fe5832724b7956c017824d4e5e3e80b2226278e78cf2d36f5c3cb30cc6e211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324300073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9ad869cc435f69d995def276eff92bbb57790556475c1ce15eec6052aa89b6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4d7c750dee99fc4f87ba2d4a7a97efd437e614ec9079e7fbf547ab9ce640bc68`  
		Last Modified: Wed, 21 May 2025 22:29:21 GMT  
		Size: 49.6 MB (49617866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b158d051d6fdc917c4a2f2c9c640867150d5c68a1439dd536c0ff065f9eab`  
		Last Modified: Thu, 22 May 2025 02:48:22 GMT  
		Size: 25.0 MB (24976033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ec4c1b10ede551eb1553f94290e8793e9558296a1221a501ace332d77dd68f`  
		Last Modified: Thu, 22 May 2025 09:19:21 GMT  
		Size: 67.9 MB (67868897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe9a83b4e284c8644e539892c0010aebd2c9ed62f38745ecef178ad23df68d`  
		Last Modified: Thu, 22 May 2025 12:29:43 GMT  
		Size: 181.8 MB (181837277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c76ba4510ff499f41b1a6646530de787111f236d33b8440e03a1576d3e577859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16134090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07035f74e7f08cfff444a10a23e5d32a2f55af04de630d339bca7af3ff6beb64`

```dockerfile
```

-	Layers:
	-	`sha256:1cb475c1e326dde11c574cb71e075cfe22eb1e7217ad5f74c69d2ece628db81e`  
		Last Modified: Thu, 22 May 2025 12:29:39 GMT  
		Size: 16.1 MB (16123834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6971baea913db71dff593e7deb831057b90f8ff0672a7f3deacf54bc815a7caa`  
		Last Modified: Thu, 22 May 2025 12:29:39 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9c97171eefd5a6945a5432c42cf3152a71c9bec4ce76ddded46173dc1c5f98f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342801333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a5e1c3b3b8063c9272e00e3e7b85f336bcd9a98218364f0b8ad9c61b4d0623`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c296d6dda96e0fb26dc4760b3366cec8a0723558334f5c902e1c373d0e43ab6`  
		Last Modified: Wed, 21 May 2025 22:28:10 GMT  
		Size: 50.8 MB (50760379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a77ccac61e5d039233fd2cf7db2ad5fed48827a001629e91bc009eff166aeb4`  
		Last Modified: Wed, 21 May 2025 23:19:45 GMT  
		Size: 26.7 MB (26745468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61c02e4c2f4cf8b97da95199eb210e94faa26e3fbbf359e109faa57c15cbd38`  
		Last Modified: Wed, 21 May 2025 23:37:36 GMT  
		Size: 70.1 MB (70120201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4e229f03fd37c6b9bc4e0d5c0e3e162856aa56d7e0ef3c3bc7e7ed3fbaa73b`  
		Last Modified: Thu, 22 May 2025 00:12:58 GMT  
		Size: 195.2 MB (195175285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c85c4b2f672f81a12e240ab03fff4093c42431024bd548bf44f9a917bf8ea09f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16019715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdc51c3e7d7a551713160b551206dec2d1b7a8ca0c96cb2ffa4bad873d4cb00`

```dockerfile
```

-	Layers:
	-	`sha256:41ce78a1defbb11d46254a13d7fabd832d27e625189d6d34f4a61decd4cdacff`  
		Last Modified: Thu, 22 May 2025 00:12:54 GMT  
		Size: 16.0 MB (16009561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a00b2263ce7f65b59088280bedcad4a0dab7b825ebe342705273573641d15d1`  
		Last Modified: Thu, 22 May 2025 00:12:54 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:955e9f45d95462ddb7c68bf71f39d0bff0c8c7e5790095b9257eee8e8b98ea0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313741095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ceb3df745dd66b7661fcffa5592d8c4b3e331cdd6a54ebe47678c8c7517f4ce`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d206785716d2e915433eb85845aaf9607094981ed3c32854f9401982e23a7af`  
		Last Modified: Mon, 28 Apr 2025 21:11:40 GMT  
		Size: 49.5 MB (49535121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d46b0656b2eaf48d740fb0cc28ea93ea835c76c41dc63d12f18a3fd227d3d57`  
		Last Modified: Tue, 29 Apr 2025 12:45:17 GMT  
		Size: 25.6 MB (25618095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b53c377a8e6571103378ce926b4efdaa12bf0271ca14fa02f969e6c3d97192`  
		Last Modified: Tue, 29 Apr 2025 21:19:44 GMT  
		Size: 67.0 MB (67015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac08213c25ed6d62c60f5a436de9d0f48ea9d0d7e695b46014601a8c1cef4f`  
		Last Modified: Wed, 30 Apr 2025 03:25:45 GMT  
		Size: 171.6 MB (171572244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a2da1f9d2506df2dc7d1751e20784b81b596a442c49d93e45fc2449b4ab0cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd6bb88afc48d8f737bce603e00b63f757ff62e6db40ec33f1567bf944a456b`

```dockerfile
```

-	Layers:
	-	`sha256:f1e9d048e1f22679328e61561f21ac97cae87cd2d5ec2959df95542afd470474`  
		Last Modified: Wed, 30 Apr 2025 03:25:29 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4b9ae7b17128e025ab97c2f2407d51d3bd4e81907ef672f92043ea742d907d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338716615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b3ee1eae68ea0103bc3e8601ee20e3170c31f579cc31eabbe331b3c238fca0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1745798400'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2d320c0b02fe20eeef6a5432aed2b294506f621139378d9f899d155d81d1080d`  
		Last Modified: Mon, 28 Apr 2025 21:22:39 GMT  
		Size: 53.1 MB (53078100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e713da9ea3255a6f791030cf59cd9bdead64cd96fffafbed2a4a6fe1aaeb2b4`  
		Last Modified: Tue, 29 Apr 2025 00:38:55 GMT  
		Size: 27.0 MB (26960240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cab10ca498aa4aa931178447c0fd221d2105fe390900e832573ae0d70bd2a58`  
		Last Modified: Tue, 29 Apr 2025 04:37:55 GMT  
		Size: 73.4 MB (73356141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a860ec664ef616cc952e2b5c636fffadbace1cd95b6444e62cf94fe841533cd`  
		Last Modified: Tue, 29 Apr 2025 08:03:07 GMT  
		Size: 185.3 MB (185322134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f332ac565e9b6113d167ca9b29bec04b1b70f0f3dd2c400471973f077b09982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15933540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a666fd34c44726ace39f4e0ab0ca49e497a5ababfd74d3ba2309978b65967efe`

```dockerfile
```

-	Layers:
	-	`sha256:3f8442a54bf3f155c69d050c54e989cd7bcd4bf60b7e69234be5a7b932e5d3e5`  
		Last Modified: Tue, 29 Apr 2025 08:02:58 GMT  
		Size: 15.9 MB (15923332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a271fb50c2e9053236f60ac8a7865c20df9e08ef421c69a7c540ce5097d24a46`  
		Last Modified: Tue, 29 Apr 2025 08:02:55 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0d83223e3f53c52e666f313ba3a00fe274d50b62d9378f76d5d34f87998c08e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.4 MB (408389960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ec1fbe7245b75d6577550b9de8fea50b78e4ed042956475499949e89e6743`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:70274c6f176412a652733a045be62228bfceb31afa5c428bc73eb440514be7e5`  
		Last Modified: Wed, 21 May 2025 22:29:51 GMT  
		Size: 47.7 MB (47737557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db4d1c372b0a8bcc5558ebc33a0807a079cce1bf7f64840912ce33adbe79d6f`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 24.9 MB (24915395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d77ca161501cc8afd738216058d54ab2ad4f404972c41e87bffedc3f8f0766`  
		Last Modified: Thu, 22 May 2025 01:09:16 GMT  
		Size: 66.9 MB (66891223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5afbeb1d7adfdf8c5da2c61d9a3ddddc1979f60739963d3d305e86b3f0f68d0`  
		Last Modified: Thu, 22 May 2025 02:29:16 GMT  
		Size: 268.8 MB (268845785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f8449c958b0c1612b661417a4ff2f6dcd03a4dda71c56c944c2f3c4f22e72a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16105694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b019ecf8f33e9773567d6e5b57cb867ebad6c897eb1c91ad141ead96fbb51cbc`

```dockerfile
```

-	Layers:
	-	`sha256:27a755c73678df61e7b03ac3b8599ad8a78bf7e837d462ab72673506d2fd9a57`  
		Last Modified: Thu, 22 May 2025 02:28:41 GMT  
		Size: 16.1 MB (16095486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af7578894e3d71d395e9492e0d1ec744692d25f681b329aa2dda5ad518cc77f`  
		Last Modified: Thu, 22 May 2025 02:28:39 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9637254345ee0358e50d9241c5b01e32ae057eda193642857509009daddb5b7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.3 MB (306291431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b73ac55402c2b40e672474e8da0378ae13a686fc0c2cf5e0285d4055601770`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:719077674b144dec5ce39e78bd5eb75fa6363d159411371db443b10356484cce`  
		Last Modified: Wed, 21 May 2025 22:29:06 GMT  
		Size: 49.3 MB (49325662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279b96ed4b6a4d60a4f4cae771f06c0b94acf2fcdaafdb528c367ec96583697`  
		Last Modified: Thu, 22 May 2025 01:02:36 GMT  
		Size: 26.8 MB (26753393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7c2e2b167b6b97a9912e58f820f9ac156c2b2b363c5456b8345d2dabd44b39`  
		Last Modified: Thu, 22 May 2025 04:38:13 GMT  
		Size: 68.7 MB (68668880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a57274db12cc06cceb5fde904f0d342e62e940a0de5434938c00023c6d596b`  
		Last Modified: Thu, 22 May 2025 06:42:00 GMT  
		Size: 161.5 MB (161543496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b670e740aec359154fa6f87a7ad7b30af530b90292afee49edf9e2adfa87c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15813908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ab59435766373f171503ee6c14c9e5a5bc47d110ec3d812d25bf1b4db92aa43`

```dockerfile
```

-	Layers:
	-	`sha256:a22d4b51f99554de578faa7f30466c16c57cd23c25732397a09ffbdacab5261d`  
		Last Modified: Thu, 22 May 2025 06:41:58 GMT  
		Size: 15.8 MB (15803733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2b24dc47ca613af4d54d3814b29de99ad2bdbcf1a3e1927a0b67abd7e3fe37c`  
		Last Modified: Thu, 22 May 2025 06:41:58 GMT  
		Size: 10.2 KB (10175 bytes)  
		MIME: application/vnd.in-toto+json
