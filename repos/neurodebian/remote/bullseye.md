## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:07ec8826455f71116f0cd09239fc693befdb03e4e448a03bb910f07a99cf31d0
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
$ docker pull neurodebian@sha256:57b3cfc433347afaa2097cff075b9a0e638baa919a18d49f4fcc663f4b2a4bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c16e8bb784bdff112f0b4f7e93f2824a3c4de2ea90e1df160f767eec517056`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:26:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd834ead99fe4ea0884686321217c38494a7a0c7327e2a5ed98d978011de7ddb`  
		Last Modified: Tue, 24 Feb 2026 18:43:07 GMT  
		Size: 53.8 MB (53756434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f4e9f390893de3473c4948066d96861d3545a9549bda7e6585720b178aaea`  
		Last Modified: Tue, 24 Feb 2026 19:26:28 GMT  
		Size: 11.1 MB (11103516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25e38dc4ee057693afcfc50f120be00455e01bc370c07e44d8b4923831f80e5`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9834a298c42cd179aaf5e753b162aaff4ec1361a600ad12a3adfc4503464149d`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f930e026dc45975f4861f2f8fce6f504dad34150458ad7fb274aa89bdc644`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 101.4 KB (101390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef9e27f0a2da3da17ae1a9f5c8be6874617e694d196edd6d560055601920cdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3776dfee860dab83c5cec022fa0812ae0882590feaa6a6743e224b04d270e43`

```dockerfile
```

-	Layers:
	-	`sha256:04959d0085768d7c51ac2afc4a9a103fb8055e9cdd1afda0d91a43d6d3c488b5`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f114a6480469f96c3baea36be2befd19e5abb382fdf607297d61d74c369b7674`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1fb13a20d8b38a6d245ea9fb46ddb887b6e7b602551f976efafd4bc68b135189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63471415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a84e7fef8e6e1b2c50c977788ce20cadfc58f82392c6c45de4882f1ffbdae81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:30:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:30:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:30:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:30:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0509053f2cf8072309184287dd2fd397e589dc5db17a1ddc469001be80ea07a3`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 52.3 MB (52258392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f112b140a2e5ac9f26401235529c19a27af696239d36f0f656d0716c07411328`  
		Last Modified: Tue, 24 Feb 2026 19:31:07 GMT  
		Size: 11.1 MB (11109751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a4f15bbb566fdd6bb259b35ab798ca442464882b9970eb8f67701ba65b893`  
		Last Modified: Tue, 24 Feb 2026 19:31:07 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9189331932b7f9a32d2ed2b5a39fdc6837ff44c2acfce0a66bbdba2ceb315623`  
		Last Modified: Tue, 24 Feb 2026 19:31:07 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf66b7c8c79b8e4b0226220bb238af8fc7fe22ada6a2c418535a1717162ff587`  
		Last Modified: Tue, 24 Feb 2026 19:31:07 GMT  
		Size: 101.1 KB (101115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a5dbe47d4a8da807830628fdd688273bcb4eec533c634673a8c65f8814f2f540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bc29aea6145ab811acc30ec935dca40ecc915dc0dc1a150ac0fd2d2cbf2969`

```dockerfile
```

-	Layers:
	-	`sha256:eb35aeca99d7fce65d95fb5d23e8d906f1913412034d38583a30c7d7267c7099`  
		Last Modified: Tue, 24 Feb 2026 19:31:07 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53be794dfee6636487ce94a83a71a7d5b60d89febabc2b1ffafbbba97841f50`  
		Last Modified: Tue, 24 Feb 2026 19:31:07 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:5c09cec2cd512b888928d6d0e96310a64a86f19dcc23d5efa14db3a72eec1398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b53e4e8305b545fdcf0b0e93653af7502e62290b757059d1dca5b9eaf00b20`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1771804800'
# Tue, 24 Feb 2026 19:25:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:25:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:25:41 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:be7de57c5a292b6137b558f622789891088c38f02c67ce301a1559809fbe8ae2`  
		Last Modified: Tue, 24 Feb 2026 18:42:22 GMT  
		Size: 54.7 MB (54699784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca5839c44f47b8b0fcfb90abd746773774e10ea067ca65fd839528361e5abc`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 11.5 MB (11502348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9df8709d6cff3c66afc9577586ce2aa5d99746df5dc5f6f9a67d9f34c83ad3`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21f471f30c474d678a6488106f00112f5618106783f3b11cd9eeb2c02253980`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ad7c207cf59387421378643482361868e7889431584e43be0224222f7e5e13`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 101.3 KB (101273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f550c88e5d103f7cacd430b4cf8f957c890d307c55922ff9452a30a5d919096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c799c374e6a1ce13631c4f9deafd458654147f26af243bc12c81cb7125d627`

```dockerfile
```

-	Layers:
	-	`sha256:d13d598f875d245f270aaf50e962c68594fee4f79d965dd6deb842512bc7bf08`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22462bd2990b8863af14d491b0ffe916d621190bbc29786131b73b7a56512958`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json
