## `haxe:latest`

```console
$ docker pull haxe@sha256:9ce23b347510f1595187a75d3a1d66f1a7ecb48a2ab2631a88ebb55f694d3589
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:6c36358158ba0fc86eb0f2f26f1f820bed9a5f8788e8e7f7cca1ce6463deaa8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.6 MB (398588831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909d8ebfba3a162b68bd7028ad69af40c583d89821f148c40b8a66edf7912c1a`
-	Default Command: `["haxe"]`

```dockerfile
# Thu, 08 Aug 2024 23:50:52 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Thu, 08 Aug 2024 23:50:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 23:50:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 23:50:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
ENV NEKO_VERSION=2.4.0
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
ENV HAXE_VERSION=4.3.6
# Thu, 08 Aug 2024 23:50:52 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6afa3f266c11e8960349e7866203a9df478a50362bb5488c45fe39d99b2707`  
		Last Modified: Wed, 04 Sep 2024 23:01:16 GMT  
		Size: 24.1 MB (24053153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66a70da0bec13fb3d492fcdef60fd8a5ef0a1a65c4e8a4909e26742852f0f2`  
		Last Modified: Wed, 04 Sep 2024 23:01:34 GMT  
		Size: 64.1 MB (64148018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4bda12a423c3da63dcc5fe344dc8b4a628b8aac1443844299da9e40934a265`  
		Last Modified: Tue, 10 Sep 2024 01:06:42 GMT  
		Size: 1.3 MB (1251146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806d705c383b590679a355144aa7f54d85964eb3c4643056b304714069c11013`  
		Last Modified: Tue, 10 Sep 2024 01:06:42 GMT  
		Size: 1.4 MB (1383933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c01e713e54e0150fa8368b207b340aff0ce6301ff52e7c28101adb34e2ba036`  
		Last Modified: Tue, 10 Sep 2024 01:06:48 GMT  
		Size: 258.2 MB (258195879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:a526220d180632c9cf5f8a0aa5619519369fa103c945540a0975f9216bcd5c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 KB (18950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a799fc5e1934113728b9506cc49444e23ef340c6207eb13a1aed13a5bc714eac`

```dockerfile
```

-	Layers:
	-	`sha256:356e1e50029407b4e52f5842ea530e131af0b53ffac5aded223c888f2e09685e`  
		Last Modified: Tue, 10 Sep 2024 01:06:42 GMT  
		Size: 18.9 KB (18950 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:952b3b4f8d6a1083c8fd581d58c7ea9f29de3c7515bd17e6e3525af41df6a9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.3 MB (361313140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f36c80c59489a30bf8eece2d6139bd8bf61ba733c9ec659524f4f839eba5a7b`
-	Default Command: `["haxe"]`

```dockerfile
# Thu, 08 Aug 2024 23:50:52 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Thu, 08 Aug 2024 23:50:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 23:50:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 23:50:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
ENV NEKO_VERSION=2.4.0
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
ENV HAXE_VERSION=4.3.6
# Thu, 08 Aug 2024 23:50:52 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57cf6f4c9870e4cf546b689e86c09f99b2cad92c3bdf867254a97385052d41f`  
		Last Modified: Tue, 10 Sep 2024 05:12:19 GMT  
		Size: 1.1 MB (1147064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4354afa8f34be00e20c23b7fccc22257731d9bf12e71c6d8237f348f196b9ba`  
		Last Modified: Tue, 10 Sep 2024 05:12:20 GMT  
		Size: 1.3 MB (1325769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9136edd444d41bfc6a3c9a64068c16e25046e2a79ecb786005d36bdc287c44`  
		Last Modified: Tue, 10 Sep 2024 05:12:24 GMT  
		Size: 232.5 MB (232506009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:4e9a0bfd5877493cb10ec9f6a62509e6afcc13002e1c2176ebee7b2db3c1291b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 KB (19054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331d6cef71e38326bc9bced6286d42ac06e9da73271421a7b921546725767ddb`

```dockerfile
```

-	Layers:
	-	`sha256:c22e507e6c511e2cc31476613d72ee113f168a68a37aa9de3cbc3f2b6c274ade`  
		Last Modified: Tue, 10 Sep 2024 05:12:19 GMT  
		Size: 19.1 KB (19054 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:0c3e2712b60c07e410653b47d32febde17d63c366bc037fd96bc227c1fa97544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401439029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a2ef166b8c1011a8d7e83bfae44bad8b7a3f79b51c0a22b63e4e6aab98e6b6`
-	Default Command: `["haxe"]`

```dockerfile
# Thu, 08 Aug 2024 23:50:52 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Thu, 08 Aug 2024 23:50:52 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 23:50:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 Aug 2024 23:50:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
ENV NEKO_VERSION=2.4.0
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
ENV HAXE_VERSION=4.3.6
# Thu, 08 Aug 2024 23:50:52 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Thu, 08 Aug 2024 23:50:52 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Thu, 08 Aug 2024 23:50:52 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364d19f59f69474a80c53fc78da91f85553e16e8ba6a28063cbebf259821119e`  
		Last Modified: Wed, 04 Sep 2024 22:07:56 GMT  
		Size: 23.6 MB (23594279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b1d8321825bc8302752ae003026f13bd15c6eef2efe032f3ca1520c5bbc07`  
		Last Modified: Wed, 04 Sep 2024 22:08:14 GMT  
		Size: 64.0 MB (63997467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4711072fae9056f229debb57d3d7bd76f22b1bd9f01ddafb1882dd8046ea6de6`  
		Last Modified: Tue, 10 Sep 2024 03:41:40 GMT  
		Size: 1.2 MB (1247530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a2faf59e2fa7805eb4ceef7c5c6f37686682b35abbdcac89d9b902e6612ace`  
		Last Modified: Tue, 10 Sep 2024 03:41:40 GMT  
		Size: 1.4 MB (1419123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f3c9cc4024ea24ad6d1e39ba9b9d53b3b44bdb1580dbd7c867c57cda15cab4`  
		Last Modified: Tue, 10 Sep 2024 03:41:47 GMT  
		Size: 261.6 MB (261595007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:800ed0942870c2f813a4453005076926da41254fd4eb7f7d3644e796c93d7b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be123cd7036f1095ed85255df5ba6074783d83c01ddb5ac6efa221d8f2b30ed5`

```dockerfile
```

-	Layers:
	-	`sha256:abe7243acd43cb1ecd187dcddb4441805ff4bbb37747829a1e2eba894b818110`  
		Last Modified: Tue, 10 Sep 2024 03:41:40 GMT  
		Size: 19.3 KB (19276 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.20348.2700; amd64

```console
$ docker pull haxe@sha256:f493e0ca0ce17c0ae7615e629b4d29252a3d40bee96c076fe442c59191f23fc1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1490845107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32ff0da39f37204e469cca6385a46b82b40571fbedea8f366e0d268b3f1600b`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:01:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 00:01:31 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 11 Sep 2024 00:01:31 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 11 Sep 2024 00:01:32 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 11 Sep 2024 00:01:33 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 11 Sep 2024 00:01:33 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 11 Sep 2024 00:01:41 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:01:59 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:02:09 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 11 Sep 2024 00:02:09 GMT
ENV NEKO_VERSION=2.4.0
# Wed, 11 Sep 2024 00:02:27 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-0/neko-2.4.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:02:29 GMT
ENV HAXE_VERSION=4.3.6
# Wed, 11 Sep 2024 00:03:24 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.6/haxe-4.3.6-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:03:30 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 11 Sep 2024 00:03:30 GMT
ENV HOMEDRIVE=C:
# Wed, 11 Sep 2024 00:03:36 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:03:45 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 11 Sep 2024 00:03:45 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60669acae3eae361a62d294137604dde9712f182a7252de788d1897265464cb2`  
		Last Modified: Wed, 11 Sep 2024 00:03:52 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a535b836ab73baac608762c460e492f3db9f0232df9ef75bf23a55565463abf0`  
		Last Modified: Wed, 11 Sep 2024 00:03:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7ee431b148cc048cecbea455f98fe5fdb9c84ffd0bf6d78497f7276f465bef`  
		Last Modified: Wed, 11 Sep 2024 00:03:51 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5265d52f5bbffdd83f6e3b7c79022eeeab76a6ab9e6aa931b3388d8eac6e3cfe`  
		Last Modified: Wed, 11 Sep 2024 00:03:51 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7750ac48f4f104524d79b15cc342984793f9c0feb319cd5dcf641771198919de`  
		Last Modified: Wed, 11 Sep 2024 00:03:51 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe039951908845b72cccdc353792f14b150c1e93b57fcb96a9eef457f1f8334f`  
		Last Modified: Wed, 11 Sep 2024 00:03:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238c95b4a3ccc0e2d0ed312386c94421f0e79e06fd512d585857c709e3191f7b`  
		Last Modified: Wed, 11 Sep 2024 00:03:50 GMT  
		Size: 347.3 KB (347317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4194c14dbb405bbfd5d7a084e5e731da33b6a828cad4635daa90f326847470af`  
		Last Modified: Wed, 11 Sep 2024 00:03:51 GMT  
		Size: 12.9 MB (12920005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bc6bd49b64a116d08a2f768e1b4d73870b1c8c560061ab9fa566ec76f21e2e`  
		Last Modified: Wed, 11 Sep 2024 00:03:49 GMT  
		Size: 367.8 KB (367761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45d144b4a9457f4c7d2e42cad2ae34318c688d9c21393549b71a52052c50e31`  
		Last Modified: Wed, 11 Sep 2024 00:03:49 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3e607ab890eab4e9f24387bcb1d8322a071266d217ad48f5da93016b044b5d`  
		Last Modified: Wed, 11 Sep 2024 00:03:49 GMT  
		Size: 4.3 MB (4328953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1f67c13973e2feee207dccc2e3a1102da5cf75604ad02d4eaa8679db35b3e6`  
		Last Modified: Wed, 11 Sep 2024 00:03:49 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6470c2539036314ead2b2b4682ea775ac9369fb545fd0f654dda19b71e54f3`  
		Last Modified: Wed, 11 Sep 2024 00:03:51 GMT  
		Size: 9.5 MB (9527796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717f7992a35f5f75a8f93c98d98779c494ca6767a519ef434da34ec47fa81889`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 368.1 KB (368065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794ee3ce717ac45602c0e126c850e92d2363f19b41054821d4059f19f09d95b0`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c1a66f103e377605c79460123a68e8903e1160af1683ec2b1550880eb38478`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 380.3 KB (380275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3bf8cffdf3a654c0e124e7865d9adbcf14b2cc04705451b8a7ab1f89a65b97`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 399.5 KB (399512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58599da5f35d80fb55a6cc9e028643f7c4d874f422d4350bf91dc07d40f4bc3`  
		Last Modified: Wed, 11 Sep 2024 00:03:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.6293; amd64

```console
$ docker pull haxe@sha256:d76bdf384c0acd5ae568ffa118c1ff0625a822488d05cc4d00fffb6bca89b212
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1748762286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f4a23af593f5ea0c5642f807ff25d12849b49c2225d69d3045228db0f42bff`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Sep 2024 00:02:07 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 11 Sep 2024 00:02:07 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 11 Sep 2024 00:02:08 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 11 Sep 2024 00:02:09 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 11 Sep 2024 00:02:10 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 11 Sep 2024 00:02:24 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:02:54 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:03:14 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 11 Sep 2024 00:03:15 GMT
ENV NEKO_VERSION=2.4.0
# Wed, 11 Sep 2024 00:03:41 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-0/neko-2.4.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:03:41 GMT
ENV HAXE_VERSION=4.3.6
# Wed, 11 Sep 2024 00:04:58 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.6/haxe-4.3.6-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 11 Sep 2024 00:05:04 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 11 Sep 2024 00:05:05 GMT
ENV HOMEDRIVE=C:
# Wed, 11 Sep 2024 00:05:12 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Sep 2024 00:05:23 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 11 Sep 2024 00:05:24 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03bd07b1ad2bb82553d29f67e042cfaa858cd3509bf975b2875c3dc74161e323`  
		Last Modified: Wed, 11 Sep 2024 00:05:30 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9066ba440f908317c99bd75399010959761992405b934ff99b867654d6cb1243`  
		Last Modified: Wed, 11 Sep 2024 00:05:30 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cffee4a9813c48ce5b182d246d0ccd6f19bc7ef05ac72a5e2013097ac41cf8`  
		Last Modified: Wed, 11 Sep 2024 00:05:29 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c36d1dbffc1479146fe23a3648fee55318a22977e8bd3c3346a2585e2235f6`  
		Last Modified: Wed, 11 Sep 2024 00:05:29 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c08fe8f355d3c2f1506918b3c5abd760a64589f8ae0d500f59d9f5b507cfaa9`  
		Last Modified: Wed, 11 Sep 2024 00:05:29 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec030edef39d420f0efc68a25fd1f8ed6cc0286d4d47954c1ff51e71ab77d566`  
		Last Modified: Wed, 11 Sep 2024 00:05:29 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e5e5454dabb6fa77417fa2229cf558341a95bd247f5ddac6953b8a7e63938`  
		Last Modified: Wed, 11 Sep 2024 00:05:28 GMT  
		Size: 329.6 KB (329625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e2e9e9897b4c69dafaf3d791d3131efe41aa07e47da3ec76e91070a458acba`  
		Last Modified: Wed, 11 Sep 2024 00:05:29 GMT  
		Size: 12.9 MB (12936602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af95771fff3e7002b8a38b17ced1b3f99715719495c4b451a4ffec561b5ba0e1`  
		Last Modified: Wed, 11 Sep 2024 00:05:28 GMT  
		Size: 347.5 KB (347470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2806bbf46295b089db0b0a580aa3372695c17ce32a289016ee1ee4e8ef5c252d`  
		Last Modified: Wed, 11 Sep 2024 00:05:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66190db7c5e5f8748fbe0975e7244570da6e07ef72b1616494ef14ecd3f7e87f`  
		Last Modified: Wed, 11 Sep 2024 00:05:27 GMT  
		Size: 4.3 MB (4306234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52d639cc95ff03cfc596458ede9f405dd2d541dffaeb14bb7b7c0fedc530cd1`  
		Last Modified: Wed, 11 Sep 2024 00:05:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c11036f15b76bc7f6dbc5a71a9ae0a80afeefa9a7369316987f2bef8bd3d48`  
		Last Modified: Wed, 11 Sep 2024 00:05:29 GMT  
		Size: 9.5 MB (9505663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de6bd8b8c5f18f59767f87c496f7bc0becfd7df7a2a29ea8788205a4ac6de67`  
		Last Modified: Wed, 11 Sep 2024 00:05:26 GMT  
		Size: 344.0 KB (344011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2129d33934ba43d4c203e2d4b8667f2e668efd7ba938c29bbc8de43a786c72f`  
		Last Modified: Wed, 11 Sep 2024 00:05:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9337487a38eb9bbee0a11f952470326b863c3759d13fc3398146731736473bf6`  
		Last Modified: Wed, 11 Sep 2024 00:05:26 GMT  
		Size: 348.9 KB (348895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dfbb9ca9cafe6b8fac5cb1230cd49cfd1791adfc3e8f2984f1dcc11d4031a4`  
		Last Modified: Wed, 11 Sep 2024 00:05:26 GMT  
		Size: 362.5 KB (362511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d666d8f4f45c2b344633d077807bd1f1bc07ffafb04030c6c20484274deccde0`  
		Last Modified: Wed, 11 Sep 2024 00:05:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
