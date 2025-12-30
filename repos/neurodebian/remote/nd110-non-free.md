## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:19e070721f6f446c6f0715d7a61ca345bec983c48b6d8ea2dfe1df6ed9e0f01d
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
$ docker pull neurodebian@sha256:d06d9b009045ce17aed7bc1da254d287d715f32c947bebcad1e1ba96f1f4dcc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004ed954cc469bf5e178cff35d5b19a7b30c2e172bf68d68da3dcdfa51135032`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:48:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:48:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:48:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:48:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:48:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:025f128203ca36b1f5bbcf71b38334a935a5d6b64f4bfdd4dee99a843a623eb2`  
		Last Modified: Mon, 29 Dec 2025 22:25:07 GMT  
		Size: 54.7 MB (54699587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8889e3c7faa6d6d171a602343765c1bb2d3ddc22e9fb420eb2d01183142a0fb`  
		Last Modified: Mon, 29 Dec 2025 23:48:35 GMT  
		Size: 11.5 MB (11500382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c00dd733ab634e1040c63414271e3dbc90d4083e1ea35aea1107c734d992118`  
		Last Modified: Mon, 29 Dec 2025 23:48:34 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637d0fd86613028c0d493be53e1175fd49c16d1d2fed4537a278c6cdf6d1a3d2`  
		Last Modified: Mon, 29 Dec 2025 23:48:34 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23eea37c7a6d0fbee4b25a9209b88ee482257633368885a89aebebe589cbf1`  
		Last Modified: Mon, 29 Dec 2025 23:48:34 GMT  
		Size: 101.2 KB (101244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f25c9487659c3a94229aea1cb89be67d8b7cd68155d222b4f4d95d71895aa5b`  
		Last Modified: Mon, 29 Dec 2025 23:48:34 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed3d4e5fe0836c7e7d93649f74454cfc3e7d3266a8b16850955a4df96170cb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c189ef99cbb43b4c049bca8915f84f03075cb22ea366957867e60c90e871f205`

```dockerfile
```

-	Layers:
	-	`sha256:fdc816147d2d30ef493e94f6575d737267c0acde5258db013f714672b81f6cc6`  
		Last Modified: Tue, 30 Dec 2025 05:08:03 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e097ec199e12e39e44da45aaa639b5612a9c7bec5827a242ca39fbea98ad968b`  
		Last Modified: Tue, 30 Dec 2025 05:08:04 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
