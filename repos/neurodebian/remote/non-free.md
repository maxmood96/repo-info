## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:9a1e78ff7194ccd99640b7d1d86bc7c8cb0466427157f45b873500c0fe7886f8
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
$ docker pull neurodebian@sha256:9b74c3202ff1d28a9bc492b31b8ea9e8c9b9be6b63bcb68e0aa15fe63e173047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733c6cc1679ff8846e1c2db00fdfa0a14c44d7830f4ddbc5241391dc645b802f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9443e90dd36b4d7df0ce4d2bd3a9f86ccde7df420c85200869452e1d2c310a3f`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 10.3 MB (10294066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b311040279a30f28e966f2a5f173993093cbd64887ef01d6e4aaa7d6c49715d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8afd3a0920f39400ad7fb5ad3a3d14689c9cc1c7252860a938da81870f71c5`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118da0436bfad5757b22eb7483dfb8d4caa8dce58fda3d5e745f38892404501a`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 90.4 KB (90387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaade245ece996568fb7645f92a893e7db0b8361b850a93fccfd2a9d94a7675c`  
		Last Modified: Thu, 11 Jun 2026 00:46:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:28e7c75fee510a7acd4fc200e0d667d9cfd91e9ab8cca5e946e378b1b1e4ec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2eca42e82561b2771d46a87c47c776316b6e839cd802e995555cbfc8465b7`

```dockerfile
```

-	Layers:
	-	`sha256:36cd5b6c3434365f2cf71c0b9bd5700b02ac52aca67b173355b3f58bc1f7948c`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 3.6 MB (3614204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4b92efa6ac90e31135660a7259903bca1ded723e7162654d117bc591dd1faa`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4f735a295bf56114dc844067c8559b447376008a394f05dc7bfa19b3cedb5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1fe4fe93d83961ba13a917f6bc125e566db9df7f299c05d3b878ae060062c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d619e0dd73deeb9db2b25df205732643c98352d9d7155abdaa4c445585b7`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 10.1 MB (10079193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f03c6928c07168f2bf548e6930872e19baf37abc1cf0af526897654a7d8b4b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685d980ae5b64951b7260afeea4aff7557f31fd69a01a970bbbb9446a664b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675ff08b6519b01acde1fd7cae45036ddd625bd1f8ad29726f13b0c2d8e9550`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 91.0 KB (91040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf2d6bd6dd274b0fc66d385da6ef377cbbf87c7b53b2ffd1d82140014e913c5`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a992e0d49e73cfc21fa6db8235421e67f6a92ebdb3674d279e7dbbb82500f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472593d75487081cd96f86808b920d371d5794341e8330a5b48716f70fa189a6`

```dockerfile
```

-	Layers:
	-	`sha256:e942ca8eb7f884ac336651d2badfbba2ae0e1c3b2707ceb693a8dafcfed43268`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 3.6 MB (3615094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a70c74b7bec526e65bb31fe6513941cd08cd11448342af81a777e368b4903c`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ba55fdf29b76d9a6fa3fcc409bbd8b25ca5da3b0b13997a30956548b570f4eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61397904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6da215c6f0c8bbf5f29e85a3b18a4a168e3f9553a236d8b28fdf5cc034dbe57f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:b32240bef83f1a91259785f4f0dac80386c2d42ea09a3339118c915f47000b2f`  
		Last Modified: Wed, 10 Jun 2026 23:40:31 GMT  
		Size: 50.8 MB (50835563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e738cb1ceb88ca93b48e46391fca14a2453c6b28bf04b3f259957845d2c1285`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 10.5 MB (10468197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3813de1d4b6737b778cb0481960ad48ab76a08b846ba22ecc73667dd9b0be5`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5a5db62ce6cc0853e2fbd0c2e8b7fb72243739d8e72332ac093939d5bf056`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92a3c19bfcf828486f3d3d24bc65e7437d50bdcd54dd7faa442507acd9d6df6`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 90.8 KB (90796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2662812f973b46690ce7067465584113462b5024e4883fa7e369c49fa3f84702`  
		Last Modified: Thu, 11 Jun 2026 00:46:27 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44f16607b3a5a7c4f7d6d76c92f2a6e911daa38609723e409e3e2ac59a9c15af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfa1cf9f73b3e9d51454fc87de8e5a66a7e3332691e74f4cf0852e92b4fc61a`

```dockerfile
```

-	Layers:
	-	`sha256:e1f89e434cba8fb4d15664a2a2521718c5372c01aa9e91b27a3b96090417cd8e`  
		Last Modified: Thu, 11 Jun 2026 00:46:26 GMT  
		Size: 3.6 MB (3612152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f80982c64577a8144c703637517361a23b157ec5d3538836f1ea2e98208d9d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:25 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
