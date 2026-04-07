## `haxe:latest`

```console
$ docker pull haxe@sha256:402254d18593c0bdf28045466df0d816c72b97722c0bf5e3bee221aa4c357a51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:e3643d5bbe7a9198217117c552d6279c71ce840593f1ba1e1b4ac7ef272b5746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398539911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af24b57901fda2a556e6a893026d6e915ec357666ea244e9adfac1cae2f57a6`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:42:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:24:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:24:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:24:06 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 07 Apr 2026 03:25:28 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 07 Apr 2026 03:25:28 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 07 Apr 2026 03:25:28 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 07 Apr 2026 03:29:11 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 07 Apr 2026 03:29:11 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de73ef470b7b271fede6f98a4c8376971bd059ce04ebc13b9f86e34e534b89ae`  
		Last Modified: Tue, 07 Apr 2026 02:43:01 GMT  
		Size: 64.4 MB (64396012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b770f830fd2045a586c5236439b7c6f3008cd9f1157b5ddf2cb68e122e3d93a`  
		Last Modified: Tue, 07 Apr 2026 03:29:43 GMT  
		Size: 1.3 MB (1261584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35f84cdc5cdd2e1f61dfb1ba5101a9b00ffd4174d966385d9f7d4b27ae4801d`  
		Last Modified: Tue, 07 Apr 2026 03:29:43 GMT  
		Size: 1.4 MB (1385249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c35a707c0849a9a3c131c97d8c3002e1dc44642d4430489d47abdf781e6a46`  
		Last Modified: Tue, 07 Apr 2026 03:29:48 GMT  
		Size: 259.0 MB (258969974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:726f38792583a8a28914bdfe15fbaca3e80a201ff70fe54b0c417fffceb06c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b707edef55148899c464c41057e88b5ec5c3e0c56727a7876e827290bd871c`

```dockerfile
```

-	Layers:
	-	`sha256:12e7e5ea0ee3f8a0183412788c9aec0f53cb0acf4bcd6b0479eb8ed52f539b2f`  
		Last Modified: Tue, 07 Apr 2026 03:29:43 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:5f7853b2a638ee05a53501ba87199ab08b6c4c28159d1c43b5e0c1d24d6da715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.6 MB (361563466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21da0c2fde3f20073f445695e2b4c387e7fe99edc9026473709483f4a549ba`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:49:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:29:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:29:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:29:38 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 07 Apr 2026 04:31:01 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 07 Apr 2026 04:31:01 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 07 Apr 2026 04:31:01 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 07 Apr 2026 04:35:14 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 07 Apr 2026 04:35:14 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626437a99246a6d3dc330350016eb9ecbf357123cec9028fd988893fdf863224`  
		Last Modified: Tue, 07 Apr 2026 03:49:22 GMT  
		Size: 59.7 MB (59651814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6636cd53b4c81586cae5bb196b1f0223b60302aa0a3a837fb549746895d903`  
		Last Modified: Tue, 07 Apr 2026 04:35:44 GMT  
		Size: 1.2 MB (1159592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdb011cbeb9fd1d4bc1c11fddd24c3e49fe73de0b5c01846765678e5e6543e0`  
		Last Modified: Tue, 07 Apr 2026 04:35:44 GMT  
		Size: 1.3 MB (1326820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0585c0408530ad8cf4548d37166e8ad98f2c09ccfdeeb0aea9cc28bb31089d08`  
		Last Modified: Tue, 07 Apr 2026 04:35:49 GMT  
		Size: 233.3 MB (233275340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:aaa0e5b75a445c034d8b2fc0ffaa8793de5ce3949b3b42f4c8f1e0a0e6b84180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d56f2ece1e865bd0373b69c46c926f75783e3921079933ba6de7c5ede9b5e1`

```dockerfile
```

-	Layers:
	-	`sha256:9d6485c8ab34cd89973e11aa8f72dd41804f7843d31c3529982ea50d6072e3b7`  
		Last Modified: Tue, 07 Apr 2026 04:35:44 GMT  
		Size: 19.3 KB (19264 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:0bd19027bb74f9b0489f95cb6cbc0561d6d6e9ede4be6abf7232f71d4cc7f504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 MB (401535781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a487bb78854fa73b3dcbfa20c96deda583a6668855157c36ad00a02a8be97a6d`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:52:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:35:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:35:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:35:55 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 07 Apr 2026 03:37:14 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 07 Apr 2026 03:37:14 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 07 Apr 2026 03:37:14 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 07 Apr 2026 03:41:10 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 07 Apr 2026 03:41:10 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b913dee6e116304b9bb2391ef8aedbb1f5ee16d167338920c7609a48bdd772`  
		Last Modified: Tue, 07 Apr 2026 02:53:06 GMT  
		Size: 64.5 MB (64479508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb44c01090a830891333b858cb572263665b32a1a046e799c5b499ca48cfeef`  
		Last Modified: Tue, 07 Apr 2026 03:41:46 GMT  
		Size: 1.3 MB (1258047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c131131fd901b1e884e2cc8dc29e7f8aa475aec7b4cb207907c030f2874a4868`  
		Last Modified: Tue, 07 Apr 2026 03:41:46 GMT  
		Size: 1.4 MB (1420020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:807503ae7e3d38ebaef4b9ffb1914a7c56a5a179c38203be51bc50fa17fca725`  
		Last Modified: Tue, 07 Apr 2026 03:41:51 GMT  
		Size: 262.4 MB (262400239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:e93b4d50345530d6d88255df8feaa88d0d8ac7ebc71cb78bd04a8d9d9b2b163e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff19355f22c67d4cbfb89258927f5d23df18aff4cb55828c487eb8726bc84cd`

```dockerfile
```

-	Layers:
	-	`sha256:1977739550032c94066fad36f571b98e256fa94567938ebdf1252e33ad1a0c0c`  
		Last Modified: Tue, 07 Apr 2026 03:41:46 GMT  
		Size: 19.3 KB (19297 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.26100.32522; amd64

```console
$ docker pull haxe@sha256:b03889a0ee3f957a11747a63e807c607b0498fcb7d19c479bff5aca9de509b08
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111444970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b157a40c8efca31c86c0f41d9fddeaca161df41122b254614cfec1aa24e5f89`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 22:05:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:05:49 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 10 Mar 2026 22:05:49 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 10 Mar 2026 22:05:50 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 10 Mar 2026 22:05:51 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 10 Mar 2026 22:05:52 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 10 Mar 2026 22:05:58 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 22:06:18 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:06:23 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 10 Mar 2026 22:06:24 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 10 Mar 2026 22:06:36 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:06:36 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 10 Mar 2026 22:07:38 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:07:44 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 10 Mar 2026 22:07:45 GMT
ENV HOMEDRIVE=C:
# Tue, 10 Mar 2026 22:07:50 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 22:07:57 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 10 Mar 2026 22:07:57 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23ac2fb6021a21901ae5b830e0757b4be97b3d345b8b93264f904926ae97421`  
		Last Modified: Tue, 10 Mar 2026 22:08:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf33a96b1d5385f55063638f881c55776de65131082df8df438e3d96ba251cf`  
		Last Modified: Tue, 10 Mar 2026 22:08:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272fc814b75abe2c455c78e5f0e38940e7bddd0d31b7b3be85abcf3583d98357`  
		Last Modified: Tue, 10 Mar 2026 22:08:07 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef37be8ce59023202eb97b7286c13959fb38a46987820f1d1e3a2fa432dc8f`  
		Last Modified: Tue, 10 Mar 2026 22:08:07 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce28c2fb3d2817d4cb0d34f6d4a6a0a8b0e130cb3b1873e76311d74b16d9b98`  
		Last Modified: Tue, 10 Mar 2026 22:08:06 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2254406b8a1c91709ef15dc326ca60181816be03ab02767ed50723b19798fd22`  
		Last Modified: Tue, 10 Mar 2026 22:08:05 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235d8c8da3ab29bf5a50aa6e826246d39a9807d7c60aa903b9f5decb3b5760a6`  
		Last Modified: Tue, 10 Mar 2026 22:08:05 GMT  
		Size: 371.9 KB (371927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0756d70b2d6feab5f8b7d0dce9c5568cbbc999e85d75eb1bdfb70431fcf893b5`  
		Last Modified: Tue, 10 Mar 2026 22:08:07 GMT  
		Size: 13.1 MB (13079136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306d8a9ab96e38f3b99a0427fa453927b7e1ea0a69500233d7d8e63a505c7c73`  
		Last Modified: Tue, 10 Mar 2026 22:08:04 GMT  
		Size: 379.8 KB (379822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d46992e4c34e742061ac0984cf22efd1e3ae891587ac7156e40eb42876bd283`  
		Last Modified: Tue, 10 Mar 2026 22:08:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42717d86b30b88aa29fd2df5fbe46a2b5eb33f245354568b9fd39fcc4a129a96`  
		Last Modified: Tue, 10 Mar 2026 22:08:04 GMT  
		Size: 4.4 MB (4406364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6520498a15b438364cc0b27cb0f47af45f95a987888e388b75924fac23da0a13`  
		Last Modified: Tue, 10 Mar 2026 22:08:03 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298389d2961e6fa284d7862584faca40891a6d46e0bfd82626f613c95b514cd8`  
		Last Modified: Tue, 10 Mar 2026 22:08:06 GMT  
		Size: 10.8 MB (10849720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7cfcb1c4c6af51698cf50d4a826cb13eb84199781e43322e916ee212776823`  
		Last Modified: Tue, 10 Mar 2026 22:08:02 GMT  
		Size: 374.4 KB (374398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10c4b5817dac50b23cc2c24c5c1106d8745a449a2b93718f92dbc887555d1d2`  
		Last Modified: Tue, 10 Mar 2026 22:08:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4828aade46b2bfe5492bc3e05529d7041d29b1a81553e06bd6b68eb9802b21d`  
		Last Modified: Tue, 10 Mar 2026 22:08:02 GMT  
		Size: 379.1 KB (379101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2980b7c56ea6c2846cf4c929ddf5d4e27342ccb00426f9b7d3e5dd3991da0ec`  
		Last Modified: Tue, 10 Mar 2026 22:08:02 GMT  
		Size: 395.4 KB (395362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd8080501a89f276e74276634a5780534838df1b0484aade2e5d0e8abdd1a9b`  
		Last Modified: Tue, 10 Mar 2026 22:08:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.4893; amd64

```console
$ docker pull haxe@sha256:1cb7fb5f44743d2b34756213ebc372ffc30fb5b41b9ecd8fe0b7d7c4944dcf0d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2012427926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad1726dc14c3eb40135766e583777e9ce244e88f78988aca6c1ba30c6b5b755`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 22:08:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:08:34 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 10 Mar 2026 22:08:35 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 10 Mar 2026 22:08:36 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 10 Mar 2026 22:08:36 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 10 Mar 2026 22:08:38 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 10 Mar 2026 22:08:45 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 22:09:03 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:09:09 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 10 Mar 2026 22:09:10 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 10 Mar 2026 22:09:23 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:09:24 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 10 Mar 2026 22:10:32 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:10:38 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 10 Mar 2026 22:10:38 GMT
ENV HOMEDRIVE=C:
# Tue, 10 Mar 2026 22:10:44 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 22:10:51 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 10 Mar 2026 22:10:51 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7844febc2b3fc230db18cb213fc8393b6e366b0df81fa90676409b67dd0c203`  
		Last Modified: Tue, 10 Mar 2026 22:11:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021886ee07be7d7264d554df26527c3243f88ec3f9a846f05517aa2ccf85ab0a`  
		Last Modified: Tue, 10 Mar 2026 22:11:01 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f265cf81f650b00f71e35efe075fbd617b5f66b0c7a1ed79e50f61b9ffa6b5ec`  
		Last Modified: Tue, 10 Mar 2026 22:11:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa82d2b656d4125a5950227ba7bd9d8b7f6019f50504d1236e3f614d8586db7f`  
		Last Modified: Tue, 10 Mar 2026 22:11:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97816e33ab15c2703e75f769e5218390184dfd1f6bb92e8fdb933acf8515148`  
		Last Modified: Tue, 10 Mar 2026 22:11:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7328eb241c57b1906a48fb40f5a716049b6e5898099a2a6f7c0834f02f407794`  
		Last Modified: Tue, 10 Mar 2026 22:10:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7387c5eb71c87c8bd196f79e9fae52df7f2913a7b53bfff3eace47ac0ddd53`  
		Last Modified: Tue, 10 Mar 2026 22:10:59 GMT  
		Size: 489.3 KB (489329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af265b853bff8a3fd374c93a691bc145c78451b7fab36e809a05341dd23a0ccc`  
		Last Modified: Tue, 10 Mar 2026 22:11:00 GMT  
		Size: 12.9 MB (12923739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2850dff9bca9067d5258e6c06552a809ba3cc1c5177a100c690cf8d77a717bf7`  
		Last Modified: Tue, 10 Mar 2026 22:10:57 GMT  
		Size: 368.8 KB (368780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772f42058510f4e512eed660f02fbaff7f1fa35af5e017fc141efeb81319d4bf`  
		Last Modified: Tue, 10 Mar 2026 22:10:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c1f24a8f4bca5c75bffad135d5eb673814c1adebf00a1d27ebfd0b8db3f23a`  
		Last Modified: Tue, 10 Mar 2026 22:10:58 GMT  
		Size: 4.4 MB (4387276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34dd1fa6797ba341fd21618bc3705d71ef1584aaabddee9fcf2da771d9f7a605`  
		Last Modified: Tue, 10 Mar 2026 22:10:57 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148029e59807a16b56999c4598e734dfbe28888d2d9ac9c7b376f884e9b1c312`  
		Last Modified: Tue, 10 Mar 2026 22:11:00 GMT  
		Size: 10.8 MB (10839131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21f926e66f8fb02efedd8bc2678c8efac4c639194ad7801f75383f5fe3a63d4`  
		Last Modified: Tue, 10 Mar 2026 22:10:56 GMT  
		Size: 364.5 KB (364542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75efc1e72561cb5f396361bdb38e80dd40c567faeabec694004137c053c45e52`  
		Last Modified: Tue, 10 Mar 2026 22:10:55 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173745c4d0aca80fc2a70906fffeef9b171beb76a9fa1b7aa7a75da6ee1a1d56`  
		Last Modified: Tue, 10 Mar 2026 22:10:56 GMT  
		Size: 374.7 KB (374736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82265afcae0c1feabd3e5517c17cbaf76d01862dff1a0fee33497ab32612f30f`  
		Last Modified: Tue, 10 Mar 2026 22:10:55 GMT  
		Size: 385.9 KB (385912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf5c0d7359c1497e1dc56faf0c1807f0cef99a58ba4038703e9963989f52acb`  
		Last Modified: Tue, 10 Mar 2026 22:10:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
