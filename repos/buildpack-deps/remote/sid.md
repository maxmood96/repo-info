## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:c470272696bf3a5fa5a2df46c7125f2619f56af44ffa38c4ecedde04a3e4a8ce
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2cb9d1e21230a34d2756ed3bc7e7c2974c7e2719d68bd4b91d0d3a508f51570c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334556179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942834980133fa8c3d0d1ce767c50b59f2a19154fd308bf3047b03ca6d066eed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6b1598688dd5948f64dc955f58b0dcf5627fc6bbc5754f5ea08612c6d3bace8b`  
		Last Modified: Tue, 10 Jun 2025 23:26:12 GMT  
		Size: 49.3 MB (49263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cec2bdcd950987565d27e6bef170159a9fdde6f46531b0889933354046db48`  
		Last Modified: Wed, 11 Jun 2025 00:01:47 GMT  
		Size: 25.6 MB (25603931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbea8bacad06666c3210aff4437aaea1773f797c5f0e58c28f9f9d0f3ca5ec62`  
		Last Modified: Wed, 11 Jun 2025 00:02:53 GMT  
		Size: 68.0 MB (68042724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b1a15ead1fdc2b27741cd129b839bf3c769c50fda44e4c60084fb500a01680`  
		Last Modified: Wed, 11 Jun 2025 06:50:39 GMT  
		Size: 191.6 MB (191646207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:225762f5db004be7e702dac553662d84fb88cd9c5d2caa3675385decb5738c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16321843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37317bb4186b26931fe654152af2e331d5d8de08f8d682d3d870cb7a835daace`

```dockerfile
```

-	Layers:
	-	`sha256:077164af1f646145cfcf31f5a72df654e06d6b326a74a375ac45f4e6c70cc8a1`  
		Last Modified: Wed, 11 Jun 2025 04:20:45 GMT  
		Size: 16.3 MB (16311667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff00ebd206d719e4d5ab0b8f80e69a328f5d8e3a9b4e7ea48aef6145fb1bc00`  
		Last Modified: Wed, 11 Jun 2025 04:20:46 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7f1c8fa4d15ce5a71703cdb0924ede66bde31c60fb1c354bca651e0e3bb61030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299719569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e2b8b561df5a7771e37fc228d404544208d42aac4cfad0f8d0b811964c9385`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8344b2028cc05a08f8b0b577cc9430fd30421d98f7302a20cc79a7392635ca51`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 47.4 MB (47435203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e8ec6927bc0cb7d56e990391b853ec23d7d3eb74a5f1f9500df8d5cf23ea4d`  
		Last Modified: Wed, 11 Jun 2025 03:13:46 GMT  
		Size: 24.3 MB (24328621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2085f136199cc5a804201375aeae18b933264b5486014fd2d2c46cfb68e131fc`  
		Last Modified: Wed, 11 Jun 2025 12:21:44 GMT  
		Size: 65.6 MB (65640755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e204187b29a43e4ec106f4ad6c42a78478cdf09f7ab0ba5d8e27c8151c087e`  
		Last Modified: Wed, 11 Jun 2025 09:09:16 GMT  
		Size: 162.3 MB (162314990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b21303a657b816d65c5263c412f255a390099185975b10380173d9bf98c1f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16093223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d204d4905184e5ee7c1e755b4deb5111287485f061f8e7e1e4c9c3f111986323`

```dockerfile
```

-	Layers:
	-	`sha256:b675300656ddb88f39d9241e4f5c3747e64f5e8fa9c0b1d619fbdabc94eac2f8`  
		Last Modified: Wed, 11 Jun 2025 13:20:43 GMT  
		Size: 16.1 MB (16082987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5315cb718648785f3f1ad5894c2bcabbd95026f0f38c90becc8385e6a2739593`  
		Last Modified: Wed, 11 Jun 2025 13:20:45 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8b8fd75c6ddb76e7b6881b9c175217bc3a5ce876a69d29e9baa9d16e333dfdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282940363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c319a7e8cf2224dd89f312ee6607fcd89ac713d094d8409954c4d63d15fea165`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ceacdda8a07413d9c26c141b0f4894fae020e6ab65ff0188cce0bfe5e0c66eb`  
		Last Modified: Wed, 11 Jun 2025 01:10:03 GMT  
		Size: 45.7 MB (45707825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b841f0ab46f7d7bc86d75d499d470af27c2315d80feaa41746c1f9e6d995ef`  
		Last Modified: Wed, 11 Jun 2025 04:58:57 GMT  
		Size: 23.6 MB (23601456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b703c4341425792b641192b1633584b31d3164c5bde6219fcbd37175e45bb2`  
		Last Modified: Wed, 11 Jun 2025 13:14:31 GMT  
		Size: 63.0 MB (63015556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85b69e87c980f17dd8f84b28e8ed63351b861562111262841aadfece81db21`  
		Last Modified: Wed, 11 Jun 2025 18:16:37 GMT  
		Size: 150.6 MB (150615526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b991eace02c5615fdcc2952969649857e81e11b254db148210b239655e3033d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16089514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71f877033c49e07c0bb438fd522ecbf82836fdca41306e8d94daea3773c998`

```dockerfile
```

-	Layers:
	-	`sha256:e22d8be388602630f8bf1e2c168126766d2da5e743944f08176826043604b2a6`  
		Last Modified: Wed, 11 Jun 2025 19:20:49 GMT  
		Size: 16.1 MB (16079278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9175abc5f34b57c60dee48d2014d51039d08acacf328f3aeb52ccc42d6f59af`  
		Last Modified: Wed, 11 Jun 2025 19:20:50 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:36cd5d886223ad0244c348bdfb7fb39b3903261824a40c868a0655499f756e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324443256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e059b179e8903cd6d253c5b824cb9f3470ae69199397a38c9c6b347ef84ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4b10e85b1b46df396d3cb4118de7b2483607b89bcd163318c9756c711f9a3ef9`  
		Last Modified: Wed, 11 Jun 2025 00:37:10 GMT  
		Size: 49.6 MB (49629348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae44e59140036c47291ca98d6f5cbe09bbc2c6ff2f7067e6ed8f93f2a9ed0b71`  
		Last Modified: Wed, 11 Jun 2025 08:13:09 GMT  
		Size: 25.0 MB (24998868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1842d0d17df930326b268986cae23d9f266eff7b38d9a7a69d040cf74bd3fa`  
		Last Modified: Wed, 11 Jun 2025 15:10:50 GMT  
		Size: 67.9 MB (67901215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ae760546480e2453321a26fc6dcd7c752fa657059171a38f48610465648727`  
		Last Modified: Thu, 12 Jun 2025 04:48:58 GMT  
		Size: 181.9 MB (181913825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2b09284e54963b7549251fad2e9ee20afc2fe3636bec66f924f607104d194105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16406082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5900153655dc6bba17d6c667f0688789256c46642a4ebe02170621e40c1c144`

```dockerfile
```

-	Layers:
	-	`sha256:d314350ae1e0c9f056d82c8c7de3429deb936164a01bdc3ad30a225e3b11f091`  
		Last Modified: Wed, 11 Jun 2025 19:21:02 GMT  
		Size: 16.4 MB (16395826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59835d3f84b9f5d5710097a36114bdd56d15d34a5abaf46379e13ad065b4059f`  
		Last Modified: Wed, 11 Jun 2025 19:21:04 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6657cffdf30e0c2d8ed41058489d44a657f1fa80f9943fac04775b586378645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342894158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b5930cf1e788ef575b61ef4f91afbcb635653e442d64d3c9c02d6413bb694a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a1a02b91b1c2266da4734f34b831bb020d740f7bfd0647d1828242b377de717`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 50.8 MB (50786017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c1899ec001f75529ee8cd455eb4a23c4b9c5414c63db7730474213c55437b`  
		Last Modified: Tue, 10 Jun 2025 23:36:16 GMT  
		Size: 26.8 MB (26759161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521cd224c201b94f36b1b9e6ba5db4b89c6a8f696946eeacb5bc6b1ac6ed6f5a`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 70.1 MB (70135021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9f8295eea0ba780cc76f5f5386ee69e8ded62413d3c410f0c2e4115397fe2c`  
		Last Modified: Wed, 11 Jun 2025 01:14:52 GMT  
		Size: 195.2 MB (195213959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f821e02088d7ac0ed211fd203253a025afa9e2976d1f805536ee219429c88e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16291688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86959247ea0abba2df79d3138d75914e206d769227a6182945e4933a0830c6ae`

```dockerfile
```

-	Layers:
	-	`sha256:53c7b3cfc966152c77a7f74201f1cfdf9b55f0bbbdb827cd8362d105ad4bec4c`  
		Last Modified: Wed, 11 Jun 2025 04:21:39 GMT  
		Size: 16.3 MB (16281534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a779960f8cc74acbc1413a545969066bc5af083af37b00114965844c8cbe25b9`  
		Last Modified: Wed, 11 Jun 2025 04:21:40 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:39e2aea94bcb83ff5174d83f77cf91775102cc589eb06af5fba1f88a2f381eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313831045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8220b3082d1ab8355804f02e65fc8726abc1435dced31fe215a33e1469777b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:27b34307efc56192fd4ca945f6323e2158a324121ac08b2b6be4739d1a7a2345`  
		Last Modified: Tue, 10 Jun 2025 08:48:47 GMT  
		Size: 49.5 MB (49538322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff848add2d23cbb649ad48161ea5c02c3695dbc152c477b6b7b6ddde8893826a`  
		Last Modified: Thu, 22 May 2025 06:18:44 GMT  
		Size: 25.6 MB (25629837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0328e102aaf6d1ba040810e1f44f2d4a53bb52688eaba926e1237110a438c0e2`  
		Last Modified: Thu, 22 May 2025 14:32:23 GMT  
		Size: 67.0 MB (67034333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f904d88e08bbb9fcf13920ac8532537a0d9caaf511da40144a066c17e06ec17`  
		Last Modified: Fri, 23 May 2025 04:44:02 GMT  
		Size: 171.6 MB (171628553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a449ee4a68377e0621d1c6703334173c33422f7ca17f822007c936e1661f4e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69347511eeabfeb20c79083b7e2e78e7e25be862af8422b6be584e551bfae57d`

```dockerfile
```

-	Layers:
	-	`sha256:07870d3074339ca747ab1a9c8b9c4196ddf53c76c4e6215e1750e14031ee8347`  
		Last Modified: Wed, 11 Jun 2025 04:21:51 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:405ebfacc917de4974d7f2bee2168e041b4f7738724e757daa105d13b7a63102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338824891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f63b539aa4e5f6616c7ae054c091bfac68d5af5e9a0073797b8f60e35fb0d02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f34e3f5941a9b9d7f66cc62bea1f477c727df8c87b640bd63d443c8cb4c08203`  
		Last Modified: Wed, 11 Jun 2025 00:27:42 GMT  
		Size: 53.1 MB (53098680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f227a2066e39def58b490c6183c1c743b3db44ed881ae2f1d7f6c8febfbc6b1`  
		Last Modified: Wed, 11 Jun 2025 17:42:13 GMT  
		Size: 27.0 MB (26983625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fa176b0ee9b3a9a511ef65649d379d0d0d4e1a342fc2d3e54b6d5e65171edc`  
		Last Modified: Wed, 11 Jun 2025 19:14:57 GMT  
		Size: 73.3 MB (73341809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f7364d6157bebbce38c131919d7b9d1b2f458adde75b9ad55512c9af3ba4d9`  
		Last Modified: Wed, 11 Jun 2025 20:53:15 GMT  
		Size: 185.4 MB (185400777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:70980a08aa1394c1ebbcdf93aa5f8310c84228c38bdd4efd50775d0927a74201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16315853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24c36116feb0b1ca72b8ee5d5f675a01addb6a76f91bfd759bc2288eaabdac7`

```dockerfile
```

-	Layers:
	-	`sha256:aac84d0e21e0f647666340ab9ca753cd12e18258cb16630550fec6fa535d0b4b`  
		Last Modified: Wed, 11 Jun 2025 22:21:00 GMT  
		Size: 16.3 MB (16305646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cefb0ce04c7ad2cbabaddb8c380d197d24ec3474c557b623aae2c824600309de`  
		Last Modified: Wed, 11 Jun 2025 22:21:01 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a0dd658780d047e539158b05c8c5b1cdbe503fcb2c8b0dc974c7bdf2794702d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.7 MB (408710519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becbb47ea3cb2020057cf9741e41925888763c53e3802628e7647ebb22f1f264`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0009e91f3f8c4153a02b39dc6e9b3c5a36cc3c8e1a157d73e8f9e91097515059`  
		Last Modified: Wed, 11 Jun 2025 02:03:30 GMT  
		Size: 47.7 MB (47749671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df49454d4e709bab7fd6d2461b736d24ce3db865904adb84e1af7a3e0716ace`  
		Last Modified: Tue, 10 Jun 2025 23:34:49 GMT  
		Size: 24.9 MB (24939799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d5419b50e53679e06a4b73e768cb2cd1c6fce73cac408ba77b0431e99651ce`  
		Last Modified: Wed, 11 Jun 2025 11:59:20 GMT  
		Size: 67.0 MB (66986454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f950540a50cc2731865d0aa17fc70a43bdbc08afb050eabd1313dd204e4d0c`  
		Last Modified: Wed, 11 Jun 2025 17:21:27 GMT  
		Size: 269.0 MB (269034595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8004eef293e05714210672f63a3fa38652b5c00c8b22f249ac3f73c7938faf46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16377682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915e43b25710087d1913b9bd40aef3c830c1838b052b8b56c9e825bceb76a9c9`

```dockerfile
```

-	Layers:
	-	`sha256:e97688eef277ce3f2103bc4ead9fb6b38197bf6453ed7f3617303fdb90d288fc`  
		Last Modified: Wed, 11 Jun 2025 19:21:39 GMT  
		Size: 16.4 MB (16367474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c942feb7fb223cca67fba734862f0c2b2d556a640f08add653a51d2ee9d4d4da`  
		Last Modified: Wed, 11 Jun 2025 19:21:40 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d57c7ad545bc0c38ab2758c2c2a06f75a1e06b4a728a32366c81218428670ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306499661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8026cba8778485ddeea5c4b6f063f257ccefd75c9b722f137f829ea2e8a2aa3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a52b4c8ce9959e1107790b0cf878188904eecb5b1ccf411d93d6ab16036dc160`  
		Last Modified: Wed, 11 Jun 2025 02:03:33 GMT  
		Size: 49.3 MB (49343092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0965e23eb9d70e72f15582a2cb686bcf1857eb924b4d704542fc37d206146`  
		Last Modified: Wed, 11 Jun 2025 02:51:24 GMT  
		Size: 26.8 MB (26769281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc44cd2b9aa97b3fbb56995ed62a657167162e1278b818c7bc6bd60f13d1e12`  
		Last Modified: Wed, 11 Jun 2025 07:20:39 GMT  
		Size: 68.7 MB (68689048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a662117a21d6756827011b9a9ab400fa9db860df9a5da8d3d1a1a8597172c7`  
		Last Modified: Wed, 11 Jun 2025 11:00:40 GMT  
		Size: 161.7 MB (161698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98a10f6e1cacddf487ba9d6cc84e03a9aa69ff01ad2c3ae1f7e6689ac2f67da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16088768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38867d0847e9aa3cc7858d65dbb7277cecac6ea10846276e2eeea3f0070a6a87`

```dockerfile
```

-	Layers:
	-	`sha256:6c5a5481488bbe4a9be4f7f0a03b2001cca8feeeb6e48826bf380c6b6bcc2649`  
		Last Modified: Wed, 11 Jun 2025 13:22:04 GMT  
		Size: 16.1 MB (16078592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922e6e6f9518f191e7921c07bad9fcfd114eb50637eb14e095a971de69370ca0`  
		Last Modified: Wed, 11 Jun 2025 13:22:05 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
