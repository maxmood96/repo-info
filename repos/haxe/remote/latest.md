## `haxe:latest`

```console
$ docker pull haxe@sha256:c242eeba70cba5aafdc0936c7f3354a7748dbe5ece83bc13c92810cfb72edb53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:8f8213622e2e64d6660fbc576eed0030636c07edee664f7b7593da8e72776ee4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133575056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f29905b84890855f922464bc50d088117718622f793e5f7837f6e293ea1583`
-	Default Command: `["haxe"]`

```dockerfile
# Sat, 10 Apr 2021 01:20:08 GMT
ADD file:e18bc3e10e7c743f18bb8be65ec94a62c03764af7dbdb4957f9a600237730212 in / 
# Sat, 10 Apr 2021 01:20:09 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:54:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:35:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 23:36:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 23:36:01 GMT
ENV NEKO_VERSION=2.3.0
# Sat, 10 Apr 2021 23:37:09 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Sat, 10 Apr 2021 23:37:09 GMT
ENV HAXE_VERSION=4.2.1
# Sat, 10 Apr 2021 23:37:09 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sat, 10 Apr 2021 23:42:07 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Sat, 10 Apr 2021 23:42:07 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:bd8f6a7501ccbe80b95c82519ed6fd4f7236a41e0ae59ba4a8df76af24629efc`  
		Last Modified: Sat, 10 Apr 2021 01:24:48 GMT  
		Size: 50.4 MB (50432971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44718e6d535d365250316b02459f98a1b0fa490158cc53057d18858507504d60`  
		Last Modified: Sat, 10 Apr 2021 02:01:57 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe9738af0cb2184ee8f3fb3dcb130455385aa428a27d14e1e07a5587ff16e64`  
		Last Modified: Sat, 10 Apr 2021 02:01:59 GMT  
		Size: 10.0 MB (9997183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37aabde37b87d272286df45e6a3145b0884b72e07e657bf1a2a1e74a92c6172`  
		Last Modified: Sat, 10 Apr 2021 02:02:22 GMT  
		Size: 51.8 MB (51841093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9d9f3f4679bae129fc0842f042d53c42215345256e1c27521b17634bd17610`  
		Last Modified: Sun, 11 Apr 2021 00:07:55 GMT  
		Size: 1.3 MB (1312584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7c76cf89e22324abdb3b59d7e51d2fc45043344aa4c129c0b931a56e01537a`  
		Last Modified: Sun, 11 Apr 2021 00:07:56 GMT  
		Size: 2.3 MB (2308153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef16b91f5cce127403de91c8513ff564a10820fad47f02141ba93a10a54bdbe`  
		Last Modified: Sun, 11 Apr 2021 00:07:59 GMT  
		Size: 9.9 MB (9850128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:2ed6819b16e74aa7535bef7748e30e307ee4e381c96c382415a4752204dd96fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122729836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b15e39d67ff4d6345f81e6a1f3783400964879f8da3a54fb593be0c3bb4f389`
-	Default Command: `["haxe"]`

```dockerfile
# Sat, 10 Apr 2021 00:59:18 GMT
ADD file:bd2081229497eea2b33310cb1582b965581ca78b00b87cc8e42bdc8b9f350678 in / 
# Sat, 10 Apr 2021 00:59:20 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 06:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 06:05:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 06:06:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:32:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 18:33:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:33:03 GMT
ENV NEKO_VERSION=2.3.0
# Sat, 10 Apr 2021 18:36:34 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Sat, 10 Apr 2021 18:36:36 GMT
ENV HAXE_VERSION=4.2.1
# Sat, 10 Apr 2021 18:36:37 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sat, 10 Apr 2021 18:45:37 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Sat, 10 Apr 2021 18:45:40 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:de0ca59eb81518ffd92fbcd386251018f950dc16b1bd8ad2e642184db76be2a1`  
		Last Modified: Sat, 10 Apr 2021 01:07:26 GMT  
		Size: 45.9 MB (45915598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed23bfa8aaeab64a1ca00d3bead680f790be28326d14305705b2ee5227b4f2b7`  
		Last Modified: Sat, 10 Apr 2021 06:19:54 GMT  
		Size: 7.1 MB (7124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a12824e68a5072613049fad15fc8f0d209526ddd9d85787cc60d1b0d5073c0`  
		Last Modified: Sat, 10 Apr 2021 06:19:55 GMT  
		Size: 9.3 MB (9343784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da73a12ad465a34e484807c20e78927bd0dbd29a487e06024dbf3a1e21ba8a39`  
		Last Modified: Sat, 10 Apr 2021 06:20:19 GMT  
		Size: 47.4 MB (47356313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ca8680bd116af3d1316246ea9e7187c6eac62087aed2a80d6225e0147d4a8e`  
		Last Modified: Sat, 10 Apr 2021 19:43:57 GMT  
		Size: 1.2 MB (1234924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eed243ed39c49cbb39f1dcf9749836a3d0576b8ef655c172957a37fee9a6185`  
		Last Modified: Sat, 10 Apr 2021 19:43:58 GMT  
		Size: 2.3 MB (2250040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740469066f21218739e9d013ac7b11a7559a0317ce481a27539a4d38e8c1b7e4`  
		Last Modified: Sat, 10 Apr 2021 19:44:01 GMT  
		Size: 9.5 MB (9504996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:42e43458bbdf3922114d91c4519d4c3d2d93dcf1fdc4ab700679783981b54e0d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134753576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc1e405ec26a506a3cf08cf3c6417532b7a67337c6cbd86a71783a71d4a905b`
-	Default Command: `["haxe"]`

```dockerfile
# Sat, 10 Apr 2021 00:40:59 GMT
ADD file:320ad0e2a3d6c676ddb8ce5646b5a94d18d82a8868955da3a9379a261dfe1ffe in / 
# Sat, 10 Apr 2021 00:41:01 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:46:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:46:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 10 Apr 2021 01:47:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 21:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 21:50:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1c2 		zlib1g 		libpcre3 		libmariadb3 		libsqlite3-0 		libmbedcrypto3 		libmbedtls12 		libmbedx509-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 21:50:11 GMT
ENV NEKO_VERSION=2.3.0
# Sat, 10 Apr 2021 21:53:18 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre3-dev 		zlib1g-dev 		apache2-dev 		libmariadb-client-lgpl-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk2.0-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-3-0/neko-2.3.0.tar.gz" 	&& echo "850e7e317bdaf24ed652efeff89c1cb21380ca19f20e68a296c84f6bad4ee995 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache
# Sat, 10 Apr 2021 21:53:20 GMT
ENV HAXE_VERSION=4.2.1
# Sat, 10 Apr 2021 21:53:21 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sat, 10 Apr 2021 22:02:20 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre3-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 				opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 			' 	&& git clone --recursive --depth 1 --branch 4.2.1 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 			&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] && opam install /usr/src/haxe --deps-only --yes || make opam_install ) 		&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 			&& eval `opam env --revert` 	&& rm -rf ~/.opam 		&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache
# Sat, 10 Apr 2021 22:02:21 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:01cf0f0da10ede0eec0fc1c5fbfdeb63a447dfcc0a3c4419c0a4c3f0a2826636`  
		Last Modified: Sat, 10 Apr 2021 00:47:28 GMT  
		Size: 49.2 MB (49225782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c667eb56cd05909001c1c50e81cbc75e290fd8e353f974bab4246a0d4fc484ca`  
		Last Modified: Sat, 10 Apr 2021 02:01:00 GMT  
		Size: 7.7 MB (7695101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ca15a4cef673e0e1a7bc3e659f4653df9bce82b945e367475e436852cc7880`  
		Last Modified: Sat, 10 Apr 2021 02:00:59 GMT  
		Size: 10.0 MB (9984406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7f1cf823a7fca9771e278355d8924fac8d9cef1f8e3ecbc87332c4859d1d4f`  
		Last Modified: Sat, 10 Apr 2021 02:01:23 GMT  
		Size: 52.2 MB (52167974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9465ab1a7f81d61e6ec3091b8259c7a58faaaf0d2ffc8351d09d56a88297ca5f`  
		Last Modified: Sat, 10 Apr 2021 22:53:40 GMT  
		Size: 1.3 MB (1303745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a19089836af6d216474b3a4c9ea589aa024d6cc50d46f001afca76fe1f8ba5`  
		Last Modified: Sat, 10 Apr 2021 22:53:41 GMT  
		Size: 2.3 MB (2303958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ed144f476c23062bf8ba8f93f9b8e2d2395c00b029d31e43d959ca747f93d6`  
		Last Modified: Sat, 10 Apr 2021 22:53:50 GMT  
		Size: 12.1 MB (12072610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.1879; amd64

```console
$ docker pull haxe@sha256:4888959c588425326656b6926fc60c182f682ab11e775649f084ff5d9607b0eb
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2505549475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249ab3f6960616097952deafb8b3c75fea6e8b11e7643ad978b4ac582781ea19`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 13:10:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 13:10:30 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 14 Apr 2021 13:10:31 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 14 Apr 2021 13:10:32 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 14 Apr 2021 13:10:33 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 14 Apr 2021 13:10:34 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 14 Apr 2021 13:11:45 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 13:13:12 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 13:13:44 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 14 Apr 2021 13:13:45 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 14 Apr 2021 13:14:42 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 13:14:43 GMT
ENV HAXE_VERSION=4.2.1
# Wed, 14 Apr 2021 13:19:35 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.2.1/haxe-4.2.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (68caf3d86f6e707a0f0a655a9bc367a8489233f08daafb90945d2b195090f307) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '68caf3d86f6e707a0f0a655a9bc367a8489233f08daafb90945d2b195090f307') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 13:20:08 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 14 Apr 2021 13:20:09 GMT
ENV HOMEDRIVE=C:
# Wed, 14 Apr 2021 13:20:42 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 13:21:19 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org') >$null
# Wed, 14 Apr 2021 13:21:53 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://d1smpvufia21az.cloudfront.net') >$null
# Wed, 14 Apr 2021 13:21:54 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2159a5d0f75ce11e6fe71e4260ede5c3c88a9eb76a0ff43ac6746b2b9b96775`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b16e575ea9087b4f21af2ce39d967accb81c2d9813df1fff07772bd6045a038`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87537e4356d004aa83dd5d3999797ff263af6ceeea868f8bb83aaca2822beb5b`  
		Last Modified: Wed, 14 Apr 2021 15:37:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3beb45da98c40966b391d3eb55065d68b141fd7baff01d82b6ff0e61204cf65`  
		Last Modified: Wed, 14 Apr 2021 15:37:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1143ab74b24a71aa92d8a42be9e83a393e587d26f331f8cdc1bbbe8d6b5f162c`  
		Last Modified: Wed, 14 Apr 2021 15:37:07 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc00710fffd49cbdaa249db1ebf17ba5aeb0265bb66964bc41bcf4bc3b5f585`  
		Last Modified: Wed, 14 Apr 2021 15:37:05 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c18cbf70a68cda1df3c962ff7d0b917e07f8732ea03da0ae7b04711746345e`  
		Last Modified: Wed, 14 Apr 2021 15:37:10 GMT  
		Size: 5.1 MB (5071334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f44ea5fb27530e21d98dfcc4164fec27a53be309c235dd1c955ff6b8dd6348d`  
		Last Modified: Wed, 14 Apr 2021 15:37:06 GMT  
		Size: 12.9 MB (12930625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc1466b18572c164a4fbeb6e9b640112a56379272b70dde9f58ae16aa40e013`  
		Last Modified: Wed, 14 Apr 2021 15:37:02 GMT  
		Size: 331.6 KB (331594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8102781c9def2b7feb4495534196cad83e9ab91e980b6a58b4942740a13edf1f`  
		Last Modified: Wed, 14 Apr 2021 15:36:59 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c89549bfff9dca24bb9f6b162114f239b7da9689f2f9f1af8c4ce6f1dd7175`  
		Last Modified: Wed, 14 Apr 2021 15:37:01 GMT  
		Size: 2.2 MB (2153693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8355386ba65d9415e01240edb9802812ee2374b19d57a86d729479064c6fe574`  
		Last Modified: Wed, 14 Apr 2021 15:36:59 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa5e0de87644c2c093589c8bf7eabb51f76e8c1adf038cddec0d23b54a5ca15`  
		Last Modified: Wed, 14 Apr 2021 15:37:07 GMT  
		Size: 13.8 MB (13757880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d813f6707b2b70a15313e1481f9ef35a142e2ed252a4cb1c51b77bf641ed7cd`  
		Last Modified: Wed, 14 Apr 2021 15:36:59 GMT  
		Size: 365.1 KB (365089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9749a282bd508b46470411acf2603d4ebfadd79e4b583aa32df83194d1d5bd08`  
		Last Modified: Wed, 14 Apr 2021 15:36:55 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085bfd6567cb976f8e33bd61a1632926a2c2df0f1693c0a8b9619d3ce5a006a5`  
		Last Modified: Wed, 14 Apr 2021 15:36:56 GMT  
		Size: 376.3 KB (376312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17e447bebf4e9105b6c722f128b6f34fca17152e6b2d8861e62f37ffaba093cc`  
		Last Modified: Wed, 14 Apr 2021 15:36:56 GMT  
		Size: 385.3 KB (385283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294947af76034fe395683f71839eafa275620562ad66f5999aa59472edccb0a2`  
		Last Modified: Wed, 14 Apr 2021 15:36:56 GMT  
		Size: 409.7 KB (409696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d783ed225b91aa28b297291d47bbbf6dae49dac6ffc962cf61164793a766e9`  
		Last Modified: Wed, 14 Apr 2021 15:36:56 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.14393.4350; amd64

```console
$ docker pull haxe@sha256:33e2ee2a40c0dffe294001343f51464eea2c38dc7b0642fe04f33f0b5edc266a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5882578096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7f1648c2033e949e61b68f7408110875a74351d663f88a7537091a59269d96`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 13:22:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Apr 2021 13:22:03 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 14 Apr 2021 13:22:04 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 14 Apr 2021 13:22:05 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 14 Apr 2021 13:22:06 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 14 Apr 2021 13:22:07 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 14 Apr 2021 13:23:57 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 13:26:27 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 13:28:02 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 14 Apr 2021 13:28:03 GMT
ENV NEKO_VERSION=2.3.0
# Wed, 14 Apr 2021 13:30:16 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-3-0/neko-2.3.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (d09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne 'd09fdf362cd2e3274f6c8528be7211663260c3a5323ce893b7637c2818995f0b') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 13:30:18 GMT
ENV HAXE_VERSION=4.2.1
# Wed, 14 Apr 2021 13:35:57 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.2.1/haxe-4.2.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (68caf3d86f6e707a0f0a655a9bc367a8489233f08daafb90945d2b195090f307) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '68caf3d86f6e707a0f0a655a9bc367a8489233f08daafb90945d2b195090f307') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 14 Apr 2021 13:37:29 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 14 Apr 2021 13:37:30 GMT
ENV HOMEDRIVE=C:
# Wed, 14 Apr 2021 13:39:08 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Apr 2021 13:40:42 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org') >$null
# Wed, 14 Apr 2021 13:42:21 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://d1smpvufia21az.cloudfront.net') >$null
# Wed, 14 Apr 2021 13:42:22 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f616bb7876e6f944d82fa1802ffab5ca4931a63e1b999f0851b52120cda83539`  
		Last Modified: Wed, 14 Apr 2021 15:37:43 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11323237319303fe91d704885b17fff2699f40aa6d6ef62c0f1fc89e880c6478`  
		Last Modified: Wed, 14 Apr 2021 15:37:42 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3578c20accfd9a6e7093e1a8f25dff3c3827052010982f0d12c16686719713d`  
		Last Modified: Wed, 14 Apr 2021 15:37:41 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fafbb710269acfd92b2542046ce2630f53672eea4d1379784a60489c4ebc89`  
		Last Modified: Wed, 14 Apr 2021 15:37:40 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc3122d9e171286151585d2eb708d33ec99b8cd357f94d678cf89d0f866e4ed`  
		Last Modified: Wed, 14 Apr 2021 15:37:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e6596d1881dff4703deb471f67beac462beff95cf4ca1476f57428e1264eec`  
		Last Modified: Wed, 14 Apr 2021 15:37:37 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2de79fce3ea07d1c0f77b4853f4910ce1e1d6d7f02c9f52bf3df338973162e`  
		Last Modified: Wed, 14 Apr 2021 15:37:36 GMT  
		Size: 5.6 MB (5643619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ec8e41e416b35b63364cc62ff82d3f8811d2ce2faa17ad88d38f1fe044ec19`  
		Last Modified: Wed, 14 Apr 2021 15:37:38 GMT  
		Size: 22.7 MB (22670999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d16f9a0756b500b0cbf066f8079f09ff92d5c79a6b4db4ebc79647c992ee43`  
		Last Modified: Wed, 14 Apr 2021 15:37:33 GMT  
		Size: 5.6 MB (5591531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f38b6245920554dc8cf7ad0e97cd6d943f24a248e11d8a3547aab37c2928b93`  
		Last Modified: Wed, 14 Apr 2021 15:37:30 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee2b42005051d191e30c8980ffc53b4816959e344e578da4cbf5714d65de7d1`  
		Last Modified: Wed, 14 Apr 2021 15:37:41 GMT  
		Size: 11.9 MB (11903778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14f9c1075ab2707af3fa0eb2dfa0497cfeeed476fbc49ca20dbbf8beba1a9e7`  
		Last Modified: Wed, 14 Apr 2021 15:37:27 GMT  
		Size: 1.4 KB (1409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89e6b8a8b7c11f35d6dfaec0f75df6efd6b6b2b19712cb4db4ff725c5a921fc`  
		Last Modified: Wed, 14 Apr 2021 15:37:41 GMT  
		Size: 19.4 MB (19390617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c8016e190a4acad00a4214c7bc75bffe0e574efc6b5c18933c56be2cfaa146`  
		Last Modified: Wed, 14 Apr 2021 15:37:26 GMT  
		Size: 5.6 MB (5615323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf33df9461a877e1d2c8a179678f3e1df05c18eb101e8a11e272d2f79173a36`  
		Last Modified: Wed, 14 Apr 2021 15:37:22 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc371364b95d28b9cbaa5af8d36a25fee52112be9541d73390ebac2b5563b80`  
		Last Modified: Wed, 14 Apr 2021 15:37:24 GMT  
		Size: 5.6 MB (5615659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c7a7662967245a795619d98559b0d03d9cd10c5b0c1d04446f873296a80e67`  
		Last Modified: Wed, 14 Apr 2021 15:37:25 GMT  
		Size: 5.6 MB (5622829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1feb744494c41abfced40dedc3ae9d52026373b6dc1d46b58be8669c3932f43b`  
		Last Modified: Wed, 14 Apr 2021 15:37:27 GMT  
		Size: 5.6 MB (5626450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea69b50ea736800e6af1fb2e311f12c407e31686d4d315abab260e5fb556e9`  
		Last Modified: Wed, 14 Apr 2021 15:37:22 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
