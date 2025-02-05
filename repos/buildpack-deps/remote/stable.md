## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:0374937123613379712d981633966e49355915b83865b779001fffeed815f12f
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
$ docker pull buildpack-deps@sha256:e7c6d07cb9b481de9609912bbb49dde977f6989d9a5abd1e58a877d25ee62baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348260383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a28b23ee01d152ebfcf4c1687e2584877089ca3ab4550256ebe7e14df2e8a231`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 04:37:13 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 05:19:13 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576b00d9bb10cc967bb5bdeeb3d5fa078ac8800e112aa03ed15ec199662d4f7`  
		Last Modified: Tue, 04 Feb 2025 06:14:28 GMT  
		Size: 211.3 MB (211328049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4a3dacd4e6c66cf75566584dfa9afd045080a4f3cb7838d7b19bdf30386bd8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15482039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9745f0d897e65d430c556d16a3c325def078d21a52bbb041e100967e95bcb9`

```dockerfile
```

-	Layers:
	-	`sha256:d4539b9f2e09894ecde147e82b09f847fc1cb06d936b130a9294f2544a903dd5`  
		Last Modified: Tue, 04 Feb 2025 06:14:25 GMT  
		Size: 15.5 MB (15471499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac139212500e131144b63fc9539d38787370de7cc310e05d7c357c0311687a7b`  
		Last Modified: Tue, 04 Feb 2025 06:14:24 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a83883a22760febadd59a5f9dbcee3274ad8e29a3721729caff1d538b14169aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315359212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bd2fc9911efe73bc7196ef0b6034a2b83caa039a8fb7b62851437cb9f1123c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8816181beac5d7674f87060fb5deb0c2c6221a62562265e16f54a617961cbc53`  
		Last Modified: Tue, 04 Feb 2025 01:38:08 GMT  
		Size: 46.0 MB (46006574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28060e71ea1173228ae8eefd6f5fb4296e8c1c73672a593f2d0d8e6e5483072`  
		Last Modified: Tue, 04 Feb 2025 08:03:04 GMT  
		Size: 22.7 MB (22733102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f77895e90931fefcb9b0f936aeec6e8c95f160c764c504ceb6084ffc29b46c`  
		Last Modified: Tue, 04 Feb 2025 10:20:41 GMT  
		Size: 62.0 MB (62003807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1293092f82d991d58072eac031a86360954b6f4021cae9377a435006dbe3bc7`  
		Last Modified: Tue, 04 Feb 2025 11:42:01 GMT  
		Size: 184.6 MB (184615729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dbf7f817719a28df7a5b0171007394ed210843d7eedd3e5f60dab9c54ea16a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4329461743dc38347b3338b873032c837143ab544d4d8b0cb96a7c18daec6f`

```dockerfile
```

-	Layers:
	-	`sha256:e768728e70f32ce146520e69c30ec9ced53352e7567637f487df05ce3d7d7129`  
		Last Modified: Tue, 04 Feb 2025 11:41:57 GMT  
		Size: 15.3 MB (15270417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9491464fec5e26fdf277d68ee891162483ab440c7fd77e5e08cfb03348e7798f`  
		Last Modified: Tue, 04 Feb 2025 11:41:57 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:edfcd06c9f9280a0a5684aff441e2e546f75de85aeb85371f8e73e9177e13707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301064587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353a38af250438d455724a5c3afb9e241707d8f30cc15e473d41764d98338a7d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 01:37:07 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 10:41:49 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66806698bb37ab9f15c9072a66ade0dcacacec8794e48afd7fdc2e801ccb928a`  
		Last Modified: Tue, 04 Feb 2025 16:20:53 GMT  
		Size: 59.6 MB (59639147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb08f2dfbcde333a583952948ebc4e632dcbb5e80617adcb1cf802d99c434d0`  
		Last Modified: Wed, 05 Feb 2025 00:17:42 GMT  
		Size: 175.3 MB (175281303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f497d6671a3d1bef0b2b41e1f00fac813b2117b3c55c50bb306cc56e6c577c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15286499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123f31c9b000960fcb71407865982cc5ce0fe3e0264e0d90e3caa8ebad20f84a`

```dockerfile
```

-	Layers:
	-	`sha256:fb74bad668425d0fa6c4e3a4a5748d522d644c46996d1b2f625e2dfbab5bb0e7`  
		Last Modified: Wed, 05 Feb 2025 00:17:38 GMT  
		Size: 15.3 MB (15275891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00ffef54c6e3318c865b6d27432503915bd8c5f658dcbc02fcf93109dccd5f7b`  
		Last Modified: Wed, 05 Feb 2025 00:17:38 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:735a72ed215fd45959ad09fd6cdf89da1717a26af3e38d5986a7401c5c5e32fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338980890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96539734cfc32d2d915ac20d446472b6ca4e12473d3d116c9ce577b14b88b7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Tue, 04 Feb 2025 09:00:06 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Tue, 04 Feb 2025 19:01:50 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611c2b713640ce0f9156445b244c4da5e621183b56c0901d97a8b6d54ce10d7`  
		Last Modified: Wed, 05 Feb 2025 01:38:07 GMT  
		Size: 202.7 MB (202718404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:abbc0cd211b04d1c6d6eee86eba498d03f6703b1cddc14b523a281254f50a13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15510643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d3cac96de5e5d1180ab7aa46d5b96ffd655014af40ed208949952bbbcc3fbc`

```dockerfile
```

-	Layers:
	-	`sha256:7189bcf175080b446ed5d6a5c325d80adb3cfc6fe15f880cef90faeccef8edb9`  
		Last Modified: Wed, 05 Feb 2025 01:38:03 GMT  
		Size: 15.5 MB (15500012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e9869a1794ca698ee121fc45995778e10d1700ab388afc32229805ae2335c54`  
		Last Modified: Wed, 05 Feb 2025 01:38:03 GMT  
		Size: 10.6 KB (10631 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:882a152f2e57fff2b4e424ea3fb6a7d5273b93066678dfd0bdb95b0efba857c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350837945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9097785ed06e1ce4239bd8a49450234addc5a2f2cae02b789c3f0c6688239e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7d7e5b6420845d0479145c8a18a31030093be0de73e11194d97fee1ac58ef5`  
		Last Modified: Tue, 04 Feb 2025 04:23:48 GMT  
		Size: 24.9 MB (24899338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43394bbbaab482132a05c8eb702c9ebbbf5ecccd558ce05fdf40c651b7fbfa10`  
		Last Modified: Tue, 04 Feb 2025 05:15:47 GMT  
		Size: 66.2 MB (66236925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a443d7b60dbf868d9542c672117d7e30786e753c999878424f61b36b47cb37e5`  
		Last Modified: Tue, 04 Feb 2025 06:14:56 GMT  
		Size: 210.2 MB (210244226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54a789932b9f341ad41a0f58003c64ea627a572cfb7c893198b963e0f60b687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb037878e3a2b9b326d57a9255d1516b726264d93cdf05e3e5072ecf804fcb2`

```dockerfile
```

-	Layers:
	-	`sha256:65c94f4e47cb5c1d276ce88454d05b51a88e1f8b6e58588a30fcf1e870c57f76`  
		Last Modified: Tue, 04 Feb 2025 06:14:51 GMT  
		Size: 15.5 MB (15450089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a66dedb1b7b06480192ffed582731683a156dc109dbe02f773f96c60f11a9a78`  
		Last Modified: Tue, 04 Feb 2025 06:14:50 GMT  
		Size: 10.5 KB (10512 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:4a1e146fd4ed0345093359de7cf06a978e59b8bc81b6df468175c0659276d31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325624000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:288e34b322e64d6e3944522e9ac04efccd67ec17196b55a0bbcad2b06ac4e011`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:467081b053e1cbae3c04ca1529cea6d968f9b38249f5cdd15b07f60be084dd00`  
		Last Modified: Tue, 04 Feb 2025 01:38:28 GMT  
		Size: 48.8 MB (48757800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7faf65582b7e0fbb4eea14df7537078630b3bff0936e1fc964a494519326b5b`  
		Last Modified: Tue, 04 Feb 2025 19:25:23 GMT  
		Size: 23.7 MB (23652224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12393adfa37a97fbcfa8d29955e04828c6bd657b4d83082cf837413910af04a1`  
		Last Modified: Wed, 05 Feb 2025 02:53:44 GMT  
		Size: 63.3 MB (63306362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63804284b8ce6a2c44bc7e10737c5060fcbf1ae87b2f923d57cc93f3f65b661b`  
		Last Modified: Wed, 05 Feb 2025 07:48:12 GMT  
		Size: 189.9 MB (189907614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8f33ffeaae9790b2d32365b726bcd6fb36c0f53a19122045829de140be187ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366a9dcd69f76fd8f9ccd2d4212d9fc500f55bedc568b601cac7b9266344d83b`

```dockerfile
```

-	Layers:
	-	`sha256:f502e9b67ab85179714645146ddc9908ffe43ce95fb5b31b8d599c85fd1f63c3`  
		Last Modified: Wed, 05 Feb 2025 07:47:55 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:35e78ee85e07e4e4cb8346fd4ce32395bb5d4371ed97b669ab319345167ca7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362239302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbfed454a58e076c10083bed325c7a3cfc666ffa2b579ab328586b147d97bf4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 01:37:34 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Tue, 04 Feb 2025 07:24:32 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7451c2aa1d936ee2bec4ea4db323da11f1dc2694095c250c16b70763100f29cf`  
		Last Modified: Tue, 04 Feb 2025 15:46:48 GMT  
		Size: 69.8 MB (69842739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556dba2526850ef13f84af87d0289a40f2451777be07098d04c55f33c7f76b83`  
		Last Modified: Tue, 04 Feb 2025 21:55:09 GMT  
		Size: 214.4 MB (214366038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cac51cb0a942f02bd546e19e1815e8b8de33f1f9c5344f2d9dad768660bc31a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15458456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f87d8d04721422aab0c795ae007897259223e640e95b08768a48dabc5a38f20`

```dockerfile
```

-	Layers:
	-	`sha256:717b9992e2cedaf357af4ac93da39d025105d156e8b364e77ebcb41bfdb68e87`  
		Last Modified: Tue, 04 Feb 2025 21:55:03 GMT  
		Size: 15.4 MB (15447878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fa14071236e991a2a1e1d27a53f87ec9718e9c6c564c6b6374c9f1f5ee40267`  
		Last Modified: Tue, 04 Feb 2025 21:55:02 GMT  
		Size: 10.6 KB (10578 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5325f57c776c09a2d9b27ffbdce4c60ed3b6b0bcb8725ed55de3cca76d4da7d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318053850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e70b77abb35e9e7f65b0243f1c54293052dd79e96f228a7904e87b96c2c4fbc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 01:37:03 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Tue, 04 Feb 2025 07:30:08 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Tue, 04 Feb 2025 11:34:34 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Tue, 04 Feb 2025 17:51:50 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:stable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a779583e8fba77f3ac42ee4dc09cae8a77da251c683941b37505a7bf38471b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15294729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23f15a3299b23d2f64599420aad3080b703a9109238eb0ceb0bc4302d9a3e4d`

```dockerfile
```

-	Layers:
	-	`sha256:af2bda491b92448860994a9c14e5ae416d3498bde888e34d392f7c6d1e8ac67e`  
		Last Modified: Tue, 04 Feb 2025 17:51:46 GMT  
		Size: 15.3 MB (15284189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdfa34c3a2c63bbc552bd4337bcbe25c3d95f012c93c2fb856ae9c58020c247c`  
		Last Modified: Tue, 04 Feb 2025 17:51:45 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json
