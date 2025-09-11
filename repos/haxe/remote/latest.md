## `haxe:latest`

```console
$ docker pull haxe@sha256:2ce284d61cfcf5a4bc126147314ffb005df00794fbc865bfcf2de3b390863b49
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.6584; amd64
	-	windows version 10.0.20348.4171; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:194f1e14442069d15015ec334bd3dd66fd8d21c6481b1c93028b10d5ecad47fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398456689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f77777dcf35795e90cd0063770154d1d423b1bf9c176fa3e61083120fba393`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Jul 2025 00:36:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV NEKO_VERSION=2.4.1
# Sun, 20 Jul 2025 00:36:05 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV HAXE_VERSION=4.3.7
# Sun, 20 Jul 2025 00:36:05 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sun, 20 Jul 2025 00:36:05 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5073558d5a5274440fddfe987f56645dc90b8b84481e9e3dc858ac3311e33e`  
		Last Modified: Mon, 08 Sep 2025 22:13:51 GMT  
		Size: 64.4 MB (64396915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f576a536927dcb8708d26b5b34d0ec6fe4ac4d4d722a559f90f1d32820a9dff0`  
		Last Modified: Mon, 08 Sep 2025 22:38:30 GMT  
		Size: 1.3 MB (1261463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37519f5951faa333b1c7fa719d2483ced01f6f872d0c6a78a4e3a41e1fa5294b`  
		Last Modified: Mon, 08 Sep 2025 22:38:37 GMT  
		Size: 1.4 MB (1384593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3270682cc162fdf2c750722b98117b7904e957f19ecb2434ae70a02e52e37145`  
		Last Modified: Tue, 09 Sep 2025 00:25:15 GMT  
		Size: 258.9 MB (258907112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:3177813a4143709b4f603cbc225f9d172bdd1c1e5550c73caf5d0599756dbea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8206a19b4e60ed995f01d6ec093f5272e10cf9e13b3764b86f312d58df39d0`

```dockerfile
```

-	Layers:
	-	`sha256:7f5af677f8eda4d917d53dc572f06a496c340aecd4b251a10c3d8709b8f2ddbf`  
		Last Modified: Tue, 09 Sep 2025 00:24:19 GMT  
		Size: 19.2 KB (19194 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:ef1be359c3c5726bd8c8ce201584175fd954006bd5e8532e992cf4673803c6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361476583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6631b6842862164aa2899ceea4880887d8e8f6a13afa2ce47fa35f03173cdb58`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Jul 2025 00:36:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV NEKO_VERSION=2.4.1
# Sun, 20 Jul 2025 00:36:05 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV HAXE_VERSION=4.3.7
# Sun, 20 Jul 2025 00:36:05 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sun, 20 Jul 2025 00:36:05 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 23:37:54 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ad8fb006981127731180a5d548f700fd609cacd7e365cb66fbcaf2fd1e979c`  
		Last Modified: Tue, 09 Sep 2025 06:17:59 GMT  
		Size: 59.7 MB (59652826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31a573ebe528d0a909cb2bc3ba796941024b9af01cb79222543a690d4e4833c`  
		Last Modified: Tue, 09 Sep 2025 06:40:47 GMT  
		Size: 1.2 MB (1159523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754a59073b6237dfaf948138aefe51bda05a37faaf47b4704fe0868b24e4541f`  
		Last Modified: Tue, 09 Sep 2025 06:40:54 GMT  
		Size: 1.3 MB (1326729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be3b9b15e0b2d636f7deab0c961eea666aa0050ec110b3cfac83607ff481680`  
		Last Modified: Tue, 09 Sep 2025 07:35:08 GMT  
		Size: 233.2 MB (233210428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:e395f3a9d5bd1210605321276d59cdd7177dc85053f3b670b201d9536c26361b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9c4888b5c361729ff310004503eb267d83705c65dddefec1667d6bdb9c4e575`

```dockerfile
```

-	Layers:
	-	`sha256:071b649c1a3b7ba20be59a1fdeb05215797e366d849dc9e60f91fec7dde8c1ee`  
		Last Modified: Tue, 09 Sep 2025 09:24:20 GMT  
		Size: 19.3 KB (19308 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:8d2585974fd557580bdd08a30985eb0e3855856c4676f08db5548c7db5fdd181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.3 MB (401341396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8c895c42285fff6b0c71f282dc96030dcc522cf5a03c8533e8030fc690da8b`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 20 Jul 2025 00:36:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV NEKO_VERSION=2.4.1
# Sun, 20 Jul 2025 00:36:05 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
ENV HAXE_VERSION=4.3.7
# Sun, 20 Jul 2025 00:36:05 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Sun, 20 Jul 2025 00:36:05 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Sun, 20 Jul 2025 00:36:05 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133142790bc081eb3e5455996df5c3f98df543c5a224c3643437a19d4d6a7d93`  
		Last Modified: Tue, 09 Sep 2025 02:12:12 GMT  
		Size: 64.4 MB (64371181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b6d751914b4503ab43b912ad89d51aa62bfb7b30157a7a6cfb5e68786039f0`  
		Last Modified: Tue, 09 Sep 2025 02:59:57 GMT  
		Size: 1.3 MB (1257887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b712172e258bbba9d9fe0e25b4a95a943e70bf7e155e3a0f20d78e8035e14b9c`  
		Last Modified: Tue, 09 Sep 2025 02:59:56 GMT  
		Size: 1.4 MB (1419834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c234d11a3f892f0c947fa40384c26ee3000852839b7e475b4d42a8386185d20f`  
		Last Modified: Tue, 09 Sep 2025 03:24:39 GMT  
		Size: 262.3 MB (262338686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:1fd70b36f73651e9aa55927cb4e1500d0476dace4baa85db9d22dedcf83d4778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6516426bb3881eef3872de8305842efe4c13fdea2457b88a8ece2fcb293ce87c`

```dockerfile
```

-	Layers:
	-	`sha256:be06272da0e5df17d7239a70d4c7ba8ef909af657f73ee36ea70b3b5886d2697`  
		Last Modified: Tue, 09 Sep 2025 03:24:21 GMT  
		Size: 19.3 KB (19340 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.26100.6584; amd64

```console
$ docker pull haxe@sha256:cf9d9faaf28eec97e9fed94c106edfa2b893230ae421eb44542d4c60d89d4995
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3601383327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cad5f5842414d42ce160e225cd890fb8eb15b3a10586f4c32331ee7751d891`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Sep 2025 21:58:07 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 10 Sep 2025 21:58:07 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 10 Sep 2025 21:58:08 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 10 Sep 2025 21:58:08 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 10 Sep 2025 21:58:10 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 10 Sep 2025 21:58:16 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Sep 2025 21:58:34 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:58:39 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 10 Sep 2025 21:58:40 GMT
ENV NEKO_VERSION=2.4.1
# Wed, 10 Sep 2025 21:58:54 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:58:54 GMT
ENV HAXE_VERSION=4.3.7
# Wed, 10 Sep 2025 21:59:55 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 22:00:00 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 10 Sep 2025 22:00:01 GMT
ENV HOMEDRIVE=C:
# Wed, 10 Sep 2025 22:00:07 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Sep 2025 22:00:16 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 10 Sep 2025 22:00:17 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe65d833e07b77e91dac787141b255d3435c59c1ec3fb7582320d87ad55b8648`  
		Last Modified: Wed, 10 Sep 2025 22:00:43 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bf3e6654fa74c3b19ca49ad4c9e9ec0a58f9d7c08e53fb530dbc7b71d6e1d9`  
		Last Modified: Wed, 10 Sep 2025 22:00:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb848f47c72f3afe5d47fb3a9a38207bf69d89ecbf50d03877858ffeff298c5`  
		Last Modified: Wed, 10 Sep 2025 22:00:43 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fe63ffc1a7e355fba999cd24e910ee4f944720eae427dfc06bc48d4892c759`  
		Last Modified: Wed, 10 Sep 2025 22:00:44 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda4f9ca9de657aa48d80a3daa8ff18b77bc5b0baf11af2feae8ed31ca2e4e12`  
		Last Modified: Wed, 10 Sep 2025 22:00:44 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b1beb8e6380524c8cb70c6acac46c02b98cdca5bb96ab881c0095b55e02497`  
		Last Modified: Wed, 10 Sep 2025 22:00:44 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a97c36d6b2dd45c77a5cd17986889938ff9ef6ad3a57209bf86f9491f5a3b1f`  
		Last Modified: Wed, 10 Sep 2025 22:00:44 GMT  
		Size: 348.6 KB (348567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05368b8a5f20203e75224e951138800ed7a86ff4cfeb8f32612ca2db7eb9b232`  
		Last Modified: Wed, 10 Sep 2025 22:00:45 GMT  
		Size: 12.9 MB (12916807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8744faf50dceacf16163196d5031099e6420e97d1117e1de15b339ff22b7b41`  
		Last Modified: Wed, 10 Sep 2025 22:00:44 GMT  
		Size: 360.6 KB (360616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6703ca6279445c473b7d239332a5d5fb39a5b2dd39f341299287abd9af18d5e`  
		Last Modified: Wed, 10 Sep 2025 22:00:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9680abed3533ce70aa254e98afa679f4a7ffceecbba98e4e832d48655f45292e`  
		Last Modified: Wed, 10 Sep 2025 22:00:45 GMT  
		Size: 4.4 MB (4378954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dabaf68a9aa24051dd979760328466893129187747bd1ea075730bfb0747736`  
		Last Modified: Wed, 10 Sep 2025 22:00:45 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb43044aceaf59b30fbe8837d6dea707e2a2463e5cdcadb34675311704a6cdf`  
		Last Modified: Wed, 10 Sep 2025 22:00:51 GMT  
		Size: 10.8 MB (10830567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7206f57cad3aa9fa518ac8113c3b238b4ce12543c4142ed862ea8fe91c50e6f`  
		Last Modified: Wed, 10 Sep 2025 22:00:45 GMT  
		Size: 352.6 KB (352605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b200861145b8762f72c90994b286ac282291f8590fa2d4159c7d9dccd06e0ee6`  
		Last Modified: Wed, 10 Sep 2025 22:00:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3572fdd0fbc1a5eda4cca07f9b54a41893d0e930cec716c43f876886b48c5e15`  
		Last Modified: Wed, 10 Sep 2025 22:00:45 GMT  
		Size: 363.9 KB (363851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9977d3dafb27a34d3ae9a97b9b4e30bc23b3e26e7a61b5d54a2f2ab68f8b8369`  
		Last Modified: Wed, 10 Sep 2025 22:00:45 GMT  
		Size: 378.5 KB (378510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750ad691ea23ea9cc198abdd75ce521357c761a06d9e6f0b9c7002e8ae09c3b5`  
		Last Modified: Wed, 10 Sep 2025 22:00:45 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.4171; amd64

```console
$ docker pull haxe@sha256:e0076486ce8f3f170fef2c13dce0260936fce4d2fd1a9a56ce1c1c6f73687946
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312132920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363acb2c487f0ccb22edd44f0e5a75785673d75f167ef5a596406afe8ea42f63`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:55:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Sep 2025 21:55:29 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 10 Sep 2025 21:55:30 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 10 Sep 2025 21:55:31 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 10 Sep 2025 21:55:31 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 10 Sep 2025 21:55:32 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 10 Sep 2025 21:55:38 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Sep 2025 21:55:59 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:56:05 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 10 Sep 2025 21:56:05 GMT
ENV NEKO_VERSION=2.4.1
# Wed, 10 Sep 2025 21:56:19 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:56:19 GMT
ENV HAXE_VERSION=4.3.7
# Wed, 10 Sep 2025 21:57:32 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:57:38 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 10 Sep 2025 21:57:38 GMT
ENV HOMEDRIVE=C:
# Wed, 10 Sep 2025 21:57:44 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Sep 2025 21:57:52 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 10 Sep 2025 21:57:53 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2555b17f4c9e13734f1b3d4c9070c60cb3eb9dc8b8f732ab6d3c058c4d0916`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531654c030e897c97e600b7bab80bbae549be33b78a1cca321122898a5a607df`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211674d5f46d68fc6f9a8684e1d3b15a868795e317fc851dee6e3d811ecc22bd`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91daf0b0bc30f2a7e5ac118b6cd57fdc9f082253e6764c750eca92564d6f4b0`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ee6c23f43941bfca174a9e62a1dcae0772974edd11827ccc15d5655480ae11`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00c829f5815873db5afc6dd914e6f7e1c063c412c87b4dbdcf68655d83ca4f3`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926b2ae91350fd53b4a5fb7c5a6c34eab98480001d2b886ad833ff40fca3e596`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 348.2 KB (348187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ec5bd6217de28139597d0dbea95fdd27b2e5cf70508b987ce61ae915e873780`  
		Last Modified: Wed, 10 Sep 2025 21:58:38 GMT  
		Size: 12.9 MB (12921062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d0f778c378c6bd045b3960542ca28a9562227e6ffb185343a63da52cc9e288`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 366.6 KB (366578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919b24fdd216f4288bfdb5b63cf022b3e83a9ce67c2c25dc40a972ab5ea4c9d2`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b9a02ee105d213769b99079d5457c3e585dbbaed359f05e3bf11b21485e809`  
		Last Modified: Wed, 10 Sep 2025 21:58:33 GMT  
		Size: 4.4 MB (4384426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c48ab51a8b7c4b27515e4d38acbadfd873d446a51d1a496e8b7fa98b57dc78`  
		Last Modified: Wed, 10 Sep 2025 21:58:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa74c1c5681d4e388bf5f4f24093b8c81cad2cdce0959c95267e5c332f8a21cf`  
		Last Modified: Wed, 10 Sep 2025 21:58:33 GMT  
		Size: 10.8 MB (10835546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242e96bbbfbca5f4c81ec87029e0240cb749078cc832479bf806e0b5ba6f31bd`  
		Last Modified: Wed, 10 Sep 2025 21:58:33 GMT  
		Size: 361.2 KB (361167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f78c4dbc4afb205d67388c5bf73bffffb3ccde94212f1eb760132cbae039de`  
		Last Modified: Wed, 10 Sep 2025 21:58:33 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a3082280c466aa232c514a30d53f1e0d15189d02509de748b4c1dbfb0a8949f`  
		Last Modified: Wed, 10 Sep 2025 21:58:33 GMT  
		Size: 371.8 KB (371849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88d6834c9bae7ab7b1bb08d5bea568d0f1332f071dc578077923ca1b279340b`  
		Last Modified: Wed, 10 Sep 2025 21:58:33 GMT  
		Size: 386.0 KB (386005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6168c4aac6c1c732fb7b285174568a2bde254f692aca04199ac2ac596b7a1bc8`  
		Last Modified: Wed, 10 Sep 2025 21:58:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
