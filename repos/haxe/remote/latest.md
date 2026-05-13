## `haxe:latest`

```console
$ docker pull haxe@sha256:2e369bb5e29ef08b7088d7cdc2523db8136a3e32fe141be38f16cde9970e9400
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:96edec9c2936f5e8d45ce9be8be106283c0b5da0af463ca14fa8778f2d4f911c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.6 MB (398573597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc47aa12d4bf99c8fb63ca1760cd8ef23b514597eac6300662be45141a4fde3b`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:17:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:47 GMT
ENV NEKO_VERSION=2.4.1
# Fri, 08 May 2026 21:19:01 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Fri, 08 May 2026 21:19:01 GMT
ENV HAXE_VERSION=4.3.7
# Fri, 08 May 2026 21:19:01 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Fri, 08 May 2026 21:22:12 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Fri, 08 May 2026 21:22:12 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0eaa638f8e62fae795eecb031faffb0f41028e3e1db020a0e4536f6a095c98`  
		Last Modified: Fri, 08 May 2026 21:22:42 GMT  
		Size: 1.3 MB (1261582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0720e793ed453c34df169bc77ed7fa00a0d565bb5f65f8df0bfb0c782450ac7c`  
		Last Modified: Fri, 08 May 2026 21:22:43 GMT  
		Size: 1.4 MB (1385195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c37adf6fd8ff6bf8013343ff8a0a6705e23699ce0b005bc0891e01675e95a34`  
		Last Modified: Fri, 08 May 2026 21:22:48 GMT  
		Size: 259.0 MB (258998928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:51e6a74318411aa01749a9b6760506cf79cdbb8f4e8fcbfadb9ce56e89ece0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba7dfba1f70fd88b2e4a96e3112b1c831049ba2db550c49598be1e550000dde`

```dockerfile
```

-	Layers:
	-	`sha256:2966529e488c10543b73a368a251453d8d97137fcd1294f49b243bd1976f43b5`  
		Last Modified: Fri, 08 May 2026 21:22:42 GMT  
		Size: 19.2 KB (19151 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:887cf1cf9405c7a4bf083989b42b9d418c13ddffaf8758b7c8b0517eb4be7b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.6 MB (361599631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0483aeb6560827d1015e32bd0dce7032ac7878b3654a7164261a52b8add25e54`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:13:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:13:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:13:59 GMT
ENV NEKO_VERSION=2.4.1
# Fri, 08 May 2026 22:15:19 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Fri, 08 May 2026 22:15:19 GMT
ENV HAXE_VERSION=4.3.7
# Fri, 08 May 2026 22:15:19 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Fri, 08 May 2026 22:19:19 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Fri, 08 May 2026 22:19:19 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef2e4eed112ac2d8730e2603fe97cab1d0ce708d52061992fd2f72e1db7e12`  
		Last Modified: Fri, 08 May 2026 21:35:07 GMT  
		Size: 59.7 MB (59653543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2d98e16f73acac3eb5e4893d22ea25f3c55e8e8cd5699ec990d85485e908f0`  
		Last Modified: Fri, 08 May 2026 22:19:46 GMT  
		Size: 1.2 MB (1159598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc80ab06da2e0660bc6f67ed2e92faa79c4ae5365658ac9f5fdb5e08e7dfeb4`  
		Last Modified: Fri, 08 May 2026 22:19:46 GMT  
		Size: 1.3 MB (1326816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dd0dc54e5ac78d91c936b533dbb84ada9d9c79bbe259e2cf5e78f4a71c0d85`  
		Last Modified: Fri, 08 May 2026 22:19:51 GMT  
		Size: 233.3 MB (233305586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:16f460c61aac5869ea7d3c2283aeae1a701c6b2bd87954bafe1d15c03a57cba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5cbc0b046ca756a8357af1aaa2d97bf62b5f143fcbb48a25e1f08484227d62`

```dockerfile
```

-	Layers:
	-	`sha256:35c4fc74ff521fd536b584a9a7d13676694d9d2475e4bc95ae7dd2251f69efb8`  
		Last Modified: Fri, 08 May 2026 22:19:46 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:bf127272de8a7afa2c5731e6894786f9f75b6cf7893c602478aec8bf3c894fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 MB (401570578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cfa73c8caf1ad9daf64d368a3613b3a351e2055fb88aebabc4e4b10cec68c53`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 21:17:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:17:37 GMT
ENV NEKO_VERSION=2.4.1
# Fri, 08 May 2026 21:18:49 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Fri, 08 May 2026 21:18:49 GMT
ENV HAXE_VERSION=4.3.7
# Fri, 08 May 2026 21:18:49 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Fri, 08 May 2026 21:22:18 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Fri, 08 May 2026 21:22:18 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c74ff4a440e66b105a4d4e7eb4a8d3fd7fdfd41ef1e53f7f537ab827254adc0`  
		Last Modified: Fri, 08 May 2026 21:22:54 GMT  
		Size: 1.3 MB (1257970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df946e1b67910bb75740bfabb5af8ab647ab16b46d063455828b801307f256`  
		Last Modified: Fri, 08 May 2026 21:22:54 GMT  
		Size: 1.4 MB (1419864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3331a383139c34ac30b850f60578b9ee42da732a8198bc8c85b2a693d1752ff`  
		Last Modified: Fri, 08 May 2026 21:23:00 GMT  
		Size: 262.4 MB (262430496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:1d803c3f520698030037ddd3e693fe72c1ae1004ff15393e2b030a370f34660e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdfd4e821aa073aa514a1dcd933f0cf2eec4c6b694c01abf743832529f63c9a8`

```dockerfile
```

-	Layers:
	-	`sha256:a21f6f74061c87ae8a8ada0ab68b9578a33a17bc83c6d24f35f84276d808c8f6`  
		Last Modified: Fri, 08 May 2026 21:22:54 GMT  
		Size: 19.3 KB (19297 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.26100.32860; amd64

```console
$ docker pull haxe@sha256:f7d0e50dffc9485bde9e05dca9b3cb022e01fe236afe9ec3221120e6db4e2424
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2236155577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92f1b53f71c82af4fa601091e72600c33c4471ed005d38e5b5447d038c5801e`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:47:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:47:22 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 12 May 2026 23:47:22 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 12 May 2026 23:47:23 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 12 May 2026 23:47:24 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 12 May 2026 23:47:24 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 12 May 2026 23:47:32 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 May 2026 23:47:52 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:47:58 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 12 May 2026 23:47:58 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 12 May 2026 23:48:11 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:48:12 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 12 May 2026 23:49:14 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:49:20 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 12 May 2026 23:49:21 GMT
ENV HOMEDRIVE=C:
# Tue, 12 May 2026 23:49:26 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 May 2026 23:49:33 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 12 May 2026 23:49:34 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c01c6e65eb3561acb41a0f9f67620de06599757c161048a9b26eaeca542921d`  
		Last Modified: Tue, 12 May 2026 23:49:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da7aa30624ad077b027ef195ab5efcb48d2f641e23445f413752c17896035fb`  
		Last Modified: Tue, 12 May 2026 23:49:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191eca7f7c4618257ffe46f3979fb2ab0a50e652968b4904d804e131aa485a96`  
		Last Modified: Tue, 12 May 2026 23:49:44 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14ad2bb6baec653900c4000901322a6cdbf8132fcd240f67063a62c7103ecbc`  
		Last Modified: Tue, 12 May 2026 23:49:44 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc963b74c63ee19db4c78bc72b83cf6566ea478cdc67152bccf27222a86353ac`  
		Last Modified: Tue, 12 May 2026 23:49:43 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be066d29a278e94487700ceaf77179eca8be990003439dc74ea5b0f2a12a485`  
		Last Modified: Tue, 12 May 2026 23:49:42 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f12463c8d51670df877e60b20ead3681dcd67b25dbab5858f1727ac65bc2553`  
		Last Modified: Tue, 12 May 2026 23:49:42 GMT  
		Size: 391.3 KB (391316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a668bc378dc644127fd866a7380fa860b6a52f33e16fcf8d4ef574fbd1946c20`  
		Last Modified: Tue, 12 May 2026 23:49:44 GMT  
		Size: 13.0 MB (12953285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0038c49b3a4904edf3ee7feb8db1f88d03a586dc9e63106baa580443a3d3d069`  
		Last Modified: Tue, 12 May 2026 23:49:41 GMT  
		Size: 392.4 KB (392356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea0e2364a8b7243f2ef4ed13eff16f1e7ef309ad870dcd039e837adf5ddad37`  
		Last Modified: Tue, 12 May 2026 23:49:40 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b773eb7f37afa76de354d9b7bf4335913900b65c198c8c85c6e935374f7d55`  
		Last Modified: Tue, 12 May 2026 23:49:41 GMT  
		Size: 4.4 MB (4416379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c964a49023acafde4edfa985cb00558b0e470ca5369521a532b26b96b5e0c5d`  
		Last Modified: Tue, 12 May 2026 23:49:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8723f1f090630e0d553409960702467b1e01168e3eb8f186a0fbb99010c17b94`  
		Last Modified: Tue, 12 May 2026 23:49:47 GMT  
		Size: 10.9 MB (10864112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8358954408f75f5bf321d427920d547413ff216178a39e941b60cd4bd62d6df`  
		Last Modified: Tue, 12 May 2026 23:49:39 GMT  
		Size: 385.8 KB (385794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9c6329f56f082abc46b2d7f8094beb6802e50f1532fa4b8e31fc8a2d51bc47`  
		Last Modified: Tue, 12 May 2026 23:49:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d684f88f9e0b18396a876a7a6f864e3706a0fcd2b8df57eaaf73e42ee434774f`  
		Last Modified: Tue, 12 May 2026 23:49:39 GMT  
		Size: 389.5 KB (389490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76d82e8675f28cad26687971e7e66267e942ba72da0a08bc46d8610c082e22b`  
		Last Modified: Tue, 12 May 2026 23:49:39 GMT  
		Size: 407.7 KB (407748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aa31c12e305f55ce9d7267e64ad6018c752b9991e23ae3c3ca79d80265a788`  
		Last Modified: Tue, 12 May 2026 23:49:38 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.5139; amd64

```console
$ docker pull haxe@sha256:1e4b6dba9f429fa4bef65123f81e42ba1e5c82c837234795d002ac932a92244c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2152561611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04073c40b9373420bab594d9ed58545321e7f735d6696501aa2f2453e3bbf214`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:46:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:51:37 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Tue, 12 May 2026 23:51:37 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Tue, 12 May 2026 23:51:38 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Tue, 12 May 2026 23:51:39 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Tue, 12 May 2026 23:51:39 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Tue, 12 May 2026 23:51:45 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 May 2026 23:52:04 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:52:10 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Tue, 12 May 2026 23:52:10 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 12 May 2026 23:52:23 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:52:24 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 12 May 2026 23:53:31 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:53:37 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Tue, 12 May 2026 23:53:38 GMT
ENV HOMEDRIVE=C:
# Tue, 12 May 2026 23:53:44 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 May 2026 23:53:51 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Tue, 12 May 2026 23:53:51 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035b5e8417e640b2f6485083912f09cb265e121a7738e800f18f5ee557c17cb1`  
		Last Modified: Tue, 12 May 2026 23:47:11 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3fe5d07e1e5a9e74ca24be1dc8fada70aaf5e6cbe7088db7ba69574143b849`  
		Last Modified: Tue, 12 May 2026 23:54:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:224844734b72ccf9e9262aef2543a511cf7c610c747a379853b0b2a443a34c4b`  
		Last Modified: Tue, 12 May 2026 23:54:01 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d124ffef651ac698b4eccba400d3a95c16c24f49aab4080c8e4e55ebec2841df`  
		Last Modified: Tue, 12 May 2026 23:54:01 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438f519ed7013ac25a7d8af8ce10f5241e3ab40676518677ed908c1a5e68490b`  
		Last Modified: Tue, 12 May 2026 23:54:00 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2560ad29c741a89945f63334645f37f018cc0b4adde066714d7492072a0654`  
		Last Modified: Tue, 12 May 2026 23:53:59 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289869461d7b854e583b16547d20a19d1e5acb3768dd3977aa7248c09afd5d82`  
		Last Modified: Tue, 12 May 2026 23:53:59 GMT  
		Size: 486.0 KB (486045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f636da2fc8e52eef26e8f9b46d724146461cf3f094c0afe90176a6ab55eface`  
		Last Modified: Tue, 12 May 2026 23:54:00 GMT  
		Size: 12.9 MB (12920595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36cbb54f0e9165832e1afefc8d67ff96261534ae7c1213d4e7019a11ff5c16`  
		Last Modified: Tue, 12 May 2026 23:53:57 GMT  
		Size: 367.0 KB (367046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf31ae866b98e8b20936cb9a61edc02b886b7210150ac18522bd8738e50e0af`  
		Last Modified: Tue, 12 May 2026 23:53:57 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d990eb2945becfd88eed6e28d171748067ee101116ed82c410b2350c965a1586`  
		Last Modified: Tue, 12 May 2026 23:53:58 GMT  
		Size: 4.4 MB (4385641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df6f7ca41d9d92430715da9cb5d04d9a04baf9ac2464cb1cc6d336eaa1f3b2e`  
		Last Modified: Tue, 12 May 2026 23:53:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906856536e2367e9b3ca60765347bdfeab116b2154a036afff702f0d0da37e86`  
		Last Modified: Tue, 12 May 2026 23:53:59 GMT  
		Size: 10.8 MB (10846490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e88fe9133fbcbe5432a2133e7586cab04a6ad12cb80646f79846b1c472b23d`  
		Last Modified: Tue, 12 May 2026 23:53:56 GMT  
		Size: 363.2 KB (363193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0185f7edb6c91d4d663a00c0b1c48148f65725a930918e997b20c999718249`  
		Last Modified: Tue, 12 May 2026 23:53:55 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1560bdcc7393df3bf3bba6bc913cf72901011e3acd6025308ca7f6a6de96ba19`  
		Last Modified: Tue, 12 May 2026 23:53:55 GMT  
		Size: 373.4 KB (373380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d96f2c9ab2e62034c6d0b165ff55e70b89fbc163e4a21ee4fd407f6dc84f448`  
		Last Modified: Tue, 12 May 2026 23:53:56 GMT  
		Size: 385.6 KB (385583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fbbd73d3fa7d9ad112e8cc4833f25cd5e67ddda3336d909a234d2dee09fbe93`  
		Last Modified: Tue, 12 May 2026 23:53:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
