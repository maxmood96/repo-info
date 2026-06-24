## `haxe:latest`

```console
$ docker pull haxe@sha256:d66f2b9fc43a1fae6fcc6f2a732c3ebe604f1db118165fb6d7bd115ed67aa249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32995; amd64
	-	windows version 10.0.20348.5256; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:7904130a8ccae528e2d96affeb3c088e857a219ea84a4f6b0563b93371225e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165312858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958a6ad44224fafbabbb3008500fbea33440e00ed28177a0ef1eb47ee30fe8d6`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:17:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto16 		libmbedtls21 		libmbedx509-7 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:51 GMT
ENV NEKO_VERSION=2.4.1
# Wed, 24 Jun 2026 03:19:05 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Wed, 24 Jun 2026 03:19:05 GMT
ENV HAXE_VERSION=4.3.7
# Wed, 24 Jun 2026 03:19:05 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Wed, 24 Jun 2026 03:22:35 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& opam pin add luv 0.5.14 --no-action 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on=luv || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Wed, 24 Jun 2026 03:22:35 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:aa3e9ef32f73c30e8b065800ee66429992d3bfea6a1fb8224afdd878ab5b994f`  
		Last Modified: Wed, 24 Jun 2026 00:28:33 GMT  
		Size: 49.3 MB (49317255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f59c84a786323367a79d4959142649bb24b16c989bbaae7f273550b47325959`  
		Last Modified: Wed, 24 Jun 2026 01:41:50 GMT  
		Size: 25.6 MB (25634938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d0db852850114cc79598cc8ab1ec19da54691d9e3267288bb3458d7488f125`  
		Last Modified: Wed, 24 Jun 2026 02:28:58 GMT  
		Size: 67.8 MB (67778134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5c811c078754cb07e6cab76023d049a8347fdd6a39454778ae6abd22a9feb1`  
		Last Modified: Wed, 24 Jun 2026 03:22:41 GMT  
		Size: 1.5 MB (1478605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc25905a6077737e3e52aa7d6e3a3962d444dc4ac21b7b7505856aabef02455b`  
		Last Modified: Wed, 24 Jun 2026 03:22:41 GMT  
		Size: 9.4 MB (9405367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed41e9b0ee635d89e9225cecdc28930e0b0dfe5c44bf16457caf6942c2663b7f`  
		Last Modified: Wed, 24 Jun 2026 03:22:41 GMT  
		Size: 11.7 MB (11698559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:4fce81d98a4bbd8668d159f4659857d3f1bd6f4c3d16f0b437534d44004cbeab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb350a0a1840eccc057df521fc806f98afec6130418e12187c4f0cb96a6f6be`

```dockerfile
```

-	Layers:
	-	`sha256:bd0cdd72b74083fc8d5123ae9c1e778699fe8c596d30f5215925c9d1157ab330`  
		Last Modified: Wed, 24 Jun 2026 03:22:40 GMT  
		Size: 19.1 KB (19052 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:894b3b22487aab91fa9dcb2ee49b5df6699a42dc2ae8afdcaa66cc2d9508170a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.7 MB (153730244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a0350bc66bc7fc00867a2fbaf0360472e2d442cb77d5f61893f021d39a93be`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:27:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 22 Jun 2026 20:50:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 20:50:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto16 		libmbedtls21 		libmbedx509-7 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jun 2026 20:50:04 GMT
ENV NEKO_VERSION=2.4.1
# Mon, 22 Jun 2026 20:51:36 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Mon, 22 Jun 2026 20:51:36 GMT
ENV HAXE_VERSION=4.3.7
# Mon, 22 Jun 2026 20:51:36 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Mon, 22 Jun 2026 20:56:20 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& opam pin add luv 0.5.14 --no-action 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on=luv || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Mon, 22 Jun 2026 20:56:20 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:df041f2d52cc5410fddc569f8ab35cdfdd35a38e037f7aab971e409724bfd203`  
		Last Modified: Wed, 10 Jun 2026 23:42:20 GMT  
		Size: 45.7 MB (45748641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04879054973f6f0ae366a776f1ee6e23a5ae9b6072a5861ec514fdf29f7dbd68`  
		Last Modified: Thu, 11 Jun 2026 01:27:20 GMT  
		Size: 23.6 MB (23635995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e960af1a374080feee4d695210e1cc29cde28cd70c56fad7cb555534519a7e`  
		Last Modified: Thu, 11 Jun 2026 02:45:25 GMT  
		Size: 62.7 MB (62746530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026c6f6a1c034be45dea6d2a378e1077b3975295e4b96d33ca14303bd79d1030`  
		Last Modified: Mon, 22 Jun 2026 20:56:26 GMT  
		Size: 1.4 MB (1363632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14739ffc51f4fbd54bd231769f3c916dbc8cc50d26be54d78ed42c9f15586bcb`  
		Last Modified: Mon, 22 Jun 2026 20:56:26 GMT  
		Size: 9.1 MB (9072803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be51ac2f91dddc712febc5315f0ac512ea7fbcde1a82f71a7ecb04f4032eb87a`  
		Last Modified: Mon, 22 Jun 2026 20:56:26 GMT  
		Size: 11.2 MB (11162643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:f5984625e66775fc89bee938480f152f190cc57c8c0bd6832295e9a486e3fbad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9022aa310590e37d308fb61ef781adcfffdd70866ec20df80cd2f801897ada`

```dockerfile
```

-	Layers:
	-	`sha256:80c88652cadbec594309434953f7b03e03db65376020236cddebcb202c8eec26`  
		Last Modified: Mon, 22 Jun 2026 20:56:25 GMT  
		Size: 19.2 KB (19166 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:8ffd7ba24fc15d6fc8e4d11dcdc380e83047cf217a9c90c721bc967adfb8d50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166548292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6985f832b9d9c3b21d3e1cbbc94f9210ea75d84cfd5ce39a4e3c8f8fa60100a`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:45:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:17:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto16 		libmbedtls21 		libmbedx509-7 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 03:17:44 GMT
ENV NEKO_VERSION=2.4.1
# Wed, 24 Jun 2026 03:19:02 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Wed, 24 Jun 2026 03:19:02 GMT
ENV HAXE_VERSION=4.3.7
# Wed, 24 Jun 2026 03:19:02 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Wed, 24 Jun 2026 03:22:33 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& opam pin add luv 0.5.14 --no-action 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on=luv || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Wed, 24 Jun 2026 03:22:33 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c8a311258fd162f6aa0db134045a19154c81a2244ff9ed7620256c95ae5d6b69`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 49.7 MB (49678395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe059c57e3bc40ea8086d6be574927bed6c0a000b182f3354b758009265e197`  
		Last Modified: Wed, 24 Jun 2026 01:45:26 GMT  
		Size: 25.0 MB (25026863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf605f6b62a65326644e598c84134d29702579734c83dfca4cedf5dad7fb6d3`  
		Last Modified: Wed, 24 Jun 2026 02:35:43 GMT  
		Size: 67.6 MB (67592645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2036f5cecb1b7475069fa47c9d8a93ba3afa483743ca3ba32683fb35a70fcd36`  
		Last Modified: Wed, 24 Jun 2026 03:22:39 GMT  
		Size: 1.5 MB (1477016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf124d6741bdcbe6776113bd66bf542b7ef8fc3ea7e244cdb78e2c6ca62c79d`  
		Last Modified: Wed, 24 Jun 2026 03:22:39 GMT  
		Size: 9.4 MB (9351006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b668c7e7cdfe73f3316ad14ecb9c6fc32da0c2a22b900c8d37bbb9c9dbae468`  
		Last Modified: Wed, 24 Jun 2026 03:22:39 GMT  
		Size: 13.4 MB (13422367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:246c56b2617c49259f05311f443260ea150c2c66a07db1f4d1b7854b69b210a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e680b09484ada294576cf618a901638f6b818e89b15a50a69aa13dd5e71d55e`

```dockerfile
```

-	Layers:
	-	`sha256:3281151bc4ec2e30c43a398ff87a105ae11ed9b9efbb6c31aa50ba1e364b8230`  
		Last Modified: Wed, 24 Jun 2026 03:22:39 GMT  
		Size: 19.2 KB (19198 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.26100.32995; amd64

```console
$ docker pull haxe@sha256:e4774ec8808081bc669987ff4613491685c3710b33d02538a1b7e394cdf508aa
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2309252036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c738d6897d41809749df206c29488caa09feac3bd8627a9fa5e06e110e3c5f0c`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:22:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:22:23 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 09 Jun 2026 22:22:24 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 09 Jun 2026 22:22:25 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 09 Jun 2026 22:22:25 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 09 Jun 2026 22:22:26 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 09 Jun 2026 22:22:32 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:22:52 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:22:58 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 09 Jun 2026 22:22:59 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 09 Jun 2026 22:23:11 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:23:11 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 09 Jun 2026 22:24:15 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:24:21 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 09 Jun 2026 22:24:21 GMT
ENV HOMEDRIVE=C:
# Tue, 09 Jun 2026 22:24:27 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:24:33 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 09 Jun 2026 22:24:34 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c790f81620f3588d543165b872d3245a8e97c748896384a2829d3a8e474e02`  
		Last Modified: Tue, 09 Jun 2026 22:24:45 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3393c73af178f47eddcb2f8872130438e274391b5a37482cd09cd26ab9ca11`  
		Last Modified: Tue, 09 Jun 2026 22:24:44 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219df33cee2125cd049ce4748d81058a3d50d0ec1042ee4e3d975f039a85a3e3`  
		Last Modified: Tue, 09 Jun 2026 22:24:44 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e7243b74367bb6b1fbfadaa08077fc3a760c7e75770384fb0d1cd975c069b85`  
		Last Modified: Tue, 09 Jun 2026 22:24:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a821d59c73f5f4c8d091a3541d0428653fdbb95e504584485bfecc28207a58`  
		Last Modified: Tue, 09 Jun 2026 22:24:43 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c807fe78d1e036dd8321f9d4facba832bef5f9a0a74e59ffd5f33144bfa5632`  
		Last Modified: Tue, 09 Jun 2026 22:24:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6776648a377dda785ac5c199447249c53f4eecabec716919199e6b888d09a3`  
		Last Modified: Tue, 09 Jun 2026 22:24:42 GMT  
		Size: 370.2 KB (370171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08a37578e5a6e116a1f31b83f485451bf64e13ce8c9678d9b6115c994f0397`  
		Last Modified: Tue, 09 Jun 2026 22:24:44 GMT  
		Size: 12.9 MB (12939744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1635376e694c911ed18f269c2b5ae10b62dc54d32fa8c5e496e66ce19e6b60c0`  
		Last Modified: Tue, 09 Jun 2026 22:24:41 GMT  
		Size: 378.4 KB (378375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92524975a890c0c03638ef385c4fbead6f9039b5c6c5148a231bd6b3bbad786f`  
		Last Modified: Tue, 09 Jun 2026 22:24:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a222b071f41c1250bb41ef880bb084004b52342ce3516919e6d468d28bd17b4`  
		Last Modified: Tue, 09 Jun 2026 22:24:41 GMT  
		Size: 4.4 MB (4404756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf2642ab311ef98ea3a3e56025b37e72d8194ebb4052ddadb25271e4c508e53`  
		Last Modified: Tue, 09 Jun 2026 22:24:40 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9cf1e8ca93b508a38268d2c2d5e82c86021176e134ee342c1e04569c6d2a85b`  
		Last Modified: Tue, 09 Jun 2026 22:24:42 GMT  
		Size: 10.8 MB (10848712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3479ae261295394aa5c6fa940a43e926c925e8c3d9a97aa01a576b51d7e7fc`  
		Last Modified: Tue, 09 Jun 2026 22:24:38 GMT  
		Size: 375.5 KB (375505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddbf2224c2ffec0a8c2c5f32c3de97d881122da9074d2a4d34f6914ff4b9a77`  
		Last Modified: Tue, 09 Jun 2026 22:24:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d376a841329f901fa3a5290e01f54f0ddf41eca4c9af73fc1f253a1e9f18be92`  
		Last Modified: Tue, 09 Jun 2026 22:24:38 GMT  
		Size: 380.0 KB (380030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6629b7be8b9fcc543edf075aac641b3051897848fb401e4ad45fa713b847b45e`  
		Last Modified: Tue, 09 Jun 2026 22:24:38 GMT  
		Size: 398.8 KB (398799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe308660145938a793bfb13f20df8cdd13bb1e07fb1b52ccc8eaa2a8886eb65`  
		Last Modified: Tue, 09 Jun 2026 22:24:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.5256; amd64

```console
$ docker pull haxe@sha256:293b08677907696729286a1e9325555caee5202c55fac6ce5d7c780fc8d45c77
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2162257471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140f00aefeb37fab69d892640144956d819dde7e503f53d92a9ac7cc87ac4fce`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:21:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Jun 2026 22:21:35 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 09 Jun 2026 22:21:35 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 09 Jun 2026 22:21:36 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 09 Jun 2026 22:21:37 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 09 Jun 2026 22:21:37 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 09 Jun 2026 22:21:43 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:22:04 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:22:10 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 09 Jun 2026 22:22:10 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 09 Jun 2026 22:22:23 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:22:24 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 09 Jun 2026 22:23:30 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 09 Jun 2026 22:23:37 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 09 Jun 2026 22:23:38 GMT
ENV HOMEDRIVE=C:
# Tue, 09 Jun 2026 22:23:43 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Jun 2026 22:23:51 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 09 Jun 2026 22:23:52 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42bd05c6eace9b3d2b7a54918556307d072055152009d32427e3187ac0f09af`  
		Last Modified: Tue, 09 Jun 2026 22:24:03 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3cb896763537303db0e364d3c801498fefba122b07e9518edf671c68f7dff5`  
		Last Modified: Tue, 09 Jun 2026 22:24:03 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df0d454e443c191da7be15a2e1559cc68fcf58650f8e5a269d10978ce0faa12`  
		Last Modified: Tue, 09 Jun 2026 22:24:02 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c74b191aaf017043681dabd8eb4eb41fe202cec5317cca79e715c690d16fb9`  
		Last Modified: Tue, 09 Jun 2026 22:24:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23bdf6c0a18c57dc165788da44894cd973c5fabe81d5aec723dec0215a1ea91`  
		Last Modified: Tue, 09 Jun 2026 22:24:01 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea4e625db774634f4ddae5c00b2ae2d71e1ee12c25c501d2eb338bb1a1f8ef0`  
		Last Modified: Tue, 09 Jun 2026 22:24:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427cf1d4794b9c690a90201326b68301099955980c0a350247523e0abd897ba3`  
		Last Modified: Tue, 09 Jun 2026 22:24:00 GMT  
		Size: 486.4 KB (486386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abc70efb414f83d35a933bff5f00b6a96e5ad6c5d1c58e891c14f9a05cf99cc`  
		Last Modified: Tue, 09 Jun 2026 22:24:01 GMT  
		Size: 12.9 MB (12922758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acba3616f5caa18fefb21a5dd6713a1020c013af822d749bd89418fc25882bd0`  
		Last Modified: Tue, 09 Jun 2026 22:23:59 GMT  
		Size: 368.3 KB (368260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fb074721704111030a419bcc45b25bd76a22405799e9e6d22c4a8e62ec3c56`  
		Last Modified: Tue, 09 Jun 2026 22:23:58 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6c1ecef0d159663cea1909df0614eb8d400945f773536c1a95fa0c09c6300a`  
		Last Modified: Tue, 09 Jun 2026 22:23:59 GMT  
		Size: 4.4 MB (4386844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1854f885b07f176b23b2a7fdb12a47b12a4719c07e8f19272c8944869d877a3f`  
		Last Modified: Tue, 09 Jun 2026 22:23:58 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc60aba09cc2745b99813f423ae0f0cd6595daba0aa908f91296f28a687657b8`  
		Last Modified: Tue, 09 Jun 2026 22:24:05 GMT  
		Size: 10.8 MB (10838367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb2555578a87bcbb3e74a28f19d46defd33720e649a240006906d5e87ecf85f`  
		Last Modified: Tue, 09 Jun 2026 22:23:57 GMT  
		Size: 357.8 KB (357764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd108cf6a363158a0584c4a29c9f9e50a16d9255654863a407b7fb5cb8ea2c2`  
		Last Modified: Tue, 09 Jun 2026 22:23:56 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7bb4bf476bc1dbc7679349752f0fc420d036bf29766569229e6bc6058b144c`  
		Last Modified: Tue, 09 Jun 2026 22:23:57 GMT  
		Size: 373.3 KB (373267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd5f86132707fb1dbdb1e38a6db5c97e15ceb8990758e6d26e6c9ac19a80b99`  
		Last Modified: Tue, 09 Jun 2026 22:23:57 GMT  
		Size: 385.2 KB (385237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbffce09e231f809ed32b091856873e90d18ca7b2198d2c85e4af6ef3821b95`  
		Last Modified: Tue, 09 Jun 2026 22:23:56 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
