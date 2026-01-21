## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:414968e711b0c5cd2ae0e7872c2934a27836c406610e10216d058d3b00679455
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
$ docker pull buildpack-deps@sha256:fd7adb9598a4c5a8cce2839269049cc392dfb01c41753b30a39d0b0003f21392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.0 MB (344049679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91565050906d938723f3b79bf2dc0323675acb3b9bde71ffae9eb599eeec0a0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:10:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:53:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:48:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:743b991b49b557d24658aa3fd7faa6c90234b4433dabd04078e1e4904b8e483b`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48836497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5cc7988ae660728c0f960c88dd8ffc588e150f0fa908011ebc32d0a0227664`  
		Last Modified: Tue, 13 Jan 2026 02:10:45 GMT  
		Size: 27.3 MB (27286782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5befc138bfaea9178db6d5216fd469b66a2ada49e942c1f2136f3947ccc0d34`  
		Last Modified: Tue, 13 Jan 2026 03:54:03 GMT  
		Size: 68.5 MB (68493380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e33a6d75064848ff98029b1b34478c0b0412fc6ad961820c7d3ece54c732311c`  
		Last Modified: Tue, 13 Jan 2026 08:22:37 GMT  
		Size: 199.4 MB (199433020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4f2a383c8345e59b73e0f99c022a6555ec1d1acfdb8dbdb17ab8e8af5ed18bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16269828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9616e4a1507f7862ae053092d3cb23576d73b9e4c836f8e5752ed05f62f56c`

```dockerfile
```

-	Layers:
	-	`sha256:51a048f3320e1c4cbf1447fe1dce91f3260dca5d936ababb73f342ca7d375733`  
		Last Modified: Tue, 13 Jan 2026 08:20:43 GMT  
		Size: 16.3 MB (16259684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68ead0f24c862a9fdb64d9dce37859c261d9c4e267d632a9210814ba45f57575`  
		Last Modified: Tue, 13 Jan 2026 04:49:07 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b0bd13d9b128f79755c056177eb72c96898c9d6bc0f79970eb8583a5094636fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291768102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dfec56c979116f54a2129201e3b2f0aa450dedcf1c38e0295462fa5cfacfd86`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:19:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a41adf61a59d65bb732f71b8fa9e215ce26d7adaa7742f1d0d7dd0c7dec51f11`  
		Last Modified: Tue, 13 Jan 2026 00:42:35 GMT  
		Size: 45.1 MB (45128498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0f426cd5bf7128cd82a97f8d8519866322dbcfdac81bb42dc04e8d0b748092`  
		Last Modified: Tue, 13 Jan 2026 02:58:25 GMT  
		Size: 24.9 MB (24897006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f7ce38916b5f5ca3464d0db876b0f01969a64f2458908e6d7c5095b270bd53`  
		Last Modified: Tue, 13 Jan 2026 04:26:11 GMT  
		Size: 63.3 MB (63339146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0207f1da3b494d5542229fc4319459860fe13860c61db80918686b871ce7824`  
		Last Modified: Tue, 13 Jan 2026 05:20:08 GMT  
		Size: 158.4 MB (158403452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43190046df91207badc92187996debdae5ea351367ae1ba941228bac80f61d68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16025574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbbd548143031966e250762e7bf1c6b637e4c009a4d60ca1751fb55e98827e4`

```dockerfile
```

-	Layers:
	-	`sha256:f3e78fcadc6cbbb39e1f08a5c4b392e1531f80353975ddef0d4cc014e4cab42d`  
		Last Modified: Tue, 13 Jan 2026 08:22:34 GMT  
		Size: 16.0 MB (16015365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59e94adb3c97074a534c0c29777b9df518a7c7e019a328d0ed31d9eea801cb6`  
		Last Modified: Tue, 13 Jan 2026 08:22:35 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:11f6d914b651cfeb78c4b3ea514dc909d60fe8188ed978f52cee892278a444ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332945241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6d5cf4437a1d5f7d5a6c3f25283a1eb1501123f167d7996f1de96e5b4d856a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:14:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:56:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:50:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f0e1c9ce589fdc56e77162978a9037d5d8c63c2e5d6fb4fd4b325ce20394aa61`  
		Last Modified: Tue, 13 Jan 2026 00:42:11 GMT  
		Size: 48.8 MB (48820809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ddda3e83ee00d5d39dbd5cc1fe3a7c03a3c55275d87214b98204362e0a3f8`  
		Last Modified: Tue, 13 Jan 2026 02:14:34 GMT  
		Size: 26.5 MB (26548140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfe9cda83f157d908d08806a88c1bcb73fc8850f3d1b5ac78fad66e9654ac30`  
		Last Modified: Tue, 13 Jan 2026 03:57:15 GMT  
		Size: 68.2 MB (68193360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd416a3327a8c8b6b8c8b9ac5f0519059ec4f6c4df861ae9ebfd3a0a0dc6d5b9`  
		Last Modified: Tue, 13 Jan 2026 10:43:25 GMT  
		Size: 189.4 MB (189382932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bded5b4dd91684468dfef86bf805eff6834312119bcc2955cb8db51778378067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16344457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e9d78f3c7b5d4d06ff93e17cab3bdb664c5c6c4b86159132e770cef1dc83d3`

```dockerfile
```

-	Layers:
	-	`sha256:7cc23623b642eddd32a16d073b3e1aa44eb0240faecb292dbbcb5c15d0785097`  
		Last Modified: Tue, 13 Jan 2026 08:22:48 GMT  
		Size: 16.3 MB (16334232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87959fc6af40f761053e2415774067f6514bceb1c8b98ebed0d4fd60e03be98d`  
		Last Modified: Tue, 13 Jan 2026 08:22:50 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:697b249e3b8f1ba65b4e7e3b8e43a922eb3797257c739c9cf575afcebfa75593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351135786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64e38388eb12da3bdf4f45442c862bdbacb861f2d9118d42dfce3d6a05a55ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 02:02:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:03:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0f5a7611eb50e1c295ff4c244485263852c6e6c8f18836cf55dc8b5a4162740c`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 49.9 MB (49944546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f497e693fd9e81b15eb76e6f64e3f07e2363e9777ec10af3b185695fa33f90a8`  
		Last Modified: Tue, 13 Jan 2026 02:02:45 GMT  
		Size: 28.5 MB (28467609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86da8e97a2559ed40d50ccb3015d8b2b66b61ebe4e7b0eecacc6d9ed00ba65d4`  
		Last Modified: Tue, 13 Jan 2026 03:04:08 GMT  
		Size: 70.5 MB (70456052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935b7f4df4b82d15af6f7fa621095a3391390bd671501a660e3a66b7eceb6b6d`  
		Last Modified: Thu, 15 Jan 2026 21:23:54 GMT  
		Size: 202.3 MB (202267579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e3238e806c29182cd2660acc2e88c50deb35fcbbb1c6f014d3fdce761900b42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16239565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e588efe7c13cd51a8fe4c8a0b9f03876d327c8c3bdcd596cbaf6ad104e405a`

```dockerfile
```

-	Layers:
	-	`sha256:f5568568dbeccd09c4acba9edf4e5161e71216a6cbc508750a579a89f6073444`  
		Last Modified: Tue, 13 Jan 2026 05:23:40 GMT  
		Size: 16.2 MB (16229442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6800156bef6362a531af6489527f36606b06345baeba13129ab1dc091d45a8a8`  
		Last Modified: Tue, 13 Jan 2026 05:23:41 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f55601d4e1b95ebd8b8a5ae796be918fa91d35fe0ba9eda9e499b7596dadbea5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (348993747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4874c35d22390bc216bf8976298c35b6a0fac5eba1a5d884b04a58321e0977`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 03:37:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 06:37:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 08:51:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7bf02b202abcdb3d6a49a7ce4605beb0852cfcc4e8237bffbef88f800d821593`  
		Last Modified: Tue, 13 Jan 2026 00:56:06 GMT  
		Size: 53.5 MB (53516184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34c011037bb419c8e273f4c6f037f35bfbb4e208b971ed3dded7a3716d2b26f`  
		Last Modified: Tue, 13 Jan 2026 03:37:47 GMT  
		Size: 29.4 MB (29429707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3134f00788557e5662c70eef06decab809cb7a0a69c7e9d3bd5e921e979dcd28`  
		Last Modified: Tue, 13 Jan 2026 06:38:40 GMT  
		Size: 73.9 MB (73938436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f048d25bab4c2576e0dd8fa73c152e21d1c184cbf289d37ea8a5084882290d6f`  
		Last Modified: Thu, 15 Jan 2026 21:24:18 GMT  
		Size: 192.1 MB (192109420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5875d6e48bf6b2ed6be30552bde7f07eeba4ee1bcd2a6791f2913c086f9ee446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16241146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daab67c97a5f6873efb9ca20316385d48b860118d76ed98f938712d3fcd3e69`

```dockerfile
```

-	Layers:
	-	`sha256:05441ac66ab855c0a3939e511becff07474207cce8a0d83ee45dfe08dee5534a`  
		Last Modified: Tue, 13 Jan 2026 11:20:59 GMT  
		Size: 16.2 MB (16230969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c72ec06ad8b21feb6695317ce4be7a2a4682d8d20fcb13d95aa081d4949fe91`  
		Last Modified: Tue, 13 Jan 2026 11:21:00 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9d9019937b437ed2827fffe755c63da8988e0469c58c86fe4e391d3619437744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **461.9 MB (461853687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde03cdee35fdec4b3bdbb4e4e5f01e6337ae008460c7f9b16ec56222b16073d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1768176000'
# Fri, 16 Jan 2026 06:40:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 18 Jan 2026 22:45:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 19 Jan 2026 17:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0d152d1dcac9b1a7bbc763f3f2f3b2328b12317f387036c0ef1af1b70d3cf327`  
		Last Modified: Tue, 13 Jan 2026 00:52:42 GMT  
		Size: 46.9 MB (46854463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2df243ee2ea0a1e6a943f1e15516b1ef52c050634f2ee4c2fb36ff3ea6ef909`  
		Last Modified: Fri, 16 Jan 2026 06:42:16 GMT  
		Size: 26.7 MB (26732374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b2afbb087c50a06d13575b8aa32cff67ff6304587c83a51e23a0c8c08456d`  
		Last Modified: Sun, 18 Jan 2026 22:49:20 GMT  
		Size: 67.2 MB (67233793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cf3f63ac7d4294329ee5309a5944b5c430291e00ea6bce9b6173ada3db577c`  
		Last Modified: Mon, 19 Jan 2026 18:26:41 GMT  
		Size: 321.0 MB (321033057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa6de2e08cc416277b91feb4d6717a746e49bb484b8741645f03454f57a98ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16374703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eba53f7bbb35c276d2808a7c33ff50b960fe1d690c79d90e4932437f4f074ff`

```dockerfile
```

-	Layers:
	-	`sha256:90f0bfd4f57e3528ba54ff8c15a87d19be9e5b59c01f5ae01669e46f767cfd45`  
		Last Modified: Mon, 19 Jan 2026 20:22:10 GMT  
		Size: 16.4 MB (16364526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703414846aee4c72c2dd3f629ccc983ade701c5468b894aec7078ae30b0f088c`  
		Last Modified: Mon, 19 Jan 2026 17:17:56 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:68917ad4982e4668a7f21a247f556c03b6f280b650c69448cbcda4b35aef81fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316419382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab43605df363d930fbf6c94a743062df932d1f17af6e00de32e3ff232cfdb77d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1768176000'
# Tue, 13 Jan 2026 03:47:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:17:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:15:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3dcc5871821327b982eb5b773ab24bb0eb85ffa1e8b8f4ae6dd4e94832450146`  
		Last Modified: Tue, 13 Jan 2026 03:09:57 GMT  
		Size: 48.4 MB (48389296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622d22fb8fceb11ceaeb6109becb26df50c34175655fc06dc916318e56c9cbb3`  
		Last Modified: Tue, 13 Jan 2026 03:47:28 GMT  
		Size: 27.0 MB (26991951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d515a03edf6881bc28ae1107dbfef65f876121ca2ff049e05446fdd49a1465`  
		Last Modified: Tue, 13 Jan 2026 04:18:01 GMT  
		Size: 69.2 MB (69165519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97913d465d003cf44f58b34adadf298d5a3260332d76dbb780b7c27218c9f094`  
		Last Modified: Tue, 13 Jan 2026 05:21:37 GMT  
		Size: 171.9 MB (171872616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75977dfd8e8d41161dedc9ed7d0e6e954b882b053a2469a8ec198b965a70c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16047002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0478938606658345c8ac980fe4cac6fcdbd6b470c1d3fff5547f8ea0e0a5961c`

```dockerfile
```

-	Layers:
	-	`sha256:850881dced1057b41791d1e66c956dd43bb897cc773f4464a3b95700d4e04f04`  
		Last Modified: Tue, 13 Jan 2026 05:16:45 GMT  
		Size: 16.0 MB (16036857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07990ba1524dfcc605be574435937ef7feab0429c43e16c9bf6168404b537747`  
		Last Modified: Tue, 13 Jan 2026 08:23:53 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
