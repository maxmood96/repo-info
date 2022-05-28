## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:d42f41d6a967a5d8d730afc2dfdb212b1a9ced2fbe36d00000fce711a9e21617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:eded6a17ba9e14443f9b739162335d865de0dd5e36545fce46b91887643a826e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338971063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb5cb7ca30e571638b39ae187a15671cb26b5284353a6aac0894407f505a8e4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:21:32 GMT
ADD file:dffa51e87e58558bb4b777e117ecb18500d90a9646513d0d8d9724bb5c949dc5 in / 
# Sat, 28 May 2022 01:21:33 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:43:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:43:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:43:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:44:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7fa02d3fa6e2ab30d6142a096f5321227237c89c02dd890ff9fa745dbf0790d1`  
		Last Modified: Sat, 28 May 2022 01:27:35 GMT  
		Size: 53.2 MB (53161898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0597a54f85d6fe31261321fa5abdce192dd72a61160f5a30e14cfb698b933373`  
		Last Modified: Sat, 28 May 2022 02:51:29 GMT  
		Size: 9.3 MB (9287856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0544dfe1044f9dd59f41f2b606fdedfe343ea2f2e7d6ac305fa10a471e369e8c`  
		Last Modified: Sat, 28 May 2022 02:51:29 GMT  
		Size: 11.3 MB (11264553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1758dc74532aa30f33a69018fed7293e1b1be73f54a3e385d575426ebbc6bbdc`  
		Last Modified: Sat, 28 May 2022 02:51:48 GMT  
		Size: 58.0 MB (58007355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7064d60734d8e3aba11cf1d1cb25b4236e88512cca96ea937da21db141f5fa00`  
		Last Modified: Sat, 28 May 2022 02:52:24 GMT  
		Size: 207.2 MB (207249401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:27444e860eab9366fa0e3c89857cbad92d526cbad91fcf0e93121f1740b6ca1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309590239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d132ff5fce9001e82fc52f8ad28fecbba8181711b1958330b34de1661e55e2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:06:33 GMT
ADD file:e64ba6aa11d10902c0a4ef8d3e05a21ff17f500ec2beb0d0704f12a033eecd07 in / 
# Sat, 28 May 2022 02:06:34 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:15:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:16:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:19:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:84223462af5a86d80ca0b6ee4295740a256dc6c036fd9bf8911e3d45aac34d9e`  
		Last Modified: Sat, 28 May 2022 02:23:20 GMT  
		Size: 51.0 MB (50961426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f88c92295b4fa5d01d5c7dd27b573f1426efbbe47348df31dc55de977a42f8e`  
		Last Modified: Sat, 28 May 2022 03:36:29 GMT  
		Size: 8.7 MB (8725167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb95b40f6f03c3c9f4041396fccdad464a167dcdabf7faa4ce59545b10eff9e`  
		Last Modified: Sat, 28 May 2022 03:36:30 GMT  
		Size: 10.9 MB (10927897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af801cca276fe8a8c2fa1f3f2f395ef1bf390a44b25cbcd5f6c27c81ee430fe5`  
		Last Modified: Sat, 28 May 2022 03:37:20 GMT  
		Size: 55.6 MB (55639049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658afdf25f2e6775d484a7e45081dc44520de0cccec63acb63e5cdc458e0b549`  
		Last Modified: Sat, 28 May 2022 03:39:23 GMT  
		Size: 183.3 MB (183336700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4b49b903f4a605bf006634512ba3446fdb753f01d7967577b13e41d6ca9f0987
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296398553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55be5dd021b0dbc7138f8b48b4f995747e08635f4f1d80458f2f85578e66c83a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:03:25 GMT
ADD file:8021dbeb20862f976e9f6edfab38dfb8756a92dd1ede73d49af4c657334e675d in / 
# Sat, 28 May 2022 01:03:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:50:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:50:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:51:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:53:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0e42766a606a457d26f0182502f6f1920959f31aa96f3bea8438d9c1662a0e5`  
		Last Modified: Sat, 28 May 2022 01:19:59 GMT  
		Size: 48.7 MB (48693491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c18451f312662604904a27a75c2a619f95996c3f8953c2894835994ef1938f`  
		Last Modified: Sat, 28 May 2022 03:14:46 GMT  
		Size: 8.4 MB (8394033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ababb74aefd4519ecdc1de94bab8271fdc2ba7a6a0b2288e65d7452f33cf91a`  
		Last Modified: Sat, 28 May 2022 03:14:46 GMT  
		Size: 10.6 MB (10572851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96a64aad191116b0a523175f0713d0852be12924ca13142989d6feaecc7dd86`  
		Last Modified: Sat, 28 May 2022 03:15:34 GMT  
		Size: 53.6 MB (53563481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b718326b52a435522150cdb4a4eb7ac5e54bfa12a581db5599491436e16dfab`  
		Last Modified: Sat, 28 May 2022 03:17:23 GMT  
		Size: 175.2 MB (175174697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e172b19383e8f5ac1b7d66544ebc41331678722a0efdaf2d56221c7b14741e15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.6 MB (331579021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5631c5b0533fd7b9c1831f9486ac16b2f39e8b69e3883338d3b75d80b834356e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:42:02 GMT
ADD file:759f672e6b6df1008eaa41bb27f3166127eb98b40bb49919dd41fa53f7e9d598 in / 
# Sat, 28 May 2022 00:42:03 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:09:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:09:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 11:09:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:10:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eab2172da7bda865d054e2983e44baa941cea4422c5c64ceeb52f19efc8e9a16`  
		Last Modified: Sat, 28 May 2022 00:50:07 GMT  
		Size: 52.3 MB (52261302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a768e7fb1617046d5d64129137bf35747a2d6d2015e07b401b154dc7cab9609c`  
		Last Modified: Sat, 28 May 2022 11:19:27 GMT  
		Size: 9.1 MB (9127458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d3aa946e9b0c8414bb8ac3a4a28825a22da28c77e3c6a62a17638c8cf7cc27`  
		Last Modified: Sat, 28 May 2022 11:19:26 GMT  
		Size: 11.0 MB (11041982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9139da2aa77188296cd4e3ffb0b74e9f99e5eb8b29415a2240694ae2252205`  
		Last Modified: Sat, 28 May 2022 11:19:46 GMT  
		Size: 58.0 MB (57980235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc7d1127f96f27f9a13045841ce0c4f19ac5a90394bbff38d498fc3f20daa0a`  
		Last Modified: Sat, 28 May 2022 11:20:23 GMT  
		Size: 201.2 MB (201168044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d4a49eb9de58cb6413868615fb3dd9443d4d1dd956a9701c6ff08c421da94a96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.1 MB (342070575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca3062b51aee7ebe833c434205bba8d3950f702bdf00f7918f52ee3277facdf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:03 GMT
ADD file:dd10bdbf07bc13b42a7021b48621548cda7b383bf0edb8dff1e35d908f50c392 in / 
# Sat, 28 May 2022 00:41:03 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:14:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:14:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:16:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e233042357300fc1ac460e8583f90e2b88388d7c2a9016f91be99da315c46fcc`  
		Last Modified: Sat, 28 May 2022 00:49:18 GMT  
		Size: 54.2 MB (54158716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312c6075d7bd54d76868fa2bfad3038339123706e4120edfdacf8be48665b2fa`  
		Last Modified: Sat, 28 May 2022 01:23:48 GMT  
		Size: 9.5 MB (9462060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e741e6836ace09c243fa9be77aa56380eeef9635c1dfa4f211ea482b290a4784`  
		Last Modified: Sat, 28 May 2022 01:23:48 GMT  
		Size: 11.5 MB (11464411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81a6911feb95db15f083eaccde4a7497085fd4d68ac9f7f6ceae43f6483b9b2`  
		Last Modified: Sat, 28 May 2022 01:24:12 GMT  
		Size: 59.5 MB (59477302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c71aeddc878b3c709ede78696e48a559dc7766bcbe9026bb003dd368d4177c1`  
		Last Modified: Sat, 28 May 2022 01:24:48 GMT  
		Size: 207.5 MB (207508086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:90b5ed050acbddf9a8c694e0cfb40890a2e7394294545223d626c4ed54061c8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.2 MB (319197229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7f494a1755d791268f8ebcd383e081d1cd611287b247bff036e5fd840429a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:14:06 GMT
ADD file:1687a4039bc00edb9de7ba18be7ce08c7df3d2cf6a4b7a30cb5bb60f41d3c082 in / 
# Sat, 28 May 2022 01:14:11 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:12:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:13:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:14:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a7336e150b70b2115ef0d770279f4e6f79de8d6e16c87dd256445530c1c68d1e`  
		Last Modified: Sat, 28 May 2022 01:24:53 GMT  
		Size: 52.3 MB (52283200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d31486dae68c1e92361c28f610c582d55f682b8dc91e6fadc6ce7d2f167d0f8`  
		Last Modified: Sat, 28 May 2022 02:30:37 GMT  
		Size: 8.7 MB (8654895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a846f26a733756e5b7a30ab3e72a8147961effdf03d7e9b981808ea3ffc7a6d`  
		Last Modified: Sat, 28 May 2022 02:30:37 GMT  
		Size: 11.0 MB (11019421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f22fde9ffb3511f19f6a84ee5511872740b6a37e844fdb93326adc895f8dde4`  
		Last Modified: Sat, 28 May 2022 02:31:27 GMT  
		Size: 56.6 MB (56621054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835cb71964c0b8f5e94466a46b6d004b0f3c861bcc1c853a3f3e279f27a4ad75`  
		Last Modified: Sat, 28 May 2022 02:33:37 GMT  
		Size: 190.6 MB (190618659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fb498fbfff93344ba755ba5b6c26910bf43459a5eab2ddac155602fd7c9c8063
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.5 MB (349476888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f165ccb43b3dd0eed4e187e01a69a05c356c16d5496633954ed24d03e48dc3d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:25:12 GMT
ADD file:ae9857e5f5e911c083920a02f175061f1626b33e8244c6b286b16a61fb6326ab in / 
# Sat, 28 May 2022 01:25:17 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:23:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:24:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:25:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:30:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:37e804d95f71e07756995895c16c589fb7c512c0b5fda75c9e57d4ba10ea4c27`  
		Last Modified: Sat, 28 May 2022 01:34:49 GMT  
		Size: 57.4 MB (57378472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7461effc372e5ee4bd7909ed036e44f7b839da66ba136f7add0d1221c18cbd`  
		Last Modified: Sat, 28 May 2022 03:38:27 GMT  
		Size: 9.9 MB (9880924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3a54c3d4f16e2101943055448a74b563c54f32ad957a68eb5dba4c980373c3`  
		Last Modified: Sat, 28 May 2022 03:38:27 GMT  
		Size: 12.1 MB (12065230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d030f83cb04ad5b06d1396bcda4925db17a6880b92c2161c73a4a52615c076f`  
		Last Modified: Sat, 28 May 2022 03:38:52 GMT  
		Size: 62.8 MB (62755153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5805742b88e53045692feebd6eb6ebb29a36560266cc5a98a48b0521259d2c6`  
		Last Modified: Sat, 28 May 2022 03:39:39 GMT  
		Size: 207.4 MB (207397109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:48f7b5303233d86faef463a0f3008a19e4ff0bfdae3cc34996d959e404a6961b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349184976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69ccee7c07abab2f6eaebdc0b36ce2226ac54b80366790e290d024cabd9de42c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:15:02 GMT
ADD file:2406fc75a54a3bdd547095c2a1dba6a536074c482469bd532302201fd8585b5c in / 
# Wed, 11 May 2022 01:15:05 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:34:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:39:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:48:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:642ffa8f974e66e7604ce50484153cb3846bd0cb22b2911d01ae5ea68df5291f`  
		Last Modified: Wed, 11 May 2022 01:33:44 GMT  
		Size: 49.4 MB (49377677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b907969c96c55da8d5b6b71e6af3f13438e5d6fdd5dfe41d51bbedd23697a79`  
		Last Modified: Wed, 11 May 2022 03:17:33 GMT  
		Size: 7.3 MB (7258557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38d53965d18bb01a1ca71823c7fcbe5f088068e2ef79d5e1c6a55c4d71c5b4e`  
		Last Modified: Wed, 11 May 2022 03:17:35 GMT  
		Size: 10.7 MB (10650582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942330f4ec5637f6c0393c379b17ad805deb19c2fbe710dcaff8061460659625`  
		Last Modified: Wed, 11 May 2022 03:19:57 GMT  
		Size: 53.9 MB (53923051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fd6bb34a19b7c27ef07deb19dc486565079a54662f3806f95b3624b02813d6`  
		Last Modified: Wed, 11 May 2022 03:26:18 GMT  
		Size: 228.0 MB (227975109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:194fbc367b32366ad8a9ea24273807ce3e6be26f1177807e54559c1d93c09e64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.8 MB (310802251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b18cab60bd380c6793d277eb4ce112f6c27e3725fa1e87fc3f1a99748e00b3b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:44:37 GMT
ADD file:03a528116badd98d1660ab1a83ce0462a11168a2dae972be4891032c54483f22 in / 
# Sat, 28 May 2022 00:44:41 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:28:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:28:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:28:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:29:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0cf941fb152b37e3fda284ae5eceb3dab36c26511fe06a7105ee43081ca68554`  
		Last Modified: Sat, 28 May 2022 00:51:02 GMT  
		Size: 51.7 MB (51703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ecd77e960fd212da3eca4e59b9c918e4d7af7e1ea705150c26c05f5967f79`  
		Last Modified: Sat, 28 May 2022 02:36:52 GMT  
		Size: 8.9 MB (8938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b6e701baf55072de709e3a913641d40af39439387278f3abde5d58deb12714`  
		Last Modified: Sat, 28 May 2022 02:36:52 GMT  
		Size: 11.2 MB (11157585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394d800eeeea5c5491bdadd4fd5e6397e7591cca3df4558fab6201da7b3eab68`  
		Last Modified: Sat, 28 May 2022 02:37:07 GMT  
		Size: 57.3 MB (57296990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a139bd14a98f73dd54d99904f7c257ace0627eda96a049883763eda277f197`  
		Last Modified: Sat, 28 May 2022 02:37:35 GMT  
		Size: 181.7 MB (181705540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
