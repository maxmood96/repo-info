## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:7cabbdfa5c16924d0ac4ab5ceb239f43cf4a823fec7ab0cd6cadba76e8886f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ed6dc7c001795064792293f37afb1d7a68fcd651189d0c21c207bd2e2dc36b89
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322061897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2db005ba57f401e6f5f55e4a1091780b7b99c7a999ebee975c864c05c0c2bef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:50:01 GMT
ADD file:3d2836abb42f177ad29a584ba02ccc6421b1613f73325823603fc98578f17445 in / 
# Tue, 30 Mar 2021 21:50:02 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:05:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:05:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:06:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:07:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff28f9110f9a07cc7303cdae0cac6dceebc733170af8336bff099af5e4b0eed1`  
		Last Modified: Tue, 30 Mar 2021 21:55:15 GMT  
		Size: 54.9 MB (54868057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b440922f9fc7a15146adf7cc4d35ea9d0bc9a6a6004a905f240fcad22cfe0bcd`  
		Last Modified: Tue, 30 Mar 2021 23:15:47 GMT  
		Size: 5.2 MB (5169284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd6e01879bcee5c3b6f0a9e069f1f61a436d7e55e344931794bbe2af8c7fde1`  
		Last Modified: Tue, 30 Mar 2021 23:15:48 GMT  
		Size: 10.9 MB (10868877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a1ec4cc9f7507b54cfb235d70eeca2d974ec61b19d36b484b471f9ebb939e9`  
		Last Modified: Tue, 30 Mar 2021 23:16:13 GMT  
		Size: 54.8 MB (54797320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af37c2043eb0bf9f17de756a08201c4f1ff5396246487b44b194e2b3becb190b`  
		Last Modified: Tue, 30 Mar 2021 23:17:10 GMT  
		Size: 196.4 MB (196358359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a033c57f2c41992694fc262994b22dc429ed9baf794c527537f649a65255e6f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295131065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1458fd2addc2c97dd195b9970c4ed0d8104e5750772865a64ae8fe48a1189784`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:52:17 GMT
ADD file:c74b1cfc1e5bf1a62d213de82dd043a95a19f0f67a947b54c449d8ee5d53fb37 in / 
# Tue, 30 Mar 2021 21:52:19 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:51:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:51:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:52:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:54:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:06ea7b1cac1276634323a37913fac1e0f60820f2aae1fd14d07c2c573bfbce6d`  
		Last Modified: Tue, 30 Mar 2021 21:59:54 GMT  
		Size: 52.4 MB (52402138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d6173e3da10cc42bd51156af90984c02eeb52327364153f9648d30fe084fec`  
		Last Modified: Wed, 31 Mar 2021 00:03:10 GMT  
		Size: 5.1 MB (5073685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918922db8190bce87e065be6997a39e948ef367b3b3f4ab60ced0d40e98f335f`  
		Last Modified: Wed, 31 Mar 2021 00:03:12 GMT  
		Size: 10.6 MB (10570432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b91d9b6d16cc2001c2119f05de27cd1ac2695a58451ac1a9280a1cc8f18b5d`  
		Last Modified: Wed, 31 Mar 2021 00:03:36 GMT  
		Size: 52.5 MB (52497765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a2d5fbecbca484b51ae0bb36d3869347be0709448117fef736a10cceff284d`  
		Last Modified: Wed, 31 Mar 2021 00:04:34 GMT  
		Size: 174.6 MB (174587045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c1baf6d0bfe9dae2bcada6e693febdda0d8c91f0aeac6bc25e7a52de1f746529
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282570422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02afe6a325f0cb8fe7cbfebf971c41ba7059bf6c6ac19ea91855bfa9ae1a9dbc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 23:09:57 GMT
ADD file:3c49310ff7c2a9c21073b7ca0884f4b8e783606a6653a2d74d1aa04196a3ed8f in / 
# Tue, 30 Mar 2021 23:10:01 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 01:25:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:26:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 01:26:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 01:28:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f41ab33290e85402afe03e9a82d0262689d71eccbba0d79246595731d24f2688`  
		Last Modified: Tue, 30 Mar 2021 23:17:34 GMT  
		Size: 50.1 MB (50070962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d173ac9612777e7e6d56bd74819357eb0a74fdd29dd54af742a5652ae5ac6d`  
		Last Modified: Wed, 31 Mar 2021 01:38:18 GMT  
		Size: 4.9 MB (4934354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b41bd459aeb849bf22b88bf2563aeffb2527f25a09c92049467c43605bdc30`  
		Last Modified: Wed, 31 Mar 2021 01:38:16 GMT  
		Size: 10.2 MB (10218235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac4b6fcf9d7014405b480814f8a95c15f4f875f267145cf47283fb0315a7ec4`  
		Last Modified: Wed, 31 Mar 2021 01:38:41 GMT  
		Size: 50.5 MB (50514433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d236d27cc2a6699f4661433efbf6be31904da6b7b220e81a1a977f9063106e0`  
		Last Modified: Wed, 31 Mar 2021 01:39:33 GMT  
		Size: 166.8 MB (166832438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a70e45f679f1ae10d405f8bdef24e93495c5f93440c13a3889db850b6fa23cf9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313756139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:725253f95eead7dca4d6b36cd5cb1bb909b5ae980834c69a4f79f76a0cac67bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:48:22 GMT
ADD file:367b87909b67093178b79312d10fd1e5f34fd8f2d88ff86d5db05018c84e1de6 in / 
# Tue, 30 Mar 2021 21:48:25 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 00:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:19:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 00:19:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:21:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f6f2092d4e11ede8755fdc276c7abb424692833ac06435c47705ad7024c2459`  
		Last Modified: Tue, 30 Mar 2021 21:55:24 GMT  
		Size: 53.6 MB (53555909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7329ddb16965a8f564ba84df809cf2bf57cef4de5272f15c7ea208a725068c`  
		Last Modified: Wed, 31 Mar 2021 00:31:34 GMT  
		Size: 5.2 MB (5156631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800c7b57132ff5a24ff23004e5ee11478f43b53d722d70dab97db2330112cbaa`  
		Last Modified: Wed, 31 Mar 2021 00:31:32 GMT  
		Size: 10.9 MB (10868555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783e459fa97ce997828e5ffa35f58e51e2294e6d9a4a720acbd65041899adaea`  
		Last Modified: Wed, 31 Mar 2021 00:32:04 GMT  
		Size: 54.9 MB (54920716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ff8634f522a934d1876f2656fd8d8a02bebf95ff5f4bb1bf80c2173b52fc9`  
		Last Modified: Wed, 31 Mar 2021 00:32:56 GMT  
		Size: 189.3 MB (189254328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:75f47e98cf0af3bc3395ced1d036d2bbea5839049e1950e69167824cd439a59a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327938952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae24a23b3a3687e83fbe37d9854b71827bcb85d0f7ba08cb54f68e1475763aab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:40:35 GMT
ADD file:1f041945ff890476db13a1209d904306e018db9cc0c3ddd68afde8ba20721441 in / 
# Tue, 30 Mar 2021 21:40:35 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:59:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:59:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 00:01:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1abc0a07df2794b8c01aadbeeb9293997b8a54aaa313f435b4d2d676f888235`  
		Last Modified: Tue, 30 Mar 2021 21:47:59 GMT  
		Size: 55.9 MB (55881675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5ab305c1c154665b02986b2328de2fd181084b0c296c4d76f131107ddef04`  
		Last Modified: Wed, 31 Mar 2021 00:09:46 GMT  
		Size: 5.3 MB (5298115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95df009a7c979f03789affbb069b0972638a182a6594760beb04e5d621ca33b`  
		Last Modified: Wed, 31 Mar 2021 00:09:47 GMT  
		Size: 11.2 MB (11249054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2268237c64ae5a91b7f0d8e740b5f590a7da88c2ae88e6e9356441350ab351`  
		Last Modified: Wed, 31 Mar 2021 00:10:17 GMT  
		Size: 56.2 MB (56194937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3610a79bdcdc0adf7228d3861a0cc861f7be9f315dc880fd1fc27bb0401ebc3`  
		Last Modified: Wed, 31 Mar 2021 00:11:30 GMT  
		Size: 199.3 MB (199315171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:178040891ecd0c5cf06a74c0c579c9cc24888e0622131940d53d9e4d52d3a72e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301545307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bc1a472c71f68987be06aeb515811542eca188699eab20b073c58c3c14b1e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:10:14 GMT
ADD file:4d20c8e17f6123a0d4b72a62f938dec2586886ad6d87f246ee55a11ea923b684 in / 
# Tue, 30 Mar 2021 22:10:15 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 23:14:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:15:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 23:16:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 23:18:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ec4a0a6790f3ff962dc7c25a161644b3cc5e5b8758356dab4f112068aa643317`  
		Last Modified: Tue, 30 Mar 2021 22:17:08 GMT  
		Size: 53.1 MB (53127307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90333279e95c41e8d6dddbd8d32157d7b6e64b62fb5b735d17ca9d796904a82f`  
		Last Modified: Tue, 30 Mar 2021 23:25:27 GMT  
		Size: 5.1 MB (5127929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af84110c224d7e9e68767940402f621ab1b3a77a6c7b483749668ff6fccc186`  
		Last Modified: Tue, 30 Mar 2021 23:25:29 GMT  
		Size: 10.9 MB (10871030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdb6bb50d1af41bf34c49f39682b20bd8653e9a206ac5213a9829c3a3b339fd`  
		Last Modified: Tue, 30 Mar 2021 23:26:19 GMT  
		Size: 53.6 MB (53588998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00cdad45212b6b4bf24a5e55f4b73415f5f5726ee0bb744a3e582c90ecae63a6`  
		Last Modified: Tue, 30 Mar 2021 23:28:27 GMT  
		Size: 178.8 MB (178830043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2387aa52c138e572b62175ad3035121c026b5c5abb69a137502e43c574cc2869
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330632597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4602cb16d1fc2f8e457620b4255f62c47cc5ab058d739c47083026047828e67e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 22:36:24 GMT
ADD file:169fa80cdaf558a1257d6751dc92cc0e23d49d492d49b2b3ee54f7402eccc5f4 in / 
# Tue, 30 Mar 2021 22:36:34 GMT
CMD ["bash"]
# Wed, 31 Mar 2021 02:54:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 02:56:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 31 Mar 2021 03:01:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 31 Mar 2021 03:22:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9192555ba03aa965b78e644fac9cb4305e27386da5748f2669982c47d7b4c5ba`  
		Last Modified: Tue, 30 Mar 2021 22:43:07 GMT  
		Size: 58.8 MB (58782965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754d65100617a4401cecee0e9aab2c897181d1ae44b0233afd31cb0bb4003f0f`  
		Last Modified: Wed, 31 Mar 2021 03:28:09 GMT  
		Size: 5.4 MB (5419626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5eb7e11b59e3e544a1588a8f7ce7715a221932c63d82819800360e78a0246a`  
		Last Modified: Wed, 31 Mar 2021 03:28:10 GMT  
		Size: 11.6 MB (11621189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0b473f96a1bab44e88724dde6d6e332c21c41f65e95a3968a2d04cd60b07128`  
		Last Modified: Wed, 31 Mar 2021 03:28:33 GMT  
		Size: 59.1 MB (59138309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d04a0fe7a4d9decf5fc70724ed379f44196bc4560e80d246c2b88caa6918a4b`  
		Last Modified: Wed, 31 Mar 2021 03:29:31 GMT  
		Size: 195.7 MB (195670508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2fb9cb5cb75153c8807462392d2edfd3f74acfee4d6d9ce1015cf7724156d8c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295683601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a1ba353ded943019eb93641fab99fc15e08418f80a89ab6ac742591003b81d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 30 Mar 2021 21:42:56 GMT
ADD file:c96fcc34ba5121a1c8780b0148c4b2ceaaa9ce733fac0a9830e3f557d45d7c9c in / 
# Tue, 30 Mar 2021 21:42:59 GMT
CMD ["bash"]
# Tue, 30 Mar 2021 22:44:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:44:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 30 Mar 2021 22:45:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 30 Mar 2021 22:46:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bcb476920ff38aa084b50cb5a5e43afc962acdfea91e11abaaef6fc258b79a0c`  
		Last Modified: Tue, 30 Mar 2021 21:46:39 GMT  
		Size: 53.1 MB (53147808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9941cdff622917fbf0a7a90b9b9bd51d58de5471a94cf52add39fa8b62837d6d`  
		Last Modified: Tue, 30 Mar 2021 22:50:37 GMT  
		Size: 5.2 MB (5150758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bd7897b18d3d481ba626f3a769e62e5ba9a769adc21d00817aec4735d3e628`  
		Last Modified: Tue, 30 Mar 2021 22:50:37 GMT  
		Size: 10.8 MB (10758625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2735f65b850bc9c170b085eb2e58a02e3133df2f70463125e24ead7d249cfa`  
		Last Modified: Tue, 30 Mar 2021 22:50:55 GMT  
		Size: 54.3 MB (54255762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f64df8ee25c5868a7a5d6f44c0076a88375423adc86ab59502ff2f386b87738`  
		Last Modified: Tue, 30 Mar 2021 22:51:29 GMT  
		Size: 172.4 MB (172370648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
