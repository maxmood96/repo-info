## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:153d0f8ea39702ca508397f8cfd25c2ebab06d63d1fd055d0bbd99cb36687a5e
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0434585d0e6839a6e443d5fda8170c58e37fe2a400e7727dc697f48db29e9ae6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.0 MB (322047936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7885940ab6e819fa9219d03f22307e554ae5aa058e39b203b0570d03df7897bb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:22:32 GMT
ADD file:2077716d4a510c614acac732f9b9130b649ac696764e3becc6e21e732f39e9c6 in / 
# Fri, 26 Mar 2021 15:22:33 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:55:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 05:55:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:56:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6db1addbc87ce8e502d75dae59834703a516712298c58eaee03f40a399e8292`  
		Last Modified: Fri, 26 Mar 2021 15:30:40 GMT  
		Size: 54.9 MB (54868141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c35419454804f7f03cee42332003684321f19b8eeabb984508adeca960915a9`  
		Last Modified: Sat, 27 Mar 2021 06:05:21 GMT  
		Size: 5.2 MB (5151380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a653a12fbf3681c630c113c136ea8fb5d543bd19153c6cf29b64de9459ad295f`  
		Last Modified: Sat, 27 Mar 2021 06:05:22 GMT  
		Size: 10.9 MB (10868989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c33f008f2e304e642bb8f66a59970deb0d5d0528df27d71197659ed414617fe`  
		Last Modified: Sat, 27 Mar 2021 06:05:48 GMT  
		Size: 54.8 MB (54797490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c3e77dfedd3aa53fe4f39dd7fbaf6b4d887142209ace9f26dae5ada5b8c0f6`  
		Last Modified: Sat, 27 Mar 2021 06:06:35 GMT  
		Size: 196.4 MB (196361936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:829f23aa689a909f163572ce833d222f2cc4a46e7c91f55d07cb7fa75d9a7eef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295104645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08eb1e2079aff6e09561be8610a0d48803d406ef8336fcc2d9bc093db84b373`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:54:14 GMT
ADD file:ac1ac9f39520995697d7545a4221ddb94e841eedef2eaa8bfc265b3840c9d873 in / 
# Fri, 26 Mar 2021 07:54:16 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 09:15:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:15:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 09:16:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:19:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b6ade6f33ef6b8c4fc72e7adf3004838c72714ea31573c675126f6144bbc650e`  
		Last Modified: Fri, 26 Mar 2021 08:02:48 GMT  
		Size: 52.4 MB (52402425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59c5c8b0fd74f36c82afb1a6f410dc3d75f681362b9f141a9904658804af12c`  
		Last Modified: Fri, 26 Mar 2021 09:29:14 GMT  
		Size: 5.1 MB (5060923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f841801148a4983446f3f0e72c194c22a654c192eac11f102bc7f05a2e5f6c7`  
		Last Modified: Fri, 26 Mar 2021 09:29:15 GMT  
		Size: 10.6 MB (10570397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039badaf78e1b39f8343970b477e6192b14f2f1a3a29c08fd53f30bc23ad2d27`  
		Last Modified: Fri, 26 Mar 2021 09:29:38 GMT  
		Size: 52.5 MB (52498023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1668a1e122bf8d91e19dc33b2033e25f8988391dd0737feb5cb88abe511f92`  
		Last Modified: Fri, 26 Mar 2021 09:30:44 GMT  
		Size: 174.6 MB (174572877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d5af6bf34a6db9204bd245401853971fa28ea254a37ab9194a38b0f0f9186523
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282556868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce8e17770336c0e50e79bf662a7b6b2f22406e63160200a30dfaf8a107cb371`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:20:34 GMT
ADD file:f0720ec9bf7f39f48d23428e3a1efab23881784e0db60db3031465e45c1d4893 in / 
# Fri, 26 Mar 2021 11:20:38 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:26:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 13:28:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:30:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9215022a83fc46d1d35467f5bc69faee0fabb5fa515b7fe907a7f483cf1e6223`  
		Last Modified: Fri, 26 Mar 2021 11:29:54 GMT  
		Size: 50.1 MB (50071169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c633ce4b5971f906b64dbb1f40d78e435bd4f582179e60994bc399bf45ffe158`  
		Last Modified: Fri, 26 Mar 2021 13:53:35 GMT  
		Size: 4.9 MB (4920691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efbcabf672b68dab52cce7bb41819db259dd2a29a05c53c36a0e536ac293ad49`  
		Last Modified: Fri, 26 Mar 2021 13:53:37 GMT  
		Size: 10.2 MB (10218177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8cd95acbc46bef96617f3164ad54136cadeb8f83ee8ad9cb03e7a5163291b9`  
		Last Modified: Fri, 26 Mar 2021 13:54:14 GMT  
		Size: 50.5 MB (50514544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c94ac7b7688d1c295451cca43e3e948d221f7023b3ca379d4be4dc1b0adec3`  
		Last Modified: Fri, 26 Mar 2021 13:55:16 GMT  
		Size: 166.8 MB (166832287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:270fdd1e364a9b59aa4d2d5bcdf067ce806c7e42dc91c6d298f92d976c8221a0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313739729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b321973d418f905dbbdefc515fcfbe00011a40997afd0c51193f5b5bd3f74cc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:42:57 GMT
ADD file:f4996084bc36b7fb278fffaf4537c601ae8dd7242e317c6a7375ebb583a47de3 in / 
# Fri, 26 Mar 2021 15:43:00 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:17:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:17:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 04:18:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:20:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:95ada4763c46cfdb13ca1bf668b156e961a0b65481b836ad37f8ad1c69235782`  
		Last Modified: Fri, 26 Mar 2021 15:49:44 GMT  
		Size: 53.6 MB (53555994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2b48c3e8db9adfa9005d7a5070e70d8147f69737e3683a908a04f35af56afb`  
		Last Modified: Sat, 27 Mar 2021 04:29:24 GMT  
		Size: 5.1 MB (5140788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d2ee4c7d66039c5dad756b89ccb3b270e058f38063748585bacb2c5db88dfe`  
		Last Modified: Sat, 27 Mar 2021 04:29:25 GMT  
		Size: 10.9 MB (10868501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dbab1a501e990f9975d868499a8cb465a2c32ba33bd3881981c1a16e8c124e`  
		Last Modified: Sat, 27 Mar 2021 04:29:46 GMT  
		Size: 54.9 MB (54921135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd0800880443c6e9b4032233416e6b783a50115118437ea7f072c74273ccc7f`  
		Last Modified: Sat, 27 Mar 2021 04:30:35 GMT  
		Size: 189.3 MB (189253311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b828dc773991da308248d153afd42f254fdc491f2962bcaf6f531b66e8eea6b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327906403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b98fbd0a4682eeaebe808e2c0884f6187b02bb543b5417a991372609391eef4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:55:01 GMT
ADD file:325ae30975853b6389efde932aad38dd1eff2d79da625d4986da0e4690222e98 in / 
# Fri, 26 Mar 2021 13:55:02 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 22:45:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:45:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 22:46:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:47:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f257c933d0ea6db1761240613e31039e161f54a3dbb897ce7f0da89b673a0e1`  
		Last Modified: Fri, 26 Mar 2021 14:04:49 GMT  
		Size: 55.9 MB (55881747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c690f0b66f608bc78a5f86e42e06190e29ff50df3d9076b8641d56d498c69946`  
		Last Modified: Fri, 26 Mar 2021 22:58:21 GMT  
		Size: 5.3 MB (5280228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949c2a8ae70678580d6ab562e1cc96e6698fa81a6e115fc69251ddf840983125`  
		Last Modified: Fri, 26 Mar 2021 22:58:22 GMT  
		Size: 11.2 MB (11249035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c53f34f8d3d2e454d46fd78e6e0fd068549deb2810aa6480d768f46ce96e27`  
		Last Modified: Fri, 26 Mar 2021 22:58:55 GMT  
		Size: 56.2 MB (56194294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef612c63ef520e244b709a56e15f31a24d0ac8bd904824eb6e09ee9d27977878`  
		Last Modified: Fri, 26 Mar 2021 22:59:45 GMT  
		Size: 199.3 MB (199301099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:35c7d28769713a94a122626825394e9483c08f1067cb2e0ae563c9ed25699b4b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.5 MB (301512806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a509d69f435d10f9eae094ec6fec7aee9db9b16ac6531ae43bcbe5f2133c61`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:10:22 GMT
ADD file:45a8dd112a282d4aa23c7808fe9a53a90aed8669a8c0886cbd1b014e6f666e5c in / 
# Fri, 26 Mar 2021 08:10:23 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 18:23:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 18:23:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 18:24:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 18:26:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dc0d626a86c29f3dd61b7699812357277c6ad4db66ed29b70e541593f9a413f7`  
		Last Modified: Fri, 26 Mar 2021 08:17:18 GMT  
		Size: 53.1 MB (53126824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dbc70ea4ba58905300e32d855fc4d13e3e008870c30e837cc6f6dfcdcab138`  
		Last Modified: Fri, 26 Mar 2021 18:34:02 GMT  
		Size: 5.1 MB (5112937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41493924139fb5a5080623341557e04fd10346da8a0160b092abe10a70a9bd68`  
		Last Modified: Fri, 26 Mar 2021 18:34:05 GMT  
		Size: 10.9 MB (10870966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c018885aedaa8429663a15cf82500c6ef6a38fa4825e54b92b34617d9f1195f`  
		Last Modified: Fri, 26 Mar 2021 18:34:57 GMT  
		Size: 53.6 MB (53589126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfedecb8a8e118fadea753d9fdc31cadf293815111fdd7a4b1adf67247d92eb`  
		Last Modified: Fri, 26 Mar 2021 18:37:13 GMT  
		Size: 178.8 MB (178812953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4391fbcc9c9922f91881288e0ea90d2916d39842a7328b176011923cca025b96
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.6 MB (330612347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f275b7d562ad798bff1da5ccac11d538e799b97bc9968f950cf7c150c4f8b0aa`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:14:45 GMT
ADD file:7106c38838d3049ea5f78c190ea790f58ea352546fd1b55d2b07a152c34377c3 in / 
# Fri, 26 Mar 2021 15:14:59 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 17:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:57:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 17:59:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 18:15:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9927b5cbb0465e067777696ede5217a35993b727460cf5c92037d8823b48a09d`  
		Last Modified: Fri, 26 Mar 2021 15:22:31 GMT  
		Size: 58.8 MB (58782693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58a377d45252b512386356a873c76bee0b1dfb06189ebc9b0b723496f735b20`  
		Last Modified: Fri, 26 Mar 2021 19:47:59 GMT  
		Size: 5.4 MB (5399498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6380788cb9eda4a73e189b4139db3eda3a7b9f06d4e61e07160541bdec59499c`  
		Last Modified: Fri, 26 Mar 2021 19:48:02 GMT  
		Size: 11.6 MB (11620804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ab28fdcd101d36e0d65b5b21d6b4f2e279d3e3c3e3c697731427cc603160d8`  
		Last Modified: Fri, 26 Mar 2021 19:50:09 GMT  
		Size: 59.1 MB (59137708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbbc6d9c3d4f8f62c9f32f71132b4f98e4e48be5073d0b073cebe97d252c964a`  
		Last Modified: Fri, 26 Mar 2021 19:53:50 GMT  
		Size: 195.7 MB (195671644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fc7b44e0dbadb593021213579cf510d3603fbc2017c722933f074520b7790667
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295660228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b077422ff7a2fa61887e8857d6e5bbc6829c2457253b82736a0374e2821b14c6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:54:01 GMT
ADD file:8073185e7ca9ded5b755d41c6e6b271ac3eeb13accedefc51935a2ef173aa944 in / 
# Fri, 26 Mar 2021 10:54:07 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:48:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:48:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 15:49:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:51:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0602fc01f39ffcae884dcb0ce753aa9f918b25b3dbf0527130db85a52ae23c87`  
		Last Modified: Fri, 26 Mar 2021 10:58:00 GMT  
		Size: 53.1 MB (53147418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1644fe478d2fe4baf12ec289cf704ffeae47219f908c0003d9f85b69ba5434a2`  
		Last Modified: Fri, 26 Mar 2021 15:56:09 GMT  
		Size: 5.1 MB (5134178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebd6937ebe551c76ff20b4d4376d63cb8df6517263728ac6c8f13d7bdac6399`  
		Last Modified: Fri, 26 Mar 2021 15:56:10 GMT  
		Size: 10.8 MB (10758784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4236076fdb459093d3aea87350bdd03ac58a0e3808165e133ff6662a874e4`  
		Last Modified: Fri, 26 Mar 2021 15:56:29 GMT  
		Size: 54.3 MB (54256129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce36c1fa894c15ca3bc0fbc78457e9138ba0b1c10e391a448cc92f2b772c07cd`  
		Last Modified: Fri, 26 Mar 2021 15:56:57 GMT  
		Size: 172.4 MB (172363719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
