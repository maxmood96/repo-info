## `haxe:latest`

```console
$ docker pull haxe@sha256:dc3080504b7eb13c0cbda27f8cc287b49e68a79a32ba998ea4065899d9af452a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.2655; amd64
	-	windows version 10.0.17763.6189; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:d98d70dbfca7f83be974c3e4f1f8f094068b88429f62b656b32341e79337e4e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.0 MB (398989977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f6cc74c34381eda00cc70c0b00a61c58873e0435ac7b3308b3caaab5fb4880`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:09 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Tue, 13 Aug 2024 00:20:09 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:43:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:43:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 03:53:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 03:53:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 03:53:26 GMT
ENV NEKO_VERSION=2.4.0
# Tue, 13 Aug 2024 03:54:47 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 13 Aug 2024 03:54:47 GMT
ENV HAXE_VERSION=4.3.6
# Tue, 13 Aug 2024 03:54:47 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 13 Aug 2024 03:58:10 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 13 Aug 2024 03:58:12 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbbe86a28c2f6b3c3e0e8c6dcfba369e1ea656cf8daf69be789e0fe2105982b`  
		Last Modified: Tue, 13 Aug 2024 00:49:47 GMT  
		Size: 24.1 MB (24050697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed93aa58a52c9abc1ee472f1ac74b73d3adcccc2c30744498fd5f14f3f5d22c`  
		Last Modified: Tue, 13 Aug 2024 00:50:05 GMT  
		Size: 64.1 MB (64143347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9799d5da53d098092bd0661c8a25e7df6c9125d4952c2e345aa3c143b93d60be`  
		Last Modified: Tue, 13 Aug 2024 04:22:11 GMT  
		Size: 1.5 MB (1462943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b47768a4a12942ae9dcfc56ec58ae29892a6c766ad01b06a34ae5b57488c57`  
		Last Modified: Tue, 13 Aug 2024 04:22:11 GMT  
		Size: 1.4 MB (1391096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f16091d2490630d724d6323ee4a06b3c0878d3bb2658d3b5c4029213f539f`  
		Last Modified: Tue, 13 Aug 2024 04:22:47 GMT  
		Size: 258.4 MB (258387814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:471d7e275f74a42f9f5b7b8972ebb18edf3601475dc5754f4bba41b1647d438f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361714775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92668bf1af7dc64a0235df78c1f574549d5c5d1a6c49abc087aacbba7978776`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:26 GMT
ADD file:e3c71ceb3b7032e8a78ea70e306ec97b152570eeaae849a0c97bb61b2b12287f in / 
# Tue, 13 Aug 2024 00:57:26 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:24:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:24:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 03:55:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 03:55:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 03:55:31 GMT
ENV NEKO_VERSION=2.4.0
# Tue, 13 Aug 2024 03:57:24 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 13 Aug 2024 03:57:24 GMT
ENV HAXE_VERSION=4.3.6
# Tue, 13 Aug 2024 03:57:24 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 13 Aug 2024 04:01:10 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 13 Aug 2024 04:01:13 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:fe61db625a1b529903f1126ded0caa9e4e1c247503d524cd43bc15454b6bcc2f`  
		Last Modified: Tue, 13 Aug 2024 01:00:32 GMT  
		Size: 45.1 MB (45148160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06599d70e5763853acd56f8e4938729e068e7942382f335f96ce0ae3bc5a63a`  
		Last Modified: Tue, 13 Aug 2024 01:32:20 GMT  
		Size: 22.0 MB (21954622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3af44a3c0ce16617696528373b53738420f91f3383cda1666cc673cbf6fe50`  
		Last Modified: Tue, 13 Aug 2024 01:32:41 GMT  
		Size: 59.2 MB (59221928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556ad903f6b2e3563c1b2661913997cf5c221185dd2ca96cf8b66e48fe9491ad`  
		Last Modified: Tue, 13 Aug 2024 04:25:41 GMT  
		Size: 1.4 MB (1358680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2505d7e94a4075d3e646439245e798f6e3d1ea9879032d5f3c5f95f473f3c`  
		Last Modified: Tue, 13 Aug 2024 04:25:40 GMT  
		Size: 1.3 MB (1332641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68932d5217292ef88e2c5c666d8251d81076286d80dc4a13270472184770954c`  
		Last Modified: Tue, 13 Aug 2024 04:26:21 GMT  
		Size: 232.7 MB (232698744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:76741df48176fe03a44945c1b585670007488761bd042231b530464ca6b17fbf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401842514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7538d9074766ac5580fcd6388e396394fe5c6f8d2c22bde159583e178d3a6e18`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:42 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
# Tue, 13 Aug 2024 00:39:43 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:02:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:02:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 03:45:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 03:45:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 03:45:17 GMT
ENV NEKO_VERSION=2.4.0
# Tue, 13 Aug 2024 03:46:34 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 13 Aug 2024 03:46:34 GMT
ENV HAXE_VERSION=4.3.6
# Tue, 13 Aug 2024 03:46:35 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 13 Aug 2024 03:49:21 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 13 Aug 2024 03:49:26 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1593650c75729f64218ae272e8ffff9da7bbba9599bd1815877da99a2651fd9b`  
		Last Modified: Tue, 13 Aug 2024 01:09:17 GMT  
		Size: 23.6 MB (23592427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275677961327bd0cf394699228e29d7caf27f171c627899a20ebc9eeb550e209`  
		Last Modified: Tue, 13 Aug 2024 01:09:34 GMT  
		Size: 64.0 MB (63994880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddf2b211e20bf88cd99863b6e7efdc0cb2facc2fb11f7ccd05fa079d7e37862`  
		Last Modified: Tue, 13 Aug 2024 04:09:53 GMT  
		Size: 1.5 MB (1459394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c148d79fb8dc73f75d2fe2cf6f56e215df72b756e446c9aa0cd2add08b03c8b`  
		Last Modified: Tue, 13 Aug 2024 04:09:53 GMT  
		Size: 1.4 MB (1423068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf30066ddccef3f0df9ed0d6293c9e4c51549ab1608f5c63d85b12df84619f5a`  
		Last Modified: Tue, 13 Aug 2024 04:10:23 GMT  
		Size: 261.8 MB (261784153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.2655; amd64

```console
$ docker pull haxe@sha256:a14c2b32fc5d5c79930bd0c7b8a472e097028cb836e1983e715329a2e7e01ca3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170065273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c8996245560b06ba1d496a25156a30c245fe259e9064c80e0a9082fdf2f710c`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:59:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:59:27 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 13 Aug 2024 20:59:28 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 13 Aug 2024 20:59:29 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 13 Aug 2024 20:59:30 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 13 Aug 2024 20:59:31 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 13 Aug 2024 20:59:48 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Aug 2024 21:00:38 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 21:00:55 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 13 Aug 2024 21:00:55 GMT
ENV NEKO_VERSION=2.4.0
# Tue, 13 Aug 2024 21:01:29 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-0/neko-2.4.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 21:01:30 GMT
ENV HAXE_VERSION=4.3.6
# Tue, 13 Aug 2024 21:04:27 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.6/haxe-4.3.6-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 21:04:46 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 13 Aug 2024 21:04:47 GMT
ENV HOMEDRIVE=C:
# Tue, 13 Aug 2024 21:05:02 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Aug 2024 21:05:20 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 13 Aug 2024 21:05:20 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83535e7f20f1586259fc80964aa6b228b1984e716b1aba5ce0e6fd621a1ab585`  
		Last Modified: Tue, 13 Aug 2024 21:49:46 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296105f7eb597344e26cc05d655c705c5f636ead9853fb23de0e181ef4f1bd10`  
		Last Modified: Tue, 13 Aug 2024 21:49:46 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8093cc293e5f5dea908c62065316875a1ce62cf6f1ba203e0c7f00ede41ef7d9`  
		Last Modified: Tue, 13 Aug 2024 21:49:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2821cd2f21410cdaf8a16dc1000f0386eb4315681228babd641abd4ffde948`  
		Last Modified: Tue, 13 Aug 2024 21:49:45 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa006c11d35fef757d15d108beaf4605a49642b91cbec392099f94d2aa5da71`  
		Last Modified: Tue, 13 Aug 2024 21:49:44 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50abe448329c7857907865988bcbdbb226e984d815d712e7b1ac6b5c95de3f3d`  
		Last Modified: Tue, 13 Aug 2024 21:49:43 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7685c14c50a2e1de7a1713f7e42a188e150b06c5af318975fde2a482fd229a1`  
		Last Modified: Tue, 13 Aug 2024 21:49:43 GMT  
		Size: 312.0 KB (312032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aafd60ff49b73be4dc9dc56933e30d164c5cef79d611d607b79bb4a57c3cf1`  
		Last Modified: Tue, 13 Aug 2024 21:49:44 GMT  
		Size: 12.8 MB (12846301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e495703f22531be87a85ef314da932994ee9273398a4d7bab66a6b63cb69851`  
		Last Modified: Tue, 13 Aug 2024 21:49:41 GMT  
		Size: 293.0 KB (293031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84618b3da8b87e369185e6cc9cebf02422e4d8cee338fe042486d0679eceb61a`  
		Last Modified: Tue, 13 Aug 2024 21:49:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e946d087c13158bf010b46d5378fde95e261511332b47f90fd6dfbc4a3bf1f`  
		Last Modified: Tue, 13 Aug 2024 21:49:42 GMT  
		Size: 4.2 MB (4246907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb89e97e4b3ff3266a5ae58004a7f5c14e6641b15572cdae5d1a95b909d05436`  
		Last Modified: Tue, 13 Aug 2024 21:49:41 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85507fa518f5f0d18f25a6869f8d7985c9b3480fa68a3d74f460d3681efdf5b7`  
		Last Modified: Tue, 13 Aug 2024 21:49:44 GMT  
		Size: 9.6 MB (9588518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac4ac090e3d8c1d73ad5c654b02a0938e129d378159f4cf7afb10a88623441`  
		Last Modified: Tue, 13 Aug 2024 21:49:39 GMT  
		Size: 325.2 KB (325153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01250e16eb301dc652389431c843f93bc54cb9ab3484aff1f855abe57ae56ad5`  
		Last Modified: Tue, 13 Aug 2024 21:49:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de8538466874932336365ef79c002f59b56c561fec9029a074d5aa0183d61ae`  
		Last Modified: Tue, 13 Aug 2024 21:49:39 GMT  
		Size: 327.9 KB (327949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2f81a9d65a2394a44d1701343eedb6d4e1965187dec058d81684162c46a444`  
		Last Modified: Tue, 13 Aug 2024 21:49:39 GMT  
		Size: 346.5 KB (346512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b5f615d8aab77c16170af1b5467860498d050fbec7cb02c9278e9c9ae8f874`  
		Last Modified: Tue, 13 Aug 2024 21:49:39 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.6189; amd64

```console
$ docker pull haxe@sha256:41f4c5ad6966a8f6040a74aad875ff7af103fd9d23229c7b1b30fe3bfc9598d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2273615205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7977d10258bd7767b22c6f31d3b00846b70be49b89c5163ad7c2fd32432c829f`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:45:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 21:05:41 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 13 Aug 2024 21:05:42 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 13 Aug 2024 21:05:42 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 13 Aug 2024 21:05:43 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 13 Aug 2024 21:05:44 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 13 Aug 2024 21:06:38 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Aug 2024 21:08:07 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 21:09:01 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 13 Aug 2024 21:09:02 GMT
ENV NEKO_VERSION=2.4.0
# Tue, 13 Aug 2024 21:10:13 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-0/neko-2.4.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 21:10:14 GMT
ENV HAXE_VERSION=4.3.6
# Tue, 13 Aug 2024 21:13:59 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.6/haxe-4.3.6-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 21:14:58 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 13 Aug 2024 21:14:59 GMT
ENV HOMEDRIVE=C:
# Tue, 13 Aug 2024 21:15:52 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Aug 2024 21:16:47 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 13 Aug 2024 21:16:48 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47a01ddac643cbd49eec6aff688d037d7a551e855201124b4b91f640dc4af4b`  
		Last Modified: Tue, 13 Aug 2024 20:51:13 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810b5723ab1a241c634e7626bc7cc8cc7d841fc5828223301e1adf2421847c0d`  
		Last Modified: Tue, 13 Aug 2024 21:50:01 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e428d5fc95af19baca6bce1da31cbca6bb67656ff665effd996539c366e39723`  
		Last Modified: Tue, 13 Aug 2024 21:50:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f8e2f0c518a722697ee1cae7b719e7bae7986b7975775ece36c9dccfcad299`  
		Last Modified: Tue, 13 Aug 2024 21:50:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a1b6fcc8a0986c94058c1097847c9413c73f12d0f307005f39c1e7ddcb2ed6`  
		Last Modified: Tue, 13 Aug 2024 21:49:59 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113b34ff56f8c2ee6614d5ffe49c02324326d761f4878837b03a64fdd5bd73db`  
		Last Modified: Tue, 13 Aug 2024 21:49:59 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dab6428936506dff363473a21cd6ccea21ca0dd801d83b938d003c04f7927c8`  
		Last Modified: Tue, 13 Aug 2024 21:49:58 GMT  
		Size: 451.8 KB (451753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ef97b6c677648bf3b1fbcd57ef82e49c5e30d2f2ab8d7daafb6a38935afce5`  
		Last Modified: Tue, 13 Aug 2024 21:49:59 GMT  
		Size: 12.9 MB (12889809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70aec204904a891db50fe1b2691f654cdc3a472d64eb70c3cc9385af6a2e65c9`  
		Last Modified: Tue, 13 Aug 2024 21:49:57 GMT  
		Size: 297.5 KB (297503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b2dd77b027b4200c7dac8e5740f59cfc5fa1c06d07b62d1250755a2bf68116`  
		Last Modified: Tue, 13 Aug 2024 21:49:56 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e685122f5d4b99afa3e52f28141a618a47b559bc2678c08b1c7d22911b71c745`  
		Last Modified: Tue, 13 Aug 2024 21:49:57 GMT  
		Size: 4.3 MB (4258224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468a0c4f0774f6c3d898abba26f4d1438d024ee8f54c027c693fa259719dfdbc`  
		Last Modified: Tue, 13 Aug 2024 21:49:56 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a90ad121c1ea8dbf698cd442e7f42f00651e77a7530bbb9bfb65a4228fddeaa`  
		Last Modified: Tue, 13 Aug 2024 21:49:59 GMT  
		Size: 9.5 MB (9497984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d996a64ac2885e39c362412267fb7bd97db323361b140684c5a14e3cffa55849`  
		Last Modified: Tue, 13 Aug 2024 21:49:54 GMT  
		Size: 328.3 KB (328298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00adec008320728f462fe5481f0e9de90ab0a2fe0476c32eb74600f8d5328f7a`  
		Last Modified: Tue, 13 Aug 2024 21:49:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8d696fa3b3661a85d9986bd0c1b888f5b5466db01f69562da352c54b7a9d53`  
		Last Modified: Tue, 13 Aug 2024 21:49:54 GMT  
		Size: 332.6 KB (332624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539244a0d25352528ea7d7c97d98beb4867f57c1e0da1ab309c513c0b1f22c3c`  
		Last Modified: Tue, 13 Aug 2024 21:49:54 GMT  
		Size: 341.8 KB (341790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3eca47b11b52a8a7522d2dc38e76ccef2296600a72d570c763e2395c3c79961`  
		Last Modified: Tue, 13 Aug 2024 21:49:54 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
