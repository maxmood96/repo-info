## `haxe:latest`

```console
$ docker pull haxe@sha256:0ae96a5eeb615314f75ecba28c7435e1d881cb0aeba7e42fcdf2ae3390817a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1366; amd64
	-	windows version 10.0.17763.3770; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:c5bec2e3930987e4c108160d8cbb302cfbfb0bacbce7020f0f8ff92c61c98ebb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140008250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a36a96bd513dda418cb1c4bb9b0eea606721edecda17fbbb804870fbbe19bd`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 11:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 11:13:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 11:14:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 17:22:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 17:22:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 17:22:32 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 21 Dec 2022 17:23:57 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Wed, 21 Dec 2022 17:23:57 GMT
ENV HAXE_VERSION=4.2.5
# Wed, 21 Dec 2022 17:23:57 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Wed, 21 Dec 2022 17:26:48 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Wed, 21 Dec 2022 17:26:48 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa1d4c8d85a4e064e50cea74d4aa848dc5fc275aef223fcc1f21fbdb1b5dd182`  
		Last Modified: Wed, 21 Dec 2022 11:21:24 GMT  
		Size: 5.2 MB (5163298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c796299bbbddc7aeada9539a4e7874a75fa2b6ff421f8d5ad40f227b40ab4d86`  
		Last Modified: Wed, 21 Dec 2022 11:21:24 GMT  
		Size: 10.9 MB (10876681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81283a9569ad5e90773f038daedd0d565810ca5935eec8f53b8bcb6a199030d6`  
		Last Modified: Wed, 21 Dec 2022 11:21:43 GMT  
		Size: 54.6 MB (54584566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a202f488d0709eb4ece7df5159dca58ed57b9cadb0fa5d1307b4b3a7613c65d`  
		Last Modified: Wed, 21 Dec 2022 17:51:56 GMT  
		Size: 1.4 MB (1369662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0131dd7054818a6d4f1852c95ef97fb7037dca9835295cad77454062b5a797a`  
		Last Modified: Wed, 21 Dec 2022 17:51:56 GMT  
		Size: 1.4 MB (1447356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3572fac8d831eb99b7e59d0ed83101688e53dd8b9f8a3d8b7c74445632887af7`  
		Last Modified: Wed, 21 Dec 2022 17:51:58 GMT  
		Size: 11.5 MB (11541521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:3d7883d23659078e94cc41f8aae973df44544b40862848bfa1be1a0aec7f1719
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129482841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0172466125a4a744d595014fde600c8c2c4c8b97e3de3e216f3cb2521f63acc5`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:30 GMT
ADD file:72eaf12ec65c98e9cde1654b6adb2b3d19f7d81c13b12801c198f699252b7503 in / 
# Tue, 06 Dec 2022 00:58:31 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 09:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 09:49:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 09:49:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Dec 2022 00:16:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 00:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Dec 2022 00:16:55 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 07 Dec 2022 00:18:06 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Wed, 07 Dec 2022 00:18:06 GMT
ENV HAXE_VERSION=4.2.5
# Wed, 07 Dec 2022 00:18:06 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Wed, 07 Dec 2022 00:21:39 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Wed, 07 Dec 2022 00:21:39 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:58e27900c24f1f8f5b6b5eacbc073583f2372b58e9f5678dfe171b496b9cd71e`  
		Last Modified: Tue, 06 Dec 2022 01:05:33 GMT  
		Size: 50.2 MB (50207085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3975e0b03a66ba4371cf2cae58e77e148d952679dd5fa1e322124604805fc6a2`  
		Last Modified: Tue, 06 Dec 2022 09:59:29 GMT  
		Size: 4.9 MB (4932853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806632ddd1d79b55318482c725338dc97649f22ca0ec8dbdf79cc8be451201eb`  
		Last Modified: Tue, 06 Dec 2022 09:59:30 GMT  
		Size: 10.2 MB (10218527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27a60e772b69f3ec8f0fa174be2d19682bdea3265044f5d56ef14d491b7457d`  
		Last Modified: Tue, 06 Dec 2022 09:59:52 GMT  
		Size: 50.3 MB (50343382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6039e014a72d249659e36d265eae0200a7f37ac5b581dbd9811c6d11fcabffc3`  
		Last Modified: Wed, 07 Dec 2022 00:49:49 GMT  
		Size: 1.3 MB (1281987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44056a929e10ecbde167165663b44a1b6a58600a70379b0d91c603241b6b0c18`  
		Last Modified: Wed, 07 Dec 2022 00:49:49 GMT  
		Size: 1.4 MB (1389092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f3f6dedfc4064564c21e6efd8c4b6559c17a32aedda3af86ec09dd6fc6af15`  
		Last Modified: Wed, 07 Dec 2022 00:49:51 GMT  
		Size: 11.1 MB (11109915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:304e20fa6da3f10d1714d4c3d9184edaf197284f030722eeb989467643aa8112
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140370285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ccac3e75428b24b0ef492ac0d367eae5a6b01bdf310e1598d5dddcc31f1f1a`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:40 GMT
ADD file:5bbdc914ec8ed60ac85293e88ee1aafc3f0290762e320fc86dc9d79fa201834e in / 
# Wed, 21 Dec 2022 01:39:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:06:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:06:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 17:09:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 17:09:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 17:09:21 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 21 Dec 2022 17:10:31 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Wed, 21 Dec 2022 17:10:31 GMT
ENV HAXE_VERSION=4.2.5
# Wed, 21 Dec 2022 17:10:32 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Wed, 21 Dec 2022 17:12:43 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Wed, 21 Dec 2022 17:12:43 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c3e6129b48b69d14c5e7a5605e2b94003fb71aac82eac46b8689f5b8007af2c5`  
		Last Modified: Wed, 21 Dec 2022 01:42:49 GMT  
		Size: 53.7 MB (53681797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0470f9572d03767b054118fe19e60a9c7e2510168b3a0868d9ac2953d2def5`  
		Last Modified: Wed, 21 Dec 2022 02:12:40 GMT  
		Size: 5.1 MB (5149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99dfcef0545e5bca269c65c0208385c886321a1e0212977299827be5346dfea5`  
		Last Modified: Wed, 21 Dec 2022 02:12:40 GMT  
		Size: 10.9 MB (10873505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940d63caabf45c64562daab3c243c8724dd47bf45054d902ef3cb6206fc9c3f6`  
		Last Modified: Wed, 21 Dec 2022 02:12:57 GMT  
		Size: 54.7 MB (54682464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d513a0430cd37170324e7bee8ad13cdf1d5f2470fe09a2462481798f88f12c`  
		Last Modified: Wed, 21 Dec 2022 17:31:51 GMT  
		Size: 1.4 MB (1360036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20917c8b9351cc6ac9008c8bd295e8274b906b7388563a2712ef116f467d1662`  
		Last Modified: Wed, 21 Dec 2022 17:31:51 GMT  
		Size: 1.4 MB (1438144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86adb958f31a5a97113f3d9e29d47297a38111402f4f9b5a6e536f6f2b92c73c`  
		Last Modified: Wed, 21 Dec 2022 17:31:54 GMT  
		Size: 13.2 MB (13184569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.1366; amd64

```console
$ docker pull haxe@sha256:62f1234b3d6d5024401ab8e9c9340d61ff3a39d1662d80b5f9ea811ca6748202
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2529558867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500f4983b1a793db9920bcf728e53a93d6e18dc18cc58a534799d3a9af9a7a2a`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 09 Dec 2022 09:36:47 GMT
RUN Install update 10.0.20348.1366
# Wed, 14 Dec 2022 01:25:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 04:01:52 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 14 Dec 2022 04:01:53 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 14 Dec 2022 04:01:54 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 14 Dec 2022 04:01:55 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 14 Dec 2022 04:01:56 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 14 Dec 2022 04:02:39 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Dec 2022 04:04:09 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 04:04:40 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 14 Dec 2022 04:04:41 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 14 Dec 2022 04:05:25 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 04:05:26 GMT
ENV HAXE_VERSION=4.2.5
# Wed, 14 Dec 2022 04:10:11 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.2.5/haxe-4.2.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (9e7913999eb3693d540926219b45107b3dc249feb44204c0378fcdc6a74a9132) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '9e7913999eb3693d540926219b45107b3dc249feb44204c0378fcdc6a74a9132') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 04:11:07 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 14 Dec 2022 04:11:08 GMT
ENV HOMEDRIVE=C:
# Wed, 14 Dec 2022 04:11:35 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Dec 2022 04:12:08 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 14 Dec 2022 04:12:09 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bfa20ce142ecceb471dc070d9582fff942cef447b7c8ff22f2223ffe3737c99`  
		Last Modified: Tue, 13 Dec 2022 23:54:14 GMT  
		Size: 1.0 GB (1021665190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8089cb1a16f1eb694714863a5048821ebd084d4fc95740d2ca48fb1089820f`  
		Last Modified: Wed, 14 Dec 2022 02:12:39 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626d0ed0119dd4fd84fd5a8957f95e5de59e7487cef59f9392981d243dd55710`  
		Last Modified: Wed, 14 Dec 2022 05:59:36 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3c5d5224fdf12fd9d82bb8cb465fa9d25839bd37262f570cd5457632acf020`  
		Last Modified: Wed, 14 Dec 2022 05:59:36 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0cd9090c5f0ccbcf8e7875372ff4eb57527704f95101028fdc3147f3578007`  
		Last Modified: Wed, 14 Dec 2022 05:59:35 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f034e22409d41d012526d1c83d61556cfd58d38a527f37b7477774fb33918`  
		Last Modified: Wed, 14 Dec 2022 05:59:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc51666645b8c2144ed5ef119333f7077a74713285ac39fb853caab830c2e7aa`  
		Last Modified: Wed, 14 Dec 2022 05:59:34 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c093983d18e6b949c0f6660f5d928effb232293a915a412f1b0fb6443286171d`  
		Last Modified: Wed, 14 Dec 2022 05:59:33 GMT  
		Size: 574.3 KB (574337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00e68fd0c381e094bbbfaca04f7cd9a34150a0eed965201332a4491d60cb80a`  
		Last Modified: Wed, 14 Dec 2022 05:59:34 GMT  
		Size: 13.1 MB (13109488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff38e300057e1da62ab1038d33eaae0118656be371897b55c9769f326bddc3cc`  
		Last Modified: Wed, 14 Dec 2022 05:59:31 GMT  
		Size: 521.6 KB (521589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4cf1a48f829ff709fcb290d1e0d1bb4c36aac01958aad7f57f68795ee09672`  
		Last Modified: Wed, 14 Dec 2022 05:59:30 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c515e1a461841ead05bcc622d87dd3cfb0034828791ab073aed13f7ad9c94b`  
		Last Modified: Wed, 14 Dec 2022 05:59:32 GMT  
		Size: 2.4 MB (2359847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcc603134ce50dade3a3ec1ae0e2c25533ec5ee4177c8a3f5cdfafe1122f895`  
		Last Modified: Wed, 14 Dec 2022 05:59:30 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc2621f944c6b394010fce96ff8f2799c10680fad302a85c6c9bf3e3dbb8a71`  
		Last Modified: Wed, 14 Dec 2022 05:59:38 GMT  
		Size: 15.6 MB (15563743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3191734ca6f8f5cf6e02ff8e335b86dc66baab83936df5f16129c38dc11eac33`  
		Last Modified: Wed, 14 Dec 2022 05:59:29 GMT  
		Size: 585.6 KB (585584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b1c18eb6f2d3e09393b0dfd7ffbeae313edb26bbee6da43e331f8290309fab`  
		Last Modified: Wed, 14 Dec 2022 05:59:28 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c1c67f46ab4e406d4d58176e065714a1ba77603f5b31d1ab739d56f27e694`  
		Last Modified: Wed, 14 Dec 2022 05:59:28 GMT  
		Size: 576.9 KB (576888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd19bc16bac57e31519011055974bd36b2b02ef21893725c006b00dfccdfd68a`  
		Last Modified: Wed, 14 Dec 2022 05:59:28 GMT  
		Size: 590.5 KB (590461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0355f408accbd567c4e616834dcdab10f15c5a69bffd096c108419bf791dc652`  
		Last Modified: Wed, 14 Dec 2022 05:59:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.3770; amd64

```console
$ docker pull haxe@sha256:60cec712a85345d2f40bb945be7be52cd755856bb1c8caa336ecb1709b680585
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2811461787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60d3ca0083a6853401e7639b296d1ae4396fbef5363be1b47277021ebacdbb7`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Wed, 14 Dec 2022 01:29:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Dec 2022 04:12:29 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 14 Dec 2022 04:12:29 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 14 Dec 2022 04:12:30 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 14 Dec 2022 04:12:31 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 14 Dec 2022 04:12:32 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 14 Dec 2022 04:13:46 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Dec 2022 04:15:44 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 04:17:02 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 14 Dec 2022 04:17:03 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 14 Dec 2022 04:18:50 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 04:18:52 GMT
ENV HAXE_VERSION=4.2.5
# Wed, 14 Dec 2022 04:24:28 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.2.5/haxe-4.2.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (9e7913999eb3693d540926219b45107b3dc249feb44204c0378fcdc6a74a9132) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '9e7913999eb3693d540926219b45107b3dc249feb44204c0378fcdc6a74a9132') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 14 Dec 2022 04:26:07 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 14 Dec 2022 04:26:08 GMT
ENV HOMEDRIVE=C:
# Wed, 14 Dec 2022 04:27:32 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Dec 2022 04:29:12 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 14 Dec 2022 04:29:13 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1d7d21a6f8359d8228f44b50aa9ad552783452100b6ce203e8f042415b5623`  
		Last Modified: Wed, 14 Dec 2022 02:14:22 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72325d21dfea436dc31b3a1e1244eb7ba17b79554dca04c0f934aa9779e98d2`  
		Last Modified: Wed, 14 Dec 2022 05:59:55 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28382605d496dc2fc92090ec9e46287e95d6c4c0dec4de2bf311367be15c0090`  
		Last Modified: Wed, 14 Dec 2022 05:59:55 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7413752a30ca1584339dd214c9385701015bb0facd9aec74b2ce092e8325d7e9`  
		Last Modified: Wed, 14 Dec 2022 05:59:55 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e555a97983fbf0d988dfb7ee6d3ab0d89e1eed711bc34b9ae00f3ebec705b3`  
		Last Modified: Wed, 14 Dec 2022 05:59:53 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a49b39686798fbd2fe8cd93fbe86fb20c860d5b08ec44856bdb45856cef31ad`  
		Last Modified: Wed, 14 Dec 2022 05:59:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057a87d71f1e7cd2ac7d1650ad2e888b3f74ec0aab460f7fad816ec7f2647465`  
		Last Modified: Wed, 14 Dec 2022 05:59:53 GMT  
		Size: 345.1 KB (345103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68edd362585c99feda84655e591009851552f1482931b3209c20febdc7f0a7c`  
		Last Modified: Wed, 14 Dec 2022 05:59:54 GMT  
		Size: 12.9 MB (12924515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a948b958018fc4a947f192ddbb13ba6f10a6d651a349f1c941df4a684c4c1c3`  
		Last Modified: Wed, 14 Dec 2022 05:59:50 GMT  
		Size: 319.0 KB (319015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd7d8e3388a5a70e5e06da5cf320a3da97117ece61355917f40d9ad5ff62353`  
		Last Modified: Wed, 14 Dec 2022 05:59:50 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febd9dc055bd4e1e51aa5441c768c93a0a878eb111c1fa240ab545e69b4f7cdd`  
		Last Modified: Wed, 14 Dec 2022 05:59:51 GMT  
		Size: 2.2 MB (2150163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e4924786f554981ba36e9de48556881e00c009c85b22f84c90150b34db1325`  
		Last Modified: Wed, 14 Dec 2022 05:59:49 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f612a49b1a0b2ed9db95feb718875db6094c4657e60acab0aee34358a89fe69`  
		Last Modified: Wed, 14 Dec 2022 05:59:59 GMT  
		Size: 13.9 MB (13889173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019d270354df0e4125421a8a1a422be27317d228faef107881dbd4bc025f1237`  
		Last Modified: Wed, 14 Dec 2022 05:59:48 GMT  
		Size: 357.5 KB (357504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471151759da1284df1ad36676a7162f83fa9f506d2d0a95e0f1cd4298f5303ad`  
		Last Modified: Wed, 14 Dec 2022 05:59:47 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb1868848f5259b8137c9db298f60d0ee47faf88919e8d116e51b9f6f899e02`  
		Last Modified: Wed, 14 Dec 2022 05:59:48 GMT  
		Size: 370.0 KB (370024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137af6981479b4a5c45178666ffa1c48c7b73e9ded390815d2eee295c0a563a6`  
		Last Modified: Wed, 14 Dec 2022 05:59:48 GMT  
		Size: 394.9 KB (394937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600ea22b5d9629de29f70fd04b6ed85acfd5c94632fdcc867b98b0975bdbd5c`  
		Last Modified: Wed, 14 Dec 2022 05:59:47 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
