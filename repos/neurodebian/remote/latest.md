## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:57bf3a66ea98601be74660a4a7797276d3badc3b433b84be07822173c01a7d42
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
$ docker pull neurodebian@sha256:0f10c55925c7daa6986178bd929a59c328e73b14d33e638b933d343ada75bffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32d537529d69d344d0eb896c9f97232c3d86f4bf97570473e3fc59c980acd6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab8a23fa26af0a8cc76053873ce7f2f4972656e8f0fce2094d6a666e3be7772`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 10.3 MB (10294155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6332aa2ff8b6e8865f809e22829bc2fa69b14363252518a815b841a1f1e96903`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d07151946d2a0886dd871c29d5af1c81bcfc8b58b498e8e10191f9018b2566`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9b52337e56a0c8b560c3f38b88a4043b2f81e9b7787f91fe3e15d9df02b94f`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 90.4 KB (90436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:253280c8c43c2b210aa41b9932a9d65d4b1937e1cc592889552a887ddf9d0c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d78b8f51492931a4c575295e525c37e9368e45303be897d48ac5cc9e6ddb266`

```dockerfile
```

-	Layers:
	-	`sha256:391817222b355feaf88eba1d4e2ec5b9e43b8395e7ba2cdde60a0a46a41e5a18`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 3.6 MB (3614164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a2708db03fe47ab7d21c2de25cd8c8bbb2d7ac4d9a3dba9f126c55a2f3bbfea`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4d733fa6ff08050595170e47efccfe107fa7fbf6d920d166495fa1ac2c2bfa2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4c08654723853eb5602234bae5feb235f2fdf5852a0bd21e23861a7de27bc5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8663f66a97521bf18781b6a8ebb14fef9360e63aed5744a8826c46b6e955ff`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 10.1 MB (10079209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898f78772560357ad8f1982fcc959f06700ed89aae96a065a560a906236d8cf7`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c646d242c23c90ed9667d2fbcfebc5fa2ff61e602411007d42b67903ef19ea3d`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0366805b83dc22dbed788828fe85a31e7d2925bac97277ead3789e69ec670bcb`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 91.0 KB (91025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d09bad896d54687ddebe1648238e4e9ecffc205b3697da54d7432644747a8ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee44725acd45051b6ab2baa0a69bb183c202e5f01eb0bb9fa46dec30e9fb02e`

```dockerfile
```

-	Layers:
	-	`sha256:6b665e7bbede387f1cc367505a144eced1dcf9237f7bfe90cddd631df2f08035`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 3.6 MB (3615054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b382e18a90a184f236343b396eace7da5a3cb00b4f6f8f273322d39f408687a`  
		Last Modified: Thu, 11 Jun 2026 00:47:57 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:69272e86cbda3b80360145b7035894858f8cfbea157d8ecb1dc592ff7f95706d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d156e7bcf79c18dd9eba9d5b14acb9798c93bfe93b50dec402f6a054d7cd0a4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:05 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:05 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:06 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96262f3a6afeeffe35b7ae82c64e4411332dadbfc81b4e151d05d1ae95ef0e5f`  
		Last Modified: Thu, 11 Jun 2026 00:46:17 GMT  
		Size: 10.5 MB (10468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9803f3a3cbbb4fa8e0527752d2fe446742a844b364b659fd3471c1412c7de7ae`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328489f211ae28ef4a19ffab0576631bbadef0b960df6e7cb234806fed854cbb`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480857bb2368ea3670f8a8b5dfce2c9a13b1b59414ec77b0efa36c938bfdac56`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 90.8 KB (90776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fcb451aa5bef61bed7700ef1c06e8f31e746f268f0ac340de5e44aad5b38345e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd93bbcf1197ba8c7cdbf851083e591e6ed5f96d4de0e879b2dfc99dc636cdc`

```dockerfile
```

-	Layers:
	-	`sha256:098c6beadc9d4944f26eb9ae6a78f28d6e0c48a29e9e44e2c14f28ded1b73576`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 3.6 MB (3612112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54b5e77ec315284c66927105a56c707e59dd8c54f41091f07f9381cc23d970ce`  
		Last Modified: Thu, 11 Jun 2026 00:46:16 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
