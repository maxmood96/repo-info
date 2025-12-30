## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:e3d76255c0105123c24c4f1777801836a8f765b8f223611b4671a46af438b488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6499766008cc053ec0b912ab66f23ce159e90bc18dabcb983bea84e09bfb4d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2604b1395cdb6aeee4e5890085b8fb3d04329bba19f625732b834e8729482f69`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:00:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da2c912bbc072214889aeea785d93b1fd8aa6ac61f78f85b74b1a2c7bfcc997`  
		Last Modified: Tue, 30 Dec 2025 00:00:33 GMT  
		Size: 11.1 MB (11105115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ff0255c58351a2bdba00dd012ac2e5cade79fbaf9d1df40944d6c30c6a501e`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435192cbd31c304b5fbac1df842572bae61d4fd458e10413c8141aa34964cb6d`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29481e40463e9c197f580cd03ddc64c30c46fa1ba531cf4869bebd8d7d0200b6`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 101.4 KB (101396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0121127037c15088a06f5d4cc6665309b3f83687431cc5142ec69c3c16e9318a`  
		Last Modified: Tue, 30 Dec 2025 00:00:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f83b90058f681f5053a1593fc0a12f4856716795661306bfbc724002d56aa874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46354a8d2d79693e43d1445e84737548a1c54070368dac19159b6f8a606c3a57`

```dockerfile
```

-	Layers:
	-	`sha256:d6ca80cab20a5068344a3e2cc4f3a9d28ce32bb29b29ae87e3fa44e15d05fa59`  
		Last Modified: Tue, 30 Dec 2025 02:08:32 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e34a7b7174f53501b30b764d19c594a3452293501cb17a2c945c2de3051d4852`  
		Last Modified: Tue, 30 Dec 2025 02:08:33 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:539dd8660e2085bb168825edb74d4ed15382a70e2c498682da2b9efc8749db51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b282bd03ed2f4cb666de301ace1692498c449a676a3e2c09c050d43280b7a47d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:00:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:00:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4150bee3f59a90f4911382dc6222dd13cc4f90ea24737fa822fd838c5c900b89`  
		Last Modified: Tue, 30 Dec 2025 00:00:52 GMT  
		Size: 11.1 MB (11106058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328a05363145dda7feeed31d22415cd120633e3b81ff7951c64a84ae766a7911`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1befde1ef3c3cb2133d055bf2666550d14799515f1d229a8dd35bb2678a0198`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8894397cad319a6153574c231eca833c7decca9aad1ff7f76c04e4aa734ce365`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 101.1 KB (101115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f061a44f9b67b704e57c1c4022f0f59aa038e70373c788ac3694c4b6a50689`  
		Last Modified: Tue, 30 Dec 2025 00:00:51 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9689afe7068ec77cd86564703ac070ca70b7920e316aadcbfed21cf14199e90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc0372e30b2dc423cbce0c822c721a46631073ab465a819eaad98fcc76bb19a`

```dockerfile
```

-	Layers:
	-	`sha256:48e4ce2a888502ee2eb216d44b41e5d56c20fc09581f399712611354271eb53d`  
		Last Modified: Tue, 30 Dec 2025 02:08:37 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e192cf3fb3f567c3f4bffa267e219ff497105ed5a570a9011162858883b82d5`  
		Last Modified: Tue, 30 Dec 2025 02:08:38 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b412ef6ea141b35d048e28eeff4fe19392ec52c81625d8a03f10763bc8381a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998a4ceda4a3ee98bc31128d7e959463d63b1bab6339855f76e607d7b810ac60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:15:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c030937cbbfb99adaf86783a860ed5d3cebcd1379d49c4e97853f3c1275263`  
		Last Modified: Mon, 08 Dec 2025 23:15:28 GMT  
		Size: 11.5 MB (11500413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805690f6ca6c5f3b783b7101716247b76abb6269b102b76142bbdd7f30da9a05`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46f35f9e3e3ad94601a7da1c16987fdc97b474cc01eeff25d712e4981dcbadb`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6664cf221203a95a3f5caa3fcee991c45d0adbfec5746b52600794de16127980`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 101.3 KB (101264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc295741e813d317bb24d92ab162ac433d018b9c312da7351fd0fe4910911596`  
		Last Modified: Mon, 08 Dec 2025 23:15:27 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73f0a417e354d3934993bd9981e3ff5ab5cdab551b690bd1a8b8cc43a5d7eecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c9c13fb82aa274bc9b1f02e17f76cbefb5e69a02c99312ab68bbc3d1962f1e`

```dockerfile
```

-	Layers:
	-	`sha256:d8676d57bfa7ce1d1ca06c7ce2221855bc19fc07d1a4c49ce60f6d934b9e718c`  
		Last Modified: Tue, 09 Dec 2025 02:08:06 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:481798e95db057aa84ef00b287c2a69c2566950f493f9240abfff8a2e6a73c5d`  
		Last Modified: Tue, 09 Dec 2025 02:08:07 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
