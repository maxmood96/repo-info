## `haxe:latest`

```console
$ docker pull haxe@sha256:d155039ee393b91734984316584e1e99b84b1a8a0a57e6356f7550d4b758d880
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `haxe:latest` - linux; amd64

```console
$ docker pull haxe@sha256:5ea9cb7711f738d35e21c37a75b3256ef5bd784b5638374071942ce243dc729d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398475801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd53fc4ad4d98f421a8e8e6d2e1897ca6fb19e1c90b977e726b2a7ede372d17f`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f279d33abc52c7384e0cbbb666ea22064ea29b50a968ec29ae3ad817f62e16e7`  
		Last Modified: Tue, 21 Oct 2025 04:46:37 GMT  
		Size: 24.0 MB (24028898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5daa5a418829f3daa90a80438cd84706b5f7fa0c795eb7936874864ef1ab7b0c`  
		Last Modified: Tue, 21 Oct 2025 04:47:27 GMT  
		Size: 64.4 MB (64396405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a849132b118707de965ae1a7bd2ac21a7782737aa346793c3568819f5ada7fe`  
		Last Modified: Tue, 21 Oct 2025 08:13:17 GMT  
		Size: 1.3 MB (1261480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55b4ad44f7ca4fa94dacbcf1eeb5044a4b141025024c0af98928351f0d9138a`  
		Last Modified: Tue, 21 Oct 2025 08:13:17 GMT  
		Size: 1.4 MB (1385067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584f8d23625f8d185aeb83fbcfd9e15e61f062e0b2befb9707e5c3dce2264c58`  
		Last Modified: Tue, 21 Oct 2025 09:22:50 GMT  
		Size: 258.9 MB (258923388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:4f6e5f1000c02b8e0bcdfeb01d1fd95b108d82af04692826a5a0b7052d671897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 KB (19194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415ade499c2558d9c06c97743bf162561781885ac02dc88930d147c953d126f1`

```dockerfile
```

-	Layers:
	-	`sha256:803702ca31f1363a07a1752d7e05988be91869daa3e5addebd8d10ca69f98bac`  
		Last Modified: Tue, 21 Oct 2025 09:24:45 GMT  
		Size: 19.2 KB (19194 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm variant v7

```console
$ docker pull haxe@sha256:460b992b3e52b788faeafc652c2cbf4729fd105c1e1918f4775776a449b36d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.5 MB (361496159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec1e294df72d7fb2a1558d765eea59b6ab68cb81cca2b7240f9190f748fba21`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
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
	-	`sha256:5dbe800c0d6104b6df988b153994b0d1b5c022197b54cf928820e3c23d00c7eb`  
		Last Modified: Tue, 21 Oct 2025 01:16:21 GMT  
		Size: 44.2 MB (44195910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:178651637d26f6ae6fc6c2a3297b37f8bbef12e80d822930b05b14f51a262382`  
		Last Modified: Tue, 21 Oct 2025 02:43:48 GMT  
		Size: 21.9 MB (21934505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14411cad8875b2a42f951ec95179ed8a844d1522990ec8b96f1c4d269ce3c71f`  
		Last Modified: Tue, 21 Oct 2025 04:11:04 GMT  
		Size: 59.7 MB (59652688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193bdb5d57444e45fdc8d279c1bae8408603560d1c1f5730ab1a5915283200c2`  
		Last Modified: Tue, 21 Oct 2025 05:29:55 GMT  
		Size: 1.2 MB (1159498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5799941eca0dccaff4019387b7dd78b820e26b82e3881216491d308fad637856`  
		Last Modified: Tue, 21 Oct 2025 05:29:55 GMT  
		Size: 1.3 MB (1326723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0289218e1e402038e93a53aa05c60d25df9cd2211ba1fb2df94575518f1acbc3`  
		Last Modified: Tue, 21 Oct 2025 09:26:04 GMT  
		Size: 233.2 MB (233226835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:287adbd9e032b66075e6c81ab77f8eb6cb92e2f566bedf22ebdbb8deefb85f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea18762b382c2042f8339133c1ee4caa5c5a19f9c32e35e39ba308ccadd86c03`

```dockerfile
```

-	Layers:
	-	`sha256:ce8123e69a27dfea8dde233dfbe2331400c3b831eb88c2d70c23d5fe120d3fa2`  
		Last Modified: Tue, 21 Oct 2025 09:24:48 GMT  
		Size: 19.3 KB (19308 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - linux; arm64 variant v8

```console
$ docker pull haxe@sha256:cc2a39994051a729b30dceccfaf57058202d87d5da1666c8d3298af4ea12ba60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.4 MB (401360312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f9bae617fb89e39fd97619513b10effa628972f7bb2664d07fa49d926234b9e`
-	Default Command: `["haxe"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add7397bc0ae282f3ecd02217ad720d86eab3a3d325f0bfed57fc864c2281a58`  
		Last Modified: Tue, 21 Oct 2025 01:46:17 GMT  
		Size: 23.6 MB (23597991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd15270faa4e93fc4bcc62caecce8d2f5dfc1443d3c99572dfb689973b24c0a4`  
		Last Modified: Tue, 21 Oct 2025 02:35:23 GMT  
		Size: 64.4 MB (64370931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23a5f3e9776f30080b22c61200018fdcee4beae3a9b4a7439c632363f2ece05`  
		Last Modified: Tue, 21 Oct 2025 03:22:48 GMT  
		Size: 1.3 MB (1257939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9022f63b2b112c7f178b5ebf67a7e01dd934eeca53194230732f96d0f8fbea97`  
		Last Modified: Tue, 21 Oct 2025 03:22:48 GMT  
		Size: 1.4 MB (1419868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217e04eb27a5f5b38e332bd79a1b2052a360b245dc5306cce0e9f0241556fd9c`  
		Last Modified: Tue, 21 Oct 2025 09:25:10 GMT  
		Size: 262.4 MB (262354587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haxe:latest` - unknown; unknown

```console
$ docker pull haxe@sha256:799ec53780870ab4b77952bae4e2c6044f06d52c0fd914481bd58b063752070a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 KB (19338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e010292c3b7d230ed457aba2594d17017ed65e7b7c5f88757fbebb7046def0d3`

```dockerfile
```

-	Layers:
	-	`sha256:3475876b7b584585f21571437ca254f469a8404dfc0e519c637d6cf55b137f76`  
		Last Modified: Tue, 21 Oct 2025 09:24:51 GMT  
		Size: 19.3 KB (19338 bytes)  
		MIME: application/vnd.in-toto+json

### `haxe:latest` - windows version 10.0.26100.6905; amd64

```console
$ docker pull haxe@sha256:87583ba6e777207872838f6ca94444f5c4639ab243ff94ebb6f960e596bd3cf2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3250544354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff089bb997e02291cf8d984f5328f386cd18046dc073f8c3a7294ef9641642d`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:23:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 24 Oct 2025 18:23:23 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Fri, 24 Oct 2025 18:23:24 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Fri, 24 Oct 2025 18:23:25 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Fri, 24 Oct 2025 18:23:26 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Fri, 24 Oct 2025 18:23:27 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Fri, 24 Oct 2025 18:23:33 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 24 Oct 2025 18:23:51 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:23:56 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Fri, 24 Oct 2025 18:23:56 GMT
ENV NEKO_VERSION=2.4.1
# Fri, 24 Oct 2025 18:24:08 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:24:09 GMT
ENV HAXE_VERSION=4.3.7
# Fri, 24 Oct 2025 18:25:12 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:25:17 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Fri, 24 Oct 2025 18:25:18 GMT
ENV HOMEDRIVE=C:
# Fri, 24 Oct 2025 18:25:24 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 24 Oct 2025 18:25:30 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Fri, 24 Oct 2025 18:25:32 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0589e6e707593dde7201d2846218e4ef0dc488df3fd3cc9667d0a63afc9103d`  
		Last Modified: Fri, 24 Oct 2025 18:25:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498113fdd7ec3dda75aefcc60ed29e684feba1d54d18871d66043ccd1b193388`  
		Last Modified: Fri, 24 Oct 2025 18:25:50 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0647806459c9e2f436f1b1578fa6e00fc66482d15f7967d8bab0494ef77d6179`  
		Last Modified: Fri, 24 Oct 2025 18:25:51 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb9a5ff87b385cab71a6d8b79bc85dddd27848a6c76d7065e560f3bd7405f8f`  
		Last Modified: Fri, 24 Oct 2025 18:25:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fbf28bfe8e9fe85161435d72bdd7304bca95599e26a4a52a5530f5f9ae1d33`  
		Last Modified: Fri, 24 Oct 2025 18:25:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2e91a0c0d20da038ce509c16a25a5bc5cbc6489163fa324cdb81051ad69143`  
		Last Modified: Fri, 24 Oct 2025 18:25:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1c6a2b54056309dbaa2358745f302104279e5b9dd5a46d3f236a0352fd6415`  
		Last Modified: Fri, 24 Oct 2025 18:25:52 GMT  
		Size: 385.8 KB (385843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6131a5852465f95ce75322e077f5bfe1aa260eefd5a4ae63185d12af8f87b5fe`  
		Last Modified: Fri, 24 Oct 2025 18:25:53 GMT  
		Size: 13.0 MB (12952063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9daf05fc89ed9dc98051e35c52b9afe046af664e2b40aa0c056497ad522b86b`  
		Last Modified: Fri, 24 Oct 2025 18:25:52 GMT  
		Size: 396.7 KB (396669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3df59338a23f084ae8813cd984625e5a1baaf44eea1e4a813df6812b33bda8c`  
		Last Modified: Fri, 24 Oct 2025 18:25:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3044f6697bfae084f3742deb4a5e8fdd1758c0e65fb21eb0e72ea276ec7e0fbb`  
		Last Modified: Fri, 24 Oct 2025 18:25:50 GMT  
		Size: 4.4 MB (4409833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a124be8ac147210a065db7f41292b10e57c7b3b2fddee4af2c7d46521094575`  
		Last Modified: Fri, 24 Oct 2025 18:25:49 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ce28921aa6df07341994d6a62e8cc82029e902883b321abcc03a54dbdd6a85`  
		Last Modified: Fri, 24 Oct 2025 18:25:51 GMT  
		Size: 10.9 MB (10860296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8695f81bb96f544bfe5b78562b9791f5b5b6caae164dc5f7778b1f099e29a6`  
		Last Modified: Fri, 24 Oct 2025 18:25:49 GMT  
		Size: 381.9 KB (381942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0e06a18dffe1e78420579a44c9556629780ef69821411e095f7541c7bd6589`  
		Last Modified: Fri, 24 Oct 2025 18:25:49 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8775df25d2915c1d3d3eefeec316951c8aab8ff9c1009926cdf2358182bb18d`  
		Last Modified: Fri, 24 Oct 2025 18:25:49 GMT  
		Size: 391.1 KB (391114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b9508d54692a64ff1005468e0bb039d2164af022c46c3971b32b35def17f11`  
		Last Modified: Fri, 24 Oct 2025 18:25:49 GMT  
		Size: 406.4 KB (406449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba98cbadb92ddd8477ccd6c36273fd7085302d221e0d3f4e138ea592b8d07a9`  
		Last Modified: Fri, 24 Oct 2025 18:25:49 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haxe:latest` - windows version 10.0.20348.4297; amd64

```console
$ docker pull haxe@sha256:b932ce736464d420d67e8339f81f1145ad0006496f409b9dc08e1e20d1b7e37c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1607251036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4111fb8836e663d3765f5aa0353e9e13bd90375729950dc60df3819da1bb1b91`
-	Default Command: `["haxe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:22:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 24 Oct 2025 18:22:29 GMT
ENV HAXETOOLKIT_PATH=C:\HaxeToolkit
# Fri, 24 Oct 2025 18:22:30 GMT
ENV NEKOPATH=C:\HaxeToolkit\neko
# Fri, 24 Oct 2025 18:22:30 GMT
ENV HAXEPATH=C:\HaxeToolkit\haxe
# Fri, 24 Oct 2025 18:22:31 GMT
ENV HAXE_STD_PATH=C:\HaxeToolkit\haxe\std
# Fri, 24 Oct 2025 18:22:31 GMT
ENV HAXELIB_PATH=C:\HaxeToolkit\haxe\lib
# Fri, 24 Oct 2025 18:22:39 GMT
RUN $newPath = ('{0};{1};{2}' -f $env:HAXEPATH, $env:NEKOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 24 Oct 2025 18:22:58 GMT
RUN $url = 'https://download.microsoft.com/download/0/5/6/056dcda9-d667-4e27-8001-8a0c6971d6b1/vcredist_x86.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'vcredist_x86.exe'; 		Write-Host 'Verifying sha256 (89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17) ...'; 	if ((Get-FileHash vcredist_x86.exe -Algorithm sha256).Hash -ne '89f4e593ea5541d1c53f983923124f9fd061a1c0c967339109e375c661573c17') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -FilePath "vcredist_x86.exe" -ArgumentList "/Q" -Wait; 		Write-Host 'Removing installer...'; 	Remove-Item .\vcredist_x86.exe; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:23:05 GMT
RUN New-Item -ItemType directory -Path $env:HAXETOOLKIT_PATH;
# Fri, 24 Oct 2025 18:23:06 GMT
ENV NEKO_VERSION=2.4.1
# Fri, 24 Oct 2025 18:23:19 GMT
RUN $url = 'https://github.com/HaxeFoundation/neko/releases/download/v2-4-1/neko-2.4.1-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'neko.zip'; 		Write-Host 'Verifying sha256 (3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9) ...'; 	if ((Get-FileHash neko.zip -Algorithm sha256).Hash -ne '3902933da42320e8bc04dbee07959ee9ff09a7848e9af48072396400cc3618c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path neko.zip -DestinationPath tmp; 	if (Test-Path tmp\neko.exe) { Move-Item tmp $env:NEKOPATH } 	else { Move-Item (Resolve-Path tmp\neko* | Select -ExpandProperty Path) $env:NEKOPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path neko.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  neko -version'; neko -version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:23:19 GMT
ENV HAXE_VERSION=4.3.7
# Fri, 24 Oct 2025 18:24:26 GMT
RUN $url = 'https://github.com/HaxeFoundation/haxe/releases/download/4.3.7/haxe-4.3.7-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile haxe.zip; 		Write-Host 'Verifying sha256 (29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9) ...'; 	if ((Get-FileHash haxe.zip -Algorithm sha256).Hash -ne '29f7acb0fb9fc66a2b9f6bd9453af3474ccb14ebd9fd0142f351d7311c4010c9') { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType directory -Path tmp; 	Expand-Archive -Path haxe.zip -DestinationPath tmp; 	if (Test-Path tmp\haxe.exe) { Move-Item tmp $env:HAXEPATH } 	else { Move-Item (Resolve-Path tmp\haxe* | Select -ExpandProperty Path) $env:HAXEPATH }; 		Write-Host 'Removing ...'; 	Remove-Item -Path haxe.zip, tmp -Force -Recurse -ErrorAction Ignore; 		Write-Host 'Verifying install ...'; 	Write-Host '  haxe -version'; haxe -version; 	Write-Host '  haxelib version'; haxelib version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:24:32 GMT
RUN New-Item -ItemType directory -Path $env:HAXELIB_PATH;
# Fri, 24 Oct 2025 18:24:33 GMT
ENV HOMEDRIVE=C:
# Fri, 24 Oct 2025 18:24:38 GMT
RUN $newPath = ('{0}\Users\{1}' -f $env:HOMEDRIVE, $env:USERNAME); 	Write-Host ('Updating HOMEPATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('HOMEPATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 24 Oct 2025 18:24:46 GMT
RUN (New-Object System.Net.WebClient).DownloadString('https://lib.haxe.org/p/hxcpp/4.2.1/download/') >$null
# Fri, 24 Oct 2025 18:24:46 GMT
CMD ["haxe"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e18310116b5856e00ef678dc3a7440e876153bfadd9ca2741444d6cdc4dd3e`  
		Last Modified: Fri, 24 Oct 2025 21:25:02 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b78124714bd0423abfd7006dcf89968c0f6fcf41bdc445bd1f7072a712c176`  
		Last Modified: Fri, 24 Oct 2025 21:25:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904807bf19d378686730cf29959bb75bcd8dcf1867b7dfaee31ea1084072fe72`  
		Last Modified: Fri, 24 Oct 2025 21:25:02 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e0cba99c178866db7cecc72bc1b1782a7318fa94a958554086a4a8278dfd29`  
		Last Modified: Fri, 24 Oct 2025 21:25:02 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48ab137a80d6927ae05deaaf62c74821af5c77cd70ac6fbc35a87766da65476`  
		Last Modified: Fri, 24 Oct 2025 21:25:02 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c207f6813b9f1daf97981c1771a31d7c23b49f5a11481db911399c038ad5b7`  
		Last Modified: Fri, 24 Oct 2025 21:25:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c70654f8b2e07220757fccdbd3e62fb1d9d5ae9203b739cb791ddfadd8baf`  
		Last Modified: Fri, 24 Oct 2025 21:25:02 GMT  
		Size: 484.7 KB (484683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79cd6ff589db9e4d4c558c7d892ebd7c10ea7efd3c33177379f2e12d0bc68a0e`  
		Last Modified: Fri, 24 Oct 2025 21:25:04 GMT  
		Size: 12.9 MB (12911935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b570f5891f1315e5ef25b72d31a20f78b3c331f14e2afc4c9de289aae71a8ba`  
		Last Modified: Fri, 24 Oct 2025 21:25:04 GMT  
		Size: 357.3 KB (357327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1109ac0f847a85136be7aa365bc260e6a4552593de92f8099a173c23fb2c7257`  
		Last Modified: Fri, 24 Oct 2025 21:25:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accb036a33ef5ae8af69a63b806cc5d6030a0f0b8592037afb95bba23f920e3c`  
		Last Modified: Fri, 24 Oct 2025 21:25:06 GMT  
		Size: 4.4 MB (4375625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c42a28fd0b61a454a19d754fbe68b603ee8e3312b483c4a95554218dd3a62cf`  
		Last Modified: Fri, 24 Oct 2025 21:25:04 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32795864bb6ecd8db7774c24482d402b04c3f9fd39e2a0d5e801b1d42b83fe6`  
		Last Modified: Fri, 24 Oct 2025 21:25:05 GMT  
		Size: 10.8 MB (10824444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a17c0f2943d5b0ec87718b7c769e51ad1384eaed14abf92eee9e5781f76e11b`  
		Last Modified: Fri, 24 Oct 2025 21:25:05 GMT  
		Size: 352.3 KB (352304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b0ba206cccb6efc4e7a481cc5cb07b3bf784ccb0e36cac095f8830535eb21e`  
		Last Modified: Fri, 24 Oct 2025 21:25:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0af2101d00917c02e7571448c27a00614b2cf8c46e2b92f07010f5ec0595cf`  
		Last Modified: Fri, 24 Oct 2025 21:25:05 GMT  
		Size: 361.3 KB (361286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e873a2b334a8b274ced447b378ac5a0694674965d2c6cf4290f435d5cba926`  
		Last Modified: Fri, 24 Oct 2025 21:25:05 GMT  
		Size: 377.5 KB (377461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1714405209540010b6baaf751b4d10afb06520e357fcdc4d93f1f4bb6136b338`  
		Last Modified: Fri, 24 Oct 2025 21:25:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
