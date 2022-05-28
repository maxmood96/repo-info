## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:c269ba99911ffdf06830399eb047ef3c09fb272f91903f22ceaac6f875d7a3d7
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
$ docker pull buildpack-deps@sha256:1200bbd948df83b25b5da35f798926d177eb25ed356a4526e21f273173dc5098
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.3 MB (308317809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2962d9b1374b455046f3a9a6cba73bd2b23bacc6d909d3b5149c3a117938da52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:53:50 GMT
ADD file:4f142f5aefa97fb474a705d0b74abadc5a3efdc7faa28a865e8f774b46affcfa in / 
# Wed, 11 May 2022 00:53:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:15:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:15:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:16:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:18:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1faa3808d790c86a331ed5dce0a7a8af6a26aa395d982f287f5d3fe6362186a`  
		Last Modified: Wed, 11 May 2022 01:10:36 GMT  
		Size: 50.9 MB (50939831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2bd191c3a53704df74788d319588194c3f1115cfa7ce0b029d942621a231b1c`  
		Last Modified: Wed, 11 May 2022 02:36:13 GMT  
		Size: 7.5 MB (7537835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8271993242928fca4b8160659ea37b8a1b4a3ca033c568f9e9c1b99e9a9e04`  
		Last Modified: Wed, 11 May 2022 02:36:14 GMT  
		Size: 10.9 MB (10927528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da3f3eaccabf091adab760ec3c2e8c7aaed5cb736e07943be5b8b69679038c`  
		Last Modified: Wed, 11 May 2022 02:37:07 GMT  
		Size: 55.6 MB (55630199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f19ac5fd8a73e1c95d6119c051e23e4527cee5cfbed5c21a047a7060edad37a`  
		Last Modified: Wed, 11 May 2022 02:39:10 GMT  
		Size: 183.3 MB (183282416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1360690109c7548550c322dd2cfe85993c501822622b32ebf69b2c366e021c53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.2 MB (294243137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac49262be93d85adf2857b51ee93344cb3ce3f881bba332e207fb097ea0c4d25`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:52:42 GMT
ADD file:5256a3df37de011e57faaf3b387bbc66fc94fceb82c48ead6b9e5775cbe7bf21 in / 
# Wed, 11 May 2022 01:52:43 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:29:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:29:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:32:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:528d9ed2cb56db465cbc360f474c45ab8e5ae05c0a0f596fae936fc1290bc68a`  
		Last Modified: Wed, 11 May 2022 02:09:01 GMT  
		Size: 48.7 MB (48678301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d1a1a1705b16f0412d469f63dae500ab636c3d7d35a70874baa189b03a3579`  
		Last Modified: Wed, 11 May 2022 03:52:19 GMT  
		Size: 7.3 MB (7269475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0226a116d43744d6f9e056ad8e8a6469b2462f8cc039fafca040cfa47dbf0da1`  
		Last Modified: Wed, 11 May 2022 03:52:20 GMT  
		Size: 10.6 MB (10573123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8b8551ee0c609b1218c73a583d5c06d28931fab52d37abda11cf0e20b75f2b`  
		Last Modified: Wed, 11 May 2022 03:53:08 GMT  
		Size: 53.6 MB (53558457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b71872a483b4294a3bd82888740cb4df6e84c5b6d37dd1cb9c49b304afde36`  
		Last Modified: Wed, 11 May 2022 03:54:54 GMT  
		Size: 174.2 MB (174163781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8649462d2e29d5e7c0b7149981f5813b0f9acbdb959fc6aba0c04bc19fa2a89b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330094884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781342ac947e325f0c41badbab10f3dd89147bd610f0e0d965ffb214a9d91eec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:48:25 GMT
ADD file:57e11874acd2dc9e0376f854ffe18bfb0b25f8a7a933a3c619d173176c08e412 in / 
# Wed, 11 May 2022 00:48:25 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:28:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:28:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:29:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5489557693077b493aaa820cc173d6947baad433930a473cb7cbbb4883ec94f9`  
		Last Modified: Wed, 11 May 2022 00:56:14 GMT  
		Size: 52.2 MB (52242857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b334af1a397894abf6045ff032026c9b4f342acb68ecfe554c22a6f0f272a613`  
		Last Modified: Wed, 11 May 2022 01:38:13 GMT  
		Size: 7.9 MB (7853722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5604865b4585f274eea230691352b972c26efb7b509f1c89ee586a4c6a3559a`  
		Last Modified: Wed, 11 May 2022 01:38:13 GMT  
		Size: 11.0 MB (11041972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7bbb22e05bd64b1830d1bc074724bb1f87693a3a59566b6c2e1ae211de5c50`  
		Last Modified: Wed, 11 May 2022 01:38:35 GMT  
		Size: 58.0 MB (57981229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f57d229b446bdc26d60a87a04a9093c604088cf2c4c93ac39e93a6f178df596`  
		Last Modified: Wed, 11 May 2022 01:39:13 GMT  
		Size: 201.0 MB (200975104 bytes)  
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
$ docker pull buildpack-deps@sha256:36c341fd0eea9e8f615d1ce40289270a34f6197511bb86ce69cbd25f7e473721
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.7 MB (346681459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:116b7d405b952c095ee4a1fa9c777df2a9e81c04b95f9e29a67c0c53e8af74e7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:35:07 GMT
ADD file:7d4f085f5fc874b6142d1d0a27c78512d764e68948baffd110bb6e1ff77c725d in / 
# Wed, 11 May 2022 01:35:14 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:22:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:23:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:25:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:42:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6f5d4115fab6dd67cca7bafe684609d704cd4e4c3229c7f62f0f1476fe5cfd02`  
		Last Modified: Wed, 11 May 2022 01:45:26 GMT  
		Size: 57.4 MB (57352362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6e8dc2a59c36e07c0ede228c6fdead6ecc03a566fd7328823d686733347f92`  
		Last Modified: Wed, 11 May 2022 03:51:04 GMT  
		Size: 8.5 MB (8492692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6348a08a5fd7953090a3d9ecb22bde8041eae82839726dcf3cfccffe516ee74f`  
		Last Modified: Wed, 11 May 2022 03:51:05 GMT  
		Size: 12.1 MB (12065584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea355dee2bda8ba0c778bfafd143f25e8d2c2ece067b8c73b09037c1734d665a`  
		Last Modified: Wed, 11 May 2022 03:51:31 GMT  
		Size: 62.7 MB (62745303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d75510289134ef71b58e6271370b0fb99b76560574e3a66f68efa41a83f17`  
		Last Modified: Wed, 11 May 2022 03:52:19 GMT  
		Size: 206.0 MB (206025518 bytes)  
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
