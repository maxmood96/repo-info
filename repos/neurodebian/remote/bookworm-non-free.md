## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:fe69c78b7324bb178dee86ba6feee10b12ce31ff043b238f974f8a6563650d1c
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
$ docker pull neurodebian@sha256:7e398bdf282bf7b2de959d4e7871a00efdba7a3b94315f38909d9ad9eaec37c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59853092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0b605439b5903c5bd63e29c9fb820b6abb0892ce58d30d207c979223b9ec1d`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8384fb657fddabb65893303e0a8f3c12bff01fafe00408cb06cb59da23a5b77b`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 11.3 MB (11266799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af38886ee03781ededd4d9c12fae87ab80880ef72a9c2e172c8d5f219d9824f`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ac60b75849f44596a182fc0d9c00455a3ec54a32e5b38069df6b450a74def`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbc24edec90455b4172e2932b5777bc5f1382faef1259e1e04ecc6bae4cbf98`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 93.1 KB (93129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29795a5744ab07889ef89525b2147edf8c116dcfe94fa2db1132658a2dd9ad0`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b87313acde5fcf89bf43bf7b3b5871cd545f8a3285587ed68bfb4b5b57e61579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53c6b4dc71ea8685a6a40ed80932879e4014a40561bdd1a447d5f358545ec1c`

```dockerfile
```

-	Layers:
	-	`sha256:6c9ecc685f67450b07394a41de82db9fbf4ad8d9e1893feceb4134ce6a4d0ac7`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 3.9 MB (3934212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b606bc0549f263243d00b7f86422fb054bfcddf31523519a277b3ef0a891815f`  
		Last Modified: Tue, 08 Apr 2025 01:26:12 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:45ad749f9bcd8e51602bd81dbd4201d29678379baa897125f9bb7f77d20f8465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59656149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddecea2fbc72473b511ca2e1fd47d21929e18fb548c9d544c0ac01712e3f9ac`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce08a29378b322d580a290ac850ee07138f732ffb563fd5c9ced94337ecfadf`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 11.2 MB (11232654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c994ce850f986eb5546d5276357b320b7bde68728c6257f9f77b9539290f72`  
		Last Modified: Tue, 08 Apr 2025 06:36:08 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c982b1954d94fe6ee8540f3d265491f3cf0dd395d3534a72e93c4fad36fbd9`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1367d165818a29284a9956a4df5e0769d1e2307631fc56bb05d36b69ca141`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 93.4 KB (93402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4af8e57251ac91dbbc525315d0377b42e6a750861089644e6f83134df5f4cf7`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:889d830f6f8c37bb97f6c577d74b44ac7134ecc7067b9e1659c0329b7051917b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3950965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e0c4c6354a373d3e63afd8b8b68da58b7b301db319e4432a32787cf11bc2a36`

```dockerfile
```

-	Layers:
	-	`sha256:f1b36a946b7421c5d1db125ead18ecf82bd46dc1d400123d4f5a8799b10fec5d`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 3.9 MB (3934466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10e4b44ba7973ffe780662ff642440c6f6ceb6d4d6578bbfded6f9aaf6ee4c5`  
		Last Modified: Tue, 08 Apr 2025 06:36:22 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:77c4a11b877bd3695148289f8a619cd0a20b104bf12de5acf55b239b72c0dc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00fb6ad261db4fd2e52ce4f0d6ccf15f1d0a4db69e6b7dd032dcea490167ed52`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c608ceda0b7454a97d884128aeeaa0bbda21fdbdf8119d7d88369c9ad0b91dd`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 11.7 MB (11688951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76c42422411b6fa3e8310cda6b4848d0ce9e210ed01e9825da2fbda0d3aa64c`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6869c5c8538c781cc3026ff93a7d2bc201709cba9d62d71943d18c2656e5a614`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883527fb04daca1643441eac1d252402727d310a2f385e3bad00cc08e0a95ea4`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 93.2 KB (93216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f0e418c69eea3da98ff7405c3faa74ae00a63913463d0cb139fea3d28916a4`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f231e6f1d97565b2e28c8e6e28278ae3ded47c6088092bba32ad9deafe1677d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48e2b84fd898e55805a1a87c6dc5ae8c4ed71d306e06cd096b5ffd8b0a9b40a`

```dockerfile
```

-	Layers:
	-	`sha256:50be1ac0d7eaa72054bc23932238bcb1c9ab939bad36afe36ddd2c47b82a387e`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 3.9 MB (3932129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e81fcc4d5a20ce3e7c427e156d5ebd3b43b59d07e310b47b711be387be00e8a`  
		Last Modified: Tue, 08 Apr 2025 01:24:56 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
