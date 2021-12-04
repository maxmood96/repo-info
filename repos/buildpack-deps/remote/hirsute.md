## `buildpack-deps:hirsute`

```console
$ docker pull buildpack-deps@sha256:8ad9eb77a56d209937b930860b6d6baa8acdcbfb11512a434282d6ce268ad3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:hirsute` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:17ed16814dafd21858df1177e17282f0149ad1851587a96763d2fff9fb4d1033
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248824266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fbe762d758e606ce8e704b60b927b929c6a462b7af7595d9a2d04bb0dc4ade`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Dec 2021 02:20:56 GMT
ADD file:b94883edb5db8add88bbf8934deeda5ddd0acb4e2ce2a19a774de29ee04b7399 in / 
# Sat, 04 Dec 2021 02:20:56 GMT
CMD ["bash"]
# Sat, 04 Dec 2021 02:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:39:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Dec 2021 02:40:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:43:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e6a0d5477cff31ce49b4d3bc07409ebd27609574e968043d0b9c10acf854ebc`  
		Last Modified: Mon, 15 Nov 2021 05:13:30 GMT  
		Size: 31.7 MB (31703945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6ac1808edf35dc4bc9c2a238338455fcd9bb473e3e2eefb62149a83d4d2177`  
		Last Modified: Sat, 04 Dec 2021 02:44:58 GMT  
		Size: 5.4 MB (5429044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c979fff1be3bf3600792310b88676b7e33d23f01d3e4ab4fd460170dc74b8905`  
		Last Modified: Sat, 04 Dec 2021 02:44:58 GMT  
		Size: 3.7 MB (3662236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76654756b0591142a7600b7119f7793b38d291a915f19aae4e231dffdd1d0caa`  
		Last Modified: Sat, 04 Dec 2021 02:45:16 GMT  
		Size: 43.5 MB (43542561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c704a3a98a6f3e45a17935b0d50890c3b4f469c40dc7c42ec0f5268ea2e20b`  
		Last Modified: Sat, 04 Dec 2021 02:45:48 GMT  
		Size: 164.5 MB (164486480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6750601f1fd76063f80245bfe8db26d1a96853abfc6dfb02fb16188a458ea329
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208963298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fe4c7546b306b1c82069e56220df647071c462704250c3ea210b3f3e657061`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 02 Oct 2021 05:59:26 GMT
ADD file:0ecbd9f51121128f5d6ca097a4f697705e11f91abe0a7f83083e18bceeeddfef in / 
# Sat, 02 Oct 2021 05:59:27 GMT
CMD ["bash"]
# Sat, 02 Oct 2021 22:24:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 22:24:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 02 Oct 2021 22:25:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 02 Oct 2021 22:27:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:615bdbfbc600b147544d8c25eedf00ddb7eebaf2e9005c1da9f5885a6bbc6c1d`  
		Last Modified: Sat, 02 Oct 2021 06:03:33 GMT  
		Size: 26.9 MB (26859487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8944eff0f4815cf5a70868ad5afaed083de9f7ead5a73bc97fa5dc147a04f9`  
		Last Modified: Sat, 02 Oct 2021 22:40:51 GMT  
		Size: 4.9 MB (4858463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed8cb9d9d7259532d0d30040f4f46ba30d3dedae6e7d37d51c4bf9f60bc54a`  
		Last Modified: Sat, 02 Oct 2021 22:40:50 GMT  
		Size: 3.1 MB (3139002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8efec2f84a292f59a270ac67ccb130692e15a90a3105f135600dd1ee32bed4`  
		Last Modified: Sat, 02 Oct 2021 22:41:32 GMT  
		Size: 40.0 MB (39953431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecfb48b1577ca4abe64edeb74c9898c20c84b004d5bc4a66957c2de97d6af5f`  
		Last Modified: Sat, 02 Oct 2021 22:43:03 GMT  
		Size: 134.2 MB (134152915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a8821b911d40601ad2753bdc51375a46567d7c7e0942900cab3cd0a0dfe8d92
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239165235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dd754201318b20db301d2a296895abba3c81a3c8206b845afa07a6a4111692`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Dec 2021 01:44:14 GMT
ADD file:f6fe7852db10c8de6e161babd3110304c6e20b10825c02c995338bcb4e41f12d in / 
# Sat, 04 Dec 2021 01:44:15 GMT
CMD ["bash"]
# Sat, 04 Dec 2021 02:03:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:03:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Dec 2021 02:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:05:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcd77b4f4e1fa4d6089acc7856f15d5d2760bf81f44a94e52eb8e81423928c6e`  
		Last Modified: Mon, 15 Nov 2021 05:14:15 GMT  
		Size: 30.2 MB (30174348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330d08f54fb4c8a29eb513eb66bcfa0c760ac8f6d038f4aacf0934c31fdf9edb`  
		Last Modified: Sat, 04 Dec 2021 02:07:58 GMT  
		Size: 5.4 MB (5401275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3135edb0f3a1007f770789719e3271330d6cdf2f5f2c634dc148953996b3e0`  
		Last Modified: Sat, 04 Dec 2021 02:07:57 GMT  
		Size: 3.4 MB (3431827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1641da95097e52ac220bd32b64969d5fff25d51626371b86e0319dda0a8b5ecd`  
		Last Modified: Sat, 04 Dec 2021 02:08:15 GMT  
		Size: 43.5 MB (43532904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7df8cfec2b66b41ec65ab9b757de589bbadfecb6c1fc5598105ec2b5738d34c`  
		Last Modified: Sat, 04 Dec 2021 02:08:49 GMT  
		Size: 156.6 MB (156624881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2907a4ade782540beeadc530701ec593f2c1899d1f9ffc71d51962b7a8bf45be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268143719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:689afc563871e8f713e32f83998d679743c14ac849d1e7a4e979dd31bb349631`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 Oct 2021 11:08:18 GMT
ADD file:4fece2b915970b36002bf98a6f85f91c3b9bfeb80b685f7e5ee749080aea6540 in / 
# Tue, 05 Oct 2021 11:08:25 GMT
CMD ["bash"]
# Tue, 05 Oct 2021 15:11:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 15:12:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 05 Oct 2021 15:14:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 05 Oct 2021 15:22:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b16b9756d17acd6ced37d43568054b32fcebdd38ee4b9bdbf35dbc3e872d754d`  
		Last Modified: Tue, 05 Oct 2021 11:11:17 GMT  
		Size: 37.3 MB (37255452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a54cbd41484567ce0ebb693b3129bf830d0e454fbe8a0eec180d9fa9f976c0`  
		Last Modified: Tue, 05 Oct 2021 15:51:52 GMT  
		Size: 6.2 MB (6153990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afff0eec9aba68bd0b14d67496cf23585cea9e37314ecee6657b63816efcd9db`  
		Last Modified: Tue, 05 Oct 2021 15:51:49 GMT  
		Size: 4.5 MB (4523714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1536544f6a113307ef8771dc9e57d3b4974edc1869ee7d08a83f9422c79b1be`  
		Last Modified: Tue, 05 Oct 2021 15:52:37 GMT  
		Size: 49.5 MB (49467145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67a0bc2994fab6d2773059eb5766490eff6f06d4c5cead29d091d284b24873a`  
		Last Modified: Tue, 05 Oct 2021 15:54:11 GMT  
		Size: 170.7 MB (170743418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a445bb89dc4ad3e2a546446073c778792b1cf88762d78ac04fd3a8fd9286c6a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.9 MB (257925643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10e0dd936c1a9ddadab2ba100ffe9ed2f196a160e87e4f254b27baf58e8c693`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 01:16:46 GMT
ADD file:3e74b3f99e917f6242f9460c55d6b1ed2c4e243bb9deeef85c260be1e6c3b3b7 in / 
# Fri, 01 Oct 2021 01:16:47 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 02:11:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 01 Oct 2021 02:14:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 02:20:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cfe1f0adec8bd7640ec8d5467a7a5553e6d58e6cb80adbbc101495501625dca9`  
		Last Modified: Fri, 01 Oct 2021 01:40:30 GMT  
		Size: 27.1 MB (27141881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747535e5ca63ea5be385acb70aaca4311fe2b78f1e44463cbfce298800f9f33b`  
		Last Modified: Fri, 01 Oct 2021 02:50:40 GMT  
		Size: 4.9 MB (4944581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0facf6815c035133c1d22c89659eabcd14838fa24ff638d7a2f822c2d42d795a`  
		Last Modified: Fri, 01 Oct 2021 02:50:37 GMT  
		Size: 3.2 MB (3177915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f4c1d69caf6add02d4549d216e9e00fdaae087f4d280cea93bbd3f8b3ec48a`  
		Last Modified: Fri, 01 Oct 2021 02:52:36 GMT  
		Size: 40.3 MB (40329415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4eb085d1eb115177f17b87572f40735eff638aa6135e73b357a2e48048b803`  
		Last Modified: Fri, 01 Oct 2021 02:58:07 GMT  
		Size: 182.3 MB (182331851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b3c2def16c32fe22c2cb9f70e4d74a42883d4d8515388ebfe85d7d0ceeb4e620
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241454874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c980d0e73bdbea135b37b503eb741d720b58cff83e1b6c933e18a872bb50f3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 04 Dec 2021 01:43:38 GMT
ADD file:6d66c98b5da6f242f1ab27703377ccbafff619c8e83fcf52e7ef7efead5c5899 in / 
# Sat, 04 Dec 2021 01:43:40 GMT
CMD ["bash"]
# Sat, 04 Dec 2021 02:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:07:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Dec 2021 02:07:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Dec 2021 02:08:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a5e1e0bcff39834997ae03f59105b3cbb3f26fcab688703ffc81b4c0b5894c6`  
		Last Modified: Mon, 15 Nov 2021 05:16:19 GMT  
		Size: 32.5 MB (32505784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc9eb43d6eb95c883a6edca33efa98e7f034a7dda1146a503ab15352a49500b`  
		Last Modified: Sat, 04 Dec 2021 02:11:11 GMT  
		Size: 5.8 MB (5801275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5925df3a30ee8e993d47fcfe7b912e8dd219a903a346cf5abbaf916e7bb7440`  
		Last Modified: Sat, 04 Dec 2021 02:11:11 GMT  
		Size: 4.2 MB (4185291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d632201b9a3763071a69f82731e615442e7842bbe1d745896133ddf999c2044`  
		Last Modified: Sat, 04 Dec 2021 02:11:24 GMT  
		Size: 47.4 MB (47399833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76b8bcaf57711db7804a1ca280ca36907feeb5d0e043bac25cdefb51bc852ef`  
		Last Modified: Sat, 04 Dec 2021 02:11:49 GMT  
		Size: 151.6 MB (151562691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
