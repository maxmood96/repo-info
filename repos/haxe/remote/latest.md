## `haxe:latest`

```console
$ docker pull haxe@sha256:1363f66e29728362eed6a70136d00c5eab72f57f7cfe94322ea117ddecece726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:77d5be0ca9465250bd816b3be3df264b03d567ecbe2ad4d515d26f5fb7252fbd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140045819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46226ed360601591f737dccf61fef6a59ebd5e058c659ea776665706d361e41a`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:42:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:42:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 04:43:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 22:00:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 22:00:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 22:00:15 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 01 Mar 2023 22:01:52 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Wed, 01 Mar 2023 22:01:52 GMT
ENV HAXE_VERSION=4.2.5
# Wed, 01 Mar 2023 22:01:52 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Wed, 01 Mar 2023 22:04:42 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Wed, 01 Mar 2023 22:04:43 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167c7feebee855d117e192389484ea8367be1ba84e7ee35f4e5e5663195facbf`  
		Last Modified: Wed, 01 Mar 2023 04:50:15 GMT  
		Size: 5.2 MB (5166586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dfff1f6f3ddd2194ea0775f199572e8b2d75c38713eef0444d6b1fd0ac7604`  
		Last Modified: Wed, 01 Mar 2023 04:50:15 GMT  
		Size: 10.9 MB (10876729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cdcd4942ebc7445d8a70117a83ecbc77dcc5ffc72c4b6f8e24c0c76cfee15d`  
		Last Modified: Wed, 01 Mar 2023 04:50:33 GMT  
		Size: 54.6 MB (54585443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892cd6c33b533ae4dba851d0dd9ecbfb922783e0fc5e21ff0b12652c8e3a13ae`  
		Last Modified: Wed, 01 Mar 2023 22:29:04 GMT  
		Size: 1.4 MB (1369698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d06d2a9eb37857f62358154a1c1e1f8ceb2fb0f0fc3b450252fc8cb94ad1c8`  
		Last Modified: Wed, 01 Mar 2023 22:29:04 GMT  
		Size: 1.4 MB (1447438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540d4c066ac9514d62b755410ffa5b388ee3df0769f062913831deb7e0cc71bd`  
		Last Modified: Wed, 01 Mar 2023 22:29:06 GMT  
		Size: 11.6 MB (11554003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:3ac3108439258a6f15bc9631ac9b346f780a2cb66a6c36c5da57121cb8b90c53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129509870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6976b92bad8d28d07475f84190666771e0b4a8ce735629cc3a0cd608f9bfc8a8`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:45 GMT
ADD file:95a5e178e353a9a46c230d78b0ef83309dd487651c34e47e972ed3dae08ea00b in / 
# Wed, 01 Mar 2023 01:57:45 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:32:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:32:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:29:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 02:30:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 02:30:05 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 02 Mar 2023 02:31:39 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Thu, 02 Mar 2023 02:31:39 GMT
ENV HAXE_VERSION=4.2.5
# Thu, 02 Mar 2023 02:31:39 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Thu, 02 Mar 2023 02:34:18 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Thu, 02 Mar 2023 02:34:18 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:30bee4bd8986478b5a9ecaaaba83525049f0b9b5a63ca88de878568bb6b83292`  
		Last Modified: Wed, 01 Mar 2023 02:02:32 GMT  
		Size: 50.2 MB (50212046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c2a83a9963df1d0618a3bef56d5f278e39b96940e18347e3575f30d199fb89`  
		Last Modified: Wed, 01 Mar 2023 03:09:13 GMT  
		Size: 4.9 MB (4934569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b6953f57698d5630bc57919975af4718f7e2eae8d6489d17ceab15dd2ab6e6`  
		Last Modified: Wed, 01 Mar 2023 03:09:13 GMT  
		Size: 10.2 MB (10217796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e676c4187d9dd900add9c8dd4b9c906be40a2b8db6cabfdaf280ac2e83cdfca`  
		Last Modified: Wed, 01 Mar 2023 03:09:35 GMT  
		Size: 50.4 MB (50355863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddcb9d88e3f8cd70bf2ea9c9262ba60a7d95a5b65486f79285978d261b6c502`  
		Last Modified: Thu, 02 Mar 2023 02:56:54 GMT  
		Size: 1.3 MB (1282669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b31b710ab4e8cb60892e592d92e64997ef4331285e95450d72681894ec8d85e`  
		Last Modified: Thu, 02 Mar 2023 02:56:54 GMT  
		Size: 1.4 MB (1387604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2e6a1c89a99284da780d425d0016af4cf280a97bd7585dc09ff78424380458`  
		Last Modified: Thu, 02 Mar 2023 02:56:56 GMT  
		Size: 11.1 MB (11119323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:7f008d8f3c74371b3fcf7629d8ed005989a93eeff74cbb559040f8cbc4cc4012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140400520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3749ea31f76e22b473c8b2e432365d657f812ec488fbdf01cae76400efeb60f7`
-	Default Command: `["haxe"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:11:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 07:11:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:35:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 15:35:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:35:42 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 23 Mar 2023 15:36:55 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Thu, 23 Mar 2023 15:36:55 GMT
ENV HAXE_VERSION=4.2.5
# Thu, 23 Mar 2023 15:36:55 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Thu, 23 Mar 2023 15:39:29 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.5 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Thu, 23 Mar 2023 15:39:29 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7971239fe1d69763272ccc0b2527efa95547d37c53630ed0a71db4e00d3ef964`  
		Last Modified: Thu, 23 Mar 2023 07:17:07 GMT  
		Size: 5.2 MB (5152756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c861b53509d61c37240d2f80efb3a351d2f1d7f4f8e8ec2e5004c1d86af89c`  
		Last Modified: Thu, 23 Mar 2023 07:17:07 GMT  
		Size: 10.9 MB (10873620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714880ecc1c021a5f708f4369f91d3c2c53b998a56d563d0a9aa9be2488d794`  
		Last Modified: Thu, 23 Mar 2023 07:17:23 GMT  
		Size: 54.7 MB (54676068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6877809716e95ba4aaede495aa6b39e3166469fa9c39cbd7ed5baf32a05cc3fa`  
		Last Modified: Thu, 23 Mar 2023 15:59:16 GMT  
		Size: 1.4 MB (1360057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b8879bef8765a882937109250a4edb91dc66db4cf8f869a0be12e587a9803e`  
		Last Modified: Thu, 23 Mar 2023 15:59:16 GMT  
		Size: 1.4 MB (1438240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7646390e06660b376b55674d097befed6c20056987c86a9a9a724e721eab14`  
		Last Modified: Thu, 23 Mar 2023 15:59:17 GMT  
		Size: 13.2 MB (13196680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.1607; amd64

```console
$ docker pull haxe@sha256:d203efc8a47097ac75a066bcad2ddccd5610a0e2b74ea0eeccfc386427d7bb54
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1748058988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e6433ffc32d9d8946e6cc4f8608db358f7b332ceb1dfd771c8c5b3a3bea8af`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 02:55:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 05:07:45 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Thu, 16 Mar 2023 05:07:47 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Thu, 16 Mar 2023 05:07:48 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Thu, 16 Mar 2023 05:07:49 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Thu, 16 Mar 2023 05:07:50 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Thu, 16 Mar 2023 05:08:26 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Mar 2023 05:09:58 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 05:10:28 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Thu, 16 Mar 2023 05:10:29 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 16 Mar 2023 05:11:14 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 05:11:15 GMT
ENV HAXE_VERSION=4.2.5
# Thu, 16 Mar 2023 05:16:29 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.2.5/haxe-4.2.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (9e7913999eb3693d540926219b45107b3dc249feb44204c0378fcdc6a74a9132) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '9e7913999eb3693d540926219b45107b3dc249feb44204c0378fcdc6a74a9132') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 05:17:43 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Thu, 16 Mar 2023 05:17:44 GMT
ENV HOMEDRIVE=C:
# Thu, 16 Mar 2023 05:18:39 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Mar 2023 05:19:11 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Thu, 16 Mar 2023 05:19:12 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d31bb6c06d038a3e1a69943be5f72e0ad656773c3f446d934ff816b71b0d631`  
		Last Modified: Thu, 16 Mar 2023 03:42:14 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702871d249ad59459fba20996868557f6ca95146703bec487fa3fd6749423906`  
		Last Modified: Thu, 16 Mar 2023 07:12:40 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33672a13328202582ab1f4a58d7b60e4dea1eb620b739aaea3890e2976b4bc91`  
		Last Modified: Thu, 16 Mar 2023 07:12:39 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05ec301d05c479fc1dbb5bf8e2f5d799bc7b675cef5444641df23646881a244`  
		Last Modified: Thu, 16 Mar 2023 07:12:38 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3327a11ef9fac220c917c3d2505c24cae547b6078ea46f38f8050f8d14d3cc3`  
		Last Modified: Thu, 16 Mar 2023 07:12:38 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25ed6933fd3b1ed7a6a4a6da54df6551a7114401d7ba7dbbb8e55e9fd25924ef`  
		Last Modified: Thu, 16 Mar 2023 07:12:37 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93852d5f9aa8014d5842f085099811cc30b8624d35f5fa6d6b421d6bbc8025ec`  
		Last Modified: Thu, 16 Mar 2023 07:12:36 GMT  
		Size: 733.8 KB (733754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcca68e23b1c9bf49cb91ebffc708dd6acd148d98228a7dcf041a0ea6631b9d2`  
		Last Modified: Thu, 16 Mar 2023 07:12:37 GMT  
		Size: 13.1 MB (13135837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb1caf9af9cd24236913d6be75f4f7318b6b7470ced595ecdbda6e730ca3703`  
		Last Modified: Thu, 16 Mar 2023 07:12:35 GMT  
		Size: 547.0 KB (547024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693f8b26337b46e868d74b9b54ee578718bd734fbfee9a4826b09909bbad12fb`  
		Last Modified: Thu, 16 Mar 2023 07:12:33 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb857ab17caacc9133d71e711be51aee630338adcf12da36dc9afbe912eb4087`  
		Last Modified: Thu, 16 Mar 2023 07:12:35 GMT  
		Size: 2.4 MB (2379973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a02a92cc3c33f58860f228a71283d6ed1acf6c3cbac81a20f84e8e68fe5d84`  
		Last Modified: Thu, 16 Mar 2023 07:12:32 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b7ef478a007db7b7fe00a8de40ebe98cbdc3b3552933201206db19f4074f29`  
		Last Modified: Thu, 16 Mar 2023 07:12:42 GMT  
		Size: 15.5 MB (15499727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a833e6c4e75cdd10fdbd7b6b8364a3a3295798dd58d2dc9795c15859d1f524`  
		Last Modified: Thu, 16 Mar 2023 07:12:31 GMT  
		Size: 596.8 KB (596754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c614141a436cb5bf62dc5d74288e4032a900d910fe4284db9e44688ae740dde`  
		Last Modified: Thu, 16 Mar 2023 07:12:30 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83f108ddce3d6491919da09cd7c229aa942adbc4d62a844c8fc49397591d8ed`  
		Last Modified: Thu, 16 Mar 2023 07:12:31 GMT  
		Size: 603.3 KB (603308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148fbe4214dbe8f1868c3eb18bf742ec307605c6a90388db56c6782d7a61104f`  
		Last Modified: Thu, 16 Mar 2023 07:12:31 GMT  
		Size: 608.2 KB (608238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea73883e1cf684ba6041d67e66f16da87baf9e6ceaf36a3cbe007ae3c2d17f7`  
		Last Modified: Thu, 16 Mar 2023 07:12:30 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.4131; amd64

```console
$ docker pull haxe@sha256:9f1222c7c74cb4f8d1cdeaf73259f18261aa24f458d82679cc1ca7f8e9dcf728
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2044621287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581e4fd9112f62b41c1b95f2d6360f7b21eb1e7b66351ad797c54cf65334d834`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 02:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 05:19:40 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Thu, 16 Mar 2023 05:19:41 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Thu, 16 Mar 2023 05:19:42 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Thu, 16 Mar 2023 05:19:44 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Thu, 16 Mar 2023 05:19:45 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Thu, 16 Mar 2023 05:20:58 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Mar 2023 05:23:03 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 05:24:16 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Thu, 16 Mar 2023 05:24:17 GMT
ENV NEKO_VERSION=2.3.0
# Thu, 16 Mar 2023 05:25:41 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 05:25:42 GMT
ENV HAXE_VERSION=4.2.5
# Thu, 16 Mar 2023 05:31:21 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.2.5/haxe-4.2.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (9e7913999eb3693d540926219b45107b3dc249feb44204c0378fcdc6a74a9132) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '9e7913999eb3693d540926219b45107b3dc249feb44204c0378fcdc6a74a9132') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 05:32:52 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Thu, 16 Mar 2023 05:32:53 GMT
ENV HOMEDRIVE=C:
# Thu, 16 Mar 2023 05:34:07 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 16 Mar 2023 05:35:30 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Thu, 16 Mar 2023 05:35:31 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474eedda733dad347e4baad9fb9f3d700b58e5788f7453d1979cebb167746b32`  
		Last Modified: Thu, 16 Mar 2023 03:44:11 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050290e029e1bab579a716997d6f4f0ec424459059405a4afd12007b7541b997`  
		Last Modified: Thu, 16 Mar 2023 07:12:59 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15d1271cfa670a89060df45848713a5bf0a7e1419e7a057cf306aefac251656`  
		Last Modified: Thu, 16 Mar 2023 07:12:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144521e1a13480dea29f27eadb817a3306cf7d39d6b9fc8b92fc26b1ed203f2b`  
		Last Modified: Thu, 16 Mar 2023 07:12:59 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57368534d7fa0a1d4df97e6cdd42eec6d41b937c56d07808a7583d21adb2ca66`  
		Last Modified: Thu, 16 Mar 2023 07:12:57 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114bca69b87080c4833a63e53e8156d587eea80a4eedab1b70437a616434c1a7`  
		Last Modified: Thu, 16 Mar 2023 07:12:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce153d48fbd8a6db80bc1dfc64a61d4a49fc975cc6a583b474fc794301212a0d`  
		Last Modified: Thu, 16 Mar 2023 07:12:57 GMT  
		Size: 478.3 KB (478297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd43f218f32d80f45276577fb99dd537344ce24c1e0207eedc0daad11de23a9`  
		Last Modified: Thu, 16 Mar 2023 07:12:58 GMT  
		Size: 12.9 MB (12933222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565696f5df8ad257b5472faf355cc978cd01ab18c5906009732ca2298c1264fa`  
		Last Modified: Thu, 16 Mar 2023 07:12:55 GMT  
		Size: 320.9 KB (320905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544251f3191a1d8eb761c620c751d8276ccb4c66f749b510b6faa6518836e7ea`  
		Last Modified: Thu, 16 Mar 2023 07:12:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849e967170ac5712ffe1e916e2ec692bb52e6386ee0372a5dd6d57603b923e66`  
		Last Modified: Thu, 16 Mar 2023 07:12:55 GMT  
		Size: 2.2 MB (2150876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1965e4da3f4a6bf772928eb78a55b6100db521fff8f0d48a964cc5237d60df9d`  
		Last Modified: Thu, 16 Mar 2023 07:12:53 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24400be5f49228ce947350629d7b6e724f7ee8515622fe75bc7d7558575283c1`  
		Last Modified: Thu, 16 Mar 2023 07:13:02 GMT  
		Size: 14.1 MB (14100430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22cfa1f6222640d2b6d7ae32611fe61edf2e50ffc31f9b3e619ad1a5917cc96c`  
		Last Modified: Thu, 16 Mar 2023 07:12:51 GMT  
		Size: 364.6 KB (364560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54982aac0d8ea608fa87ec71e9768430705ce2f7cfaa5944e6967710c9a9b34`  
		Last Modified: Thu, 16 Mar 2023 07:12:51 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4dfbc9105a892c55fd81ebad25adecac0b3d47b0a65cbadce37f72d229e82c`  
		Last Modified: Thu, 16 Mar 2023 07:12:51 GMT  
		Size: 367.1 KB (367130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8946295d4bf786151f18261f5a75ba57fd226029305bcba734727b6f3d07ab48`  
		Last Modified: Thu, 16 Mar 2023 07:12:51 GMT  
		Size: 383.1 KB (383097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5396a2fef8459bb1ce7c3d634220ba6f3962b3465f03e05d4bb226a8b129a599`  
		Last Modified: Thu, 16 Mar 2023 07:12:51 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
