## `haxe:latest`

```console
$ docker pull haxe@sha256:b8a8d966ed65af91523c6f10e434b9b7ded2dda2dfacd852e1d30546c2655a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:ed9e214dcf9124828d5cc67701aca6b1c28c0403bc7b6a47fd57044c4251089c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398844576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561ecaebc26353b0d588b1accce3716dc2b90d6a8c962cecd771c73602283ed`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 06:21:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
ENV NEKO_VERSION=2.4.0
# Tue, 01 Oct 2024 06:21:31 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
ENV HAXE_VERSION=4.3.6
# Tue, 01 Oct 2024 06:21:31 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 01 Oct 2024 06:21:31 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& opam pin add extlib 1.7.9 --no-action 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da802df85c965baeca9d39869f9e2cbb3dc844d4627f413bfbb2f2c3d6055988`  
		Last Modified: Sat, 19 Oct 2024 00:54:48 GMT  
		Size: 24.1 MB (24051386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aadc5092c3b7a865666b14bef3d4d038282b19b124542f1a158c98ea8c1ed1b`  
		Last Modified: Sat, 19 Oct 2024 02:06:37 GMT  
		Size: 64.4 MB (64389695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0605c09e522d7dea84fab19d40f82b0d02922fdd7580661411e4b634967d2a14`  
		Last Modified: Sat, 19 Oct 2024 03:01:00 GMT  
		Size: 1.3 MB (1251096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3f3ad1ff955f9b70e38d9ed12d67f439941ccd5919fbdcc00cff6084c2248`  
		Last Modified: Sat, 19 Oct 2024 03:01:00 GMT  
		Size: 1.4 MB (1383969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc0405d63c40bcf3a4168f68fbe8d54a6622c4bd236b2227e792940f50d04be`  
		Last Modified: Sat, 19 Oct 2024 03:01:07 GMT  
		Size: 258.2 MB (258213407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:1b035c57339153e2be7149b2edac6e6333beb3566deae639aca0ed7208323c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc7dfd7f01e4ad201903ac300394f731f7e51c5bbb668391190077895063460`

```dockerfile
```

-	Layers:
	-	`sha256:efb8048ef69280bda680c74a9161d70e7171c449e872969053f547b909630e52`  
		Last Modified: Sat, 19 Oct 2024 03:01:00 GMT  
		Size: 19.3 KB (19294 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:d8f512eae786c1e9f2570fa9d2884019e5240a672991ef25460e41966e94becf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.7 MB (361740691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b29cf44f299598fa7f714e5fdcd9c68e392319e2c81fbe8867ed40808f226d2`
-	Default Command: `["haxe"]`

```dockerfile
# Tue, 01 Oct 2024 06:21:31 GMT
ADD file:2ce9af7b514320ba230746cbff4f2f2e2b8d4a62ac035ebbe6575e17544f6416 in / 
# Tue, 01 Oct 2024 06:21:31 GMT
CMD ["bash"]
# Tue, 01 Oct 2024 06:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 06:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Oct 2024 06:21:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 06:21:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
ENV NEKO_VERSION=2.4.0
# Tue, 01 Oct 2024 06:21:31 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
ENV HAXE_VERSION=4.3.6
# Tue, 01 Oct 2024 06:21:31 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 01 Oct 2024 06:21:31 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& opam pin add extlib 1.7.9 --no-action 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:b683f99b4cdeb3cb4e487b268b3949647168e16d00d07e004e03af92331dbfed`  
		Last Modified: Thu, 17 Oct 2024 03:06:32 GMT  
		Size: 45.1 MB (45147940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332329de6b42a2c5f534a6f40381b05e4356eb62a42408f66b4d98e78cfee55`  
		Last Modified: Thu, 17 Oct 2024 03:36:59 GMT  
		Size: 22.0 MB (21957453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d531afa8550e37b4fb5ecf878018cd17fb79413ab81359496c3eedd8bb0abca2`  
		Last Modified: Thu, 17 Oct 2024 03:37:18 GMT  
		Size: 59.6 MB (59639477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6835218bb19b6fc6abd90684f6209b9037a54358326fed288dab109ecff3e0`  
		Last Modified: Thu, 17 Oct 2024 13:34:38 GMT  
		Size: 1.1 MB (1147001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8799d3e38ea8b916989af915ea61b6617aa3a56fa192d063460c0dcca00a14e`  
		Last Modified: Thu, 17 Oct 2024 13:34:38 GMT  
		Size: 1.3 MB (1325724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d87c124e1b5b751f453ae3b76277fc4d0a943c7b9b45294d29d1475a09baf0`  
		Last Modified: Thu, 17 Oct 2024 13:34:43 GMT  
		Size: 232.5 MB (232523096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:f161be9878228569585e5e763eb81bbd3f526d9c1b59e1702de1eb556feaa119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a819fa72fa7a36b9c7cdfb77c1f73c45229d89d11add763d6af4a3f6f99001`

```dockerfile
```

-	Layers:
	-	`sha256:e1d8e0658366df2df853651e8ea259039f9397eb0464179db37f6bf55c39a7ad`  
		Last Modified: Thu, 17 Oct 2024 13:34:37 GMT  
		Size: 19.3 KB (19295 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:1ca843d9293429fd1d5c60b0e9f5a5ceb35028a4a85fda5497668f1053962526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.8 MB (401809726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ea92929444ab0cc6a91f9a57c27160cd2084b6c2c18aa9fbbb1d9e7a64187c`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Oct 2024 06:21:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libgc1 		zlib1g 		libpcre2-8-0 		 		libmariadb3 		libsqlite3-0 		libmbedcrypto7 		libmbedtls14 		libmbedx509-1 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
ENV NEKO_VERSION=2.4.0
# Tue, 01 Oct 2024 06:21:31 GMT
RUN set -ex 	&& buildDeps=' 		gcc 		make 		cmake 		libgc-dev 		libssl-dev 		libpcre2-dev 		zlib1g-dev 		apache2-dev 		libmariadb-dev-compat 		libsqlite3-dev 		libmbedtls-dev 		libgtk-3-dev 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends && rm -rf /var/lib/apt/lists/* 		&& wget -O neko.tar.gz "https://github.com/HaxeFoundation/neko/archive/v2-4-0/neko-2.4.0.tar.gz" 	&& echo "232d030ce27ce648f3b3dd11e39dca0a609347336b439a4a59e9a5c0a465ce15 *neko.tar.gz" | sha256sum -c - 	&& mkdir -p /usr/src/neko 	&& tar -xC /usr/src/neko --strip-components=1 -f neko.tar.gz 	&& rm neko.tar.gz 	&& cd /usr/src/neko 	&& cmake -DRELOCATABLE=OFF . 	&& make 	&& make install 		&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/neko ~/.cache # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
ENV HAXE_VERSION=4.3.6
# Tue, 01 Oct 2024 06:21:31 GMT
ENV HAXE_STD_PATH=/usr/local/share/haxe/std
# Tue, 01 Oct 2024 06:21:31 GMT
RUN set -ex 	&& buildDeps=' 		make 		ocaml-nox 		ocaml-native-compilers 		camlp4 		ocaml-findlib 		zlib1g-dev 		libpcre2-dev 		libmbedtls-dev 		libxml-light-ocaml-dev 		opam 		mccs 		m4 		unzip 		pkg-config 		libstring-shellquote-perl 		libipc-system-simple-perl 	' 	&& git clone --recursive --depth 1 --branch 4.3.6 "https://github.com/HaxeFoundation/haxe.git" /usr/src/haxe 	&& cd /usr/src/haxe 	&& mkdir -p $HAXE_STD_PATH 	&& cp -r std/* $HAXE_STD_PATH 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 		&& opam init --disable-sandboxing 	&& eval `opam env` 		&& opam pin add extlib 1.7.9 --no-action 		&& ( [ -f /usr/src/haxe/opam ] || [ -f /usr/src/haxe/haxe.opam ] && opam install /usr/src/haxe --deps-only --assume-depexts --yes || make opam_install ) 	&& make all tools 	&& mkdir -p /usr/local/bin 	&& cp haxe haxelib /usr/local/bin 	&& mkdir -p /haxelib 	&& cd / && haxelib setup /haxelib 		&& eval `opam env --revert` 	&& rm -rf ~/.opam 	&& rm -rf /var/lib/apt/lists/* 	&& apt-get purge -y --auto-remove $buildDeps 	&& rm -rf /usr/src/haxe ~/.cache # buildkit
# Tue, 01 Oct 2024 06:21:31 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b894d63c771a6056bc65ff25192b251413259ba7d160b0076f0f5d7975dc39`  
		Last Modified: Sat, 19 Oct 2024 01:10:43 GMT  
		Size: 23.6 MB (23593834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5594266b1bacf9ad6855b00d9c5c98e721001eb115218eda673e548e04fdbf`  
		Last Modified: Sat, 19 Oct 2024 05:17:15 GMT  
		Size: 64.4 MB (64350044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835141eec8d94859ac138e67537135c78d0db2425523487919e22ae8a77f9fc6`  
		Last Modified: Sat, 19 Oct 2024 07:39:07 GMT  
		Size: 1.2 MB (1247373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8776dedd78be18e3f470d23c9ee54b34ed6d9da2ff34caf1c0674858e9996ef7`  
		Last Modified: Sat, 19 Oct 2024 07:39:07 GMT  
		Size: 1.4 MB (1419177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41561da66f3d9872c1328000fc418ea41423dd1744b28b3ec5dcfacbef83cbf`  
		Last Modified: Sat, 19 Oct 2024 07:39:13 GMT  
		Size: 261.6 MB (261614320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:bef98ef61276378fc7f5e5a475454130b9dd0cddfe3050dd6ba113c5be4a6f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 KB (19463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5903f1def67602fedee6660b79a20245d351618b78b921de179aef97c6c242a`

```dockerfile
```

-	Layers:
	-	`sha256:3c6a26ec1bee9bcc7d2e235f54cc4f4452c381e67c6b1cc69eba7e8c393889a9`  
		Last Modified: Sat, 19 Oct 2024 07:39:06 GMT  
		Size: 19.5 KB (19463 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.20348.2762; amd64

```console
$ docker pull haxe@sha256:da275e10b1bd2b25f18e50faf8512f2142ac4539e4840bb470869ac310eb81d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1828175265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bba7c244662a7ca9e43bdc920a48beafdd90ed1b7cdfb03112d4822df23939e`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:02:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Oct 2024 23:02:22 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 09 Oct 2024 23:02:22 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 09 Oct 2024 23:02:23 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 09 Oct 2024 23:02:24 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 09 Oct 2024 23:02:24 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 09 Oct 2024 23:02:32 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:02:50 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:02:56 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 09 Oct 2024 23:02:57 GMT
ENV NEKO_VERSION=2.4.0
# Wed, 09 Oct 2024 23:03:09 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-0/neko-2.4.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:03:09 GMT
ENV HAXE_VERSION=4.3.6
# Wed, 09 Oct 2024 23:04:01 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.6/haxe-4.3.6-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:04:07 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 09 Oct 2024 23:04:08 GMT
ENV HOMEDRIVE=C:
# Wed, 09 Oct 2024 23:04:13 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:04:19 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 09 Oct 2024 23:04:20 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9051cd04f9b2bede9d519e417bd2cfb972148f131c5eb6d958476b8646cdde89`  
		Last Modified: Wed, 09 Oct 2024 23:04:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4516f0a93ed4eea379f7eeb003c1cd77e4e1852cf8ea4b9dc2323f47353546`  
		Last Modified: Wed, 09 Oct 2024 23:04:30 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b091d7afda2268b61123f7ef2c04eec5cf01440516508883f9ec772434b68ac2`  
		Last Modified: Wed, 09 Oct 2024 23:04:30 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee237b7b90a60b6e36596bbd687f61bb6af9deb76459360085ca23f84a575b14`  
		Last Modified: Wed, 09 Oct 2024 23:04:29 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700e57bccf5395964e4553d95864d7d465f4e4792dd5022e5450b216f5110143`  
		Last Modified: Wed, 09 Oct 2024 23:04:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2d12c844b89b49b665bac80d53d935b5674afe724f397ab69868c5bb4afc35`  
		Last Modified: Wed, 09 Oct 2024 23:04:28 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf65260131210bb8119f4ee287e6382750bf9bf8af11d98dc03528f71a8639f5`  
		Last Modified: Wed, 09 Oct 2024 23:04:28 GMT  
		Size: 487.2 KB (487250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccdf81a1d4be56611c89246898f375d15a9dae99edddcc6fc717495d5641408e`  
		Last Modified: Wed, 09 Oct 2024 23:04:28 GMT  
		Size: 12.9 MB (12930025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b57888052cc3ab0c63a9dce2f1d1b0659107dec885c3807f92a68bbc62bd95d`  
		Last Modified: Wed, 09 Oct 2024 23:04:26 GMT  
		Size: 376.9 KB (376898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc1425d84d2b8b951486b62e9e01894efd42fd73921a43cf9acff0b8f5e34ae`  
		Last Modified: Wed, 09 Oct 2024 23:04:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3ac31d76d93ca2e20a16086f72712c02912cb688fe06930dfe82777e6a9c9f`  
		Last Modified: Wed, 09 Oct 2024 23:04:26 GMT  
		Size: 4.3 MB (4335572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d01fe9b029f5dc4b845d17a383816a2279aee5ca4197fe9a15dbe5d2effb6ea`  
		Last Modified: Wed, 09 Oct 2024 23:04:25 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f902611e5f2a2fded32b72d7f732f8c47030e08ce80d4b45450b3eed299b8864`  
		Last Modified: Wed, 09 Oct 2024 23:04:27 GMT  
		Size: 9.5 MB (9532649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec1ea775676b111d93802c447facc1449aa11eb81a70bcbb31b421e2ac1c0e2`  
		Last Modified: Wed, 09 Oct 2024 23:04:24 GMT  
		Size: 372.5 KB (372451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add4b0280214bac66ec6b840a5df2d6a2d89a4a1daa3340473b03bcfee331a58`  
		Last Modified: Wed, 09 Oct 2024 23:04:23 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9181a49ae4cc21b1e0395bff21b47236b9aafe5e1ff4c1f6ad5679273c318cf2`  
		Last Modified: Wed, 09 Oct 2024 23:04:24 GMT  
		Size: 383.8 KB (383789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022ada4060b0fbc08f1e1d7a27da52fc277833cac60e60c0db815905ca3f8075`  
		Last Modified: Wed, 09 Oct 2024 23:04:24 GMT  
		Size: 402.2 KB (402198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d6da3c2888c1b3a4b898d646554070b16132d6b1a1cb6b881d240e1a7b8ddfa`  
		Last Modified: Wed, 09 Oct 2024 23:04:23 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.17763.6414; amd64

```console
$ docker pull haxe@sha256:376a601285fe56171693df71bd3bac5dee474a70b0124ae5d24d11c6f333d9b8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1930405647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f800df834972582f5314d3484a7406a2553597851a097b1a8e842dece892328d`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:01:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Oct 2024 23:01:16 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Wed, 09 Oct 2024 23:01:16 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Wed, 09 Oct 2024 23:01:17 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Wed, 09 Oct 2024 23:01:18 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Wed, 09 Oct 2024 23:01:18 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Wed, 09 Oct 2024 23:02:02 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:02:32 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:02:38 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Wed, 09 Oct 2024 23:02:39 GMT
ENV NEKO_VERSION=2.4.0
# Wed, 09 Oct 2024 23:02:51 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-0/neko-2.4.0-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '334e192434483ddcd7062132a1af1cf961c4871258d92d2710a3c2e7a8225aca') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:02:51 GMT
ENV HAXE_VERSION=4.3.6
# Wed, 09 Oct 2024 23:03:46 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.6/haxe-4.3.6-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '336090b9c32d6cb9b674130794fea0e9c2240a72bceb7a5d6b44d37c796d1a9a') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:03:53 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Wed, 09 Oct 2024 23:03:53 GMT
ENV HOMEDRIVE=C:
# Wed, 09 Oct 2024 23:03:59 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Oct 2024 23:04:07 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Wed, 09 Oct 2024 23:04:08 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd152a07df36ba35eeca26ef87595e1b4f5541ac537ce9d06fb7ee08f953079`  
		Last Modified: Wed, 09 Oct 2024 23:04:16 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340c9ea4dad24e1e5a239f9efb51eb1f7b21f0a911383c222e6ba558d4c43a49`  
		Last Modified: Wed, 09 Oct 2024 23:04:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e85f4e01a7e0c88597e94b874e8a1e2d6a8f6a2394fed9feaabbd07f475c098`  
		Last Modified: Wed, 09 Oct 2024 23:04:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0606b7b28430e411d90ea96744c8edb3c351a09f7de203ffdea0c658d34d11f1`  
		Last Modified: Wed, 09 Oct 2024 23:04:16 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2697d954bc2c50a92a64670dc73f36111f37a0806f2f13994ae685593ce385f1`  
		Last Modified: Wed, 09 Oct 2024 23:04:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010a19b0d702359127f370a1a7859763d5f97ad0657634f14255a37652606203`  
		Last Modified: Wed, 09 Oct 2024 23:04:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729fb1ffd68a3351d34300e423bc7021e2d983b57bdf1d99400799fe53cbbabc`  
		Last Modified: Wed, 09 Oct 2024 23:04:14 GMT  
		Size: 465.3 KB (465281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0166990ff60681582358d29de73b7e12000a59ab2470dd507944adc697f2766d`  
		Last Modified: Wed, 09 Oct 2024 23:04:15 GMT  
		Size: 12.9 MB (12945835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eee3d6ebc822cd644e9318775bee691bdf519006d5773cfa058041a39618d70`  
		Last Modified: Wed, 09 Oct 2024 23:04:13 GMT  
		Size: 343.3 KB (343276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241b166b57ab8eee8c255bbcb94175e2eea245a65984e767d78733bae1b47e13`  
		Last Modified: Wed, 09 Oct 2024 23:04:13 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab7bc38d19b8ec722d724981e7add81e3c04df8410a96f52d568552a99e5a54`  
		Last Modified: Wed, 09 Oct 2024 23:04:13 GMT  
		Size: 4.3 MB (4294612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434dc5f86d42cabfb606464aa152682f72c9e10acfda286d0bad4233409542b5`  
		Last Modified: Wed, 09 Oct 2024 23:04:12 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7398249960a142e17e88db6095bb2d1c0ca27c42eab6c42e3aae5528da0154e`  
		Last Modified: Wed, 09 Oct 2024 23:04:14 GMT  
		Size: 9.5 MB (9496668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b3893b9985440c7954d43f8f321dbecfde211a0e96ddf3c79b574481d582cc`  
		Last Modified: Wed, 09 Oct 2024 23:04:11 GMT  
		Size: 332.6 KB (332634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dff3dcc9c53e5aa1cec2978d27f40d527b7bcff62b6be4808d07199937773b`  
		Last Modified: Wed, 09 Oct 2024 23:04:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e9e6967f11b90256abcc016f9d9afb4a8e19bf15b870e81f3f13bdc000f9ce`  
		Last Modified: Wed, 09 Oct 2024 23:04:11 GMT  
		Size: 338.5 KB (338474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9928f5cfe12c27c6468ab92c00a90a86ad1c81794186704449dd6bd2c7461ffd`  
		Last Modified: Wed, 09 Oct 2024 23:04:11 GMT  
		Size: 350.6 KB (350586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70aeb009b420487c918953e50d43f7e616483d0de1c2e704b30213232d13083e`  
		Last Modified: Wed, 09 Oct 2024 23:04:11 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
