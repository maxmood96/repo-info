## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:1415b943165232aeb4511f8d03b20782fc0431416666aa40bb56c5551ab13a5f
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7635e15b2a6151ca03c50893536dd315e463d85e782c28cd5f12ab528ace56ef
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.7 MB (323747572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b362ed24becf86f835368e07873f6523c0ef16f51252938bc530e0b5928fe6c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:19:45 GMT
ADD file:19778292422b784c4eb17d79e7632fc1e3619b6bbbcf16a37bb6179a5c725b1b in / 
# Wed, 13 May 2020 21:19:45 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:25:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:25:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:26:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:27:25 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5ce4ab219a2f8bc551eb2502df5b719a1d8a32c4bbb00b3629001ebb6c5e0b94`  
		Last Modified: Wed, 13 May 2020 21:25:41 GMT  
		Size: 51.4 MB (51384672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f458d7d6918561d3665fcf7c6a15ac5f015d15f94fe4c18152b31a6b390477d`  
		Last Modified: Wed, 13 May 2020 22:43:48 GMT  
		Size: 7.9 MB (7934430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a19396f1ca9e830aec22ccedc673036a5d9fa5707ad170217dadb18689b7f61`  
		Last Modified: Wed, 13 May 2020 22:43:48 GMT  
		Size: 10.5 MB (10463198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131834a7118626dab711b9bd62471ab667200154b199826ed2ae74c2733ea3e2`  
		Last Modified: Wed, 13 May 2020 22:44:10 GMT  
		Size: 55.7 MB (55658350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ef9101bc45d641716eea2e2782e37c10b0dbfa4ad403ad65a6d7613364fd2c`  
		Last Modified: Wed, 13 May 2020 22:45:00 GMT  
		Size: 198.3 MB (198306922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c01dbef4ab6f64499710b19b9df7f7dbb70c92fd63e5e5854a37f098fb6a916a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295155045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583d5a47d280ec03b087e3f89e0a39781759394f6e56bdc2b0b721e1b5414849`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:48:54 GMT
ADD file:e9c6ac7bf8b044473fb44adc857ae60fa2e57fd69c08908b01eef97b087e3aaa in / 
# Wed, 13 May 2020 21:48:57 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:25:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:26:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:27:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:30:54 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:320cb68d32ad923f9944bd8a4839f75e3e1b446fca01a999d67c9a756e55e632`  
		Last Modified: Wed, 13 May 2020 21:58:23 GMT  
		Size: 49.4 MB (49358454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba87e7b395f65b77fc7adc10d5b082bf26da938cfc39952a2c778fefe01abbb`  
		Last Modified: Wed, 13 May 2020 22:53:37 GMT  
		Size: 7.5 MB (7514341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e3e25ce7b85de9e1d951a3097b9fce980d94c1f8057796afe92a9caab58`  
		Last Modified: Wed, 13 May 2020 22:53:37 GMT  
		Size: 10.2 MB (10157745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30dd7626fa8f7db8c898aa5539da563d7599d5f8b5a67074b71bd6bd58f2054`  
		Last Modified: Wed, 13 May 2020 22:54:02 GMT  
		Size: 53.3 MB (53295562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7c4e982b8388785b84fc6ce9f9fca37fad45ec6ffdfed6d5cf40d0d8240650`  
		Last Modified: Wed, 13 May 2020 22:55:02 GMT  
		Size: 174.8 MB (174828943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bad2b3406187224a882b9a448e58fc6a418fee8e703ec80291110e7c8f50bde
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289312675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1dc95a7badef77ebe17701abbfc97a1d1a29a4048412b530bdf843db5ddc2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:02:10 GMT
ADD file:85e3bb4657a3517a43e0275a958ad028f3f1684bc8a1a2ab4370553a106583be in / 
# Thu, 23 Apr 2020 01:02:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:07:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:584761cab5c57084a1bd0e36523834571e95168e0a6245926b908313dd826549`  
		Last Modified: Thu, 23 Apr 2020 01:10:09 GMT  
		Size: 47.7 MB (47659184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e340b2750c5a3fef5b49207324ded3ab2bab0ec5b13355bc0b1479b14ed1fe`  
		Last Modified: Thu, 23 Apr 2020 04:28:03 GMT  
		Size: 7.3 MB (7255985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a158eb7564ad64eba8f5106f2f533b09bdfce834baf124daae77ec75837670`  
		Last Modified: Thu, 23 Apr 2020 04:28:03 GMT  
		Size: 9.7 MB (9672905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73dfc1241c0df6667cc7df3946c524d3e6c3ae8ddd128d21feb342d8fa7069`  
		Last Modified: Thu, 23 Apr 2020 04:28:46 GMT  
		Size: 51.1 MB (51064686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd29e0ffa9b4810768b418bb7e397e0a67b8fc7a2e32971f98f7dd2e3a85bffe`  
		Last Modified: Thu, 23 Apr 2020 04:29:36 GMT  
		Size: 173.7 MB (173659915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:88f31219ca47a6aa978648e39d1128b8853932ccbddff72145b8f808f5ed6d11
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315681707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ec611dd64d1c036b5edabfc4a13e9b2f69bcaf9c2ce2c379eb6d22b00d0ef1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:41:52 GMT
ADD file:642f1f8b3928c38913b91b5770e5ef77e0467db31d0e7342848c66b97b0cefce in / 
# Wed, 13 May 2020 21:41:58 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:19:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:19:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:20:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:23:19 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da14fdea4bf7eaa36b82ecde9ee461379c7eb32fac279c7d1bce1452edd5bf2f`  
		Last Modified: Wed, 13 May 2020 21:52:10 GMT  
		Size: 50.3 MB (50328349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d18f3d952fdbc982edca77fab71409bebc6a0b410a5f13ffe6fd2685b6020c`  
		Last Modified: Wed, 13 May 2020 22:38:11 GMT  
		Size: 7.8 MB (7809463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382abc5b67b7c0e46916f728a90e7aa0866070c3a67e581de6b5904092e6ca45`  
		Last Modified: Wed, 13 May 2020 22:38:11 GMT  
		Size: 10.5 MB (10459917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30ad6c82e2b7a536da67a837bec581308704d1e15eaf6e92c24578b56e187d9`  
		Last Modified: Wed, 13 May 2020 22:38:32 GMT  
		Size: 55.8 MB (55803040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db12f9ea2188013c93873ab0b43ec267f4b3fce432d19b3fd05e94e773d13bf4`  
		Last Modified: Wed, 13 May 2020 22:39:31 GMT  
		Size: 191.3 MB (191280938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:470abb34eccc6bd549c7f2bc4b7c75d7a2c13a7ea46afbb2f565ff2cf4b35491
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333251255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611e089dedcac15418475c933f9e6880e8779ca79c370a90b67b7c201a3794d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:38:53 GMT
ADD file:8842691c10d9cacf5f52fd9fdb3b0f3a9a5ed4212d9f2ab558d17e5efd9a758f in / 
# Thu, 23 Apr 2020 00:38:53 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:39:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:39:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:40:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:41:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bf245c0cdf57ebbfbaf49d796259272bf11094420c0537965c4d322d66b4e55`  
		Last Modified: Thu, 23 Apr 2020 00:43:49 GMT  
		Size: 53.1 MB (53124775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3766da29a92d4e7819901f2cd3fd92af428a41fa1efecc94dadb17f8bd6e6d`  
		Last Modified: Thu, 23 Apr 2020 01:58:36 GMT  
		Size: 8.1 MB (8110585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891810791eccf312b55bd366b84147115acf3dc533fd07cc22ed2ce3dd771b1`  
		Last Modified: Thu, 23 Apr 2020 01:58:36 GMT  
		Size: 10.7 MB (10657349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b2d4fc44bb2b15f9080c349ce508b8e7c2e640679fb59aaf2f9f78b4b2b456`  
		Last Modified: Thu, 23 Apr 2020 01:58:59 GMT  
		Size: 57.5 MB (57496351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6672e899d07c4422d9dbaced559f95bb0d5ee6140b5c6a476172131b2abef85`  
		Last Modified: Thu, 23 Apr 2020 01:59:54 GMT  
		Size: 203.9 MB (203862195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f4b48f3237081cae168cc74cd9bac7bd33a68996d22b6dc0800147c9a437db04
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305671815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949290776e4984545f43457f8fd2ec9ff39808d1bbfe4dbac9fbe295841cf1d1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:08:38 GMT
ADD file:01a8dba65674c16c3bae58d6e4cf7693a0616ee5efc5495e513ba4454fdaa97b in / 
# Thu, 23 Apr 2020 00:08:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:47:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1ccb563ff5d3d7b0b42a931c0aef1761ab04927c47d729b21ae98a7788ef6af2`  
		Last Modified: Thu, 23 Apr 2020 00:15:41 GMT  
		Size: 50.7 MB (50694211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cc1749bc72a1c4ea633b9f43ee46469e3c9b9fca82f799a577fbddf0a0295d`  
		Last Modified: Thu, 23 Apr 2020 01:06:10 GMT  
		Size: 7.5 MB (7460628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed375c9815816af90643e25af4799e3d5c112ac07bc80b13cc5976a394275f53`  
		Last Modified: Thu, 23 Apr 2020 01:06:11 GMT  
		Size: 10.3 MB (10324480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b47876b2590563400c1a797f7f51c2152380cb414e543cb90b037dbd2cee06`  
		Last Modified: Thu, 23 Apr 2020 01:07:06 GMT  
		Size: 54.6 MB (54585872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f39ba028ddcd6e173ca76dce16814d7bf73e4de689e3ff5705edcf7394b08c`  
		Last Modified: Thu, 23 Apr 2020 01:09:33 GMT  
		Size: 182.6 MB (182606624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d14043077a5b378ea7323d77e75815dd180c6bb176d7d435f08ae7bd8e148995
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342774999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562970dfd2104f374ad48968bae76c1f0b19ee0da1c6a863be8b3c81c01831fd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:32:36 GMT
ADD file:93aa541f8747875de57b6848e6e2df3b2ae7cdc03dcee5489fcfc1bbf45c4920 in / 
# Thu, 23 Apr 2020 00:32:41 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:40:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:41:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:49:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23044bc1c77de90086fe2791c49374dbad1ff9af6b3b4dde5f4d46fc92e6a936`  
		Last Modified: Thu, 23 Apr 2020 00:48:13 GMT  
		Size: 55.9 MB (55855771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b244e406f7e60e72181a1fc05e23631e55e349385a03256c692ed685e75d61`  
		Last Modified: Thu, 23 Apr 2020 02:21:35 GMT  
		Size: 8.4 MB (8356173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bb62044b675b46ae88158a62f5e93b36bed0459b07a8e50881cd48a7d4070e`  
		Last Modified: Thu, 23 Apr 2020 02:21:35 GMT  
		Size: 11.0 MB (10975739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3335db3829bab72102f9d1637bea7f1aeb652766860510ad63400bf5e283430`  
		Last Modified: Thu, 23 Apr 2020 02:22:09 GMT  
		Size: 61.0 MB (61002339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bf98eaf1596ff1d477b54f67a9f7f4262c973db57b18c260ce706e5ce99052`  
		Last Modified: Thu, 23 Apr 2020 02:23:38 GMT  
		Size: 206.6 MB (206584977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b88d11833f6e177b8bcbf1dd5f86cc64a2dbbbb0e3571740e64f1686c8a610a2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304558726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2746386a823c70b1c7ce44d30cfd66cc9db0d3492b1e6487093822358b44ab16`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:41:47 GMT
ADD file:fbad911feb95f3e7b45e9aa72be8710716eb8fbf3ba846fcaea87309eb9ba2be in / 
# Wed, 13 May 2020 21:41:49 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:37:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:37:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:37:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:39:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9ac9db0ba497fe825137b138e8deceb06a532f1ba6b367b8e68834caedf8e442`  
		Last Modified: Wed, 13 May 2020 21:46:15 GMT  
		Size: 50.0 MB (49994654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160b7562ce5394b96e6b7064989f4900b8d47965a7aab9b7f344e8f1514b24d2`  
		Last Modified: Wed, 13 May 2020 22:47:29 GMT  
		Size: 7.6 MB (7600664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b048fed0769ebce58b27d4fdbbae456c1810f6b85546360e3b80e36bb4be9d4`  
		Last Modified: Wed, 13 May 2020 22:47:37 GMT  
		Size: 10.3 MB (10347812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1e2837c528350ba56db4cda999ef6e93553ecf1d30819aa7eb54b31808155e`  
		Last Modified: Wed, 13 May 2020 22:47:50 GMT  
		Size: 54.9 MB (54900683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de18e2a5be7ad42c6500897b71704b2568498670ba5073c55dcbb9c2e1d04df3`  
		Last Modified: Wed, 13 May 2020 22:48:17 GMT  
		Size: 181.7 MB (181714913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
