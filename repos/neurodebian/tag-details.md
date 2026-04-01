<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `neurodebian`

-	[`neurodebian:bookworm`](#neurodebianbookworm)
-	[`neurodebian:bookworm-non-free`](#neurodebianbookworm-non-free)
-	[`neurodebian:bullseye`](#neurodebianbullseye)
-	[`neurodebian:bullseye-non-free`](#neurodebianbullseye-non-free)
-	[`neurodebian:forky`](#neurodebianforky)
-	[`neurodebian:forky-non-free`](#neurodebianforky-non-free)
-	[`neurodebian:jammy`](#neurodebianjammy)
-	[`neurodebian:jammy-non-free`](#neurodebianjammy-non-free)
-	[`neurodebian:latest`](#neurodebianlatest)
-	[`neurodebian:nd`](#neurodebiannd)
-	[`neurodebian:nd-non-free`](#neurodebiannd-non-free)
-	[`neurodebian:nd110`](#neurodebiannd110)
-	[`neurodebian:nd110-non-free`](#neurodebiannd110-non-free)
-	[`neurodebian:nd120`](#neurodebiannd120)
-	[`neurodebian:nd120-non-free`](#neurodebiannd120-non-free)
-	[`neurodebian:nd130`](#neurodebiannd130)
-	[`neurodebian:nd130-non-free`](#neurodebiannd130-non-free)
-	[`neurodebian:nd140`](#neurodebiannd140)
-	[`neurodebian:nd140-non-free`](#neurodebiannd140-non-free)
-	[`neurodebian:nd22.04`](#neurodebiannd2204)
-	[`neurodebian:nd22.04-non-free`](#neurodebiannd2204-non-free)
-	[`neurodebian:nd24.04`](#neurodebiannd2404)
-	[`neurodebian:nd24.04-non-free`](#neurodebiannd2404-non-free)
-	[`neurodebian:noble`](#neurodebiannoble)
-	[`neurodebian:noble-non-free`](#neurodebiannoble-non-free)
-	[`neurodebian:non-free`](#neurodebiannon-free)
-	[`neurodebian:sid`](#neurodebiansid)
-	[`neurodebian:sid-non-free`](#neurodebiansid-non-free)
-	[`neurodebian:trixie`](#neurodebiantrixie)
-	[`neurodebian:trixie-non-free`](#neurodebiantrixie-non-free)

## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:647359a0e3b04c65407ed71ae98bf311015dc6351ce1266046bfd723a8b5d3dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:35574ceb37ca91de80abbdd6815ed29e44478d1ad459d36856f17f7ee3beabb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bebae1c91ee919a70f18430b28a97e7811850fb8f711dc2346acdb83b8150b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558ed731281e50967671e5123143ba9b2cba73fa46d0cee98621c87450dd55d4`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 11.3 MB (11273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41efe1ba66768ed6c9c43b9af5ccb4961a74ee5a906c297cc80cffda52e3c6e`  
		Last Modified: Mon, 16 Mar 2026 22:44:49 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4790fe07dabd225b97a3f9a580079464b939e596faf06579f252559be16329`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc03361278813bb6b31fec43b564853d61c13079fc6724335dc961f66779519`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 93.4 KB (93409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1466afcfc17b7ee96e0a6b1c09ecf1fcc709ebcff582fcecb2fa7d065ba2017e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d193e96b89229f06b28307df190bd9b8692b99f4dcde78eb585314ac3c5f08a5`

```dockerfile
```

-	Layers:
	-	`sha256:689b150715b573fc5fb2e3b916565e735a68f6e1a322ec3c6e778d512d0ebf81`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61f9a96712645ce27582d05dc383e7d0fb4fb13b19bfa6e9504a1d0887dc0da`  
		Last Modified: Mon, 16 Mar 2026 22:44:49 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a01078c9eb8c1e7fd57ee11c68293f9741efa081d30d321805d51eec5d83b790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d19b7c0d45277329c25319261c3854d59748cbb99f7588ced1e34d524e0a6a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:46:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c4a041ac3cf2034ec0ec2e477075196ce371500217068b52016ac4dce558d5`  
		Last Modified: Mon, 16 Mar 2026 22:46:51 GMT  
		Size: 11.3 MB (11252945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563b675ddf3105e2103781f524056d3b7b0c99405c7ddf46af08381f369e64fa`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12a85945c44d11661b1e745f474c92bcbe41f9132cdf7bd415b01f8359b7008`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eeefbc91a2bc0faca6bee196b8a167d97e3661cb76f8e910cdfaa84a5d3ab91`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c75243dacc212fe2354daeaacfd7a7d7d637dbc73c91b8e73a8082a2a6992962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b480485c5dbfabf76214101fd9df55df183077ce7ba9eee745dfc9990fbedb`

```dockerfile
```

-	Layers:
	-	`sha256:b72bd18dbef0fd2100ddebdbaa9c80885d77b573f841ee7267303ad95228a403`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0653dd399690d4843067b134393e348553f08b1ec935cdcda849d2e3f9fe9bcd`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:b9a2c6e0e1ba11ab49f4d7585f0f0255ee6cc0bae87904a7af3850a5a8f24996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b41b98a1d881353f602c9223e06772a0d7dd1cadf50bfb7bc32595bd6f86f18`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4d1f11986cef775c515d2ffb21a7c9c7a6a751e5c85c2eed40ecc170edbd99`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 11.7 MB (11692990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41efe1ba66768ed6c9c43b9af5ccb4961a74ee5a906c297cc80cffda52e3c6e`  
		Last Modified: Mon, 16 Mar 2026 22:44:49 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4790fe07dabd225b97a3f9a580079464b939e596faf06579f252559be16329`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c228f4f623ae80f3c928a9e5ce93f437ebf575441b28000d02efd381276fc1`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 93.4 KB (93438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:75972240751c0e35a608547cbd8177f73dff3268b512a3e6e034524994e4f2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64240f714dc778a97e25450a1e2076f52f850c677e4d66f1522f8f2742766fa`

```dockerfile
```

-	Layers:
	-	`sha256:c1a90d88042f618e14fa78567f2a536b4cc70779090772efd207fb0d3bc40d0b`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729b51ed60ef9ee92ab560ef7ebe04b68cf063b5a37f7525204d5949438ad82c`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:d85a1c76c4f664ed04bbac437e25e0737e0885dc7e8c920fdaa2d885be3797b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e20510eb85a49c92b795fab0d13a6d603c8409302a5c27850e354e4ee2d075ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da05d84add778f43b34c90e4eb213783d2c3b318a820b3ff886321cb4dd4d113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb4ab961a252192c5be9e8c63671378611d52d0f34724109f6e629836bc53d7`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 11.3 MB (11273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71cb2ca05722ac51a62f208f0db98f75733c1869a7b970b3d6e9728e6d7b6c0`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d5d1fe0dac7a522ec964bbd579a3b0357f6eec985f44cd5636d3c0cab7e7fb`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017d0fc0f54797bd2aba2050d3afe8b77d26b55aabfacd01a99312e7df2ff432`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 93.4 KB (93408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9358e6a3e29c05f7244211073d6120f0badb79b3c9ee205e705a6704a50bd`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52993ddeb92f56ec85fbb569cd9eea5ff7b06d4150243ca04ac399dda36744d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d343663e9c398ee23f9a095c3bed5c1214d4b233d609fce3cb69d63b1f1a0544`

```dockerfile
```

-	Layers:
	-	`sha256:98001a2072223ab569f56d119e4012edfe4488e5826deab8f16af1e0ab31d25a`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26aeea9927fc53e73b9dd0087688c3a82279f1407cc38f5e5730e4d86255f5ab`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3679b10ad0265c286fe8cc7068ca88e407f282182e8032cf327db1187caa55f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688b188efc48999b9fb300c96d92b1a18961afdae960c7c4b544fb15dba1dbf1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b009f63f40fabbf62b60a8f36907161db1ec174f241c48c828d1146a4198`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 11.3 MB (11252967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efa4181c0f41640b93236856c6e171cd14af6ead409446252a8729f96de12c7`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7170d9480708eb8e65c37d81ebd0f0f0249ca85f420c027bf87f22d36f7972f9`  
		Last Modified: Mon, 16 Mar 2026 22:46:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f754ac6996f3755689ea24ef32042440f61bc620c7b4baca1b94aaa4e11daffb`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 93.5 KB (93550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a25894cc7c550827691f700d1c89634d25ff883e8732d06f5e611905a3820e`  
		Last Modified: Mon, 16 Mar 2026 22:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:711a3828e487b3c898c3848819d398337511b76fd48c38eb53bfebdc59e34b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6484e97b3ad88ab4b5e77b3cd1d740588372cb67df2e30ff6d0a402da4360dc8`

```dockerfile
```

-	Layers:
	-	`sha256:ba413f86b373ddcb50bf9e59ba53cd49381e972f4184a6ac602ae96f7302b323`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05392ad75b16bd0e7a41bd30945205e4723b6d7f97b7c4ac41f80c24eedc9bb4`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:784656544058292447b93e94fa60875fee7b4f9d332636b5c325ad7b8c8e838f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5a6e6d20a87459719fe2aa819e14feff590478d329837eb64e7e969c3a448a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c6743caba6d50541b062d9790addb6ecce85a4c2baeceea8f6548dc7cacbc1`  
		Last Modified: Mon, 16 Mar 2026 22:44:54 GMT  
		Size: 11.7 MB (11692936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76faf673c44e016ad78b4539dddd5832ff382ef7c8ce58fdd6ab08fb13188900`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e040d877e32d0e2211999898375fd545e15f72c45209a01e4336d4c8131700`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a633250fedc942f435168aab78b16d80bfbb5c995601098e8f5599d585a48d`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 93.4 KB (93419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f4af573ef43d21fac89dfbe526a4e2d98e7c1e3e7ed7857cb6aaaf4d344e0`  
		Last Modified: Mon, 16 Mar 2026 22:44:54 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d085ce204c95503a0a63907fcf810118c90ab52f1f3da4eaa97ed45beb8831ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd4cd459241aca69da0575888e08971d2480f995c6f985d07e6fc75b137fa0`

```dockerfile
```

-	Layers:
	-	`sha256:0099bc1cd9bd0c2a571c2c804a366023fb81ddbb6913a77746c1820ba406a749`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ef2b64859296ee30fb161693c2082ad9ac5309e7e3b6bf80cd58b6a83f211e`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:b07162317f3576e57c0a231275c3be89a7eec560586454a68bb9dafb2dc2612e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:eaa94b34440825b36470ebd3a1de940f09c274bb80710190773ddf60faca21d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64969621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3265263bcd137eb02da506d58004d92e6ca19a29e77b809189f5d2afd5416fe9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7addc24493c8608c9cd62cb82935321167819c42e6396ee0b50ae34be05288a`  
		Last Modified: Mon, 16 Mar 2026 22:44:29 GMT  
		Size: 11.1 MB (11103543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf364b196364c367d24576a4b428a5dfe1524e6bd8ba9491de415005b129652`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8131ae1500d9e304cf1ad89c44651cd788653a8336f2f0861b27781e0e41386d`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0ca962d7c61301ca3b7308e9541b6f4990c44050f750b9525e8f3595b533be`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 101.4 KB (101437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a59828173030030b9f314c164bcba3ab7831e50700deb9dd58bc28549c0d1adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9852f0db62428f9b567b24e7ab1973e2ae7ab8de6b1e5d8eeb3d3b33a9c3b09b`

```dockerfile
```

-	Layers:
	-	`sha256:03f0e517daeec27c2f94708276a96c087f14227589b673a11d430045abe5a858`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1518d9276747ff464704269b2f12dd3f8c9732358b28e94540da654ba8499b20`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6b52a09f21fcdc7c64878b412c6f2f7c31667ba15351368b16eda7b2ddc090e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63460443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e64406942027c7f6b7fad84f386aa8014248e14e52f775fbe0adc3723519ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:46:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6e080f9c7ea3b052d1126a5a62ad913ea1ce9d7b0ec8f2393e25faaa0285a`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 11.1 MB (11109761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5823a03f77e6c9c88255cff033dabc0e16b19b0971e7440ad5f20d07ebe8fcf`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0581fadb3841b2ea518c9d4ffd8fa5ac6bfa18613b64f19c5bd34d12a15f471`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be82e63bf5f0eb72466b0bbc5d8eba36d5cc2e3767b783bf4282d92f42e64cf2`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3921d812d7e0c90105325617887985f9ee7d4ba1ffc7f88eb1799507f57f704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74a5f76be424d58646e3b308d6e6b7963d895b3c64dab13fda493aaabd8097b`

```dockerfile
```

-	Layers:
	-	`sha256:c646ebe72cf4ed7dd38dc1eaee6a9a9f881eca0cf99a468eee0332587a088252`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a17d40c48290d8526721d5f252cc17cfb98f57516a990379b233598b54c57a5`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:a826de0df9722ab17679b90bfccbb4daeb362a91831ef276952e5afe09a2c1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8b02ac97f0f782b5b603637600e605c1db211441130c4f3aeeaec7eb04e245`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5bbef738f794ea891e894f8c5ee6ae58da2b56d30ea6431d5312cee5dba45d`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 11.5 MB (11502288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc289f123d617be55b09e2ecff9731379c753e8ce1267fab607b7f616403f9c`  
		Last Modified: Mon, 16 Mar 2026 22:44:43 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba98688c8232bdcb75cfff5f3805af2baee6c5877d7e54e2f74a45210dbe752`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b31a04dd7aed2e5afb0cca38d46e5d4b01b3f15b1d2ea78d3040cc1fd0b5b95`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 101.2 KB (101244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f5905d9fef07d3b8c0c86af9aed4b304a1f59d7d15c0dcd36fcad11232d0239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3256c581a83d9587378506d0e7d86476fc1cd3b66cb511b73bac7ce5f1f70acb`

```dockerfile
```

-	Layers:
	-	`sha256:cd73093764229b0167dffcf51175834128d32a03c90bda3cee4895316fd9c669`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e25cfa1360b254a50a28ca5ec0b66d2ad0d6bb424b8b5fe4723b37693d3cd7`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:173e30fe52835888cbf4c99df3681bab5301f764a08471f527a470f7b237a072
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a8fed007c8ece885918c9e11779506e9f53922c5e2949b9ca3d5cad070d8b59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64969912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc48b40d449a8162e5f1e31210abb1ca26c35c25d0d11be4114f8e58602bd07`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad505f834efce27668caf523e6f7448c25363a75b4134fd5057ba74e4a880f8`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 11.1 MB (11103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057dc6f686aa3321affbcc43d99644be568bfab4ec2debf4068d340c0fe9029f`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69924f4323530344676ca0ba491486a80bffb06e2262fc70becf9e9b918754f4`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7b65db8ace6319f2e3e23625af8178e212141849333549cf49d1afb74e287`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 101.4 KB (101395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655b7532e2534c4429e9d72442995afe02dd506eaa62f099f5097faddef6d7d0`  
		Last Modified: Mon, 16 Mar 2026 22:44:43 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a64fc4a8efe1f1b76724033f8342322cc816569ac7873003e430ea62ebf89f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84027ad37af861b608a24512e433b6dfb683b66853d9daabe19988fa537aef3e`

```dockerfile
```

-	Layers:
	-	`sha256:57129e95b5b1dfce52d22fbd3e4bb836b30c3a36cbe4ff668f233d5a627f6886`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc663e27c326eeb5745957332a05e5b6c071d629e203f62860b58495cdfabcfd`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3a079b4075c5dabbd9b4abd11084af8815b6a49706ff5df1c398180dcf9dec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63460850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e14712e78dbc88ed09b97ceac1a4c1d1d8f90e0fe337112d982d69d86f22f4c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:46:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:38 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba598ecaa898b7707023abdb9f68145125085d73ed0cc1e498b5c984cf457`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 11.1 MB (11109779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d292cabb5911ad56587ec971725c7bc8459bc5ea9d3368c65846e3764554a4`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7147b26ebc688bad683e055677559613181297547e040d516b7a298cae685f64`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be5dae1440567bafeefbbc1fc1b31ccfdf8a18b5038011af0c818813bf99902`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 101.3 KB (101268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f162b4fc51a4b5b479b1d18c642490d538aa92b39111f59e9de89331bfbc6541`  
		Last Modified: Mon, 16 Mar 2026 22:46:46 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a1deaf99a1978179d2852d8e7d6d5c1a826e8f10683d72fbc6ee379cecedb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f5bd82fccd9e2cc89023f6c7473564d0b8cfd784b3cee3c5fd96cf67dd6ed5`

```dockerfile
```

-	Layers:
	-	`sha256:2992a167cf67dbb060f8de6402a3ec5cf20427aa64cc3bda5b5b202aa51b5884`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360c775f2790a7ac33ce509443166b7249b5d1cbf414208d2f519757f59b24c3`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c2065da5b7c31855e11ab33e080379390113d959c865596fb08c1625c5f405a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d277798773164af88f8295a170e4711f25a7652e356b5512087570c4b62fe3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:12:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:12:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:12:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 23:12:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:12:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eb604cb66d26c3ee380b5e5770348a3fae759d8cfc0679ecd062d987b54a46`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 11.5 MB (11502008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc0b67b2c1547b9571f8a7988d17e001f4d68d9480f47e673256a3b7addae0b`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499562f5e1891ef1652cdd21ba8a3cae36324fda667a9a9e67f8f5cc2809b7bb`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f8aa7e057a9429c5ef7ca9093b02acc14e6aff4ee29dcaf5dc91570d02be5`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 101.2 KB (101249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc224a67a94f5073e5aab1ff260a71585c62c1473f97dd9862feba1c4ffaa99`  
		Last Modified: Mon, 16 Mar 2026 23:12:54 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:747588784e187ab85736d0525eeac59868067cd98940bbeb78a03d499f8104c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c15c128b27829cab9885becc338a4b19d1d8af4a5aa62eb5675200088378bba`

```dockerfile
```

-	Layers:
	-	`sha256:ebf0118d435c51bf0e581cc838c229dd9ca96226c60565d31b430c3453c35197`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:240454d82d04734ac54e35d69828aafd5e4128fdc67a301c7dfd2af44286e651`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:d3cd7ea9d9eeb9f2423fb9b97440178ae4fb637aea76e0e07106a206871fca80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:6a33326f00f0247e8a86c6c5e525ce83044392327a92a047297df8ef21d82dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60099811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e1a591c414bc482fa924fa687ae634a518814d22f455252f9eabc686ad018a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19357bfd71af09e26afd7dda402f901916224b7f700c069748c3186e8a918e6`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 11.4 MB (11382276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a99dd4cc6b98f202f039fad4aabf18786db50c45be9db53232d5231a40f590`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395e28d0b266a4a76b9155d01cce9cdc54f733e56c864043461f3f3af76f0643`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6c3e9cc93a96286494c5bc0808475fb4248df11dd85aee6ea49c4e20d234e`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 89.5 KB (89542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ba77b40fd9a7a932846c9a05fe2e82df03cdf4d8959134f712a7f8831e80c567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b2eb6628d7352772ae89fc9b519a81ae5baa393075586733cb3d6a1ef6839f`

```dockerfile
```

-	Layers:
	-	`sha256:f4444392266be94a13827e0ec63f58418b7c90b3bd1a894b6815d78ef8b2ca97`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 3.6 MB (3553690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11803dc5904dfccb517c17a6e83058590391274e324b646ee5a4eef4a258da4f`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6be5f297664170200d8ac0937e546dd1a4b4dc54650dde9bcee18964c2ed39ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59829690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8448827db583be8aa12200b44431d3da397860efb7c7379a68a05be881d6917e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:47:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1060b9ae7116f7c7642ee0f134028775dc85b210456446a7360ec215e4aa3a1`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 11.1 MB (11077549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d4642c95351147493373b3c6d23cb24c9914c2e5a358ab85b997e2457e266`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c6d9393dcb8dd01f79423a27bf1eb4d94e50724438523de1ac4ccd531f49c9`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3e0a8eeca03a0729195a88598421dcee62e4f7385b766988d2a3278f01edff`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 90.2 KB (90175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9917bebcc174c3fb62551d9e06ea7706f134a2236a457763dc19baf60ca71e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05ff510fa94570b01e9dd38208a06e4da9a60c58eea82f5bac5eb35aec7874e`

```dockerfile
```

-	Layers:
	-	`sha256:25791a8098cc1bcc1860275ebcfa3a49b95a05f96b0540be4380ddb5deb697dc`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 3.6 MB (3560491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42c6c4d4e082972317af2857136fd78165090d50b9aceda587ea8dad2e387a0`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:776f0a4cf196469edd1c851133fc5c34e44f70d8a38e61f32321bd870f516d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61618147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9506d730230c3f5e3d3a8c8de7ea00d4cdf7ece38c7a1e4eb7db186bd8a9fc61`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:45:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1c3dc0cb48442941a53e86451485d9a7514b92f1a62f491a2738ce3e48e9b`  
		Last Modified: Mon, 16 Mar 2026 22:45:18 GMT  
		Size: 11.6 MB (11605589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abbd68e0604fee7b24a7a2f60b00c29396c653ad267717758455bc10cc5cfb2`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca5074ff0875763fcfe5d4157c1b0b9aa108fc6841cd633f11f9ce1e870e3b`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2972ad1aa0e948b52f17c59f2b55233b5491fc22dda736f60ca8e5604ce27ad`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 89.8 KB (89781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:03cf1dd1acd8dd7beae6a63515a4ad13a05931ebc1e1b28a460439332ee9d349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242d15ad66106b470031d239f7537a762a2890144673c52df58855217a0c3a0a`

```dockerfile
```

-	Layers:
	-	`sha256:14d5408797509bc3f51507c038fa9a76e930d3a82c42f3f2c14126d64c942ac3`  
		Last Modified: Mon, 16 Mar 2026 22:45:18 GMT  
		Size: 3.6 MB (3551641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d6e2d3f96a3c7116644163d926b1386ec956c3fc97fd9bba00874574cc30c4`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:9550343ea0453f33feee4c83335d02469ffa6f6cfdf7689e92ae44929590402d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7cbcb2018dccbc119decf18339c40bc9fc736bb14cc8d74e98c825cce5b86041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d0d88329284af82434ebccf452c75e6628d4559605caa81af6af292e170fd7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744a6b4b4a9684cbb11e9ecdbc9ede0197a160227d21c42838cc3308c6b4e0b9`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 11.4 MB (11382299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1875139f86f2f68b13903493d1a046622fa09ce497f13444a0e1eb58b29425b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd243b08ecce031850e503074d833e0a24109b4960944c53a4557e51408d7b3`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3886fee5d02b6836fd7bd2c60ebd980c0e65314ce8565e7d96cf232f1071be5`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 89.5 KB (89547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e3da227b0dea7161d8bfd6d2aff718ef57225df903c4973ca36f2fbb71beed`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ad337e08555537483a7bb9dae015c1047c32d396af9afa397e1cccc55def0d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab46e1c1cc371b35e4b33ebc62b0d136edfb65dea896fbcf39af8d63b9571b`

```dockerfile
```

-	Layers:
	-	`sha256:f1b9bb67f26a56f3cf50f6861586522053195a7d15f848f0b445467dff782b7a`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 3.6 MB (3553726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f18dea4b7f0760b82dec582a851fdc534073ead289296d607451d97474b8888`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:677065d982d885d27b4eadb807570b22f44f2983db1ab259f5341e3f6e2247c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17fc94e4ce0bb45d3fe9fccc40219a8557e5eec5bf6c293554d5bfeb39bf596`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:47:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3e975b0fee3e37d66bd1496d9c27a06cbf22bb0145e1a1b09c557d7dd58e25`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 11.1 MB (11077490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404e6c74fa835fce831866b24267ff623333e069b8168d66628b785bd9746135`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d66d0e5643e22e5a105441040f5129d783e8cc3c759f5762fa7d9b9c1a9cf`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2ea8027d0eacfc714d35030b0534a0dfbcc40cdd15272c2198660c4b64bce2`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 90.2 KB (90204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c39b8d27f969e6e4b7616e229fc92dd58936cbfc8e6f93f70c51a16c8c36b4`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5abc3a2fd1c35885ac1080ce17113e45a566e09a424e06756036089aceef3ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06df2e2f6f779a1f3b7df9552310fc8ea62db1865f702b4be4b5fafbc8f0cc1a`

```dockerfile
```

-	Layers:
	-	`sha256:6b649bab6cf90da66935cd04a8fc3c09c874fc12a51043877827c9b4377ddd74`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 3.6 MB (3560527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60edffc23fb055179a0c8e87f176083693296ef6458467bbb282edb5a806551c`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 16.1 KB (16098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:80b364add1af2faf7bc55958460e350bba3e549e243e3dd8f54516b317d8748c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61618521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8358e4bad4f20174ba84ee3b8c7e93ce05e151ddb68138164b8664a2567b4f0c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:45:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30659db903268f5dcdf0fb4eae9842869002328cea186cb0491a50b2e3232e12`  
		Last Modified: Mon, 16 Mar 2026 22:45:20 GMT  
		Size: 11.6 MB (11605539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a6299c767a6b8de3f66fc6721068e6b86ace4c45d34a389016404c8cfa0778`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fbd7ef8ec04b0ac885f12960dcbfd2785562e6a46c1c6b4716ff40129bdd31`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca67de4ee3edc48b043ae4ddbf1c9677a3815215d1b2ff5e195b2daaa8f528dc`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 89.8 KB (89760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4595f94962f4c142429e3ca0eb002960df4000525b0d2e60c463b0f91934477e`  
		Last Modified: Mon, 16 Mar 2026 22:45:20 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c68211d63100c3a2c47090cc28977f44a5434ea9903be03f237aa1085b09292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61c20573f9eed374fda7260fa480dd9599fb4041f80a529e8886c86ad2d5c85`

```dockerfile
```

-	Layers:
	-	`sha256:7c214acaa1885f2699e93564c144ac761cbf5feb7121bdbdc1c20b0b47036251`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 3.6 MB (3551677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308b361b3a3fd980ba8054456a0fecc5548431fdfadeddea39b63351eaf39930`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy`

```console
$ docker pull neurodebian@sha256:a6f405f7ce0df315e79e2816670d94a410acab25933e5a44570e827fe4abada8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy` - linux; amd64

```console
$ docker pull neurodebian@sha256:684f89bb320fc15f269d733cfc19ed0b5c1f15f199d940085a3c02b90d82831a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebb4f514f1106446659c0c35b5cc154c33519bede72d75513eeea1e81f3011f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2863a40c7a7170ba503ee516d26f3a9b818e2606f0ab87535ae76ac0536c121`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 3.6 MB (3624431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547e46402d925046cbc9b8dda38ed4b4ec4ca3f6d1ff4f41bdcad1a51b430df5`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186cd36fecf717d7daa1ec85dd00593dabc4d1aaca1422a24f4c94f4be810c1b`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b72342ac61240026a61da0af1991417b699c7c5b770c54de65b56cc8fc5094a`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 111.1 KB (111090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:050a384cc4ff3ef04511d6bc797ace854cec23734e8230395615d68d79fd7665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fde8449d2e512592b6d172bd38f04836912e06bd08a3e7e4d5797564753d14`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6a29f65124fca407209fed2dffb3670b2dafb4eac073c87b2e3a537485f8d`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c407f459a18d56ccb69cbe43ea0e204e87401d236be87a31ef1e52b5672d30a5`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:56de5ce50bc6484dfad202db32b89a2f2ca4d48557aa48e4cf11d390d6da73bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913e7ec62ad9077f24a0b24e72ecc4fa55fc5e7b77ce11f79f53bf152cb8eec1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:35 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:36 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:36 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f628ca3d20e1c17214b7d1cfb648c745e7ea7a5fc3188f05a7a757a2de998d`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 3.6 MB (3604788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80793066cb18af083cfac67a17a06c1e4afd12ea6ace3fa8f6f8a613d469756`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2368eee4161f30a527478029668d0d63de762edb4a59fba3555fa62c09279eed`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3674a38a9279ec2d8a0bb18ed63f4e177a930c5e9be7229b354701d6769b50`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 111.2 KB (111153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12e4211b6e6d2c9a0ea2b79782e147901a46b2ee80063c345077a1ec63b5cd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8c580742abfd21791b0d471b0ce3169207288db6a9055b3b11eba03a1a593f`

```dockerfile
```

-	Layers:
	-	`sha256:391329d2b648bdb436cd1b6af1bdfc3a3143bfb69f62a4fb083a16013a6ae01e`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31201397be8aef44a004153ad48cb4a0c7c73f929badb242256dcd2610935155`  
		Last Modified: Wed, 01 Apr 2026 20:14:51 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:c97324dc5cee79ae5805150419af6a22c0fe79ddaaca717e33357f6520c371bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f65ab94de2b8eeb7ce8e3ca843ba825e9c7fe90ed9b6634fbaf551a4d61fbe26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce894af6d2b00fbd05af4826250646684dcbb657ac827263cc9e0f14b863a70b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4394bdcefc6fa3b661b40e6eb591c5f4d4a4948bb9f94efc8cfb2cca63ab0`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 3.6 MB (3624440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe5dd49d306503d46bfd8860d908db1bd43054f51630df3cae246cda80ab538`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc8033217859346bf8a7b9a474edfbb809fbeb1a627bad48117b921acadae46`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466de1c292093141aee6e0b2e28cdb5dead9eaa5b899e28405a08326e0afbcda`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 111.0 KB (111028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1816e7a377a6dd0ca7d84582d786a62e2eae934a80a7d10a4968032c0c09c847`  
		Last Modified: Tue, 17 Mar 2026 01:43:52 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3327cf1ff11761f7d3fd4c86c31125e43e1d212147fdd91197fb422bd6610d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42da9986bb0da24b6b98d1bcf5be809650d9e940fa3ccf81026bdeb9108e866a`

```dockerfile
```

-	Layers:
	-	`sha256:044f0f60135fd32871cae06a72337f371a8c9006584356dc984cdd534d47b695`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7e31bbe852e2d1e841c91b37d8c7c1547bbaf7a57650644745cdf4181ae15a`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:394de8222acd546223af23904aa1ed27bf129b9229cd1870d371c159048d9a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31325283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51928ab1653f2d374fa511b1c7850b344a4e33a52a58812c7a8ee6ebf75f6a8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 Apr 2026 20:14:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:14:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4019784363cefaaa0608f44a7c43404f1b49123f5490bd18ff61d334344dcd03`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 3.6 MB (3604713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac14a880a2f296e4a09554d5f7d84793b55df94e7b4c331567c990b3480470`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7b185bb1d3b8189d1af6df1aeeb5e439b37bb515e3842af0b98424dbe2a5fe`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736213a2d43cf0f24c9174b8fb31963c318bcfb6708f00ace854f394cf5e34f3`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 111.2 KB (111166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a57c1c1d3cafd08cbb99d7170a7ed6f9d171ccb1bebae7ca7ed6a66cb514d61`  
		Last Modified: Wed, 01 Apr 2026 20:14:59 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1c5645de0a996722122f4c9fe0b9ee1feb9f9fa5e235152031b99bd71d3229c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb25718c8f24128797396d2c2b144f786d6ab403adfddb2df3c99adacea0df61`

```dockerfile
```

-	Layers:
	-	`sha256:0957159b9394ba37b209348e8d8a8338cef651a44bbe52536707849659184f84`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8676f87d12d1ed89bca09e6bcafb4093ea3eeaac8b18ba0f5f60591dc4211c78`  
		Last Modified: Wed, 01 Apr 2026 20:14:58 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:fe3b81e04ddaa8fd78726011a91d9f0f3f695fa07219d8ac602692a403a1cc04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:38823791da050edc5eb8f6fa536c491e2c8ca8005a8cd254481432b3141a3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59683732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6669aa02982813b549bb24f0efb1f87ca6a0a484f7104aa429108da356fa2a73`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ee88a3265bdb3d0530757a6461555d707868eee596f1f998298c190e3f644`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 10.3 MB (10292915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef101ccc9e6d95edb0e8ce65d3ffc82d69cd46fba656e62ca670d99e42249eee`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923b7d0ba6be692a9bd27955a6d7d130f86d66f9bd9df859a7f4be07e7087af`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e64cfd12a5f906af9cbc34e19af3580efa8f976499c5ffb3c985c022c8e508c`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:85b2232400c1f431ba8cc26424452df9318c1b02c53f299adf17432331fd5610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd9443133cc72a0d386f5b16557cb5a52932d2afee8c29b96f75ff0e5d8423b`

```dockerfile
```

-	Layers:
	-	`sha256:a6a58199c85a0132c55237be5d7d27187876d7ee3f1416b14fcaaa1cc7ee98b2`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73bd9c5a29d25f9da77b0fedb2979737b707d74c6ae43bad84b50e6e266c99f`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 14.2 KB (14250 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:901b7b25ce96aa90447603c3515149806a5d64a7cc6e67690efb485ce28b27a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59836813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7795498bb7dbd01166c2b326da248bbe4cc5d0d490ea9050315b99c8419dc1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df775a7faa43f7f7252f06117029e4dd5a5cbac50c51890b0d6d3cfd8405b0cb`  
		Last Modified: Mon, 16 Mar 2026 22:47:03 GMT  
		Size: 10.1 MB (10077947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58a0f5113878ee3b18eb8ee6a2439cd3d4c0311b4a2b783a57ae7f91570cc26`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b5bbcfe31d9f345176f105df35710778037261c4780ab6b5767185e16411b5`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d101e6915fa0def37b1a745ea4ff99954c71a09f8a1d36fba13a830235ee2f37`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 91.0 KB (91012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:600774acdcdbba3fe13459a4441324f1c491857eabc5df29fc63bd89b791f89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9030a439cbc6343ab6e5529fe5513af33f6a1ea35920d12615cdca32dd0fa`

```dockerfile
```

-	Layers:
	-	`sha256:8a045eefb957935b32df8b5f3f9841257d01411ae260d6403aa68ab7a16f082b`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb422972c47227f8b51f38ac744f2746fa68bd8246da0bdc0c4a0369275bebfe`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:ed5f194f7c2abbaae636062e9e03e383495555d870ecd8a7a204c6ed0031978c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23b782793b45d233eb4c1cb7011a7c66e56885f7e893ff51d4360c3b1dc6c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e327d8697f911e128822f25c7c3a0b25075fc412d07427074366c4a1dcc06c6b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 10.5 MB (10467149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa825e034237965757272c1d539290ce5f98985c6f606968b5a15d07e4230c97`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20d220105eee5bb027f81176948567b8ebcf7b0d3e64a6f976fed93b757696`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2929ff200bd80db2d78e35ec44a161b98776d7a2a1f0470e391c0712e3e5e1e1`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 90.8 KB (90762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4088065eeaf99003a949cc4c86cdbb851614c39f97e157c3e608533525003145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973923d9da01f833bac03850854ab5ff2f09f4b5440e89c3cfb9351a84d2a6c1`

```dockerfile
```

-	Layers:
	-	`sha256:0e6bf81854fe1d14a17ca159eb87e1f89012c8acbbdcf6c314097a44fcc1ad9f`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60759a73115e1d8354102c4f15b6ca89c3ff7e7c3ddc0140a9e3ae91e615ff78`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:70ce97f6796d0bd1e6ea7d563d93fd9f0cf0bf63a8e127ac6cce87afe7284bf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:6d1fc426c529a7179490427ff1b139fc09928fc88d60bf4457cbebe436b25e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60149970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744a29bf828d9a897f7c0bdcd7643b2452b36aacb4109564bc3d3ec0b0650f40`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:44:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:224b32b461470cab0a5b83292cf42319369c28ec8beae34418e705d6d0530bb2`  
		Last Modified: Mon, 16 Mar 2026 21:52:47 GMT  
		Size: 48.7 MB (48676470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435378e6edfc7c12b4ed65b613af023d57fa606a0b2de1de8f50080d443f273f`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 11.4 MB (11381178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1875139f86f2f68b13903493d1a046622fa09ce497f13444a0e1eb58b29425b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a527387d1617429a2a96c43d1624a92101db3a1b29ec5eb4b897ad7b8dced4a`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda3bfc8cab99ab329696b3337e16a74b175a67bf860a8a5e054ecfbf0501e9d`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 89.4 KB (89418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1d440ccd085c26be74202165cc3b1128954c2b3f47733236a0416fd8fd6ee623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77c3d0f0ba756177d09af10cadbeb017c39ffdfb8f4018efff68d41a8ecd8c`

```dockerfile
```

-	Layers:
	-	`sha256:3b9bd7caf2ea52ea4337edf4c858d40e68bb08754805df3c001c44a1c3eda640`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 3.6 MB (3552870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39e1f533aa58bd0505780c3952c186eaefa6e16ea70768cef347041446e1574`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a5602e206119d499ae31f37ec778d866c2517bc33939bd34c211c16addb7ead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59885100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a6633bede2c6667f856a815cbfc4b9ec319fe7184a856765b980e6d2666885`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:47:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f8aa045b0b46f2987d2dfdc549957d53bf9eb7148b1452027f1bbe82759ee08b`  
		Last Modified: Mon, 16 Mar 2026 21:58:00 GMT  
		Size: 48.7 MB (48715175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5418123350c32272b46788d05723fde818111cd59f2e38fcc932ec52bf8fe8`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 11.1 MB (11077011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413fc3519da5d42e3e7a4e0720341191628348b309bc6ca103ece3f91c45cd1`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb5599a29b53a0abd1361980e40020e8cad1bc5b287ae4e26edd5449ec2b15c`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870365bc67ca6e2403c7a765994ce210adf4b8b4a446b30cf6e30e61908fa7f1`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 90.0 KB (90009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:083861651e2e24b282385211009a4b132faf832b34f12bec2441737e7994804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f442457820b74fd771de15f04d68e4b00d5f3b50f05cb0bb400375043dd031`

```dockerfile
```

-	Layers:
	-	`sha256:d7dae46320117521fa0297a784b4d6534e8b02a980fd8163ab267cb9ae8fbe87`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 3.6 MB (3559671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d4098ea9ca794fa9b81557858d2f1014c06c9b6c06489190f9ad2f087e3a0b`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:0620854eff36c1edaf794aa0c06278a96d50219bfcb7effa5a679e55b95bdb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61646917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd87c508951df3df21c5f3f516ef4b475b9395aa986826cf33c665918650caa7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d910d8b21d9682e89de3d97b422096e3120f61049a143cd139a1c42e9bb8b77e`  
		Last Modified: Mon, 16 Mar 2026 21:53:09 GMT  
		Size: 49.9 MB (49948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b321b1e66d39564c47555de32d340a791425b7cce9bb9cec583222c8d7ca49c`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 11.6 MB (11606315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40be60bbfbb52b308f7a3da3d6ce45f2b45d390b3a218b8962d5d180766adfa9`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5a3927c9a8ad3f0340e06b2184345914a8af2da8f0e0b9cd871831857de9aa`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a63559a329af0724eb71b76ffc8a94493d39318fe64600142629c2796050b5`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 89.7 KB (89655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15308b6f9290ae75c8ead47e44c0f9e1615b18562b59e678ef8e14c24e21202f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a966c7f4dc6dc87414338959c6433f2a3b6764d554b8a92280eaccc04454fa59`

```dockerfile
```

-	Layers:
	-	`sha256:dfe0057bfe8bce433fe945340cdaf4eaefe8fe9f9b3e138240b50c5fe795735d`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 3.6 MB (3550822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751950bfb2649acce0e08fbef36c572123014cdb7a355ba165830660ca67048c`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:401ece9b9b7a564428d1faa0c0d488a0ed344d7dcf45c7f3e2403fa74dca7203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:76e9e995f4c4f86904fe10306ac6088227b0f709013d27ebf02bd5df4430ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e19b5c754f97b7218621a2ad7415892efe2954224c83c2da86a2d5629da1d46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:224b32b461470cab0a5b83292cf42319369c28ec8beae34418e705d6d0530bb2`  
		Last Modified: Mon, 16 Mar 2026 21:52:47 GMT  
		Size: 48.7 MB (48676470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca5d772c892170c87d0a816d02bca5d34d5f7ca64e714e57c1490e7ed49f93`  
		Last Modified: Mon, 16 Mar 2026 22:45:13 GMT  
		Size: 11.4 MB (11381180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57469f7c59fb0fdcdd0b36b09dad92a22e9e27d58cbb3382c1cf96dea721f51`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534708c7790614b41fccb8d1b06f493d6f53d9ac328099d5fb668761e97f5b32`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e3dbe970409cab1f0211816b271687786f2f5c9fe9ee2102caa213515c56ea`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680101dfe5470fbe3518d073851e4e98819f1eeada5673af5a3d2b2306eb6cbe`  
		Last Modified: Mon, 16 Mar 2026 22:45:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b56c36aecfc51dfe3b41a340b400c25bebcee2404771369cfafb03eeb682072a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d987c886e7cac60b0a18a6cc934fc531b684c3bf9cac481f122b6bf5cd898814`

```dockerfile
```

-	Layers:
	-	`sha256:0d057c6c2a0dbc41f04d346d378fe95d149886bc44dfed5136278413370d47d2`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 3.6 MB (3552906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0c1add2756e6318c73674eac374bc148811486de0b783f5d373ae71030fd57`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:316a56e122edbd573a79a2de5f3d75de2aa40b0f0b076df9cb9078a8924ca94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59885398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af734abdcaae3b6dd42ab3ab31c9cc26f1b6a679b439ddb13fffa3bcae11c52a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:47:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:11 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f8aa045b0b46f2987d2dfdc549957d53bf9eb7148b1452027f1bbe82759ee08b`  
		Last Modified: Mon, 16 Mar 2026 21:58:00 GMT  
		Size: 48.7 MB (48715175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15f2120aa02b76483cbe03d606a903b0903900913698902e3d77a29d7314a29`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 11.1 MB (11076885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0488830adfbaad80a1040eec389eb3dc2bf86fa1dab231c0ed0d3048cfaea46c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a76c095666fd560b53498568dd4d4d556c26247b75aac3877c0460667b24d74`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4163bbeabab58b1e6d1b1932300651fbb20bdd6b1bc34dfd37cd2713210470ee`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 90.0 KB (90020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8ee29bdb6356fa7c9ff60276dbcec78e12070f393bf1c74149a42761b2b5f7`  
		Last Modified: Mon, 16 Mar 2026 22:47:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd2f9c32f345398ed26d176eda827c26cd495bd913f09b69e8712f2a094cf14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caf6b1e293c67fff7eaec5ae5f7307c77103c874b33811276b1fff822c47170`

```dockerfile
```

-	Layers:
	-	`sha256:98caa2b25a8ea1717a327cb56dd68e953776d481ec3ab95b60985979fb91bf7c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 3.6 MB (3559707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d6f034189525baf2b751d1e14ca27f8535e129f125bde3602b992259d4fc1c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f92cb038c1549da7e7606543cea1b37f5e33aecae18d51b680fe7b2962beee61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61647344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9097946a5841af837fd5d7a4bd991ec34712c47638a936b75fa670e1dafcd2d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d910d8b21d9682e89de3d97b422096e3120f61049a143cd139a1c42e9bb8b77e`  
		Last Modified: Mon, 16 Mar 2026 21:53:09 GMT  
		Size: 49.9 MB (49948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ccd876f6aa19c74a020294759acdeb35dd1245a040209f4ca69527dd7ab372`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 11.6 MB (11606313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce7e45512f12c2bf1b2dd24d3fa2554dfa01a69158f3f6f2cff4c673120960c`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12592a476099ae3908d871cdb1ce7a4a285d11322d73a9fb479161fb624eab11`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cb8f37b7cc492634b2cb567f2e78dd488a35a98fbe265a251a020534d44e99`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 89.7 KB (89665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07da676b418cdd0f4219b6c91a9b37116d8096542e34b7f98df066f469d8d1`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b51352ea60a625cb4386b46888d45f5533db3f02ae1037a9e158a801320f4be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baebd2f515e37ebd0dada90132cecfeeea4a30f763ebed5e184ddf44611eaa7`

```dockerfile
```

-	Layers:
	-	`sha256:c38239855257663e51b69680c2e3168694aed9b6b4a98221b20aecf6e193b98f`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 3.6 MB (3550858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc003d177c616b75b01582f33421075f7ef8d520b9fd75e138dca77a7829a7c8`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110`

```console
$ docker pull neurodebian@sha256:b07162317f3576e57c0a231275c3be89a7eec560586454a68bb9dafb2dc2612e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110` - linux; amd64

```console
$ docker pull neurodebian@sha256:eaa94b34440825b36470ebd3a1de940f09c274bb80710190773ddf60faca21d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64969621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3265263bcd137eb02da506d58004d92e6ca19a29e77b809189f5d2afd5416fe9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7addc24493c8608c9cd62cb82935321167819c42e6396ee0b50ae34be05288a`  
		Last Modified: Mon, 16 Mar 2026 22:44:29 GMT  
		Size: 11.1 MB (11103543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf364b196364c367d24576a4b428a5dfe1524e6bd8ba9491de415005b129652`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8131ae1500d9e304cf1ad89c44651cd788653a8336f2f0861b27781e0e41386d`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0ca962d7c61301ca3b7308e9541b6f4990c44050f750b9525e8f3595b533be`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 101.4 KB (101437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a59828173030030b9f314c164bcba3ab7831e50700deb9dd58bc28549c0d1adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9852f0db62428f9b567b24e7ab1973e2ae7ab8de6b1e5d8eeb3d3b33a9c3b09b`

```dockerfile
```

-	Layers:
	-	`sha256:03f0e517daeec27c2f94708276a96c087f14227589b673a11d430045abe5a858`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1518d9276747ff464704269b2f12dd3f8c9732358b28e94540da654ba8499b20`  
		Last Modified: Mon, 16 Mar 2026 22:44:28 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6b52a09f21fcdc7c64878b412c6f2f7c31667ba15351368b16eda7b2ddc090e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63460443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e64406942027c7f6b7fad84f386aa8014248e14e52f775fbe0adc3723519ea`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:46:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:20 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e6e080f9c7ea3b052d1126a5a62ad913ea1ce9d7b0ec8f2393e25faaa0285a`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 11.1 MB (11109761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5823a03f77e6c9c88255cff033dabc0e16b19b0971e7440ad5f20d07ebe8fcf`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0581fadb3841b2ea518c9d4ffd8fa5ac6bfa18613b64f19c5bd34d12a15f471`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be82e63bf5f0eb72466b0bbc5d8eba36d5cc2e3767b783bf4282d92f42e64cf2`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3921d812d7e0c90105325617887985f9ee7d4ba1ffc7f88eb1799507f57f704e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74a5f76be424d58646e3b308d6e6b7963d895b3c64dab13fda493aaabd8097b`

```dockerfile
```

-	Layers:
	-	`sha256:c646ebe72cf4ed7dd38dc1eaee6a9a9f881eca0cf99a468eee0332587a088252`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a17d40c48290d8526721d5f252cc17cfb98f57516a990379b233598b54c57a5`  
		Last Modified: Mon, 16 Mar 2026 22:46:31 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110` - linux; 386

```console
$ docker pull neurodebian@sha256:a826de0df9722ab17679b90bfccbb4daeb362a91831ef276952e5afe09a2c1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66307935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8b02ac97f0f782b5b603637600e605c1db211441130c4f3aeeaec7eb04e245`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5bbef738f794ea891e894f8c5ee6ae58da2b56d30ea6431d5312cee5dba45d`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 11.5 MB (11502288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc289f123d617be55b09e2ecff9731379c753e8ce1267fab607b7f616403f9c`  
		Last Modified: Mon, 16 Mar 2026 22:44:43 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba98688c8232bdcb75cfff5f3805af2baee6c5877d7e54e2f74a45210dbe752`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b31a04dd7aed2e5afb0cca38d46e5d4b01b3f15b1d2ea78d3040cc1fd0b5b95`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 101.2 KB (101244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f5905d9fef07d3b8c0c86af9aed4b304a1f59d7d15c0dcd36fcad11232d0239a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3256c581a83d9587378506d0e7d86476fc1cd3b66cb511b73bac7ce5f1f70acb`

```dockerfile
```

-	Layers:
	-	`sha256:cd73093764229b0167dffcf51175834128d32a03c90bda3cee4895316fd9c669`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e25cfa1360b254a50a28ca5ec0b66d2ad0d6bb424b8b5fe4723b37693d3cd7`  
		Last Modified: Mon, 16 Mar 2026 22:44:44 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:173e30fe52835888cbf4c99df3681bab5301f764a08471f527a470f7b237a072
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
$ docker pull neurodebian@sha256:a8fed007c8ece885918c9e11779506e9f53922c5e2949b9ca3d5cad070d8b59e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64969912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc48b40d449a8162e5f1e31210abb1ca26c35c25d0d11be4114f8e58602bd07`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:44:31 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad505f834efce27668caf523e6f7448c25363a75b4134fd5057ba74e4a880f8`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 11.1 MB (11103493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057dc6f686aa3321affbcc43d99644be568bfab4ec2debf4068d340c0fe9029f`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69924f4323530344676ca0ba491486a80bffb06e2262fc70becf9e9b918754f4`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7b65db8ace6319f2e3e23625af8178e212141849333549cf49d1afb74e287`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 101.4 KB (101395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655b7532e2534c4429e9d72442995afe02dd506eaa62f099f5097faddef6d7d0`  
		Last Modified: Mon, 16 Mar 2026 22:44:43 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5a64fc4a8efe1f1b76724033f8342322cc816569ac7873003e430ea62ebf89f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84027ad37af861b608a24512e433b6dfb683b66853d9daabe19988fa537aef3e`

```dockerfile
```

-	Layers:
	-	`sha256:57129e95b5b1dfce52d22fbd3e4bb836b30c3a36cbe4ff668f233d5a627f6886`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc663e27c326eeb5745957332a05e5b6c071d629e203f62860b58495cdfabcfd`  
		Last Modified: Mon, 16 Mar 2026 22:44:42 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b3a079b4075c5dabbd9b4abd11084af8815b6a49706ff5df1c398180dcf9dec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63460850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e14712e78dbc88ed09b97ceac1a4c1d1d8f90e0fe337112d982d69d86f22f4c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 22:46:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:38 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adba598ecaa898b7707023abdb9f68145125085d73ed0cc1e498b5c984cf457`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 11.1 MB (11109779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d292cabb5911ad56587ec971725c7bc8459bc5ea9d3368c65846e3764554a4`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7147b26ebc688bad683e055677559613181297547e040d516b7a298cae685f64`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be5dae1440567bafeefbbc1fc1b31ccfdf8a18b5038011af0c818813bf99902`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 101.3 KB (101268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f162b4fc51a4b5b479b1d18c642490d538aa92b39111f59e9de89331bfbc6541`  
		Last Modified: Mon, 16 Mar 2026 22:46:46 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4a1deaf99a1978179d2852d8e7d6d5c1a826e8f10683d72fbc6ee379cecedb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f5bd82fccd9e2cc89023f6c7473564d0b8cfd784b3cee3c5fd96cf67dd6ed5`

```dockerfile
```

-	Layers:
	-	`sha256:2992a167cf67dbb060f8de6402a3ec5cf20427aa64cc3bda5b5b202aa51b5884`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:360c775f2790a7ac33ce509443166b7249b5d1cbf414208d2f519757f59b24c3`  
		Last Modified: Mon, 16 Mar 2026 22:46:45 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c2065da5b7c31855e11ab33e080379390113d959c865596fb08c1625c5f405a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d277798773164af88f8295a170e4711f25a7652e356b5512087570c4b62fe3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1773619200'
# Mon, 16 Mar 2026 23:12:42 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:12:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 23:12:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 23:12:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:12:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ad236c87f3ff6b413233974bf5899e332a9ceee3a606736011b98ba6596c59ea`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 54.7 MB (54702245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eb604cb66d26c3ee380b5e5770348a3fae759d8cfc0679ecd062d987b54a46`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 11.5 MB (11502008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc0b67b2c1547b9571f8a7988d17e001f4d68d9480f47e673256a3b7addae0b`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499562f5e1891ef1652cdd21ba8a3cae36324fda667a9a9e67f8f5cc2809b7bb`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018f8aa7e057a9429c5ef7ca9093b02acc14e6aff4ee29dcaf5dc91570d02be5`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 101.2 KB (101249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc224a67a94f5073e5aab1ff260a71585c62c1473f97dd9862feba1c4ffaa99`  
		Last Modified: Mon, 16 Mar 2026 23:12:54 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:747588784e187ab85736d0525eeac59868067cd98940bbeb78a03d499f8104c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c15c128b27829cab9885becc338a4b19d1d8af4a5aa62eb5675200088378bba`

```dockerfile
```

-	Layers:
	-	`sha256:ebf0118d435c51bf0e581cc838c229dd9ca96226c60565d31b430c3453c35197`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:240454d82d04734ac54e35d69828aafd5e4128fdc67a301c7dfd2af44286e651`  
		Last Modified: Mon, 16 Mar 2026 23:12:53 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120`

```console
$ docker pull neurodebian@sha256:647359a0e3b04c65407ed71ae98bf311015dc6351ce1266046bfd723a8b5d3dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120` - linux; amd64

```console
$ docker pull neurodebian@sha256:35574ceb37ca91de80abbdd6815ed29e44478d1ad459d36856f17f7ee3beabb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8bebae1c91ee919a70f18430b28a97e7811850fb8f711dc2346acdb83b8150b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558ed731281e50967671e5123143ba9b2cba73fa46d0cee98621c87450dd55d4`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 11.3 MB (11273418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41efe1ba66768ed6c9c43b9af5ccb4961a74ee5a906c297cc80cffda52e3c6e`  
		Last Modified: Mon, 16 Mar 2026 22:44:49 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4790fe07dabd225b97a3f9a580079464b939e596faf06579f252559be16329`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc03361278813bb6b31fec43b564853d61c13079fc6724335dc961f66779519`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 93.4 KB (93409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1466afcfc17b7ee96e0a6b1c09ecf1fcc709ebcff582fcecb2fa7d065ba2017e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d193e96b89229f06b28307df190bd9b8692b99f4dcde78eb585314ac3c5f08a5`

```dockerfile
```

-	Layers:
	-	`sha256:689b150715b573fc5fb2e3b916565e735a68f6e1a322ec3c6e778d512d0ebf81`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61f9a96712645ce27582d05dc383e7d0fb4fb13b19bfa6e9504a1d0887dc0da`  
		Last Modified: Mon, 16 Mar 2026 22:44:49 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a01078c9eb8c1e7fd57ee11c68293f9741efa081d30d321805d51eec5d83b790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d19b7c0d45277329c25319261c3854d59748cbb99f7588ced1e34d524e0a6a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:46:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c4a041ac3cf2034ec0ec2e477075196ce371500217068b52016ac4dce558d5`  
		Last Modified: Mon, 16 Mar 2026 22:46:51 GMT  
		Size: 11.3 MB (11252945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563b675ddf3105e2103781f524056d3b7b0c99405c7ddf46af08381f369e64fa`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12a85945c44d11661b1e745f474c92bcbe41f9132cdf7bd415b01f8359b7008`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eeefbc91a2bc0faca6bee196b8a167d97e3661cb76f8e910cdfaa84a5d3ab91`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 93.6 KB (93582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c75243dacc212fe2354daeaacfd7a7d7d637dbc73c91b8e73a8082a2a6992962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b480485c5dbfabf76214101fd9df55df183077ce7ba9eee745dfc9990fbedb`

```dockerfile
```

-	Layers:
	-	`sha256:b72bd18dbef0fd2100ddebdbaa9c80885d77b573f841ee7267303ad95228a403`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0653dd399690d4843067b134393e348553f08b1ec935cdcda849d2e3f9fe9bcd`  
		Last Modified: Mon, 16 Mar 2026 22:46:50 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120` - linux; 386

```console
$ docker pull neurodebian@sha256:b9a2c6e0e1ba11ab49f4d7585f0f0255ee6cc0bae87904a7af3850a5a8f24996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b41b98a1d881353f602c9223e06772a0d7dd1cadf50bfb7bc32595bd6f86f18`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4d1f11986cef775c515d2ffb21a7c9c7a6a751e5c85c2eed40ecc170edbd99`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 11.7 MB (11692990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41efe1ba66768ed6c9c43b9af5ccb4961a74ee5a906c297cc80cffda52e3c6e`  
		Last Modified: Mon, 16 Mar 2026 22:44:49 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4790fe07dabd225b97a3f9a580079464b939e596faf06579f252559be16329`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c228f4f623ae80f3c928a9e5ce93f437ebf575441b28000d02efd381276fc1`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 93.4 KB (93438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120` - unknown; unknown

```console
$ docker pull neurodebian@sha256:75972240751c0e35a608547cbd8177f73dff3268b512a3e6e034524994e4f2a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64240f714dc778a97e25450a1e2076f52f850c677e4d66f1522f8f2742766fa`

```dockerfile
```

-	Layers:
	-	`sha256:c1a90d88042f618e14fa78567f2a536b4cc70779090772efd207fb0d3bc40d0b`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:729b51ed60ef9ee92ab560ef7ebe04b68cf063b5a37f7525204d5949438ad82c`  
		Last Modified: Mon, 16 Mar 2026 22:44:50 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:d85a1c76c4f664ed04bbac437e25e0737e0885dc7e8c920fdaa2d885be3797b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e20510eb85a49c92b795fab0d13a6d603c8409302a5c27850e354e4ee2d075ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da05d84add778f43b34c90e4eb213783d2c3b318a820b3ff886321cb4dd4d113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb4ab961a252192c5be9e8c63671378611d52d0f34724109f6e629836bc53d7`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 11.3 MB (11273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71cb2ca05722ac51a62f208f0db98f75733c1869a7b970b3d6e9728e6d7b6c0`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d5d1fe0dac7a522ec964bbd579a3b0357f6eec985f44cd5636d3c0cab7e7fb`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017d0fc0f54797bd2aba2050d3afe8b77d26b55aabfacd01a99312e7df2ff432`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 93.4 KB (93408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9358e6a3e29c05f7244211073d6120f0badb79b3c9ee205e705a6704a50bd`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52993ddeb92f56ec85fbb569cd9eea5ff7b06d4150243ca04ac399dda36744d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d343663e9c398ee23f9a095c3bed5c1214d4b233d609fce3cb69d63b1f1a0544`

```dockerfile
```

-	Layers:
	-	`sha256:98001a2072223ab569f56d119e4012edfe4488e5826deab8f16af1e0ab31d25a`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26aeea9927fc53e73b9dd0087688c3a82279f1407cc38f5e5730e4d86255f5ab`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3679b10ad0265c286fe8cc7068ca88e407f282182e8032cf327db1187caa55f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688b188efc48999b9fb300c96d92b1a18961afdae960c7c4b544fb15dba1dbf1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b009f63f40fabbf62b60a8f36907161db1ec174f241c48c828d1146a4198`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 11.3 MB (11252967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efa4181c0f41640b93236856c6e171cd14af6ead409446252a8729f96de12c7`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7170d9480708eb8e65c37d81ebd0f0f0249ca85f420c027bf87f22d36f7972f9`  
		Last Modified: Mon, 16 Mar 2026 22:46:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f754ac6996f3755689ea24ef32042440f61bc620c7b4baca1b94aaa4e11daffb`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 93.5 KB (93550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a25894cc7c550827691f700d1c89634d25ff883e8732d06f5e611905a3820e`  
		Last Modified: Mon, 16 Mar 2026 22:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:711a3828e487b3c898c3848819d398337511b76fd48c38eb53bfebdc59e34b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6484e97b3ad88ab4b5e77b3cd1d740588372cb67df2e30ff6d0a402da4360dc8`

```dockerfile
```

-	Layers:
	-	`sha256:ba413f86b373ddcb50bf9e59ba53cd49381e972f4184a6ac602ae96f7302b323`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05392ad75b16bd0e7a41bd30945205e4723b6d7f97b7c4ac41f80c24eedc9bb4`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:784656544058292447b93e94fa60875fee7b4f9d332636b5c325ad7b8c8e838f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5a6e6d20a87459719fe2aa819e14feff590478d329837eb64e7e969c3a448a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c6743caba6d50541b062d9790addb6ecce85a4c2baeceea8f6548dc7cacbc1`  
		Last Modified: Mon, 16 Mar 2026 22:44:54 GMT  
		Size: 11.7 MB (11692936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76faf673c44e016ad78b4539dddd5832ff382ef7c8ce58fdd6ab08fb13188900`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e040d877e32d0e2211999898375fd545e15f72c45209a01e4336d4c8131700`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a633250fedc942f435168aab78b16d80bfbb5c995601098e8f5599d585a48d`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 93.4 KB (93419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f4af573ef43d21fac89dfbe526a4e2d98e7c1e3e7ed7857cb6aaaf4d344e0`  
		Last Modified: Mon, 16 Mar 2026 22:44:54 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d085ce204c95503a0a63907fcf810118c90ab52f1f3da4eaa97ed45beb8831ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd4cd459241aca69da0575888e08971d2480f995c6f985d07e6fc75b137fa0`

```dockerfile
```

-	Layers:
	-	`sha256:0099bc1cd9bd0c2a571c2c804a366023fb81ddbb6913a77746c1820ba406a749`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ef2b64859296ee30fb161693c2082ad9ac5309e7e3b6bf80cd58b6a83f211e`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130`

```console
$ docker pull neurodebian@sha256:fe3b81e04ddaa8fd78726011a91d9f0f3f695fa07219d8ac602692a403a1cc04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130` - linux; amd64

```console
$ docker pull neurodebian@sha256:38823791da050edc5eb8f6fa536c491e2c8ca8005a8cd254481432b3141a3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59683732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6669aa02982813b549bb24f0efb1f87ca6a0a484f7104aa429108da356fa2a73`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ee88a3265bdb3d0530757a6461555d707868eee596f1f998298c190e3f644`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 10.3 MB (10292915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef101ccc9e6d95edb0e8ce65d3ffc82d69cd46fba656e62ca670d99e42249eee`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923b7d0ba6be692a9bd27955a6d7d130f86d66f9bd9df859a7f4be07e7087af`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e64cfd12a5f906af9cbc34e19af3580efa8f976499c5ffb3c985c022c8e508c`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:85b2232400c1f431ba8cc26424452df9318c1b02c53f299adf17432331fd5610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd9443133cc72a0d386f5b16557cb5a52932d2afee8c29b96f75ff0e5d8423b`

```dockerfile
```

-	Layers:
	-	`sha256:a6a58199c85a0132c55237be5d7d27187876d7ee3f1416b14fcaaa1cc7ee98b2`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73bd9c5a29d25f9da77b0fedb2979737b707d74c6ae43bad84b50e6e266c99f`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 14.2 KB (14250 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:901b7b25ce96aa90447603c3515149806a5d64a7cc6e67690efb485ce28b27a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59836813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7795498bb7dbd01166c2b326da248bbe4cc5d0d490ea9050315b99c8419dc1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df775a7faa43f7f7252f06117029e4dd5a5cbac50c51890b0d6d3cfd8405b0cb`  
		Last Modified: Mon, 16 Mar 2026 22:47:03 GMT  
		Size: 10.1 MB (10077947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58a0f5113878ee3b18eb8ee6a2439cd3d4c0311b4a2b783a57ae7f91570cc26`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b5bbcfe31d9f345176f105df35710778037261c4780ab6b5767185e16411b5`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d101e6915fa0def37b1a745ea4ff99954c71a09f8a1d36fba13a830235ee2f37`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 91.0 KB (91012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:600774acdcdbba3fe13459a4441324f1c491857eabc5df29fc63bd89b791f89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9030a439cbc6343ab6e5529fe5513af33f6a1ea35920d12615cdca32dd0fa`

```dockerfile
```

-	Layers:
	-	`sha256:8a045eefb957935b32df8b5f3f9841257d01411ae260d6403aa68ab7a16f082b`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb422972c47227f8b51f38ac744f2746fa68bd8246da0bdc0c4a0369275bebfe`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130` - linux; 386

```console
$ docker pull neurodebian@sha256:ed5f194f7c2abbaae636062e9e03e383495555d870ecd8a7a204c6ed0031978c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23b782793b45d233eb4c1cb7011a7c66e56885f7e893ff51d4360c3b1dc6c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e327d8697f911e128822f25c7c3a0b25075fc412d07427074366c4a1dcc06c6b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 10.5 MB (10467149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa825e034237965757272c1d539290ce5f98985c6f606968b5a15d07e4230c97`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20d220105eee5bb027f81176948567b8ebcf7b0d3e64a6f976fed93b757696`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2929ff200bd80db2d78e35ec44a161b98776d7a2a1f0470e391c0712e3e5e1e1`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 90.8 KB (90762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4088065eeaf99003a949cc4c86cdbb851614c39f97e157c3e608533525003145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973923d9da01f833bac03850854ab5ff2f09f4b5440e89c3cfb9351a84d2a6c1`

```dockerfile
```

-	Layers:
	-	`sha256:0e6bf81854fe1d14a17ca159eb87e1f89012c8acbbdcf6c314097a44fcc1ad9f`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60759a73115e1d8354102c4f15b6ca89c3ff7e7c3ddc0140a9e3ae91e615ff78`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:b0d72ead4f7914db488f7779d5259a33d59b18a4f3973e2e889ebfcd98ad66fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:195f8e982bb7f7edb9c996c204b1ddf8f55e2f2fd4af59a61a1da42b7f4f3ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0475b85ed0252659214671d27199f0988e3fbf8dcfdef45481ebb51adb66f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0958f60c5152275d8e2aa46f27c31bf8e62350466d9254ce5ebe1ff17628eb`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 10.3 MB (10293014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a99dd4cc6b98f202f039fad4aabf18786db50c45be9db53232d5231a40f590`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4737476d54fc963844a726785647ae72e1ac4aee6752b7e79082232ad05deb19`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682215c226f042ddd3cedea53ea769510c93b14f86b5dd01d531458742684b3`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 90.4 KB (90442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac85d07e7667fee3e1471587f9fd0b61f01b282f168d4c4935268613605f02ae`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:adcaa56d48f63f87e006d4314901e4a85e4f42f6cc57143d1847c015f4916be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c092da940be19a97a6f0d4f93e874c6efd7e0dd855d2955a4ed5636f3f7e343`

```dockerfile
```

-	Layers:
	-	`sha256:9b09648a89fd35b6d25c36f95b0b983326ab1d1930c696db1bd18f2e60f2c3cc`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f36eac91ebd943a10f26dfffcfb64cf469ec6201994405a3e0632e43fe279f`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2c289b0c2d4bb5631d73f7167cdf0b1469136d430775c9e499ed655b2e227727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99544e8d595bd4f4f730270ed8507040f7e5e54d1d5907a98249a0fa865c709`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f92c8ab9372506e674a894d9fd986fa8e5e967b72d2112de3a10396d44ded2`  
		Last Modified: Mon, 16 Mar 2026 22:47:00 GMT  
		Size: 10.1 MB (10077962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca2e88d525000038257bce1b7337532919c6947404971f468600b39f1dcb676`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7f8b4c55645ce191bd8e488c7f43b133f1a9012d1ff286ecca0bce803b557`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab02f003018b654c743fdaa120b30684485effd2a5de4335f24daa16b043e87`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 91.0 KB (91036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c50fefc97e01b6c27dda2c96f787d121d2cf01e76a012c884dafded607d742`  
		Last Modified: Mon, 16 Mar 2026 22:47:00 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9654212e73c8868169d367045704307ebf7b85f4c6d53917c6eea4945a6d206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf23371fdc78a81a3ee7507687a8bef9056a048d09049dd4392d262edc0112a`

```dockerfile
```

-	Layers:
	-	`sha256:01736020557ccdc3e3407249cd21e0e8a96572884941062bec8e07bb210eb8f8`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42579bddc23e952958f660dcb8a9bf19c229da06cef28fe92a1fd1d0b7690521`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:98100e9cec7a59df1753099be2a8adc41c8d0660b1e6c420961f7587698eb00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c789d63431eab185cd52bf6789b84bf1fc1859e61ecc43ab80d6cdd0d5a39f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37abea767e6bb8c916daf978fb4a1dac54edacd3f804121916ad31dd00d0955`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 10.5 MB (10467046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec540dbcaed9de978c5cb39191036757c8635984927ea8201c71f777e2cd422b`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6bfb517ef690ae62f0dcb8ad9abfac9e83f354ec0fe4508a61113f68f494bf`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4ed0cf4df19dedb0d14f9750f7cb7af25c17968a684c3068a6834805d289b0`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 90.7 KB (90734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ea60a0fb71dbeb5a18ead26daccafc96826a72bdcd39f8e4bd6a6d0b7c74f`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0e9bc43f78cd1cf795cc271385fea29a4f11fd54e905046c1fc5d3eb7ecc405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ca8c9009e4ae9378709fec75e4d6a18915c9072e085f61de88f8ac31f73595`

```dockerfile
```

-	Layers:
	-	`sha256:16f37269439e4540d7453667eb75ff80f7e1dd937d18e3a35dcddd7ba9418f97`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffd1eccebc7118d1a1fd1ad1dac6b36ed9ff3bd241e89034ea71a23a9e7a3d7f`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140`

```console
$ docker pull neurodebian@sha256:d3cd7ea9d9eeb9f2423fb9b97440178ae4fb637aea76e0e07106a206871fca80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140` - linux; amd64

```console
$ docker pull neurodebian@sha256:6a33326f00f0247e8a86c6c5e525ce83044392327a92a047297df8ef21d82dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60099811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e1a591c414bc482fa924fa687ae634a518814d22f455252f9eabc686ad018a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19357bfd71af09e26afd7dda402f901916224b7f700c069748c3186e8a918e6`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 11.4 MB (11382276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a99dd4cc6b98f202f039fad4aabf18786db50c45be9db53232d5231a40f590`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395e28d0b266a4a76b9155d01cce9cdc54f733e56c864043461f3f3af76f0643`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6c3e9cc93a96286494c5bc0808475fb4248df11dd85aee6ea49c4e20d234e`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 89.5 KB (89542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ba77b40fd9a7a932846c9a05fe2e82df03cdf4d8959134f712a7f8831e80c567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b2eb6628d7352772ae89fc9b519a81ae5baa393075586733cb3d6a1ef6839f`

```dockerfile
```

-	Layers:
	-	`sha256:f4444392266be94a13827e0ec63f58418b7c90b3bd1a894b6815d78ef8b2ca97`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 3.6 MB (3553690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11803dc5904dfccb517c17a6e83058590391274e324b646ee5a4eef4a258da4f`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 13.9 KB (13932 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6be5f297664170200d8ac0937e546dd1a4b4dc54650dde9bcee18964c2ed39ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59829690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8448827db583be8aa12200b44431d3da397860efb7c7379a68a05be881d6917e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:47:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1060b9ae7116f7c7642ee0f134028775dc85b210456446a7360ec215e4aa3a1`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 11.1 MB (11077549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519d4642c95351147493373b3c6d23cb24c9914c2e5a358ab85b997e2457e266`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c6d9393dcb8dd01f79423a27bf1eb4d94e50724438523de1ac4ccd531f49c9`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3e0a8eeca03a0729195a88598421dcee62e4f7385b766988d2a3278f01edff`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 90.2 KB (90175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:9917bebcc174c3fb62551d9e06ea7706f134a2236a457763dc19baf60ca71e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05ff510fa94570b01e9dd38208a06e4da9a60c58eea82f5bac5eb35aec7874e`

```dockerfile
```

-	Layers:
	-	`sha256:25791a8098cc1bcc1860275ebcfa3a49b95a05f96b0540be4380ddb5deb697dc`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 3.6 MB (3560491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b42c6c4d4e082972317af2857136fd78165090d50b9aceda587ea8dad2e387a0`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 14.1 KB (14057 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140` - linux; 386

```console
$ docker pull neurodebian@sha256:776f0a4cf196469edd1c851133fc5c34e44f70d8a38e61f32321bd870f516d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61618147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9506d730230c3f5e3d3a8c8de7ea00d4cdf7ece38c7a1e4eb7db186bd8a9fc61`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:45:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c1c3dc0cb48442941a53e86451485d9a7514b92f1a62f491a2738ce3e48e9b`  
		Last Modified: Mon, 16 Mar 2026 22:45:18 GMT  
		Size: 11.6 MB (11605589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abbd68e0604fee7b24a7a2f60b00c29396c653ad267717758455bc10cc5cfb2`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ca5074ff0875763fcfe5d4157c1b0b9aa108fc6841cd633f11f9ce1e870e3b`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2972ad1aa0e948b52f17c59f2b55233b5491fc22dda736f60ca8e5604ce27ad`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 89.8 KB (89781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140` - unknown; unknown

```console
$ docker pull neurodebian@sha256:03cf1dd1acd8dd7beae6a63515a4ad13a05931ebc1e1b28a460439332ee9d349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:242d15ad66106b470031d239f7537a762a2890144673c52df58855217a0c3a0a`

```dockerfile
```

-	Layers:
	-	`sha256:14d5408797509bc3f51507c038fa9a76e930d3a82c42f3f2c14126d64c942ac3`  
		Last Modified: Mon, 16 Mar 2026 22:45:18 GMT  
		Size: 3.6 MB (3551641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d6e2d3f96a3c7116644163d926b1386ec956c3fc97fd9bba00874574cc30c4`  
		Last Modified: Mon, 16 Mar 2026 22:45:17 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:9550343ea0453f33feee4c83335d02469ffa6f6cfdf7689e92ae44929590402d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7cbcb2018dccbc119decf18339c40bc9fc736bb14cc8d74e98c825cce5b86041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d0d88329284af82434ebccf452c75e6628d4559605caa81af6af292e170fd7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744a6b4b4a9684cbb11e9ecdbc9ede0197a160227d21c42838cc3308c6b4e0b9`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 11.4 MB (11382299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1875139f86f2f68b13903493d1a046622fa09ce497f13444a0e1eb58b29425b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd243b08ecce031850e503074d833e0a24109b4960944c53a4557e51408d7b3`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3886fee5d02b6836fd7bd2c60ebd980c0e65314ce8565e7d96cf232f1071be5`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 89.5 KB (89547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e3da227b0dea7161d8bfd6d2aff718ef57225df903c4973ca36f2fbb71beed`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ad337e08555537483a7bb9dae015c1047c32d396af9afa397e1cccc55def0d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ab46e1c1cc371b35e4b33ebc62b0d136edfb65dea896fbcf39af8d63b9571b`

```dockerfile
```

-	Layers:
	-	`sha256:f1b9bb67f26a56f3cf50f6861586522053195a7d15f848f0b445467dff782b7a`  
		Last Modified: Mon, 16 Mar 2026 22:45:09 GMT  
		Size: 3.6 MB (3553726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f18dea4b7f0760b82dec582a851fdc534073ead289296d607451d97474b8888`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:677065d982d885d27b4eadb807570b22f44f2983db1ab259f5341e3f6e2247c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17fc94e4ce0bb45d3fe9fccc40219a8557e5eec5bf6c293554d5bfeb39bf596`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:47:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:01 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:01 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3e975b0fee3e37d66bd1496d9c27a06cbf22bb0145e1a1b09c557d7dd58e25`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 11.1 MB (11077490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404e6c74fa835fce831866b24267ff623333e069b8168d66628b785bd9746135`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813d66d0e5643e22e5a105441040f5129d783e8cc3c759f5762fa7d9b9c1a9cf`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2ea8027d0eacfc714d35030b0534a0dfbcc40cdd15272c2198660c4b64bce2`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 90.2 KB (90204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c39b8d27f969e6e4b7616e229fc92dd58936cbfc8e6f93f70c51a16c8c36b4`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5abc3a2fd1c35885ac1080ce17113e45a566e09a424e06756036089aceef3ee9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06df2e2f6f779a1f3b7df9552310fc8ea62db1865f702b4be4b5fafbc8f0cc1a`

```dockerfile
```

-	Layers:
	-	`sha256:6b649bab6cf90da66935cd04a8fc3c09c874fc12a51043877827c9b4377ddd74`  
		Last Modified: Mon, 16 Mar 2026 22:47:13 GMT  
		Size: 3.6 MB (3560527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60edffc23fb055179a0c8e87f176083693296ef6458467bbb282edb5a806551c`  
		Last Modified: Mon, 16 Mar 2026 22:47:12 GMT  
		Size: 16.1 KB (16098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:80b364add1af2faf7bc55958460e350bba3e549e243e3dd8f54516b317d8748c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61618521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8358e4bad4f20174ba84ee3b8c7e93ce05e151ddb68138164b8664a2567b4f0c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:45:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30659db903268f5dcdf0fb4eae9842869002328cea186cb0491a50b2e3232e12`  
		Last Modified: Mon, 16 Mar 2026 22:45:20 GMT  
		Size: 11.6 MB (11605539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a6299c767a6b8de3f66fc6721068e6b86ace4c45d34a389016404c8cfa0778`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fbd7ef8ec04b0ac885f12960dcbfd2785562e6a46c1c6b4716ff40129bdd31`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca67de4ee3edc48b043ae4ddbf1c9677a3815215d1b2ff5e195b2daaa8f528dc`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 89.8 KB (89760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4595f94962f4c142429e3ca0eb002960df4000525b0d2e60c463b0f91934477e`  
		Last Modified: Mon, 16 Mar 2026 22:45:20 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c68211d63100c3a2c47090cc28977f44a5434ea9903be03f237aa1085b09292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61c20573f9eed374fda7260fa480dd9599fb4041f80a529e8886c86ad2d5c85`

```dockerfile
```

-	Layers:
	-	`sha256:7c214acaa1885f2699e93564c144ac761cbf5feb7121bdbdc1c20b0b47036251`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 3.6 MB (3551677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308b361b3a3fd980ba8054456a0fecc5548431fdfadeddea39b63351eaf39930`  
		Last Modified: Mon, 16 Mar 2026 22:45:19 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04`

```console
$ docker pull neurodebian@sha256:14293487cb5376d783e7b497468fcdda8313c5a5fcce8593046b201f6993b329
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:684f89bb320fc15f269d733cfc19ed0b5c1f15f199d940085a3c02b90d82831a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebb4f514f1106446659c0c35b5cc154c33519bede72d75513eeea1e81f3011f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:11 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:12 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:12 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2863a40c7a7170ba503ee516d26f3a9b818e2606f0ab87535ae76ac0536c121`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 3.6 MB (3624431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547e46402d925046cbc9b8dda38ed4b4ec4ca3f6d1ff4f41bdcad1a51b430df5`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186cd36fecf717d7daa1ec85dd00593dabc4d1aaca1422a24f4c94f4be810c1b`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b72342ac61240026a61da0af1991417b699c7c5b770c54de65b56cc8fc5094a`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 111.1 KB (111090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:050a384cc4ff3ef04511d6bc797ace854cec23734e8230395615d68d79fd7665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74fde8449d2e512592b6d172bd38f04836912e06bd08a3e7e4d5797564753d14`

```dockerfile
```

-	Layers:
	-	`sha256:8ad6a29f65124fca407209fed2dffb3670b2dafb4eac073c87b2e3a537485f8d`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 2.2 MB (2198320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c407f459a18d56ccb69cbe43ea0e204e87401d236be87a31ef1e52b5672d30a5`  
		Last Modified: Tue, 17 Mar 2026 01:43:24 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:21803a350017833c4e67370d4feda9c58b66d83e112728b948975522a375160a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31106990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7288fc53775d8a8a57940d58c2739227bfe825b6cfed8f474022a55101398ee4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:44:51 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:44:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:44:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:407f0be41f9f69ec71ea80c57c1d68fc9c020cea2e797b896e8da86e5b42427f`  
		Last Modified: Tue, 17 Mar 2026 01:45:08 GMT  
		Size: 3.6 MB (3604693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c169116b0053ebbedbf8dc7871081f849145ebc37907ac4f59535fbc6406a54`  
		Last Modified: Tue, 17 Mar 2026 01:45:07 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19ac3955e52c5b186512aa94a00bba600c1c1f492c0d27a8549cc8ecd5c9976`  
		Last Modified: Tue, 17 Mar 2026 01:45:07 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2939a8ba767ebfff6a480987cd657c98a69bd72b930e3696dfbfa30a06baa814`  
		Last Modified: Tue, 17 Mar 2026 01:45:08 GMT  
		Size: 111.1 KB (111093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:359f3d545f92512f6d3851d0c26c27c2aec965a8878354f936670bc1a34fee09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4812c3daacb9770f8f09c0cd4c812d9e76c7bad590698292abd87562904008ce`

```dockerfile
```

-	Layers:
	-	`sha256:2e5b273d9c8ec0ebd4dc3c690b2bb96818569d68295b270b60d84d4fdc397fea`  
		Last Modified: Tue, 17 Mar 2026 01:45:08 GMT  
		Size: 2.2 MB (2198580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1445889404c8bc249023dea1439b3d4b3bc25bdcf219c3b7fbfc532df12d59`  
		Last Modified: Tue, 17 Mar 2026 01:45:08 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd22.04-non-free`

```console
$ docker pull neurodebian@sha256:0563d2536caf4900b584a6744950b5933b836feca88b18f1193dff60f6db5f58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd22.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f65ab94de2b8eeb7ce8e3ca843ba825e9c7fe90ed9b6634fbaf551a4d61fbe26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33276454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce894af6d2b00fbd05af4826250646684dcbb657ac827263cc9e0f14b863a70b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:44 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb4394bdcefc6fa3b661b40e6eb591c5f4d4a4948bb9f94efc8cfb2cca63ab0`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 3.6 MB (3624440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe5dd49d306503d46bfd8860d908db1bd43054f51630df3cae246cda80ab538`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 1.9 KB (1905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc8033217859346bf8a7b9a474edfbb809fbeb1a627bad48117b921acadae46`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466de1c292093141aee6e0b2e28cdb5dead9eaa5b899e28405a08326e0afbcda`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 111.0 KB (111028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1816e7a377a6dd0ca7d84582d786a62e2eae934a80a7d10a4968032c0c09c847`  
		Last Modified: Tue, 17 Mar 2026 01:43:52 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3327cf1ff11761f7d3fd4c86c31125e43e1d212147fdd91197fb422bd6610d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42da9986bb0da24b6b98d1bcf5be809650d9e940fa3ccf81026bdeb9108e866a`

```dockerfile
```

-	Layers:
	-	`sha256:044f0f60135fd32871cae06a72337f371a8c9006584356dc984cdd534d47b695`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 2.2 MB (2198356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be7e31bbe852e2d1e841c91b37d8c7c1547bbaf7a57650644745cdf4181ae15a`  
		Last Modified: Tue, 17 Mar 2026 01:43:51 GMT  
		Size: 16.2 KB (16163 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd22.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d6a1324ed061523ef22e532caf02b5d13a7d342ae3c0581bb98378dbf5998b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31107206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d789266f761ee042462b64fd62015f0592608f8911a98f067d7c67233c491064`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:45:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian jammy main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:22 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202f320aee81dfa65dd047461f0166a121168590d3e51b1929d1b5dfc59f4dfa`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 3.6 MB (3604661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7beae3843cfbb7d29beda7d948635e8eaa8697817f1d97af9b26e6201268a8c`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7edf385ead3b8fb2f0dd3dc7542928119f98160e2be31611ce29c87fdce3b147`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54549bcc2860f4774039377e1639794661a450d3832d5477a77df95a05dc4a6d`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 111.1 KB (111056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99cd67958630ecee727aa5ffdc70e69afae561b6c827d318cec4a3933ae0e21`  
		Last Modified: Tue, 17 Mar 2026 01:45:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd22.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3e1cfe4c58bd5d2c1a8f4abb414817152200d5bcb6fb06b31541ee24a67d5391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2214919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01de9d011d760b10371e31fcceb88b7b5a15bd2720da1c846601075f89823426`

```dockerfile
```

-	Layers:
	-	`sha256:a53b614a54e6d4ffea23c6091c74a19b7dfe81b57afd8f6f1332b06b974fcce4`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 2.2 MB (2198616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c823c9828410b7a964ea17197da7b784782378fc7dfd14a237daf78286372be`  
		Last Modified: Tue, 17 Mar 2026 01:45:29 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04`

```console
$ docker pull neurodebian@sha256:79adb5f98a71a6159946a6b681f15fcd57fb27c6daec32e7f1b6a1d94aa61f23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04` - linux; amd64

```console
$ docker pull neurodebian@sha256:99cec198c10241708cc74ddb9badc7f61579e15770743a61cb7a76020efeb381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33403846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698c47689ccd15da9af1cd464a050999d7f1ad7c080c757055ffc9ac0ab58c33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd2ec225ec2a9033fe4348f140a3f8ec348f417e5042ceb69ebada72bd674db`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 3.6 MB (3564564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef17f483be9c2ebf11f63f4d9f74a665b3c6fae30c0fdcb26137614861b95f2`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feceec3641c1de79bdd0dcd16ec89f8c37f2277b29391fae5a9f0d01a48ba93`  
		Last Modified: Tue, 17 Mar 2026 01:43:54 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc4e2ec377246875f841ab25ba7e5975732e41e87749f28aeba3921aeb5bb52`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 104.4 KB (104379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fbb5db8c0e09cdff64b8f32319be07af9b6a1bbdfa7c34e6384d41d6d8452fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d841613d66ed32fe559043280b70d9e9b66e1909b225de45872710f62ed7bac`

```dockerfile
```

-	Layers:
	-	`sha256:b7ca2ca4ec1655009f26991208d8dcfc04bb060bf3089f4880cff7c384169354`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea1bf48e4d857192c9e8234db2505ace1be473b7074ad2e5f898bde4798f908`  
		Last Modified: Tue, 17 Mar 2026 01:43:54 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f245aafa6ac8f69e6188bebb3508fdad80fbdd1fb625fd621adb8a081b73a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32539513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c56ee68d80089c3f0925d8e58f1aadbf3c27908dd7512fc85c2c23e22163e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:45:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533c5edf582f6c749ef6a1c980c83140c19790fba01e023270d953596d6728eb`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 3.6 MB (3561698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e00b53b8e4686217ad4464335977ad206a0b44b2c815209a57b92579deb2c3`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4150071e6c680a3e30636e054b5eb864727fe3c9b6bc8e4e894a63bb147d2e8`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf622f6ce748df581fde435236c4025fce1294e846eb31a4c2bb114ad60de5e`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 105.2 KB (105195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04` - unknown; unknown

```console
$ docker pull neurodebian@sha256:345880f970f78bca78609af939641e1ee75bb8f43c66a887fa2d8ee357bf4356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33261a958005f1391a059daad1bcaac28d5b8b86b44eabd34be6e413a13c46d1`

```dockerfile
```

-	Layers:
	-	`sha256:4bcad4951b4567ba4ce52d8f30dd9930b9a357da1219bb3fbdc23e3ae7caab35`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506182a496a21e1b4cab38177081115a703e24a5ca3745eda65191d95f3a7545`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:nd24.04-non-free`

```console
$ docker pull neurodebian@sha256:b289304036b43b2b6f3ad612027e6859c6bdccbb50f661e67b5eb10ec2b808dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:nd24.04-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:931939e21f3e8e404e747e12a162e3e7fad01b0a7d24e5f7c820c28ded17882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabccfb9217d8ed362278ad062b465ee927cff4c7c6caa1b3fd30e65de5a622d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ab0d452cb21362d5ba044daf5df99864fb25c5d08dd9d0bd97026143a048f`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 3.6 MB (3564507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3bc17860a6a5345cef1e7af56e1244e6f30c1dc558bc2838de57efbdada052`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e70019b132acc2d97fda51b094eb544fbc9a053297a2ea80c9eb960f58d13`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ce36ff481a7c03cf8ac9e06c0bef6150a282c4d2b0d97482c9c27cb4a118f`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 104.4 KB (104354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4696bcd872eb5237c46e9c3df9ea3ca46de979cb111fc0fb249860b8fc0138ed`  
		Last Modified: Tue, 17 Mar 2026 01:44:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4b0d6c2c1629074abdf85b6f467a19fc0201a837bc4152db44603ddb186f5e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e204b0a7b6f48e64159e1115dfb3ae2ba89f75a2a92602c952449e6619d0276`

```dockerfile
```

-	Layers:
	-	`sha256:78f99f9c44f6e8511253f8e60951ae0b4cddd44ce4e91ab1c92423423b1d12e8`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69daa31095a097290e3e9d7965de683252c5e8df8d9b4ee14d18750f5f82dab3`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd24.04-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ce595481555f22799b23709984c63132aaf65f8173372b49dda0db288400aec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32540013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed632cb3d5db47f8b17ff49beef3f5dce58045dcc0def9094fdf199bfd4b738c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:45:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f6f623361c6efd56bb67aedc4f222717a42d17afef22ff4c5a31d7a7e256be`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 3.6 MB (3561747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723320ffa1c0b3494c2a8ed4ab8007e21efa59c99e44eddf2e3fc1fd2f829b4`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4229db03f200c816596816aa31c4b37e3fab83352edd9fdc7ad6907a0687515c`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693b4978166e3d1c2e71665356071e6072c778a9a42676165726a80bbe5319d7`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33985861acc8af083671e8a61968806b39e5ccf0edd830537a58a9e638ec9f91`  
		Last Modified: Tue, 17 Mar 2026 01:45:44 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd24.04-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6b7c55f14afc19e0caa0105bfd997392b6094d9e9c1ea96dcfd7971fccd8cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0cb863feaf52e97c9de309a966eb0e954946a2ff81ba964c220e106cf4e3a`

```dockerfile
```

-	Layers:
	-	`sha256:7e7ce7ddccae0a2b981eb1811f66b4f82d041a4a40fc23f89cd5994f7ce03035`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e996bedf073e79f9ab5366cfff4022fadd40eedbc816b96d8629dc5984962a99`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble`

```console
$ docker pull neurodebian@sha256:79adb5f98a71a6159946a6b681f15fcd57fb27c6daec32e7f1b6a1d94aa61f23
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble` - linux; amd64

```console
$ docker pull neurodebian@sha256:99cec198c10241708cc74ddb9badc7f61579e15770743a61cb7a76020efeb381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33403846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698c47689ccd15da9af1cd464a050999d7f1ad7c080c757055ffc9ac0ab58c33`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd2ec225ec2a9033fe4348f140a3f8ec348f417e5042ceb69ebada72bd674db`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 3.6 MB (3564564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef17f483be9c2ebf11f63f4d9f74a665b3c6fae30c0fdcb26137614861b95f2`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6feceec3641c1de79bdd0dcd16ec89f8c37f2277b29391fae5a9f0d01a48ba93`  
		Last Modified: Tue, 17 Mar 2026 01:43:54 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc4e2ec377246875f841ab25ba7e5975732e41e87749f28aeba3921aeb5bb52`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 104.4 KB (104379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fbb5db8c0e09cdff64b8f32319be07af9b6a1bbdfa7c34e6384d41d6d8452fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d841613d66ed32fe559043280b70d9e9b66e1909b225de45872710f62ed7bac`

```dockerfile
```

-	Layers:
	-	`sha256:b7ca2ca4ec1655009f26991208d8dcfc04bb060bf3089f4880cff7c384169354`  
		Last Modified: Tue, 17 Mar 2026 01:43:55 GMT  
		Size: 2.1 MB (2120889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea1bf48e4d857192c9e8234db2505ace1be473b7074ad2e5f898bde4798f908`  
		Last Modified: Tue, 17 Mar 2026 01:43:54 GMT  
		Size: 13.9 KB (13933 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f245aafa6ac8f69e6188bebb3508fdad80fbdd1fb625fd621adb8a081b73a203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32539513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c56ee68d80089c3f0925d8e58f1aadbf3c27908dd7512fc85c2c23e22163e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:45:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533c5edf582f6c749ef6a1c980c83140c19790fba01e023270d953596d6728eb`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 3.6 MB (3561698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e00b53b8e4686217ad4464335977ad206a0b44b2c815209a57b92579deb2c3`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4150071e6c680a3e30636e054b5eb864727fe3c9b6bc8e4e894a63bb147d2e8`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf622f6ce748df581fde435236c4025fce1294e846eb31a4c2bb114ad60de5e`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 105.2 KB (105195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble` - unknown; unknown

```console
$ docker pull neurodebian@sha256:345880f970f78bca78609af939641e1ee75bb8f43c66a887fa2d8ee357bf4356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33261a958005f1391a059daad1bcaac28d5b8b86b44eabd34be6e413a13c46d1`

```dockerfile
```

-	Layers:
	-	`sha256:4bcad4951b4567ba4ce52d8f30dd9930b9a357da1219bb3fbdc23e3ae7caab35`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 2.1 MB (2121934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:506182a496a21e1b4cab38177081115a703e24a5ca3745eda65191d95f3a7545`  
		Last Modified: Tue, 17 Mar 2026 01:45:42 GMT  
		Size: 14.1 KB (14058 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:noble-non-free`

```console
$ docker pull neurodebian@sha256:b289304036b43b2b6f3ad612027e6859c6bdccbb50f661e67b5eb10ec2b808dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:noble-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:931939e21f3e8e404e747e12a162e3e7fad01b0a7d24e5f7c820c28ded17882e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 MB (33404197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabccfb9217d8ed362278ad062b465ee927cff4c7c6caa1b3fd30e65de5a622d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:43:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:43:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:43:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:43:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84ab0d452cb21362d5ba044daf5df99864fb25c5d08dd9d0bd97026143a048f`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 3.6 MB (3564507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3bc17860a6a5345cef1e7af56e1244e6f30c1dc558bc2838de57efbdada052`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6e70019b132acc2d97fda51b094eb544fbc9a053297a2ea80c9eb960f58d13`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ce36ff481a7c03cf8ac9e06c0bef6150a282c4d2b0d97482c9c27cb4a118f`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 104.4 KB (104354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4696bcd872eb5237c46e9c3df9ea3ca46de979cb111fc0fb249860b8fc0138ed`  
		Last Modified: Tue, 17 Mar 2026 01:44:05 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4b0d6c2c1629074abdf85b6f467a19fc0201a837bc4152db44603ddb186f5e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e204b0a7b6f48e64159e1115dfb3ae2ba89f75a2a92602c952449e6619d0276`

```dockerfile
```

-	Layers:
	-	`sha256:78f99f9c44f6e8511253f8e60951ae0b4cddd44ce4e91ab1c92423423b1d12e8`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 2.1 MB (2120925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69daa31095a097290e3e9d7965de683252c5e8df8d9b4ee14d18750f5f82dab3`  
		Last Modified: Tue, 17 Mar 2026 01:44:04 GMT  
		Size: 16.2 KB (16162 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:noble-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ce595481555f22799b23709984c63132aaf65f8173372b49dda0db288400aec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32540013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed632cb3d5db47f8b17ff49beef3f5dce58045dcc0def9094fdf199bfd4b738c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:45:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 17 Mar 2026 01:45:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian noble main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel noble main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 17 Mar 2026 01:45:37 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:45:37 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f6f623361c6efd56bb67aedc4f222717a42d17afef22ff4c5a31d7a7e256be`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 3.6 MB (3561747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9723320ffa1c0b3494c2a8ed4ab8007e21efa59c99e44eddf2e3fc1fd2f829b4`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 2.6 KB (2639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4229db03f200c816596816aa31c4b37e3fab83352edd9fdc7ad6907a0687515c`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693b4978166e3d1c2e71665356071e6072c778a9a42676165726a80bbe5319d7`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 105.2 KB (105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33985861acc8af083671e8a61968806b39e5ccf0edd830537a58a9e638ec9f91`  
		Last Modified: Tue, 17 Mar 2026 01:45:44 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:noble-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e6b7c55f14afc19e0caa0105bfd997392b6094d9e9c1ea96dcfd7971fccd8cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a0cb863feaf52e97c9de309a966eb0e954946a2ff81ba964c220e106cf4e3a`

```dockerfile
```

-	Layers:
	-	`sha256:7e7ce7ddccae0a2b981eb1811f66b4f82d041a4a40fc23f89cd5994f7ce03035`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 2.1 MB (2121970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e996bedf073e79f9ab5366cfff4022fadd40eedbc816b96d8629dc5984962a99`  
		Last Modified: Tue, 17 Mar 2026 01:45:43 GMT  
		Size: 16.3 KB (16303 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:b0d72ead4f7914db488f7779d5259a33d59b18a4f3973e2e889ebfcd98ad66fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:195f8e982bb7f7edb9c996c204b1ddf8f55e2f2fd4af59a61a1da42b7f4f3ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0475b85ed0252659214671d27199f0988e3fbf8dcfdef45481ebb51adb66f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0958f60c5152275d8e2aa46f27c31bf8e62350466d9254ce5ebe1ff17628eb`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 10.3 MB (10293014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a99dd4cc6b98f202f039fad4aabf18786db50c45be9db53232d5231a40f590`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4737476d54fc963844a726785647ae72e1ac4aee6752b7e79082232ad05deb19`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682215c226f042ddd3cedea53ea769510c93b14f86b5dd01d531458742684b3`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 90.4 KB (90442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac85d07e7667fee3e1471587f9fd0b61f01b282f168d4c4935268613605f02ae`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:adcaa56d48f63f87e006d4314901e4a85e4f42f6cc57143d1847c015f4916be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c092da940be19a97a6f0d4f93e874c6efd7e0dd855d2955a4ed5636f3f7e343`

```dockerfile
```

-	Layers:
	-	`sha256:9b09648a89fd35b6d25c36f95b0b983326ab1d1930c696db1bd18f2e60f2c3cc`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f36eac91ebd943a10f26dfffcfb64cf469ec6201994405a3e0632e43fe279f`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2c289b0c2d4bb5631d73f7167cdf0b1469136d430775c9e499ed655b2e227727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99544e8d595bd4f4f730270ed8507040f7e5e54d1d5907a98249a0fa865c709`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f92c8ab9372506e674a894d9fd986fa8e5e967b72d2112de3a10396d44ded2`  
		Last Modified: Mon, 16 Mar 2026 22:47:00 GMT  
		Size: 10.1 MB (10077962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca2e88d525000038257bce1b7337532919c6947404971f468600b39f1dcb676`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7f8b4c55645ce191bd8e488c7f43b133f1a9012d1ff286ecca0bce803b557`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab02f003018b654c743fdaa120b30684485effd2a5de4335f24daa16b043e87`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 91.0 KB (91036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c50fefc97e01b6c27dda2c96f787d121d2cf01e76a012c884dafded607d742`  
		Last Modified: Mon, 16 Mar 2026 22:47:00 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9654212e73c8868169d367045704307ebf7b85f4c6d53917c6eea4945a6d206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf23371fdc78a81a3ee7507687a8bef9056a048d09049dd4392d262edc0112a`

```dockerfile
```

-	Layers:
	-	`sha256:01736020557ccdc3e3407249cd21e0e8a96572884941062bec8e07bb210eb8f8`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42579bddc23e952958f660dcb8a9bf19c229da06cef28fe92a1fd1d0b7690521`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:98100e9cec7a59df1753099be2a8adc41c8d0660b1e6c420961f7587698eb00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c789d63431eab185cd52bf6789b84bf1fc1859e61ecc43ab80d6cdd0d5a39f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37abea767e6bb8c916daf978fb4a1dac54edacd3f804121916ad31dd00d0955`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 10.5 MB (10467046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec540dbcaed9de978c5cb39191036757c8635984927ea8201c71f777e2cd422b`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6bfb517ef690ae62f0dcb8ad9abfac9e83f354ec0fe4508a61113f68f494bf`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4ed0cf4df19dedb0d14f9750f7cb7af25c17968a684c3068a6834805d289b0`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 90.7 KB (90734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ea60a0fb71dbeb5a18ead26daccafc96826a72bdcd39f8e4bd6a6d0b7c74f`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0e9bc43f78cd1cf795cc271385fea29a4f11fd54e905046c1fc5d3eb7ecc405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ca8c9009e4ae9378709fec75e4d6a18915c9072e085f61de88f8ac31f73595`

```dockerfile
```

-	Layers:
	-	`sha256:16f37269439e4540d7453667eb75ff80f7e1dd937d18e3a35dcddd7ba9418f97`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffd1eccebc7118d1a1fd1ad1dac6b36ed9ff3bd241e89034ea71a23a9e7a3d7f`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:70ce97f6796d0bd1e6ea7d563d93fd9f0cf0bf63a8e127ac6cce87afe7284bf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:6d1fc426c529a7179490427ff1b139fc09928fc88d60bf4457cbebe436b25e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60149970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744a29bf828d9a897f7c0bdcd7643b2452b36aacb4109564bc3d3ec0b0650f40`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:44:56 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:57 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:00 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:224b32b461470cab0a5b83292cf42319369c28ec8beae34418e705d6d0530bb2`  
		Last Modified: Mon, 16 Mar 2026 21:52:47 GMT  
		Size: 48.7 MB (48676470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435378e6edfc7c12b4ed65b613af023d57fa606a0b2de1de8f50080d443f273f`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 11.4 MB (11381178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1875139f86f2f68b13903493d1a046622fa09ce497f13444a0e1eb58b29425b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a527387d1617429a2a96c43d1624a92101db3a1b29ec5eb4b897ad7b8dced4a`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda3bfc8cab99ab329696b3337e16a74b175a67bf860a8a5e054ecfbf0501e9d`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 89.4 KB (89418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1d440ccd085c26be74202165cc3b1128954c2b3f47733236a0416fd8fd6ee623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c77c3d0f0ba756177d09af10cadbeb017c39ffdfb8f4018efff68d41a8ecd8c`

```dockerfile
```

-	Layers:
	-	`sha256:3b9bd7caf2ea52ea4337edf4c858d40e68bb08754805df3c001c44a1c3eda640`  
		Last Modified: Mon, 16 Mar 2026 22:45:08 GMT  
		Size: 3.6 MB (3552870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39e1f533aa58bd0505780c3952c186eaefa6e16ea70768cef347041446e1574`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 13.9 KB (13903 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a5602e206119d499ae31f37ec778d866c2517bc33939bd34c211c16addb7ead2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59885100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19a6633bede2c6667f856a815cbfc4b9ec319fe7184a856765b980e6d2666885`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:47:04 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:05 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f8aa045b0b46f2987d2dfdc549957d53bf9eb7148b1452027f1bbe82759ee08b`  
		Last Modified: Mon, 16 Mar 2026 21:58:00 GMT  
		Size: 48.7 MB (48715175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5418123350c32272b46788d05723fde818111cd59f2e38fcc932ec52bf8fe8`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 11.1 MB (11077011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5413fc3519da5d42e3e7a4e0720341191628348b309bc6ca103ece3f91c45cd1`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb5599a29b53a0abd1361980e40020e8cad1bc5b287ae4e26edd5449ec2b15c`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:870365bc67ca6e2403c7a765994ce210adf4b8b4a446b30cf6e30e61908fa7f1`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 90.0 KB (90009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:083861651e2e24b282385211009a4b132faf832b34f12bec2441737e7994804f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f442457820b74fd771de15f04d68e4b00d5f3b50f05cb0bb400375043dd031`

```dockerfile
```

-	Layers:
	-	`sha256:d7dae46320117521fa0297a784b4d6534e8b02a980fd8163ab267cb9ae8fbe87`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 3.6 MB (3559671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d4098ea9ca794fa9b81557858d2f1014c06c9b6c06489190f9ad2f087e3a0b`  
		Last Modified: Mon, 16 Mar 2026 22:47:16 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:0620854eff36c1edaf794aa0c06278a96d50219bfcb7effa5a679e55b95bdb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61646917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd87c508951df3df21c5f3f516ef4b475b9395aa986826cf33c665918650caa7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d910d8b21d9682e89de3d97b422096e3120f61049a143cd139a1c42e9bb8b77e`  
		Last Modified: Mon, 16 Mar 2026 21:53:09 GMT  
		Size: 49.9 MB (49948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b321b1e66d39564c47555de32d340a791425b7cce9bb9cec583222c8d7ca49c`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 11.6 MB (11606315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40be60bbfbb52b308f7a3da3d6ce45f2b45d390b3a218b8962d5d180766adfa9`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5a3927c9a8ad3f0340e06b2184345914a8af2da8f0e0b9cd871831857de9aa`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a63559a329af0724eb71b76ffc8a94493d39318fe64600142629c2796050b5`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 89.7 KB (89655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:15308b6f9290ae75c8ead47e44c0f9e1615b18562b59e678ef8e14c24e21202f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3564698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a966c7f4dc6dc87414338959c6433f2a3b6764d554b8a92280eaccc04454fa59`

```dockerfile
```

-	Layers:
	-	`sha256:dfe0057bfe8bce433fe945340cdaf4eaefe8fe9f9b3e138240b50c5fe795735d`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 3.6 MB (3550822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:751950bfb2649acce0e08fbef36c572123014cdb7a355ba165830660ca67048c`  
		Last Modified: Mon, 16 Mar 2026 22:45:30 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:401ece9b9b7a564428d1faa0c0d488a0ed344d7dcf45c7f3e2403fa74dca7203
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:76e9e995f4c4f86904fe10306ac6088227b0f709013d27ebf02bd5df4430ba70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60150388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e19b5c754f97b7218621a2ad7415892efe2954224c83c2da86a2d5629da1d46`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:224b32b461470cab0a5b83292cf42319369c28ec8beae34418e705d6d0530bb2`  
		Last Modified: Mon, 16 Mar 2026 21:52:47 GMT  
		Size: 48.7 MB (48676470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baca5d772c892170c87d0a816d02bca5d34d5f7ca64e714e57c1490e7ed49f93`  
		Last Modified: Mon, 16 Mar 2026 22:45:13 GMT  
		Size: 11.4 MB (11381180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57469f7c59fb0fdcdd0b36b09dad92a22e9e27d58cbb3382c1cf96dea721f51`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534708c7790614b41fccb8d1b06f493d6f53d9ac328099d5fb668761e97f5b32`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e3dbe970409cab1f0211816b271687786f2f5c9fe9ee2102caa213515c56ea`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 89.4 KB (89420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680101dfe5470fbe3518d073851e4e98819f1eeada5673af5a3d2b2306eb6cbe`  
		Last Modified: Mon, 16 Mar 2026 22:45:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b56c36aecfc51dfe3b41a340b400c25bebcee2404771369cfafb03eeb682072a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3568837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d987c886e7cac60b0a18a6cc934fc531b684c3bf9cac481f122b6bf5cd898814`

```dockerfile
```

-	Layers:
	-	`sha256:0d057c6c2a0dbc41f04d346d378fe95d149886bc44dfed5136278413370d47d2`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 3.6 MB (3552906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae0c1add2756e6318c73674eac374bc148811486de0b783f5d373ae71030fd57`  
		Last Modified: Mon, 16 Mar 2026 22:45:12 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:316a56e122edbd573a79a2de5f3d75de2aa40b0f0b076df9cb9078a8924ca94a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59885398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af734abdcaae3b6dd42ab3ab31c9cc26f1b6a679b439ddb13fffa3bcae11c52a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:47:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:47:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:47:11 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:47:11 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f8aa045b0b46f2987d2dfdc549957d53bf9eb7148b1452027f1bbe82759ee08b`  
		Last Modified: Mon, 16 Mar 2026 21:58:00 GMT  
		Size: 48.7 MB (48715175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15f2120aa02b76483cbe03d606a903b0903900913698902e3d77a29d7314a29`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 11.1 MB (11076885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0488830adfbaad80a1040eec389eb3dc2bf86fa1dab231c0ed0d3048cfaea46c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a76c095666fd560b53498568dd4d4d556c26247b75aac3877c0460667b24d74`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4163bbeabab58b1e6d1b1932300651fbb20bdd6b1bc34dfd37cd2713210470ee`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 90.0 KB (90020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8ee29bdb6356fa7c9ff60276dbcec78e12070f393bf1c74149a42761b2b5f7`  
		Last Modified: Mon, 16 Mar 2026 22:47:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bd2f9c32f345398ed26d176eda827c26cd495bd913f09b69e8712f2a094cf14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9caf6b1e293c67fff7eaec5ae5f7307c77103c874b33811276b1fff822c47170`

```dockerfile
```

-	Layers:
	-	`sha256:98caa2b25a8ea1717a327cb56dd68e953776d481ec3ab95b60985979fb91bf7c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 3.6 MB (3559707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d6f034189525baf2b751d1e14ca27f8535e129f125bde3602b992259d4fc1c`  
		Last Modified: Mon, 16 Mar 2026 22:47:18 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f92cb038c1549da7e7606543cea1b37f5e33aecae18d51b680fe7b2962beee61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61647344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9097946a5841af837fd5d7a4bd991ec34712c47638a936b75fa670e1dafcd2d9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1773619200'
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:45:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d910d8b21d9682e89de3d97b422096e3120f61049a143cd139a1c42e9bb8b77e`  
		Last Modified: Mon, 16 Mar 2026 21:53:09 GMT  
		Size: 49.9 MB (49948047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ccd876f6aa19c74a020294759acdeb35dd1245a040209f4ca69527dd7ab372`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 11.6 MB (11606313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce7e45512f12c2bf1b2dd24d3fa2554dfa01a69158f3f6f2cff4c673120960c`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12592a476099ae3908d871cdb1ce7a4a285d11322d73a9fb479161fb624eab11`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cb8f37b7cc492634b2cb567f2e78dd488a35a98fbe265a251a020534d44e99`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 89.7 KB (89665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f07da676b418cdd0f4219b6c91a9b37116d8096542e34b7f98df066f469d8d1`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b51352ea60a625cb4386b46888d45f5533db3f02ae1037a9e158a801320f4be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baebd2f515e37ebd0dada90132cecfeeea4a30f763ebed5e184ddf44611eaa7`

```dockerfile
```

-	Layers:
	-	`sha256:c38239855257663e51b69680c2e3168694aed9b6b4a98221b20aecf6e193b98f`  
		Last Modified: Mon, 16 Mar 2026 22:45:35 GMT  
		Size: 3.6 MB (3550858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc003d177c616b75b01582f33421075f7ef8d520b9fd75e138dca77a7829a7c8`  
		Last Modified: Mon, 16 Mar 2026 22:45:34 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:fe3b81e04ddaa8fd78726011a91d9f0f3f695fa07219d8ac602692a403a1cc04
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:38823791da050edc5eb8f6fa536c491e2c8ca8005a8cd254481432b3141a3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59683732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6669aa02982813b549bb24f0efb1f87ca6a0a484f7104aa429108da356fa2a73`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ee88a3265bdb3d0530757a6461555d707868eee596f1f998298c190e3f644`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 10.3 MB (10292915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef101ccc9e6d95edb0e8ce65d3ffc82d69cd46fba656e62ca670d99e42249eee`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923b7d0ba6be692a9bd27955a6d7d130f86d66f9bd9df859a7f4be07e7087af`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e64cfd12a5f906af9cbc34e19af3580efa8f976499c5ffb3c985c022c8e508c`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:85b2232400c1f431ba8cc26424452df9318c1b02c53f299adf17432331fd5610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd9443133cc72a0d386f5b16557cb5a52932d2afee8c29b96f75ff0e5d8423b`

```dockerfile
```

-	Layers:
	-	`sha256:a6a58199c85a0132c55237be5d7d27187876d7ee3f1416b14fcaaa1cc7ee98b2`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73bd9c5a29d25f9da77b0fedb2979737b707d74c6ae43bad84b50e6e266c99f`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 14.2 KB (14250 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:901b7b25ce96aa90447603c3515149806a5d64a7cc6e67690efb485ce28b27a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59836813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7795498bb7dbd01166c2b326da248bbe4cc5d0d490ea9050315b99c8419dc1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df775a7faa43f7f7252f06117029e4dd5a5cbac50c51890b0d6d3cfd8405b0cb`  
		Last Modified: Mon, 16 Mar 2026 22:47:03 GMT  
		Size: 10.1 MB (10077947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58a0f5113878ee3b18eb8ee6a2439cd3d4c0311b4a2b783a57ae7f91570cc26`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b5bbcfe31d9f345176f105df35710778037261c4780ab6b5767185e16411b5`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d101e6915fa0def37b1a745ea4ff99954c71a09f8a1d36fba13a830235ee2f37`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 91.0 KB (91012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:600774acdcdbba3fe13459a4441324f1c491857eabc5df29fc63bd89b791f89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9030a439cbc6343ab6e5529fe5513af33f6a1ea35920d12615cdca32dd0fa`

```dockerfile
```

-	Layers:
	-	`sha256:8a045eefb957935b32df8b5f3f9841257d01411ae260d6403aa68ab7a16f082b`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb422972c47227f8b51f38ac744f2746fa68bd8246da0bdc0c4a0369275bebfe`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:ed5f194f7c2abbaae636062e9e03e383495555d870ecd8a7a204c6ed0031978c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23b782793b45d233eb4c1cb7011a7c66e56885f7e893ff51d4360c3b1dc6c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e327d8697f911e128822f25c7c3a0b25075fc412d07427074366c4a1dcc06c6b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 10.5 MB (10467149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa825e034237965757272c1d539290ce5f98985c6f606968b5a15d07e4230c97`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20d220105eee5bb027f81176948567b8ebcf7b0d3e64a6f976fed93b757696`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2929ff200bd80db2d78e35ec44a161b98776d7a2a1f0470e391c0712e3e5e1e1`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 90.8 KB (90762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4088065eeaf99003a949cc4c86cdbb851614c39f97e157c3e608533525003145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973923d9da01f833bac03850854ab5ff2f09f4b5440e89c3cfb9351a84d2a6c1`

```dockerfile
```

-	Layers:
	-	`sha256:0e6bf81854fe1d14a17ca159eb87e1f89012c8acbbdcf6c314097a44fcc1ad9f`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60759a73115e1d8354102c4f15b6ca89c3ff7e7c3ddc0140a9e3ae91e615ff78`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:b0d72ead4f7914db488f7779d5259a33d59b18a4f3973e2e889ebfcd98ad66fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:195f8e982bb7f7edb9c996c204b1ddf8f55e2f2fd4af59a61a1da42b7f4f3ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59684333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0475b85ed0252659214671d27199f0988e3fbf8dcfdef45481ebb51adb66f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0958f60c5152275d8e2aa46f27c31bf8e62350466d9254ce5ebe1ff17628eb`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 10.3 MB (10293014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a99dd4cc6b98f202f039fad4aabf18786db50c45be9db53232d5231a40f590`  
		Last Modified: Mon, 16 Mar 2026 22:45:01 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4737476d54fc963844a726785647ae72e1ac4aee6752b7e79082232ad05deb19`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682215c226f042ddd3cedea53ea769510c93b14f86b5dd01d531458742684b3`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 90.4 KB (90442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac85d07e7667fee3e1471587f9fd0b61f01b282f168d4c4935268613605f02ae`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:adcaa56d48f63f87e006d4314901e4a85e4f42f6cc57143d1847c015f4916be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c092da940be19a97a6f0d4f93e874c6efd7e0dd855d2955a4ed5636f3f7e343`

```dockerfile
```

-	Layers:
	-	`sha256:9b09648a89fd35b6d25c36f95b0b983326ab1d1930c696db1bd18f2e60f2c3cc`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 3.6 MB (3614144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90f36eac91ebd943a10f26dfffcfb64cf469ec6201994405a3e0632e43fe279f`  
		Last Modified: Mon, 16 Mar 2026 22:45:02 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2c289b0c2d4bb5631d73f7167cdf0b1469136d430775c9e499ed655b2e227727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59837297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99544e8d595bd4f4f730270ed8507040f7e5e54d1d5907a98249a0fa865c709`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f92c8ab9372506e674a894d9fd986fa8e5e967b72d2112de3a10396d44ded2`  
		Last Modified: Mon, 16 Mar 2026 22:47:00 GMT  
		Size: 10.1 MB (10077962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca2e88d525000038257bce1b7337532919c6947404971f468600b39f1dcb676`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b7f8b4c55645ce191bd8e488c7f43b133f1a9012d1ff286ecca0bce803b557`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab02f003018b654c743fdaa120b30684485effd2a5de4335f24daa16b043e87`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 91.0 KB (91036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c50fefc97e01b6c27dda2c96f787d121d2cf01e76a012c884dafded607d742`  
		Last Modified: Mon, 16 Mar 2026 22:47:00 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a9654212e73c8868169d367045704307ebf7b85f4c6d53917c6eea4945a6d206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bf23371fdc78a81a3ee7507687a8bef9056a048d09049dd4392d262edc0112a`

```dockerfile
```

-	Layers:
	-	`sha256:01736020557ccdc3e3407249cd21e0e8a96572884941062bec8e07bb210eb8f8`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 3.6 MB (3615671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42579bddc23e952958f660dcb8a9bf19c229da06cef28fe92a1fd1d0b7690521`  
		Last Modified: Mon, 16 Mar 2026 22:46:59 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:98100e9cec7a59df1753099be2a8adc41c8d0660b1e6c420961f7587698eb00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c789d63431eab185cd52bf6789b84bf1fc1859e61ecc43ab80d6cdd0d5a39f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37abea767e6bb8c916daf978fb4a1dac54edacd3f804121916ad31dd00d0955`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 10.5 MB (10467046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec540dbcaed9de978c5cb39191036757c8635984927ea8201c71f777e2cd422b`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6bfb517ef690ae62f0dcb8ad9abfac9e83f354ec0fe4508a61113f68f494bf`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4ed0cf4df19dedb0d14f9750f7cb7af25c17968a684c3068a6834805d289b0`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 90.7 KB (90734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408ea60a0fb71dbeb5a18ead26daccafc96826a72bdcd39f8e4bd6a6d0b7c74f`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c0e9bc43f78cd1cf795cc271385fea29a4f11fd54e905046c1fc5d3eb7ecc405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ca8c9009e4ae9378709fec75e4d6a18915c9072e085f61de88f8ac31f73595`

```dockerfile
```

-	Layers:
	-	`sha256:16f37269439e4540d7453667eb75ff80f7e1dd937d18e3a35dcddd7ba9418f97`  
		Last Modified: Mon, 16 Mar 2026 22:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffd1eccebc7118d1a1fd1ad1dac6b36ed9ff3bd241e89034ea71a23a9e7a3d7f`  
		Last Modified: Mon, 16 Mar 2026 22:45:10 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
