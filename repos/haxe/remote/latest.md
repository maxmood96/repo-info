## `haxe:latest`

```console
$ docker pull haxe@sha256:be52737176382c66d4b7d5f6bc677c97232ce7ef0f22f794aa03fca1be2b8ef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:f3fd0eab6184eed9e9cce468b7a48c2b4b505df07897ca09a6132ea59431c0ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140073834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8860d1ea81792de0058958599e9c3d475fa88a647a944275e2f77fd1a6ab309a`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:22:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 11:40:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 23:20:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 23:20:16 GMT
ENV NEKO_VERSION=2.3.0
# Tue, 05 Mar 2024 23:21:49 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 05 Mar 2024 23:21:49 GMT
ENV HAXE_VERSION=4.3.4
# Tue, 05 Mar 2024 23:21:49 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 05 Mar 2024 23:25:46 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.4 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 05 Mar 2024 23:25:46 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bbf2983642e080d705d575c1da8d4d8c35507576d88e44979b5c6229573d40`  
		Last Modified: Tue, 13 Feb 2024 01:31:47 GMT  
		Size: 15.8 MB (15763532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c7d862cba465d342dbf73dca7caf5e04c2ec7b374c918ec26f305e2ba3f78f`  
		Last Modified: Tue, 13 Feb 2024 01:32:03 GMT  
		Size: 54.6 MB (54588461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8968b948b8089b14368b1f06390f07beed12cb87d4af18902d27332ddbe1fa`  
		Last Modified: Wed, 06 Mar 2024 01:01:22 GMT  
		Size: 1.4 MB (1369701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46aea0cdc0d4fea1c9a309c09c9f2921c989e06b93c653ca08b074ea0db98cb4`  
		Last Modified: Wed, 06 Mar 2024 01:01:22 GMT  
		Size: 1.4 MB (1447437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c5f6c2f02ea3f557603f686f9d51b9a4c34bac9c4bd6c3eeb9112e7a7efc36`  
		Last Modified: Wed, 06 Mar 2024 01:01:24 GMT  
		Size: 11.8 MB (11819865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:7e50b035efdb191d01a1a6eff4a9da2bdb14158cc8108f57dcb3f82c5225ebc0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129527000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479b40a6f51e511edbfc42a1cd9fba3e1f02eec7b6734aa8def0bc02f2189b77`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 13 Feb 2024 01:20:21 GMT
ADD file:a6e150be02b0758f7cb3863651ae586c1592e19949e91c78e3771ceaad602a2a in / 
# Tue, 13 Feb 2024 01:20:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:16:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 15:37:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Mar 2024 23:17:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 05 Mar 2024 23:17:55 GMT
ENV NEKO_VERSION=2.3.0
# Tue, 05 Mar 2024 23:19:27 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 05 Mar 2024 23:19:27 GMT
ENV HAXE_VERSION=4.3.4
# Tue, 05 Mar 2024 23:19:28 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 05 Mar 2024 23:22:48 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.4 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 05 Mar 2024 23:22:49 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:623a3ffac68434a8d471ef584bdb1dcbfafd4648778c484c1566ff7910d04b0e`  
		Last Modified: Tue, 13 Feb 2024 01:27:15 GMT  
		Size: 50.2 MB (50241706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c12ee536bcdc51ad528b0ed79abe7893d5c4c356dd3b5d3321eb8eda18294ca`  
		Last Modified: Tue, 13 Feb 2024 04:28:21 GMT  
		Size: 14.9 MB (14879180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eebe7ea1391c25ae1a4d9bd9382746170a0edc00c1085152e15d7ade4b3fa456`  
		Last Modified: Tue, 13 Feb 2024 04:28:43 GMT  
		Size: 50.4 MB (50357734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8672aeb1080353103282ba88808bad38fea56a381779d710f586c80398aef8e7`  
		Last Modified: Wed, 06 Mar 2024 00:07:41 GMT  
		Size: 1.3 MB (1282589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbe9d4298112a8a733ba81e2b90e87afd4713e2873f499a8e0904dc6d8945d2`  
		Last Modified: Wed, 06 Mar 2024 00:07:41 GMT  
		Size: 1.4 MB (1387749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237cb31ec15aafe7089da51424f363285b3ee273f59e0e219a3dbb73b1e3adcd`  
		Last Modified: Wed, 06 Mar 2024 00:07:44 GMT  
		Size: 11.4 MB (11378042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:eaad7716786ac620cd62d19319edeefcbb61e19e2fb711e4bca482c1f7be9ad1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140448926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ef21d2e87329135f59bbe138ac2d6dbc4cfc4bc0d3b3fab20a7f6e04d15029`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:42:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 10:42:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:42:58 GMT
ENV NEKO_VERSION=2.3.0
# Tue, 12 Mar 2024 10:44:07 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Tue, 12 Mar 2024 10:44:07 GMT
ENV HAXE_VERSION=4.3.4
# Tue, 12 Mar 2024 10:44:07 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 12 Mar 2024 10:47:06 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.4 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Tue, 12 Mar 2024 10:47:06 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1758252bacf9c470036129a31aa54a0dbb113e079014cce8457565bc379553`  
		Last Modified: Tue, 12 Mar 2024 11:16:26 GMT  
		Size: 1.4 MB (1360245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d012943b91a4bf441542fd602fdcba25b8155624deb9eb8fc577c0b03c78a194`  
		Last Modified: Tue, 12 Mar 2024 11:16:26 GMT  
		Size: 1.4 MB (1438226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108dcba3028a6a0d552fba67b63bf5137b9876cf42daa6683be2c08af9e2a6e5`  
		Last Modified: Tue, 12 Mar 2024 11:16:28 GMT  
		Size: 13.5 MB (13484852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.2322; amd64

```console
$ docker pull haxe@sha256:0cc8597a9e1401ce1af5c6f3b236a0e2db8a13aec8916c141f1438f686fee46a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1937036414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:377e849da36e4f8ae74f05af188aa0bc9f259fc931643a40f3e37fe07995064f`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 21:28:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:28:13 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 14 Feb 2024 21:28:14 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 14 Feb 2024 21:28:15 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 14 Feb 2024 21:28:15 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 14 Feb 2024 21:28:16 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 14 Feb 2024 21:28:37 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Feb 2024 21:29:42 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 21:30:03 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 14 Feb 2024 21:30:03 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 14 Feb 2024 21:30:39 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 23:15:12 GMT
ENV HAXE_VERSION=4.3.4
# Tue, 05 Mar 2024 23:19:22 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.4/haxe-4.3.4-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 23:19:42 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 05 Mar 2024 23:19:43 GMT
ENV HOMEDRIVE=C:
# Tue, 05 Mar 2024 23:20:01 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 23:20:21 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 05 Mar 2024 23:20:22 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15530311ac6487034f1099258c2c440613d6f78ac1eaa4b64fd9f4f0c8af1fe9`  
		Last Modified: Wed, 14 Feb 2024 22:36:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4011b8e5a3627b0d6caa42d83346c2dba9c54fd7c5f3e9b96f6209efb25cf6a6`  
		Last Modified: Wed, 14 Feb 2024 22:36:53 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830f6502214ed8a7640eb3b82ed22defd4e0948f778dcf51f92f1ca31e841e2b`  
		Last Modified: Wed, 14 Feb 2024 22:36:53 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f71a6e42e1b7033eeea3a544723ba73dfacba2f9c2a8693defb1674b2c3ea1d`  
		Last Modified: Wed, 14 Feb 2024 22:36:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4008bc65fde88e3a84280556ec9b7aaa2c24dd01a4aa3a2689f67e9cba65b751`  
		Last Modified: Wed, 14 Feb 2024 22:36:51 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bcd6bec806846846cd0a21b95979b81b6284b3e920e813c7abd5c7e6dc607a`  
		Last Modified: Wed, 14 Feb 2024 22:36:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ecbb5b760e48330ae768c433abb8a684243f282013c9d37d5cc2ae5b55e08e`  
		Last Modified: Wed, 14 Feb 2024 22:36:51 GMT  
		Size: 457.5 KB (457455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6cd71bf6e68ae143258f4524c7ba09953f4e151d6d0736478f97f324f794e89`  
		Last Modified: Wed, 14 Feb 2024 22:36:52 GMT  
		Size: 12.9 MB (12858865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b817d51d89bba3fc1d770c8bf6469240bd292bc3752f2930953954c4cf0191`  
		Last Modified: Wed, 14 Feb 2024 22:36:48 GMT  
		Size: 303.4 KB (303412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2395d13d2e9d01ec6c8dc3c03ab651b527d56975bd6b1905bd277898a226fcdd`  
		Last Modified: Wed, 14 Feb 2024 22:36:48 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5474bd107afaf8954c3ae4d183e7d604f7f2ecd92cc441c6ccc47db3460aa889`  
		Last Modified: Wed, 14 Feb 2024 22:36:49 GMT  
		Size: 2.1 MB (2132792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc557d75011fde75b3c2b5be70413ed7e63757458bfdd472f61497ad78085a8e`  
		Last Modified: Tue, 05 Mar 2024 23:30:30 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5477596e47730781d4af674baea9b7e7fcc83589d238b66d75cb17fcb0b0976`  
		Last Modified: Tue, 05 Mar 2024 23:30:34 GMT  
		Size: 9.6 MB (9609110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e686f54b7330e7b27d2d4063fbc9f5c38abe9e58ab265544f6713a0429b7b7a5`  
		Last Modified: Tue, 05 Mar 2024 23:30:28 GMT  
		Size: 327.6 KB (327629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e448242449c379ab8e51699f3f01ecce32da60b051d6722dbe19f601a0308d5f`  
		Last Modified: Tue, 05 Mar 2024 23:30:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3acf469ce2981d5ace0f99ad0c7cec77ca666021ee68f72eb924c4d076122c0`  
		Last Modified: Tue, 05 Mar 2024 23:30:28 GMT  
		Size: 330.2 KB (330171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e25b0c19a8089a36adbbbb4ae30f865e23aaeeead0fe2d9c80bb9a06d622ac`  
		Last Modified: Tue, 05 Mar 2024 23:30:28 GMT  
		Size: 349.5 KB (349521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cf9f30dc552c92e27c4a052b10208872f4255dcb59f4ced183d0498594a3cf`  
		Last Modified: Tue, 05 Mar 2024 23:30:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.5458; amd64

```console
$ docker pull haxe@sha256:673d180da0f311e9a10ec0b3f5dad306f3df390720a1bace7513a7e1a13c6486
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2106798148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e6cd7e8d5e6c5fb550539f9c230e2c2d4419a77c23b850e6a28b3a4b53ff80`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 21:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 21:36:17 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 14 Feb 2024 21:36:18 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 14 Feb 2024 21:36:19 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 14 Feb 2024 21:36:20 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 14 Feb 2024 21:36:21 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 14 Feb 2024 21:37:38 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Feb 2024 21:39:39 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 21:41:07 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 14 Feb 2024 21:41:09 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 14 Feb 2024 21:42:54 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 23:20:41 GMT
ENV HAXE_VERSION=4.3.4
# Tue, 05 Mar 2024 23:25:20 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.4/haxe-4.3.4-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '402ca2e8fd08477b5c08191bddc0e9af3b58484308dde4558f670a455bc3e503') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 23:26:32 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 05 Mar 2024 23:26:33 GMT
ENV HOMEDRIVE=C:
# Tue, 05 Mar 2024 23:27:43 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 23:29:01 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 05 Mar 2024 23:29:01 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3486482d07b6425fcc693b0eaca3c37fbd34ec9ca8b8989ee7127a5c75155b0d`  
		Last Modified: Wed, 14 Feb 2024 21:11:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2e9c71bf0eb2e38199b0daca8c5d2851f9e15ef0162330230f1feb258b6408`  
		Last Modified: Wed, 14 Feb 2024 22:37:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28de9da0d37869fe993a82b7ab516864800a78a07a5a2479d6bbdf914ec4f1a8`  
		Last Modified: Wed, 14 Feb 2024 22:37:11 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfe4890346c0f3985fa72b6fa5a432ed3b8da22432c9a218f3f1da3bbdd8264`  
		Last Modified: Wed, 14 Feb 2024 22:37:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0c99d893b398ff58901075a1b6e2454f995020e84172cf9f347b049b073044`  
		Last Modified: Wed, 14 Feb 2024 22:37:09 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58de1758252cdfad2cb15dfd030112d1d95fda8eb040e8ab6e7efc13aeacc83d`  
		Last Modified: Wed, 14 Feb 2024 22:37:09 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4699e320840591d221337af6c7e92cca0206796e8720d95ab6b973af1cdeb1f5`  
		Last Modified: Wed, 14 Feb 2024 22:37:09 GMT  
		Size: 462.7 KB (462737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21fc32f757bbb15da2d0059e4a62dd6775604064b3bcaf307e985ee003ae8320`  
		Last Modified: Wed, 14 Feb 2024 22:37:10 GMT  
		Size: 12.9 MB (12896359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a683aed463e5efe749c6cad123119a06ec34f0e06421a7291a987447af701e3`  
		Last Modified: Wed, 14 Feb 2024 22:37:07 GMT  
		Size: 306.2 KB (306165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f9498bcc07012371c74de7404525ba39426dae33e645712f384dfb2dd766b1`  
		Last Modified: Wed, 14 Feb 2024 22:37:06 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfdae332ff5b267b696c81f2e500c8167a44f9b42dc29fffbf8e233e959b069`  
		Last Modified: Wed, 14 Feb 2024 22:37:07 GMT  
		Size: 2.1 MB (2141307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94e78fd99b2b85d7f90a9a7bc7ace0576f9593987af484c7c404e6b8a67823e`  
		Last Modified: Tue, 05 Mar 2024 23:30:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572886e794b3f38123d04dca0c178d0e089a26c7fcd226cfaf93b16645f52d15`  
		Last Modified: Tue, 05 Mar 2024 23:30:49 GMT  
		Size: 9.5 MB (9523133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fa0c690e2c609b29b448e0ca4bf38a7da786bbaebe2d3619dd1c74c3750851`  
		Last Modified: Tue, 05 Mar 2024 23:30:43 GMT  
		Size: 331.0 KB (330956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0502039faa6acf9b1ab1d50f73e1038bf28f392aacf33ff8c2c3399a377a3a9d`  
		Last Modified: Tue, 05 Mar 2024 23:30:43 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9379f159005197e3c7ec0b27ef17f08f739d7044bcb930ec15b9575731908c06`  
		Last Modified: Tue, 05 Mar 2024 23:30:43 GMT  
		Size: 332.9 KB (332862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04d79ab514417842c9f4656ab4e7995e7d58ee1c113dfbe358126d0efef94678`  
		Last Modified: Tue, 05 Mar 2024 23:30:43 GMT  
		Size: 342.3 KB (342344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d51b7261194310821890e3f99bb0c31c2ecd289cafd94991d098e09a9b67d1`  
		Last Modified: Tue, 05 Mar 2024 23:30:43 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
