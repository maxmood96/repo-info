## `haxe:latest`

```console
$ docker pull haxe@sha256:d78ac3b6fd486a21da85d0524440e8e1e2b620e578ff89bd2cbbd93e945ebdad
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
$ docker pull haxe@sha256:5968c8573299df1a793e5ecde769c2aacb8db8c9bb7b9919b196f0e9f1f78e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398534094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654c7c099992af4a48a6af3c710f9333c40c4c13578d6339056b90c74f868231`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:39:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:39:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:39:11 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 24 Feb 2026 20:40:27 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 24 Feb 2026 20:40:27 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 24 Feb 2026 20:40:27 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 24 Feb 2026 20:43:57 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 24 Feb 2026 20:43:57 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f45a5d4d2ed2df7ec547693959fb5a3cc0a1e38a1432bb2a2fb1f91bc27974`  
		Last Modified: Tue, 24 Feb 2026 20:44:28 GMT  
		Size: 1.3 MB (1261552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcdcd8725f87a7d5140b856debeb107b0e4a02183551af48608985e5c94f6df`  
		Last Modified: Tue, 24 Feb 2026 20:44:28 GMT  
		Size: 1.4 MB (1385225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8f126769ba0e4cabad7cb526c6707b9b985dcc96421926e71c9bf980889336`  
		Last Modified: Tue, 24 Feb 2026 20:44:33 GMT  
		Size: 259.0 MB (258964237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:c1017bf374540904c5dbf78bb8523477301c9f95a30b01acd123bf8b831a31fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63c7941096c4f4fcd1ac7b9a3af615aba4085dc81d3903a87cfc3562f2e43cd7`

```dockerfile
```

-	Layers:
	-	`sha256:50b1f5239a1be64a25b11e9dd676a6ef10e6c5ae68ece53ffff81cfd81fc9e3a`  
		Last Modified: Tue, 24 Feb 2026 20:44:28 GMT  
		Size: 19.1 KB (19150 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:b86499b055758062482a7b7aba23bb5904f76c602fcceda04a9df25983c041ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.6 MB (361559437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a3c92766d9d84cbf261e7e3906e1cddb5201598e01dd76124f4aa520ac629a`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:16:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:16:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:16:33 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 24 Feb 2026 22:17:56 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 24 Feb 2026 22:17:56 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 24 Feb 2026 22:17:56 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 24 Feb 2026 22:22:05 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 24 Feb 2026 22:22:05 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742857c89c3fff9f983a1595594994ae63f49f2e0dd92faaa9d5886d69aedc6`  
		Last Modified: Tue, 24 Feb 2026 21:34:25 GMT  
		Size: 59.7 MB (59651871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79931d84ef76995a7a09ef12521d4b57c3d9f901ef989cb913a7184ee4d172a`  
		Last Modified: Tue, 24 Feb 2026 22:22:32 GMT  
		Size: 1.2 MB (1159584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3aba9f548e4198432bee1d14ac94b72e951e35949617d23c17f7823310ecfb`  
		Last Modified: Tue, 24 Feb 2026 22:22:33 GMT  
		Size: 1.3 MB (1326788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd407bbc33455ea20135fe1bb5e95abc4fbe80f2fe2d3edcf1bd7257b757998c`  
		Last Modified: Tue, 24 Feb 2026 22:22:37 GMT  
		Size: 233.3 MB (233271292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:f50d451ec5cbe80d1a6726b9907d17572a23fac59be14ac36910570b6e3c684b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed23fd6e88228e67fcd7f1e476bb2bb9746e7ee934a3970b87d350420ca35c51`

```dockerfile
```

-	Layers:
	-	`sha256:b1cc19be60f47ba186f04e4cc3bbc2ecbf8d0b4ab1e9478c015058459c6d29e0`  
		Last Modified: Tue, 24 Feb 2026 22:22:32 GMT  
		Size: 19.3 KB (19264 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:cea7c0c5f64f7c4aaf782e4a1e644ca0b5452623385d905d9da76f1842b4e8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 MB (401529784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752857c6f20ce58c0b768561d707326cd24e629e2959bd3d0ce3ea9846279c61`
-	Default Command: `["haxe"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:29:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:29:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:29:54 GMT
ENV NEKO_VERSION=2.4.1
# Tue, 24 Feb 2026 21:31:09 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-1/neko-2.4.1.tar.gz" 	&& echo "702282028190dffa2078b00cca515b8e2ba889186a221df2226d2b6deb3ffaca *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 24 Feb 2026 21:31:09 GMT
ENV HAXE_VERSION=4.3.7
# Tue, 24 Feb 2026 21:31:09 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 24 Feb 2026 21:34:46 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.7 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --compiler=4.14.2 --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes --ignore-constraints-on= || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 24 Feb 2026 21:34:46 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec306f38941f2cd760bc222b3a66fbbb3046865633f4c5b13ccbb5ff53ab274`  
		Last Modified: Tue, 24 Feb 2026 21:35:22 GMT  
		Size: 1.3 MB (1258017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e92583c26f9d13fd41e991cf62d1a62b06d909cb795b58128412752f2bcb02`  
		Last Modified: Tue, 24 Feb 2026 21:35:22 GMT  
		Size: 1.4 MB (1419926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d773ab73f78df803cf0ce66e3ce2b3c7b59bd1c2923f97443a3dfc8ea67399`  
		Last Modified: Tue, 24 Feb 2026 21:35:27 GMT  
		Size: 262.4 MB (262394489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:0a57ebc90399fdbdd7b45b96840543017ba9e84a4cee9e9d54f019e797c2f433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5591b98a79a2ac2ffaf9546520879db3d96ac0d49805147d4104f12d4edeef3e`

```dockerfile
```

-	Layers:
	-	`sha256:efbd4cb4784abe9c15d19907be3ef75b13c4d3f088d8c89972ea2aa6866ba5d0`  
		Last Modified: Tue, 24 Feb 2026 21:35:22 GMT  
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
