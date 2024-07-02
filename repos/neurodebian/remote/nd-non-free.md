## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:dd9da3972660d59d3362b8d0703c737d414e035a8cc655d86e4ba7528be89b27
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
$ docker pull neurodebian@sha256:171d7790834ff2dace09d75d17fc095f5e0ddb5a64ab2f2c6c20e979b8283e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58950607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed02da4e0059860be250a87aa0f646a80a9a97405ef1de79b37b13c9eece8a43`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf83030bc061e8d24d8a36b4edb2846333916985361600a06dfb635fd59c8068 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2d149d696b13b9c3df064cbc77767f81d4635c7804547d50ff7da0c45c51990a`  
		Last Modified: Tue, 02 Jul 2024 01:30:17 GMT  
		Size: 52.6 MB (52634573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76eeeaf4645947114337f3365b9e426c0269613f7bc3b5a498de5bfa2dc9f7d9`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 6.2 MB (6223730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bf23babadbd7e24e99d5f11987ac80999f65bba9925676b393344e7ee94208`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa10af556b8d2d97b814bc8adf79194667d8c4ce1a5024278442d4737439c5`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2986345555fbfc0e18521aea6d42886d0b779a81cfe975e9eafc9ed31256d946`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 89.9 KB (89931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0757077789f6773bec41e3ee672f0542a27c2a763cadb11bcde5a56e46ba8dc1`  
		Last Modified: Tue, 02 Jul 2024 03:20:08 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73c2c384861f8818e86257a5bb7c489fe6c75e81009f7d36a5c4787a097dd6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be47e1f771cae7b74651749d34cb0056ec051866bf7e66c883ba536bab0438d7`

```dockerfile
```

-	Layers:
	-	`sha256:174f706621926c8028ac0797d12d9ea16ffd1a2a33d41ecd5081abc4d2df9679`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 3.5 MB (3543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04024201415ee292c1e9d968a7e8f25fb4fa99f389a1ab14070d733a890e3448`  
		Last Modified: Tue, 02 Jul 2024 03:20:07 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1d6ee16b19cca79b92541bb682a4c922cfe787ab167987a257b1cb41c69628da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59201205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61af8fb9eb88cbefe347add336cf5ddfdd03de1bbd8def9760ab1aac9ad011d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:13d2e6714604c76eb37d955b64f923c5e9360ac3b98a7115cf15ce9e648a1a56 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5c22b1ba66cae5b1ecf15ba852e6873679650dcd639327a03cf68963e082f4be`  
		Last Modified: Tue, 02 Jul 2024 00:43:55 GMT  
		Size: 52.9 MB (52888757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f682e5d0d35b6507170549e927b44fa72be309150cc766e8c567a6fff21d100`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 6.2 MB (6219470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1116df5d9885f9a9ff682c06a547c1709ba2c34e3e92865cc80ef986d89e795f`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2529b60acd15a8ed1a099809bf5493031c27bd7255a688091ce443bd422685a`  
		Last Modified: Tue, 02 Jul 2024 16:02:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c43a6b60e4e33f946bea9f325fd364d2d5bd69f0848b7f74b24cbf2aa860681`  
		Last Modified: Tue, 02 Jul 2024 16:02:59 GMT  
		Size: 90.6 KB (90605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a830aa41d3e8d87799e4ca16d1813076416447501bca235a0651831bbeeab350`  
		Last Modified: Tue, 02 Jul 2024 16:03:19 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5aaa618816e5505ab338d006a538bd7aff3a3178b69f16b46b95f6d8f64338c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3559750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8b09ec1e0a532999060c6cb93a0d079d1073f63d48db887d7e839eff87c70b`

```dockerfile
```

-	Layers:
	-	`sha256:5c69f38169c1a9102899bbfa7a76dc58e3359ac9e4713d70a2f25ec4a7f28693`  
		Last Modified: Tue, 02 Jul 2024 16:03:19 GMT  
		Size: 3.5 MB (3544046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78f627c118c0b71eab6eb5458d2d3a87f5691c5e6abee6be8be9f9c1eb4baf17`  
		Last Modified: Tue, 02 Jul 2024 16:03:18 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ccd33fe92961585e691320103b2d0f3466709f199056da460ca62cbe0d5470ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60169098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca223e31f2027f0bea7325055c5d03f33eb27502dddac3a3b4213eeb1fa81e7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:a08584f3c5024aeb655047534f24f132994ce1978bc3c1b585197931050df05d in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fcc722c6a8b995b7f273820b7fc927164f6709bd0e428b87e24702a321694439`  
		Last Modified: Tue, 02 Jul 2024 00:44:25 GMT  
		Size: 53.5 MB (53522389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2067d5ad59a2a2d20bc80327b6f6ed28714940579539b9812e9e2f3157973cf`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 6.6 MB (6554505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc9e048603bc334e451f2a2ff1b8b689603b80171d863e44bdb12c8bc7a9d70`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5ed2c6d104afdf33dcc4ddf797b004d5933a8c960beb94d44ab97ea188f35d`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86bcc6164bd435f1f582154cd31a155f0749b0bfc6efc6e88c71e43f0a28937`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 89.8 KB (89832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b3440dcc43323d1971173e19bc352048910e85501abb4e5672519b888b9267`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e2c0308d75c24d63b042d64f6d4ff437b38ead191a1a197adc3d3dc0075bae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3555500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93a2eb119062ea2accb8a0e28abf2cae2a404016d635e3fea9a1e8d94f10085`

```dockerfile
```

-	Layers:
	-	`sha256:8de0478d7152d9c9a0cb48fdddef7ec88969d9806b1b0e61fd124ecbe855853f`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 3.5 MB (3540100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe08c161cbe93376c006e2d9a437eab0416700e73293e4b0d953bcef3d26d97`  
		Last Modified: Tue, 02 Jul 2024 03:20:04 GMT  
		Size: 15.4 KB (15400 bytes)  
		MIME: application/vnd.in-toto+json
