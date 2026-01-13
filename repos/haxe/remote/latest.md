## `haxe:latest`

```console
$ docker pull haxe@sha256:26b77a7393bbf6fc6ae74e6edf184b947ae51e510380c5a3273f11c2807c3d08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:690d8fdec72cfbb4afc2e9a6eb84c5dc1b4ca328e0a7197b3ee179f69d572110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398504704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8067d06ddde5149ba5d734cf576148248b01785022fe9cf7d0b58441a078284`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:51:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:51:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:51:19 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 13 Jan 2026 04:52:33 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 13 Jan 2026 04:52:33 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 13 Jan 2026 04:52:33 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 13 Jan 2026 04:55:47 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 13 Jan 2026 04:55:47 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:40 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64538a062a61add8dc8b290fa69475e8902eb839c497a5f5dcd5a950422e493c`  
		Last Modified: Tue, 13 Jan 2026 02:09:06 GMT  
		Size: 24.0 MB (24036867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1872fa12cc6b1145803f1a0679ca26cc65fa1b4e0ee389bfb30267594736b6`  
		Last Modified: Tue, 13 Jan 2026 03:53:38 GMT  
		Size: 64.4 MB (64395833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7074d1b091e75cfef6dac0934683af01ad333a1995b648e6ac3309a76eb326`  
		Last Modified: Tue, 13 Jan 2026 04:56:30 GMT  
		Size: 1.3 MB (1261556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a6fb64f75f88e57c662f4db2cb5f0d738ffdb31c094733400ea6a884bd7816`  
		Last Modified: Tue, 13 Jan 2026 04:56:30 GMT  
		Size: 1.4 MB (1385214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63394862fe380da984a5333c1876610eb86de420284fc6d7aa167403c61bf8ee`  
		Last Modified: Tue, 13 Jan 2026 05:18:18 GMT  
		Size: 258.9 MB (258943612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:05e937f6a111b4381a0570dae161e394a46b5390a5da47c895de7024c9da9129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dd4b59d78179a8dd7b4140bafe6346c266226656bc7652c6ea8894ae5c6ca06`

```dockerfile
```

-	Layers:
	-	`sha256:f4a74b6f7456a75d6bd126a02467b3bfd8e92c1b652dacbf27338534bfeaff4f`  
		Last Modified: Tue, 13 Jan 2026 07:25:38 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:9eee140e3023276856338ad59186b2fa041adce2f34de038df4be444a50677c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361525043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a98e7eb324d643565d2b3526bf08f5613f557088a166d6b23ba9fbf3c3b93375`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:57:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:25:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:25:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:25:38 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 13 Jan 2026 05:27:00 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 13 Jan 2026 05:27:00 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 13 Jan 2026 05:27:00 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 13 Jan 2026 05:31:08 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 13 Jan 2026 05:31:08 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:d1f8df344790c402ed8a818bba76e9111f5e212418c662cf0574919edf68933b`  
		Last Modified: Tue, 13 Jan 2026 00:42:15 GMT  
		Size: 44.2 MB (44198845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b61baedfd715aa7493fd2550daee1914be821a60dd0067158988236109172a`  
		Last Modified: Tue, 13 Jan 2026 02:57:25 GMT  
		Size: 21.9 MB (21941488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97f9f395cd1e9e02761196527b4253d5246be969781795c278996437891e5cf`  
		Last Modified: Tue, 13 Jan 2026 04:25:12 GMT  
		Size: 59.7 MB (59652006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4472c67329a5880827df65c26fa5c8d3b53f6fc39b11587197d00f89a4c1e`  
		Last Modified: Tue, 13 Jan 2026 05:31:46 GMT  
		Size: 1.2 MB (1159624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46238c01de3d02a1fdfefb2640e5f12fb736d0811fab5a35e07cb612a0f82a62`  
		Last Modified: Tue, 13 Jan 2026 05:31:46 GMT  
		Size: 1.3 MB (1326753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533dd3df2eba49f1be093e3d502216e906456c0ec52aa65950987ac6f51a2b30`  
		Last Modified: Tue, 13 Jan 2026 05:43:53 GMT  
		Size: 233.2 MB (233246327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:e2042d3cbe7748a84bc16ddeb8096e55aee48c65879b43bea0a48e0673ca891f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46565d0e6130fb12053c26f3eec9e3fbbbb4ca1ee6b4ae772cd250269ab4f3c4`

```dockerfile
```

-	Layers:
	-	`sha256:191d892eb027206a34c6304fa27cf11aab3d2d5a455370d408fcb8979af91bd9`  
		Last Modified: Tue, 13 Jan 2026 07:25:49 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:d6ed3a3205cc7a67c3ef1c1dcbe6b4df52f871093711e48f705652e0b7415ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 MB (401504916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdacc40a49ca57281bab2246166a77fe6384045a922bd89695f880ac414204d`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:12:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:53:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:53:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:53:18 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 13 Jan 2026 04:54:36 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 13 Jan 2026 04:54:36 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 13 Jan 2026 04:54:36 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 13 Jan 2026 04:58:29 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 13 Jan 2026 04:58:29 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:34 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72c713ab317dd7f302a6ff5a345af5b61cddc864fca2d96a23e6ef3c90a6657`  
		Last Modified: Tue, 13 Jan 2026 02:12:51 GMT  
		Size: 23.6 MB (23604814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ad46596f06c934001fa6d7bea3d1508b0bb616cffb71004efd5bada56884f`  
		Last Modified: Tue, 13 Jan 2026 03:57:17 GMT  
		Size: 64.5 MB (64479462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a4ff7f8bf5d6147655fe12fb18a3f58d93ca0063d01060fd94a7227a09fae5`  
		Last Modified: Tue, 13 Jan 2026 04:59:23 GMT  
		Size: 1.3 MB (1257968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512a289d9de3b6985f7629a69b8ccece6a147d11cfb962d5e6fbfdf9c691fe72`  
		Last Modified: Tue, 13 Jan 2026 04:59:23 GMT  
		Size: 1.4 MB (1419969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1ac6ac457d6866c3b6b84163e417f1753893f29b47ee3dbe5be834e19f6e1b`  
		Last Modified: Tue, 13 Jan 2026 05:20:33 GMT  
		Size: 262.4 MB (262376631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:5f5ad56e3690cde398848dfcd5841dedff360891f0861d1b0a530789fc6e7bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0685cf7322e5bac34ee74b02067dd2eb53a735fc9d8c7b50c60722df02706b99`

```dockerfile
```

-	Layers:
	-	`sha256:b83fcb2c2367f3fa248bcaaa68cd1b1e4e1e4ef2a5ebd6ae14d9dae3c95149db`  
		Last Modified: Tue, 13 Jan 2026 07:25:52 GMT  
		Size: 19.3 KB (19296 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.26100.7462; amd64

```console
$ docker pull haxe@sha256:2b4ddf8b6f544f528be2fc0e3b4ef79a5f0230377f6da268668af0b5d0918fd7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3283075198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5828e6cae401751e562c0d5eb767c206348ae0fe167e14ec22ffce363fb39ae5`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:45:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Dec 2025 20:45:29 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 09 Dec 2025 20:45:30 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 09 Dec 2025 20:45:30 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 09 Dec 2025 20:45:31 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 09 Dec 2025 20:45:31 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 09 Dec 2025 20:45:37 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:45:56 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:46:01 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 09 Dec 2025 20:46:02 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 09 Dec 2025 20:46:13 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:46:13 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 09 Dec 2025 20:47:12 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:47:17 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 09 Dec 2025 20:47:18 GMT
ENV HOMEDRIVE=C:
# Tue, 09 Dec 2025 20:47:23 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:47:30 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 09 Dec 2025 20:47:31 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4f2ca1b9916ca2d785a6620325dd15f7b9f948e93c575808339b9e12d20ca9`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bd03e17ac40e0bc98ab1b8f45c5794f9aa80fd9471a00e0700ffac4e212a92`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c546c807b76743ef282667efb70ed48318b7be5733fc4975655ff559b7642daf`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63674ee5430e07a18e54679fd6fc84dd0f9317a6fc16746fdd24de05ea961bb2`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93c2fd916509a690097702cdb2d66146e93d3bb78b756a1f0af826fd4434daf`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3cc0022cb6bd32034381131a584a4a17dfe38b737374db2029aa7502825f88`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f916e236077ced2b4e19792d05f66e125871a911b9c4261c6c3206077ecd1dd7`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 360.7 KB (360654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01468d8ddda5459b3c512fb5134aec6e55987a659b53b49d47d8fa1ac93c31df`  
		Last Modified: Tue, 09 Dec 2025 20:47:52 GMT  
		Size: 12.9 MB (12936043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f9eede1f1eabf941527cbd9fb5463679be499f312e1050b4b3276ac7566af9`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 356.9 KB (356930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242061efc60890469bb0c7a9030b8266fec1f81623b60dc3372b9b455801d0e8`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a2f0a74b33d65f500781e13bf4df4de8e00cac6da366f7d66768018b9b0c62`  
		Last Modified: Tue, 09 Dec 2025 20:47:50 GMT  
		Size: 4.4 MB (4378798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d0c065bda4a66c4bb8ef165d5a514a522f7d792e863d6f04199515745569d`  
		Last Modified: Tue, 09 Dec 2025 20:47:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d83455beb2b557f922456116dc726b8d71af706aad87d5710eebe5192450a66`  
		Last Modified: Tue, 09 Dec 2025 20:47:52 GMT  
		Size: 10.8 MB (10815367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48265fa17542f70cffbeb235b43e6136a9d7d53ebe76be0daabc32b0f5fbe895`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 354.4 KB (354364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c85df76168ec501525adcea02070b3b471b389313526cf3d94a05ce8df613d5`  
		Last Modified: Tue, 09 Dec 2025 20:47:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997cf05bbf3c893f040af5949af10ff5986d3c11f1a870db0507c7481b9049`  
		Last Modified: Tue, 09 Dec 2025 20:47:50 GMT  
		Size: 359.3 KB (359331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf54a2847fe546aa3a0820b1375b1cd7563fe12e37e424283e58906ad52edc4d`  
		Last Modified: Tue, 09 Dec 2025 20:47:49 GMT  
		Size: 380.1 KB (380101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cdd4ac1c4cbf230f3759716210dcb27237e29f6aad72b768d1ded56085c83a`  
		Last Modified: Tue, 09 Dec 2025 20:47:50 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.4529; amd64

```console
$ docker pull haxe@sha256:10832f12e7320a10ba5f05f1ae39e5ef70c5dde4e545c69cf203f2a0d100978d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1809994213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38888cfbb17f130ac227cf51d9bee3820e451126adaeadba2917d6b11d669bd0`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:33:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Dec 2025 20:42:10 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 09 Dec 2025 20:42:10 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 09 Dec 2025 20:42:11 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 09 Dec 2025 20:42:12 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 09 Dec 2025 20:42:12 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 09 Dec 2025 20:42:19 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:42:39 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:42:44 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 09 Dec 2025 20:42:45 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 09 Dec 2025 20:42:58 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:42:58 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 09 Dec 2025 20:44:05 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 09 Dec 2025 20:44:11 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 09 Dec 2025 20:44:12 GMT
ENV HOMEDRIVE=C:
# Tue, 09 Dec 2025 20:44:18 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 09 Dec 2025 20:44:28 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 09 Dec 2025 20:44:29 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424524764b8b3c28e8f0b395d779fd82236cff87c19d66250bad79f45ae70277`  
		Last Modified: Tue, 09 Dec 2025 20:40:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8899a252a6b56ce86e806a7058191dc03fb4f9a1d673a5b7c781c331da3783d7`  
		Last Modified: Tue, 09 Dec 2025 20:44:45 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6612d7528444597d97a83dc927559fdcfb383bf20bfc3dd23eaad2aa9a5272f`  
		Last Modified: Tue, 09 Dec 2025 20:44:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6fa2def8db1ac2cff1af2b46705ee3ec5ec46f7753be926b62fdefe141ab6c7`  
		Last Modified: Tue, 09 Dec 2025 20:44:45 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a22791ad666e4c2354bf0c8e9fb9ae78178ebeea2b93b56080616b24a2e2ab0`  
		Last Modified: Tue, 09 Dec 2025 20:44:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1007d36b2386f5f25f512efc0e7b66181798b5e22d03905b2310724f856a5b`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a26ba3725b87da2cf6f242f2e539f47b594ae8ea8151ecf2f68249a4a0aa85`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 481.5 KB (481458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d1a5735d3ac0346c3b7f08c34cbac869435d23b2401d95fb963844cd9410da`  
		Last Modified: Tue, 09 Dec 2025 20:44:48 GMT  
		Size: 12.9 MB (12920353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b073e6a775a4336f749146d0eb7a9b79fda7497b0e7e0aaf725b95eaa0482342`  
		Last Modified: Tue, 09 Dec 2025 20:44:48 GMT  
		Size: 366.1 KB (366111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f2e711e8f05253d9906dcb8cb7dfe2d4b5c065aa0067fb66f8b5c2a338f1d`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb736f4c25abce9a6ba82d745f8cf29ef79f89b31466457e3974d8de76dae7f`  
		Last Modified: Tue, 09 Dec 2025 20:44:47 GMT  
		Size: 4.4 MB (4383630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d23ec82f0f5256b8311e06708c35cdc669dc4283bd9b286116afdd910b862b`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce50ab572140d68bc646843fcd45574e456f9956598ae8c808002c909ae72fc1`  
		Last Modified: Tue, 09 Dec 2025 20:44:47 GMT  
		Size: 10.8 MB (10833511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bb1c5b5501ff8817d3c98ef68df35b18e58af74d36b8ef5298a3454f9ba33a`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 360.6 KB (360617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2c82ec3965f249a46feba23a5f1667d56203c147bd0fcdf8c36f668a9ac040`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2b8d15853f1abc8c73a5ac8eb80ee63a871ea078861c6cd4a45c759c4152e5`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 371.3 KB (371287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d85899784c0560dabbfb0a0dff3fadd61706bbc2a1922cd03dd49867dddfb9`  
		Last Modified: Tue, 09 Dec 2025 20:44:47 GMT  
		Size: 384.9 KB (384886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4f41a67b031060369e73b39904a9788f1047b6cb7561398579cc5b164ecce12`  
		Last Modified: Tue, 09 Dec 2025 20:44:47 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
