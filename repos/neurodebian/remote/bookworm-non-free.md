## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:798293a2d2400bb7041459d7101c2cb4c94ad793bfe3b9366f9e8659146fa41a
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
$ docker pull neurodebian@sha256:20a32f8567600d383fba6d77eab331b4a2141313734178651d628f2a47af6978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6200527a4aa8aa288ee0ec7ac1ce183bf610f802f99e77aa5388705673723ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5685004f5e733b959068a239ccd559409be891f72e0a4c3722650701b4376a`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 11.3 MB (11266762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3043d5c6b0762af59359511147e1809157cbf553c4aa5e6f4e2673a71d02abf9`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eedfcf6a2d59da3ef3f7c46a09cfa4bceef12887b159cf6897bb8eb43b01122`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e818ffd9ebbb5afc4129399d945779b7dfa6351f47aba92aa2a157c59bd10476`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d52d04bb2c70895dccc6983c65df4f50ac2043c5df98cf733c34c5c8d3af7f`  
		Last Modified: Mon, 17 Mar 2025 23:18:45 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:96216fb906ca37d1c9754d369e90f507a94ec0319ed72594cf19382cd65dbf10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66ccaf1c4cfa6893873161b32f8f3294da071e3e82bf14a943fc4aab5568834`

```dockerfile
```

-	Layers:
	-	`sha256:7a54c1f8c9fe526384aa17481dd2ad4d7ccdacd55d955c05b183b595d9e12877`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 3.9 MB (3932876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c80f3d168e124ca109851fdbdde7b5bc8369fc9eadd378911b348031a5d356`  
		Last Modified: Mon, 17 Mar 2025 23:18:44 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

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

### `neurodebian:bookworm-non-free` - unknown; unknown

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

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:4946beff250a03b51713fbcf71c7869c5e466396892c429ec0e6fc4698d379c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61239222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0dedc62aff44a64042f83ebc2a504d4523a6246464072883d3ee5f52c62231`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ec2587db02dcc0c4ef5c57638ec607829d8294afe02f44d9968b0d0dad0946`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 11.7 MB (11688909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e410407700357dc5f4663b4dc00600f8905dfac028c01c3779efc170d9baac09`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c1547f5883513fa5c1107b9d2212f605c4f039d32e3dbc36ab39858a7ee7f1`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af79c8a29d4fd496693dc1ce9e3e6b5910801dc2ea305ff3f2fd23781b04f7c`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 93.2 KB (93209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d756415886c6fa8cb247b5f3fc186432ca659aef8a3ac7fd5116a54a6e69bc3d`  
		Last Modified: Mon, 17 Mar 2025 23:33:40 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:25c1819ae48659438eb884c26218d9cc7795dbbe8a51011c2b92c71bf71fb69e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77049019a43b99e7b68a30df170163a40d71c91e30318f0bd861820eb4326cc`

```dockerfile
```

-	Layers:
	-	`sha256:864fba0b0ceeba292847cb330558a0f0295fe059586354f8a162d3ca900dad2b`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 3.9 MB (3930793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cebc96853d0a57d9b922acab079aa0e3df4a36e199de5b0ea36102128c9d4a6`  
		Last Modified: Mon, 17 Mar 2025 23:33:39 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
