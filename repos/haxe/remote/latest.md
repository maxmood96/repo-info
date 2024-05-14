## `haxe:latest`

```console
$ docker pull haxe@sha256:f67616d6ca2726fbd3b4cbfce48c3b48d2f7530694250b67c766e8d5abfca983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:6404bd1d0a9e9f0d2f306848f0d8df47afabbc920766693e4e2451469e541980
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140093813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4edcde0cce7758c3f7de6d3a1c3281c69b41f1a561de7f2f2b54008a7ef9b968`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:56:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 13:56:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:56:46 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 24 Apr 2024 13:58:07 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Wed, 24 Apr 2024 13:58:07 GMT
ENV HAXE_VERSION=4.3.4
# Wed, 24 Apr 2024 13:58:07 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Wed, 24 Apr 2024 14:01:33 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.4 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Wed, 24 Apr 2024 14:01:33 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbeb8ef1d906919c518d52a9eb71cedf1ee5c3247b6ea106571a6252d5a4f05`  
		Last Modified: Wed, 24 Apr 2024 04:22:13 GMT  
		Size: 54.6 MB (54589380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ab97afca50361dc691e9c55bf54b20125909c8f93983606c2d91fc1043d72e`  
		Last Modified: Wed, 24 Apr 2024 14:38:59 GMT  
		Size: 1.4 MB (1370572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4ea3c36f74a38b281ca314fe88505e013de988ce3833da0365370aff606415`  
		Last Modified: Wed, 24 Apr 2024 14:38:59 GMT  
		Size: 1.4 MB (1449214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b5ed3347a24f70943ff76a2bd2e07c6ce943b10aead392771caf5139700b30`  
		Last Modified: Wed, 24 Apr 2024 14:39:01 GMT  
		Size: 11.8 MB (11820498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:57cc61c934674af849618f3380e17042ce615b9a82476b89e1b2d65bdb2eb1b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129548496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45900966ad71f0bac6931a14743eb929882e34db7c34609742f88bdd52d4862d`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 14 May 2024 01:08:54 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Tue, 14 May 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:37:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 10:29:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 10:29:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 10:29:06 GMT
ENV NEKO_VERSION=2.3.0
# Tue, 14 May 2024 10:30:26 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 14 May 2024 10:30:26 GMT
ENV HAXE_VERSION=4.3.4
# Tue, 14 May 2024 10:30:26 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 14 May 2024 10:33:50 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.4 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 14 May 2024 10:33:50 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d6f4b9983a8ee98e2432d49e727c6278cadb8efecf5ab79268999b8d08c984`  
		Last Modified: Tue, 14 May 2024 01:48:20 GMT  
		Size: 50.4 MB (50359447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7bb1619074bd74e67b8c22aa7f19adcf8cf5a68b2c677b5f867d775bf1b8eb`  
		Last Modified: Tue, 14 May 2024 11:08:31 GMT  
		Size: 1.3 MB (1283372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d41cb4611ce1977309ac9c91affc7842328968073c4348aac8ebfe088fa073`  
		Last Modified: Tue, 14 May 2024 11:08:31 GMT  
		Size: 1.4 MB (1389868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e2f1a87c470c46d69fa2ad366fc83a924c2fcb09c63d142a1916b0c8a6d5e6`  
		Last Modified: Tue, 14 May 2024 11:08:35 GMT  
		Size: 11.4 MB (11379069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:d12d14537d87544670c28b967bf4061810f629f68309a09505f22e695cc22680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140473839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8564a9855f9ef3d80f1b6e916165b42514babf394a0392eaa49320a8083c30a2`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:45:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 13:13:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 13:13:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 13:13:06 GMT
ENV NEKO_VERSION=2.3.0
# Tue, 14 May 2024 13:14:17 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 14 May 2024 13:14:18 GMT
ENV HAXE_VERSION=4.3.4
# Tue, 14 May 2024 13:14:18 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 14 May 2024 13:17:08 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.4 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 14 May 2024 13:17:08 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dce352085291a4828eefe3a8fe5557c610cb7e308cbe4a56a62e0922171dc1c`  
		Last Modified: Tue, 14 May 2024 01:54:08 GMT  
		Size: 54.7 MB (54696093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e42f7b0e1b9f6bf3a20256c53d6f09ad3b7165b63a782d4644cf112075d133`  
		Last Modified: Tue, 14 May 2024 13:46:51 GMT  
		Size: 1.4 MB (1360851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83664f52aa631ff2780f8b01731fdd57ef725a153b8d6e9d2f64bac657537227`  
		Last Modified: Tue, 14 May 2024 13:46:51 GMT  
		Size: 1.4 MB (1440889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96e07aa00c376243d1157d9bea39ada8ee8dd7e8cbf5dd6f1f25ebfadceb9f2`  
		Last Modified: Tue, 14 May 2024 13:46:52 GMT  
		Size: 13.5 MB (13486491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.2402; amd64

```console
$ docker pull haxe@sha256:7eb4c15de63ce3501bc906d2bf824d38a4a53109ffb84196b9f8f1ef0bf0c05f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2031885892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0721b771f9db89c83fe0cb34940e7b60287ec4413299d4f0f79a45da9ffad1`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Wed, 10 Apr 2024 02:03:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 02:03:38 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 10 Apr 2024 02:03:39 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 10 Apr 2024 02:03:40 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 10 Apr 2024 02:03:41 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 10 Apr 2024 02:03:42 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 10 Apr 2024 02:04:08 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 02:05:25 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 02:05:49 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 10 Apr 2024 02:05:50 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 10 Apr 2024 02:06:29 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 02:06:30 GMT
ENV HAXE_VERSION=4.3.4
# Wed, 10 Apr 2024 02:10:58 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.4/haxe-4.3.4-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 02:11:25 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 10 Apr 2024 02:11:26 GMT
ENV HOMEDRIVE=C:
# Wed, 10 Apr 2024 02:11:49 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 02:12:16 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 10 Apr 2024 02:12:17 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e826fbec98f8151ff6cb8112b76d661597b5331209e967d7087ff713d7f80646`  
		Last Modified: Wed, 10 Apr 2024 03:15:51 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939622637cd2e719e1e7d480e63d2901b29ec592b0b7171ce657b3909875c8c5`  
		Last Modified: Wed, 10 Apr 2024 03:15:50 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a6d71fdc4638e0401290386a7512ab05a5d4f572f2ad05e8bf8ff185c719fa`  
		Last Modified: Wed, 10 Apr 2024 03:15:50 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba23e5aa8b51fc59ee2b02ed1daca24f418c7c2dc278ac8fa06fa8ec5a10b844`  
		Last Modified: Wed, 10 Apr 2024 03:15:50 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56e73a14733d75253eb3dfb83bd21e8d30e8382d37dc37c52ecc49fddf5e8989`  
		Last Modified: Wed, 10 Apr 2024 03:15:48 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d581c3a35c43a3620a14098d012e0b9426d79b9d86347bbc1b94d7abcebdcdbd`  
		Last Modified: Wed, 10 Apr 2024 03:15:48 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e680fc32d4726b9dca29ddef4e90df442967b380499fd7531ce9373a448f0f4f`  
		Last Modified: Wed, 10 Apr 2024 03:15:47 GMT  
		Size: 458.6 KB (458635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f66162f3542f92ebcf1cc4b687884bbcffeb403888ae2786255ab3ce2a7e60`  
		Last Modified: Wed, 10 Apr 2024 03:15:49 GMT  
		Size: 12.9 MB (12873485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcd753183cf7bac4eb12ce724f00d9a31d4034062164c438f2f15331226e8d3`  
		Last Modified: Wed, 10 Apr 2024 03:15:46 GMT  
		Size: 305.4 KB (305357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb97a6f5c64ba3768b2ca89da70015afc97fe2d44ebf649b2f52f69edb8fa72`  
		Last Modified: Wed, 10 Apr 2024 03:15:45 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669965b801fd0ff5807e7e65902d1c27a4be930d5372c428de8242cac20c504e`  
		Last Modified: Wed, 10 Apr 2024 03:15:45 GMT  
		Size: 2.1 MB (2134189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f299996466030909c195cc199438e4ed06444e57231263c45a8c728213b9a9da`  
		Last Modified: Wed, 10 Apr 2024 03:15:45 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8bfa732b0b9c09b5769a210f9fc1805e911d147e7a82430bb01c48fef59413`  
		Last Modified: Wed, 10 Apr 2024 03:15:50 GMT  
		Size: 15.7 MB (15675299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8dbf7a174509f67d3205652cdb29ab0508b8c264b1b448587e268b53ebaead`  
		Last Modified: Wed, 10 Apr 2024 03:15:43 GMT  
		Size: 337.7 KB (337676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171cf5d6c3ae9fbbc297c59d89fe1b89b583afb522667ac68aeb514520871d75`  
		Last Modified: Wed, 10 Apr 2024 03:15:42 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6f916c15ad6fcd6c21b62fa2fc4f2bf7f78372350f1281055e580e8f8eb8b2`  
		Last Modified: Wed, 10 Apr 2024 03:15:43 GMT  
		Size: 349.3 KB (349316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b393890e7947b8f9107cbc2a8f9d3d6ae21ac5289f5a7d9053ca2c2d40540e`  
		Last Modified: Wed, 10 Apr 2024 03:15:43 GMT  
		Size: 364.1 KB (364142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a7814da5636a15a867951674177f684e82fc9d73e043e91a80d014c6b59587`  
		Last Modified: Wed, 10 Apr 2024 03:15:42 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.5696; amd64

```console
$ docker pull haxe@sha256:e8f9ffeb55191e55e1a0aecb1b7d80189fc7f484310a9777e3b785e552230c91
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190481381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39582b413d79b12712b15ae0db57777b8b2c77996e64820c68fe4ab1f77792f3`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Wed, 10 Apr 2024 01:40:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Apr 2024 02:12:28 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 10 Apr 2024 02:12:29 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 10 Apr 2024 02:12:30 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 10 Apr 2024 02:12:31 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 10 Apr 2024 02:12:31 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 10 Apr 2024 02:13:59 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 02:16:10 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 02:17:41 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 10 Apr 2024 02:17:42 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 10 Apr 2024 02:19:28 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 02:19:29 GMT
ENV HAXE_VERSION=4.3.4
# Wed, 10 Apr 2024 02:24:46 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.4/haxe-4.3.4-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 02:26:18 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 10 Apr 2024 02:26:19 GMT
ENV HOMEDRIVE=C:
# Wed, 10 Apr 2024 02:27:42 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 02:29:11 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 10 Apr 2024 02:29:12 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6ae8ddefe4f7d0224959df0cc91d01044dce7f127ee7c23257cf0b63bfd7ac`  
		Last Modified: Wed, 10 Apr 2024 01:48:05 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b4ff00e8c73a8c44237e830a58cbd69b4013572371002532bdf9b17ec62d4c`  
		Last Modified: Wed, 10 Apr 2024 03:16:07 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbac1c646b5c1e2c3e571c7c478a9c1639193187afe4529551a7520e7dc6fa1`  
		Last Modified: Wed, 10 Apr 2024 03:16:07 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efc27386ff0301a25c496c97f91df9f9ec3acedad60db52cdc0c050b15c43c2`  
		Last Modified: Wed, 10 Apr 2024 03:16:07 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e53a6820b710febcf4764504c8900345bc047f2ec22243e627b3551f52e7350`  
		Last Modified: Wed, 10 Apr 2024 03:16:05 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39836a1a9eb8dc4cfb68a4b875ed12fb3a56a80481dbe7b6482abf0db5dee83`  
		Last Modified: Wed, 10 Apr 2024 03:16:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0964433ad48961f58cb3e94c5f50e66d1841b464c1d32a55acf4342275a96cc7`  
		Last Modified: Wed, 10 Apr 2024 03:16:05 GMT  
		Size: 404.8 KB (404837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f6f0e68bb38a2fc6e7aa2a5b7a594efea89e8cb83c95ea22baedc322f4d3d2`  
		Last Modified: Wed, 10 Apr 2024 03:16:06 GMT  
		Size: 12.9 MB (12887714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227b1825fabaffbcf889350a00a6bf83e919416e88d0f7650d5212971d3ba031`  
		Last Modified: Wed, 10 Apr 2024 03:16:03 GMT  
		Size: 271.1 KB (271075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcdf711b1e9aeaeb10fa081f4b2453760d691a52c7c7a6553832fbca439dbcd8`  
		Last Modified: Wed, 10 Apr 2024 03:16:03 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ea27a19fd72224bdcd1ce681e0d5162278c12c74a8f3fe9ed4ae2375611b18`  
		Last Modified: Wed, 10 Apr 2024 03:16:03 GMT  
		Size: 2.1 MB (2096972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613472b52267db9b07ce8fa3841c4308d684984d723c5342b53d886c715f6e80`  
		Last Modified: Wed, 10 Apr 2024 03:16:02 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd1f38beacdbbd846af4a5a12b26d04253660d41fecfc87b417d5ad0e04f68a`  
		Last Modified: Wed, 10 Apr 2024 03:16:06 GMT  
		Size: 9.5 MB (9477264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde0b3590fe7f2cd8f3ef890f423d4f8708062307dea93e55f9c07b445583ae1`  
		Last Modified: Wed, 10 Apr 2024 03:16:00 GMT  
		Size: 294.8 KB (294759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e674b67458aa98909888b290d07e2ed434ee25d5cbd6d1091d6df2f4cf3534`  
		Last Modified: Wed, 10 Apr 2024 03:16:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f7eff655869828f1f517164736331b3474743e7806534164ab2dcc98c2c170`  
		Last Modified: Wed, 10 Apr 2024 03:16:00 GMT  
		Size: 297.7 KB (297660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f08524f30fe8aead7996a97c31be61642eee141c8f389e2b237601039878a4b`  
		Last Modified: Wed, 10 Apr 2024 03:16:01 GMT  
		Size: 309.2 KB (309220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7fd570eddb347af2b42dda6332e8c2def297733721c766977ae21c063aadd1`  
		Last Modified: Wed, 10 Apr 2024 03:16:00 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
