## `haxe:latest`

```console
$ docker pull haxe@sha256:9e0a3fa1fe8a43984d0d0855c8ad4561fc8291e392ee35523c9bef840c6638c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:7b619801d8eca3274aae280e2734f1eb2a5163f94cdf0a28ed3e9468ce5a37b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140094044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a84282fc94b718946a6ffa3a52d05a767da9da2297a98c96f8ee7ce71fad25`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 16:44:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 16:44:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 16:44:40 GMT
ENV NEKO_VERSION=2.3.0
# Tue, 14 May 2024 16:46:02 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 14 May 2024 16:46:02 GMT
ENV HAXE_VERSION=4.3.4
# Tue, 14 May 2024 16:46:02 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 14 May 2024 16:49:30 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.4 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 14 May 2024 16:49:31 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f058aeb2babd189179ccc3d4b7ba9fc5b4bd957bf2ad23993df3bc969e0adc37`  
		Last Modified: Tue, 14 May 2024 17:26:43 GMT  
		Size: 1.4 MB (1370505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48df75d4ec7909707cb04e8fabb1eaab813155efe71cc11ca6b01af2df82fb7e`  
		Last Modified: Tue, 14 May 2024 17:26:43 GMT  
		Size: 1.4 MB (1449198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1a9fc507b0e42da0e5c9d49a5de4407880a55b71e738fbd187c26ee361d7f1`  
		Last Modified: Tue, 14 May 2024 17:26:45 GMT  
		Size: 11.8 MB (11820470 bytes)  
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

### `haxe:latest` - windows version 10.0.20348.2527; amd64

```console
$ docker pull haxe@sha256:68af601bd0317d727cb5172c486f519f44f4678bee0c23b7ecca8a12b57c94fb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2144333905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28a202155f9c431036c8dd987e527925d1add9c08099cdb3c555dfaa5ebc5b5`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 19:22:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 19:22:02 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 12 Jun 2024 19:22:03 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 12 Jun 2024 19:22:04 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 12 Jun 2024 19:22:04 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 12 Jun 2024 19:22:05 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 12 Jun 2024 19:22:28 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 19:23:40 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 19:24:01 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 12 Jun 2024 19:24:01 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 12 Jun 2024 19:24:38 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 19:24:39 GMT
ENV HAXE_VERSION=4.3.4
# Wed, 12 Jun 2024 19:29:05 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.4/haxe-4.3.4-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 19:29:27 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 12 Jun 2024 19:29:28 GMT
ENV HOMEDRIVE=C:
# Wed, 12 Jun 2024 19:29:47 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 19:30:09 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 12 Jun 2024 19:30:09 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f28ba04fd7442194d203e3299df3218b1caad70e628b708991af87a4c486ae`  
		Last Modified: Wed, 12 Jun 2024 20:28:40 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451d6e2ae9426ad0e7ddb6526099e44a6d912e60cd8c435f43d04332ac7d3af6`  
		Last Modified: Wed, 12 Jun 2024 20:28:39 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9503236800fcbae73610119034f2df4622f698c76ee4e4ed907cdc650e9a9d1a`  
		Last Modified: Wed, 12 Jun 2024 20:28:39 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e94153af7330bf387a5ab50ba43deeee032e1a3420dcdd9b690b4adcc77f00e`  
		Last Modified: Wed, 12 Jun 2024 20:28:39 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bae57f7697dab2e5c024ea3f17ff0a98e1e5260c9eb3b806b9d11a009ba01a4`  
		Last Modified: Wed, 12 Jun 2024 20:28:37 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a2d3124c623d617726095e54d7a00c1ac95d2745504505b7208493fc374ab7`  
		Last Modified: Wed, 12 Jun 2024 20:28:37 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8378eae58b3f0b44d186006e1398df01f169cde40413aeb2375f31be1532aa36`  
		Last Modified: Wed, 12 Jun 2024 20:28:36 GMT  
		Size: 309.8 KB (309751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd142a5ce00139c695689273f3ad3ee5e8eb6298eba41a372f8783dc8d411f53`  
		Last Modified: Wed, 12 Jun 2024 20:28:38 GMT  
		Size: 12.8 MB (12845781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9652d83a9a86bf7845cb1efff9b0c4d2a2652eb984de313aefa6ebcb2180ca8`  
		Last Modified: Wed, 12 Jun 2024 20:28:34 GMT  
		Size: 289.3 KB (289309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dca7a5ac16d69d14673000d73ef247ad6ee71c0fdd8cc501bacb29a1f4d3a7`  
		Last Modified: Wed, 12 Jun 2024 20:28:34 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283522aea29c7e179727173da6b2e72d9f9064a5cc3994baa9adb4c25f395c60`  
		Last Modified: Wed, 12 Jun 2024 20:28:35 GMT  
		Size: 2.1 MB (2121230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d6a429f48f831e25ee1e7910c5439b752195e0e56b5cc563e36fe34c87adaf`  
		Last Modified: Wed, 12 Jun 2024 20:28:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1539413ba66302f15429e0c429786d0a238a3e7281b0250701fcb8ab341d9c8d`  
		Last Modified: Wed, 12 Jun 2024 20:28:38 GMT  
		Size: 9.6 MB (9573116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e847b5cd6fcff01259bcd3b12f6a293017862f28209156bca49ac7d52acc9c`  
		Last Modified: Wed, 12 Jun 2024 20:28:32 GMT  
		Size: 324.4 KB (324392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ec2b20b524294027d4e16f6dee07704b44c4b784bd4b18459295c2b1ea5ba1`  
		Last Modified: Wed, 12 Jun 2024 20:28:32 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78bd0758020cd5bfc5ba7e8b1a4f7e662ea23b819217296610e8ef549ca7759`  
		Last Modified: Wed, 12 Jun 2024 20:28:32 GMT  
		Size: 332.4 KB (332414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cd3d6199c5fbe8bec6979a15813ba2308584a8af8db433dcb0dbb552154ac7`  
		Last Modified: Wed, 12 Jun 2024 20:28:32 GMT  
		Size: 345.2 KB (345152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b7e445a71db1b76dd81c854765e737ce83048ff119507ca3478e3d5b1982e6`  
		Last Modified: Wed, 12 Jun 2024 20:28:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.5936; amd64

```console
$ docker pull haxe@sha256:a226212db85a97a9b12c39359873f4caeea885b989f7a9d7100566c004ca65c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251441250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51160b15ee9f3a95d07fb74280c2bd1396bfb420a8c9b7a20ef26466f6f0dcec`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:59:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 19:30:23 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 12 Jun 2024 19:30:24 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 12 Jun 2024 19:30:24 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 12 Jun 2024 19:30:25 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 12 Jun 2024 19:30:26 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 12 Jun 2024 19:31:32 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 19:33:24 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 19:34:29 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 12 Jun 2024 19:34:30 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 12 Jun 2024 19:35:58 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 19:35:59 GMT
ENV HAXE_VERSION=4.3.4
# Wed, 12 Jun 2024 19:41:17 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.4/haxe-4.3.4-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 19:42:32 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 12 Jun 2024 19:42:33 GMT
ENV HOMEDRIVE=C:
# Wed, 12 Jun 2024 19:43:49 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 19:45:03 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 12 Jun 2024 19:45:04 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6e3a886b0409dde5276640ebcea6a4dac570684e6e28fbc210293a21af0dd`  
		Last Modified: Wed, 12 Jun 2024 19:06:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d20312f2a17d731ea811cfd435f855e562e93b982af6c04069c354785ea9f62`  
		Last Modified: Wed, 12 Jun 2024 20:28:56 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8bde9fa7ed2643fbcd6226d226c5bd18385fc9b747c9d37574b912bd4f1f30`  
		Last Modified: Wed, 12 Jun 2024 20:28:55 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d791639a898c13f2ada132963d9a703d703b977b9259a8d828ae590900868907`  
		Last Modified: Wed, 12 Jun 2024 20:28:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b576b0e4f2a8b37070dadf45fa9a1c6337bb5b5dde974190112a4a69ecf5750`  
		Last Modified: Wed, 12 Jun 2024 20:28:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6378c374db47e8573cf66fd1b6a4b0bc73a53c4d169b3c66f57cf6b41962d6`  
		Last Modified: Wed, 12 Jun 2024 20:28:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3871ae401054b59a8af76a9f43ff67433ffb2493ac68a805c1c80ee53dfbb69`  
		Last Modified: Wed, 12 Jun 2024 20:28:53 GMT  
		Size: 436.1 KB (436122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ee8cfef4de14885bf8877db7dfbf028526c7965f1703f8f768466b8bc06e78`  
		Last Modified: Wed, 12 Jun 2024 20:28:55 GMT  
		Size: 12.9 MB (12872012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bcf300b51dcc5ca658f8a43a690a462b54e485ff599e0f5aa6c7e59cc22d4f`  
		Last Modified: Wed, 12 Jun 2024 20:28:52 GMT  
		Size: 282.0 KB (282004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b584e56470921a6c2c179bbb125719c3ef5794aaa1b834e7bb9b960f944dd7`  
		Last Modified: Wed, 12 Jun 2024 20:28:51 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56777edfc783c3cf2716ad449be312b09b969b802051dd17cf3aabee69b98cce`  
		Last Modified: Wed, 12 Jun 2024 20:28:52 GMT  
		Size: 2.1 MB (2119120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7898d2847aeb70165676fa76bd50617ea77c0a42702e87fbbdd0ced16cd48aa5`  
		Last Modified: Wed, 12 Jun 2024 20:28:51 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0f6e4877d06b7bfd95c0d1e4a123778d7249f4d1ca32449974764e7e208855`  
		Last Modified: Wed, 12 Jun 2024 20:28:55 GMT  
		Size: 14.0 MB (14043319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d9804aeefee9e73f5e44bb3d660efa653f4963db1fe5e5a7f72293a283e3dd`  
		Last Modified: Wed, 12 Jun 2024 20:28:49 GMT  
		Size: 324.8 KB (324843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fcea46f4a5f37b90dbcefed412c009ac7a80cf48e049b01ab341242c66f7a0`  
		Last Modified: Wed, 12 Jun 2024 20:28:49 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e304e775d7098ebaf214a6a9d20d295c5b560feda65c1103a50c796a929abf4d`  
		Last Modified: Wed, 12 Jun 2024 20:28:49 GMT  
		Size: 330.3 KB (330321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d171df65c41190bb9433d8c26b0076ea46091167c849db26a97f513340be5f`  
		Last Modified: Wed, 12 Jun 2024 20:28:49 GMT  
		Size: 338.7 KB (338726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b46c45bdbeca8a1ca21066941c98be2558d7e364a3ea3ebce669ec6a34342f8`  
		Last Modified: Wed, 12 Jun 2024 20:28:49 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
