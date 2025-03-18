## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:1b8d92d3f95605dd791cc78598d2fc0664b306adc7ac16a74d121325bc53f864
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
$ docker pull neurodebian@sha256:e7beaf31077364243232dc2fbba0eb44266e4559b52e9501638ab5d4ae08f4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59829977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab17032466a8c007742a8f9848a79182bfca8e2376bf9894148129b16b9961f`
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
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fac63c7d9f7ef110a69d77fbe8182216d989e18f3fa90b631d4d0f82ec2d846`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 11.3 MB (11266804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b6747529bf8fc1a2bcfc006509fb8f20ce93d3013c4e62cd6c22f7a96b47c7`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9501f0564def637560b9a43f495ffe5eb6b36a0582b15289318bd03a1e0786b6`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30ff8a7840cdab0d8fafa473a8206a44bd21f05ec8f7618c13a40b191222f90`  
		Last Modified: Mon, 17 Mar 2025 23:14:46 GMT  
		Size: 93.2 KB (93163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4de88b8cd6776389d9d4093b0956d512529dfe454805ecf854d4bc5e235d7e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46520d3b0a0b7122434db269818778d9c04d6bf6ef8aa1aa709ced28eb078824`

```dockerfile
```

-	Layers:
	-	`sha256:37649676f20c25aac3939a5931107fc6081d315df30b12f32a19d0bfe0e43996`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 3.9 MB (3932836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4a38f1743d2b7e69328691bb1263d1b7bba2dfc21e3f372b02ecfdc3be7171`  
		Last Modified: Mon, 17 Mar 2025 23:14:45 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e651935ca1f03939fe4ed9455800c3c1e8ef1612d42bd36995e03670e3384c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59633066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bd1caab4861a9612fbb5f117ea9e9381404e7e0bb14a07fefcf03617ccdc64c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae967afd60b725a25b5331c9cbd34561c12da2a8301149a9639c98480a289de`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 11.2 MB (11232645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c54c780d253d7d0b4b86fb4897f07cd19e7204b2716b66a38a7b0c91394d6`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1ff626d1597d172c9a62957b7cd16bb94528c7b3bcc13d7b6ae48e55ac3d8f`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf94fd4ac50b6c92e2ea9fb5686379af98e14585c1fb021c63b31c3f93024ff`  
		Last Modified: Tue, 18 Mar 2025 03:46:01 GMT  
		Size: 93.4 KB (93391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:46d085013c014e2837557269b4b40ac8ecf252474c52b2c59240b75fe997cc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f0c34b48d331f616bde5abee0e6f645eea6f724a646cc55f12fa3a31f8049c`

```dockerfile
```

-	Layers:
	-	`sha256:43c0703f7acafaddf1bccdbfe31daa0d336feaa460b19e63bb09db9456e7cdec`  
		Last Modified: Tue, 18 Mar 2025 03:46:15 GMT  
		Size: 3.9 MB (3933090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74838dc6370fd63907944e920b3d8cee54a5a4c159f6d97737d95da082d6fb29`  
		Last Modified: Tue, 18 Mar 2025 03:46:15 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:845820d3cb18c53d7917d64acd4cdf435fc5e6e9d0665d673708145a76eead55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61238765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407ebe7e9e963870cf12226b6d730b5c5bd3474b5dc3749126c49d1d774d42d1`
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
```

-	Layers:
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb27fab9db91706335a011f83fde5a35592a369f97cf21bbfde9353598995adf`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 11.7 MB (11688908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99467902761ec4b28d838dd4f8ae200a6302e1f42c430209495d60f927aebd`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40f1c295b4ffbefbcf1cff56ad1af7fb30fc0425899d98c643e12886edfe8ce`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce5055b6aaf4f93465c5343859d563f693e9a1fb6f18a359da46ff3e77cdbf3`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 93.2 KB (93203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3d0e14e7fd72d80868c48becd300960bb2a3480422f9d1bab5f473c7045c9be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bd47cb5fcb40aab35579339bbe1f842a713c6118b264972c4cfcf1b31125685`

```dockerfile
```

-	Layers:
	-	`sha256:69093413e29bbcb0dc43e20c42d776158212cea2f0926a4c75caccbf26161af4`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 3.9 MB (3930753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d42342c086ca4c9be6a6f1ab7a4267e68585526df263f94ad060bc7e5ed30d28`  
		Last Modified: Mon, 17 Mar 2025 23:35:30 GMT  
		Size: 14.3 KB (14282 bytes)  
		MIME: application/vnd.in-toto+json
