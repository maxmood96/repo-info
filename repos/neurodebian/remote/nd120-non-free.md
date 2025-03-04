## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:f0157dea62e36694142a3352d67378c67662113bbbc12102e73872fca85ed4b3
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
$ docker pull neurodebian@sha256:069351bde6cf26a7ecca78ceb3c4fdb2faf2b7f8b020493d9c85742e978d3a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59838710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832362990aa15ae4fe2c6583850d85eadf09c7e1dee09dc97d5e45a4538721d6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbaa660fbbecd5c48154c81991b6ea6cfc1b26a6084f186dd353e56fd7ad451`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 11.3 MB (11266816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1023c259e18a20d5697dd01624a544563e5319e4ab3f1f5b4ba4a8f223140a46`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 1.9 KB (1904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf1fd050755792c16337c24b3484188526a9d7cbb3c8173584cade8f7c8a86`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0911208721e5b3cd72019b88d1b90f094c2514899435ddca431dee40b1dff210`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 93.2 KB (93165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce2c1d0bb7425eca43ea351e91eeb73b07fb9b4d5d38a9ebbe4988da9b7a8b3`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f021f99077cff3d54a89cdcf5369ebd47278cb0888b9292f4c4840608579d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dec4357d9ff91dd6bfa4eca6cd1be6982520f1497ce4043351a3158c526b0c8`

```dockerfile
```

-	Layers:
	-	`sha256:820a032f5af878d9915fa44617a1551d6929b97679448663da95f43c831a2830`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 3.9 MB (3932868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b79ddfccea83f234025ba11fc8e32b65ad0b656fa77332dd9f1a3b9b95bdb3`  
		Last Modified: Tue, 04 Mar 2025 00:29:25 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c9132ee4d33a0b351502b0da50911ad773b0db0b965ca95079b806fe7bae8ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6220af8a84d5b3ac3140f7f9e59a3dff239f8407fd5cea63a4e0448fbea9a6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f934fdd885043c38d5ca3311bc219b22c6b73a0e7858d6b2f280b43194e664b`  
		Last Modified: Tue, 04 Mar 2025 00:35:24 GMT  
		Size: 11.2 MB (11232534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606a2d4a3a2584c4c7d955389d138d52a3609637cd3eb74998a5ee5c8b20b4d3`  
		Last Modified: Tue, 04 Mar 2025 00:35:23 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc81288c2e2e7c51508531a4ec9e32086ec519cf09e49a0ea58c3219a247321`  
		Last Modified: Tue, 04 Mar 2025 00:35:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acc512a0ea219679579dffe3e7d4b1ed1ba1900e5b906eb85085207d86ca620`  
		Last Modified: Tue, 04 Mar 2025 00:35:23 GMT  
		Size: 93.4 KB (93395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8454510eda1b933ea1c35e6fa8a9d25f653905b4287fb840441f6180fc31902`  
		Last Modified: Tue, 04 Mar 2025 00:35:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6061c47d27cc155f64e35e3dbe7124cf9b60a0cb83b5ff999ff3c6170ad532ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8da60fa41dd5da476b0fa9ddddab3993af60584667051526cd6b74a465cb534`

```dockerfile
```

-	Layers:
	-	`sha256:d06f8b36ce8a7131c85cce44b79ba433cf8b53b2fc78f673c52388e67ffe5f97`  
		Last Modified: Tue, 04 Mar 2025 00:35:24 GMT  
		Size: 3.9 MB (3933122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72221dba7a2c90dfeef51195529b81e5e217287097b2053858922bce33b8e5ee`  
		Last Modified: Tue, 04 Mar 2025 00:35:23 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:108b299d55303299388d883015a7d961ecb8711936d7d8f5736ddb835014816b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61243304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8522aabf29cf088d1ba651d1b71653f0816a1d3384063c409a0aeca0bf637a5b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:72a1355d66794053c103a8d716f9b4ee62b851248a331655e9fc395b489cded1`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 49.5 MB (49458452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e143c4d981ab9419de3aac00d7b56e528c60071768182964b2055f30616c2b`  
		Last Modified: Tue, 04 Mar 2025 00:29:29 GMT  
		Size: 11.7 MB (11689008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4e7b80fcac41ba9ee304f5e06e75159bf9bc84d9c5b10796cbce677e5149c7`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcb4848621da4c32218ba35f21b6f9b3fb9df31a112ea95f0ba81e2e842a182`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467488168e2abdcccc61a1aa4bba398fdde358646dbfa604331707a4c8260590`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 93.2 KB (93215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d67f95a18f66954122ecbeb329c77aee751c0211f680c2542f74cf8c2b18ee6`  
		Last Modified: Tue, 04 Mar 2025 00:29:29 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c3c7fef16d09d07f49dd179bebe00d3a6fe20594e712d839fdda41db862bb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5c81c22c29a4741854820a4514bed7c11ce785975b4d3c8993efc7e33caaf9`

```dockerfile
```

-	Layers:
	-	`sha256:f0dc966523c3bd974a251f4b3c08b11faed66a7215caae9b58b98d1726ee3085`  
		Last Modified: Tue, 04 Mar 2025 00:29:29 GMT  
		Size: 3.9 MB (3930785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5aabc6203b7348f2417f35d70e928713e394f117c2ad27e843fb3d5d4b2f10f`  
		Last Modified: Tue, 04 Mar 2025 00:29:28 GMT  
		Size: 16.3 KB (16310 bytes)  
		MIME: application/vnd.in-toto+json
