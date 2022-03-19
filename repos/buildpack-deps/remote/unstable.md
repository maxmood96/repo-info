## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:bb797473421a3988e61b50c3dda719015f193e0a7c18262efe2c80d10031702f
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:537c450e26570d166c08b4a4229592c9c5d50e8693f064b0a2a4de080fba17e5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.4 MB (335350081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361561e7ffa759ecb911798f862d38defc1fbc276944b34ceef36d0a1d6f8304`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 04:05:54 GMT
ADD file:20b1068c276c223839818edd0aca3981a1b8139130064d19f9ec38e26a94ff27 in / 
# Thu, 17 Mar 2022 04:05:54 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:33:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:33:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:34:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:35:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab40a96ab944197ee11d696f776db9c1130db9825e9996a5e8939611fcf5e470`  
		Last Modified: Thu, 17 Mar 2022 04:12:27 GMT  
		Size: 56.0 MB (55984715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214f624759443498bdf804a19e1294b81976d28ed00d521e85a6ef33658ab378`  
		Last Modified: Fri, 18 Mar 2022 07:05:57 GMT  
		Size: 5.3 MB (5269458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59203613ecfdfcaa48f715e4d48dfb31fde19bed9d8d6dd6886973ca3d859f7`  
		Last Modified: Fri, 18 Mar 2022 07:05:57 GMT  
		Size: 10.9 MB (10924378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a88b822c644e86ce744ca1d166b2e420d9afa87c5a9d8f72b763751621710e`  
		Last Modified: Fri, 18 Mar 2022 07:06:21 GMT  
		Size: 57.2 MB (57193465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac98ad5917f47a068934121d57d49b1a3ffb0679a6d377a4f720b2f184455400`  
		Last Modified: Fri, 18 Mar 2022 07:07:13 GMT  
		Size: 206.0 MB (205978065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:85b23d31cbb8dfbf10de80f5407385d1c0a54ffa182455c4ee204d83bf952474
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305788063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a33e3b03a0aa1952b1bc8ac5a34ca1562fc7aecfd870c4eea5da39cc1c3b03`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 05:23:03 GMT
ADD file:a9d4a5aa739c9c980a2e0b3342f616a0ef24327457038a7d2d1f054b47bb869d in / 
# Thu, 17 Mar 2022 05:23:04 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:24:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:26:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:28:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1b1560f4e7f4d5dc335516eb5f16007a5ba8efcbedcc5584f361684738e508d`  
		Last Modified: Thu, 17 Mar 2022 05:39:40 GMT  
		Size: 53.4 MB (53393523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3688991f52d334055cd012a6287b39073e9b4ac6c7cd7012b2c8be6c4cf410`  
		Last Modified: Thu, 17 Mar 2022 19:44:30 GMT  
		Size: 5.2 MB (5164495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247526418f56b9d635ff39e99bd9d2058cdf75fa52ee8a6fb0e2a007868a5e12`  
		Last Modified: Thu, 17 Mar 2022 19:44:32 GMT  
		Size: 10.6 MB (10597460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46eb17078ce0bb185a36f41062c74581f4ba10f530a5751c9f5b4a0565ef41`  
		Last Modified: Thu, 17 Mar 2022 19:45:08 GMT  
		Size: 54.8 MB (54805847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b052ca53bb7c0bcbf29714d8462923cd7d57a6e20a97449d2216e4ca804d67`  
		Last Modified: Thu, 17 Mar 2022 19:46:21 GMT  
		Size: 181.8 MB (181826738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5d126e3e1621d581fe49bea7f6611fcf991fa6f89c76bde7d97ced1e00c8c35f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (292995514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff4229230bad5268276e82a4983543d6913f1713db0ebdad884b99b1ab5ed7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:34:34 GMT
ADD file:9aa47fa903f49c3cddd2c04ea6dfc8adc7cb3e1b8f49392eb4ef30199e306b55 in / 
# Thu, 17 Mar 2022 09:34:36 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 02:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 03:00:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:02:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5abaa3393d9da88a4f8667cc7ed186e0fcf756926f31ba33f3b531a2db42031`  
		Last Modified: Thu, 17 Mar 2022 09:51:00 GMT  
		Size: 51.0 MB (51008095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a92e937e95ec8c4708c51bf5b42788af6dc7933017024adfe3755af9a222a4`  
		Last Modified: Sat, 19 Mar 2022 03:34:48 GMT  
		Size: 5.0 MB (5023856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f9c704ba15933d332549e911b8ecf5197b7956ef44f600fb06943964d50581`  
		Last Modified: Sat, 19 Mar 2022 03:34:50 GMT  
		Size: 10.2 MB (10244633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b84168887f66171a81e384a0ec065ccce1eed8938b60a25c845862b96da581`  
		Last Modified: Sat, 19 Mar 2022 03:35:37 GMT  
		Size: 52.8 MB (52834495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a49bc4f8ca4cbddbb3456d9c8e52b57be4cbdf7a555fd7b4179fb2a0da4dc2`  
		Last Modified: Sat, 19 Mar 2022 03:37:25 GMT  
		Size: 173.9 MB (173884435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef9de6e4f596758293eeb2344168dbf055e87dbe126c9f14d2ddaa26cc1f9f82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327711371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b32d2fbe518a5e74d8120809d1f96b98af3b39be146af4bee3e9d21b645b0b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:23:19 GMT
ADD file:1d38d88879da25d9a1bc7a4c5e36bc54d45209f4c931e6da3f7a5121498cecf5 in / 
# Thu, 17 Mar 2022 03:23:20 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:13:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:13:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 22:14:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:15:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1bb23fb7eb3b065e76a0f28cfe8d85ecc762b7cff467fdbcda2f70363c88087`  
		Last Modified: Thu, 17 Mar 2022 03:31:11 GMT  
		Size: 54.9 MB (54916866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c42e541f9a190ed5b1572f38d77d9a07c7899f7b9640e25460c12e849991f1`  
		Last Modified: Thu, 17 Mar 2022 22:23:20 GMT  
		Size: 5.3 MB (5255457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556c64db2922b5a87b5591ed9b67221014a21677b094903b77fc24099a5a1f3c`  
		Last Modified: Thu, 17 Mar 2022 22:23:21 GMT  
		Size: 10.7 MB (10693240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a84215e2a63ae365e4e0fa67da1b0c8f3b996b8f6f063442e4530fbcc3411e5`  
		Last Modified: Thu, 17 Mar 2022 22:23:40 GMT  
		Size: 57.2 MB (57227764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c549492ab6887e2141e7f726464a89ee0d1f13e7f1faf4fc4601e35c1879aac5`  
		Last Modified: Thu, 17 Mar 2022 22:24:17 GMT  
		Size: 199.6 MB (199618044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bdcda8f4f5c104cf0f92911cbefc4bddb6e0d4b77945e31bf30d984ec15e31e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338670165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fed2698898995e6833b77c0ed73d26f3e6289ecb85e7e28e0abac3d2995cfea`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:17:34 GMT
ADD file:2cb9c8978846d8941a8213d064afc34b86f2f04e601b9ab365a29fff596c2aa5 in / 
# Thu, 17 Mar 2022 08:17:35 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:30:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 14:31:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:32:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23f252c494b0d56260da77f35c850c42d26d01946241721f649418fdd13ddb96`  
		Last Modified: Thu, 17 Mar 2022 08:26:58 GMT  
		Size: 57.0 MB (57031438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713c087b701c0e96ba52a634dca0b79b7bfc26336946b8ef9b7bb6deda31d1c1`  
		Last Modified: Fri, 18 Mar 2022 14:46:45 GMT  
		Size: 5.4 MB (5401519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c902ee6ab20573e3958bbd0b3e2ec3a189d08dc0fdac8987424bf548e32cde9`  
		Last Modified: Fri, 18 Mar 2022 14:46:45 GMT  
		Size: 11.3 MB (11322536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722bbd8ae920e50c9410f926a8e92f3781c08987e33e82b3fd5d3530ae5456bb`  
		Last Modified: Fri, 18 Mar 2022 14:47:11 GMT  
		Size: 58.6 MB (58609478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b23772060cfb4ad0040e9c78059230109d4b359cb5e6c977fdca8c007d7d05`  
		Last Modified: Fri, 18 Mar 2022 14:48:03 GMT  
		Size: 206.3 MB (206305194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8f1c26b9523b138b29e45b3fe83265b77bf8af67603beede47e4bcbebdbc2390
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315090755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c45c47e9ab7e059dff56d0eff7c78a4290e206978860b5ad503a444d21a4177`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 08:55:47 GMT
ADD file:2015a98f802a1e28eca2c4eba0b574f58c2cd7844c0d94dbf0e29e8180aea210 in / 
# Thu, 17 Mar 2022 08:55:51 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 19:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:39:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 19:41:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 19:46:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d194d6caec7e92bc6e1448edd24c61790b7372a62bd6808d5cd0c5a6eda1736`  
		Last Modified: Thu, 17 Mar 2022 10:46:33 GMT  
		Size: 54.6 MB (54636832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6d8d6c495a88dc95c7cdb4d3ae2e01617fbe355ec506b682a16ac6bd71546a`  
		Last Modified: Thu, 17 Mar 2022 19:57:08 GMT  
		Size: 5.2 MB (5222583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91053236c731557db21c8cae8dadcde7f25967ff5d460c9f67f4789ecb8b3be7`  
		Last Modified: Thu, 17 Mar 2022 19:57:10 GMT  
		Size: 10.7 MB (10673017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c156ba31cbc1cdf259de80c19d95c4eaf735a0d8b5715a38c58be0755d068c4d`  
		Last Modified: Thu, 17 Mar 2022 19:57:58 GMT  
		Size: 56.0 MB (55951214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6147e27c9111eca3d9bb8674c30c819a81e06bae1c5d18bc779ac623f146bb1a`  
		Last Modified: Thu, 17 Mar 2022 20:00:06 GMT  
		Size: 188.6 MB (188607109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d9ba1b8cde069181d8569cba60eb2549ed5485e6510f0d5fe41501c46c312af7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 MB (345624007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f587dac2210ffbe656137c9dab26ad24804802bf26a06f686f42fbe35f18265`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:20:22 GMT
ADD file:52ac257bb3e9b43a436c32541c15e9c3a00323e3e1d0b20273b81a572fb8d66f in / 
# Thu, 17 Mar 2022 11:20:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 05:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 05:59:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 06:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 06:08:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d022277e505c1e9a57478a80b1b82e11b58551ebc0afcb5e723535b6ee105cc8`  
		Last Modified: Thu, 17 Mar 2022 11:30:38 GMT  
		Size: 60.4 MB (60406211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5191baf63a49f74aafee330281325a08a8d65451cc0ac632e8aa56129d9dca63`  
		Last Modified: Sat, 19 Mar 2022 06:45:43 GMT  
		Size: 5.5 MB (5543862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471dd71263fc10a8a1efc9a8fc7652bc8d0e227dafa1f6f9493a5a9779600d7a`  
		Last Modified: Sat, 19 Mar 2022 06:45:43 GMT  
		Size: 11.7 MB (11702261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b11bc794149909ceb1decbb8091901df40d21ad217894f0b435df98f07d5ec`  
		Last Modified: Sat, 19 Mar 2022 06:46:35 GMT  
		Size: 61.9 MB (61922448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ae284d96f0fad1536b463086fcf157b6739852e7262f87b4fa0c60d4a6415`  
		Last Modified: Sat, 19 Mar 2022 06:48:47 GMT  
		Size: 206.0 MB (206049225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8eba6bd76e364d31f470138d12d10a3c1604ee5a3cef225f1a3f478f5abfc74c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342740508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a6357ff1e99d258d501d195f32663948044cc626d7fe2fa1ec67b1a910baae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:14:08 GMT
ADD file:1dc8a81ea9c954e594eb32623a82cdfb528586b569a915ba8f70a49f68a6f7fd in / 
# Tue, 21 Dec 2021 02:14:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:02:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:10:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6b741955e06623f1924320507da1630323c4cf1d6489febc99917464e765860`  
		Last Modified: Tue, 21 Dec 2021 02:30:31 GMT  
		Size: 51.5 MB (51541457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91689f9aadadd96fe4e4ad4ed92ff1cb6a48034aedc9f41e14d54cf85bcdd039`  
		Last Modified: Tue, 21 Dec 2021 03:34:04 GMT  
		Size: 5.1 MB (5089016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a290be0dbc2a1d1f5f12db96d9dc0949f33b55d33712a23f37c71cb89606a3`  
		Last Modified: Tue, 21 Dec 2021 03:34:07 GMT  
		Size: 10.3 MB (10320854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44222df82131b4d925c2f594e50c018b1fb6d67154b22de79d99eb4cd4a356c9`  
		Last Modified: Tue, 21 Dec 2021 03:36:17 GMT  
		Size: 52.8 MB (52817006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71e08edf3534b3a52b84e74759377bd253863a9cf43fa9dde36a31debd1990a`  
		Last Modified: Tue, 21 Dec 2021 03:42:27 GMT  
		Size: 223.0 MB (222972175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d032eaf0f6770565c875255fc4e20e3400fa595724ba6fdb2245f5b9cbc50d62
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.1 MB (307058105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b595ff544d0290d392654fee44bf11f86b57e77578bdf8def010699f612de0a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 03:08:11 GMT
ADD file:4a7b0c9e8bc60d35d06240af5417427853918fe6624688050d4aca10a22b433f in / 
# Thu, 17 Mar 2022 03:08:14 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:23:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Mar 2022 18:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:24:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8e1d6cb1e553f745f248c4d7a409401acdb697f1bd597e8c1c08d6fcd5db0f2d`  
		Last Modified: Thu, 17 Mar 2022 03:13:59 GMT  
		Size: 54.2 MB (54246705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99267e3e8ccd599670f5059d59cf2f80cafc0773fc8b74ba953d5d5cb2189fed`  
		Last Modified: Thu, 17 Mar 2022 18:30:46 GMT  
		Size: 5.2 MB (5245707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3282440b854d7908290c041b1619604c86d6fb3ec5e2ed67356bbd4ef1847863`  
		Last Modified: Thu, 17 Mar 2022 18:30:47 GMT  
		Size: 10.8 MB (10819596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d19b2ec710aa05189651236530efc7d84062cf9d7d6fd4a3d22965342a45839`  
		Last Modified: Thu, 17 Mar 2022 18:31:01 GMT  
		Size: 56.6 MB (56562096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bec8b2539c0c5adea8d81224f6f73686970403543edd954440ee04cb16bc0f`  
		Last Modified: Thu, 17 Mar 2022 18:31:28 GMT  
		Size: 180.2 MB (180184001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
