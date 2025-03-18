## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:f97f7c1408730a52232379c91698952fbfd7694661007a22978148522602ec5c
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

### `neurodebian:latest` - unknown; unknown

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

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d341df33dc4a4b564b0c87796350ae270ce86256347b63e316e9e0e2f2193e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59636114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fa60e5f8a6f867c62db1e223fc0cad0c482d0a8e5bd16d1712ddcc59d25f65`
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

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:07ee22283455e9c1bce91c123beb7418317e3ee75a8da9b9f8998a3c88cd53c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d20a2abdcb9b2c08cdc94df1c9b148853b7767b5a910814c34c233673b920a2`

```dockerfile
```

-	Layers:
	-	`sha256:0521310e15e47494eee3d6673506a46142a9a64ac5437009c816a43932a7bd25`  
		Last Modified: Tue, 04 Mar 2025 00:35:38 GMT  
		Size: 3.9 MB (3933082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09adba5af8d580a4c464c88c7206025de6ffd3493c431cbb122f63179399238e`  
		Last Modified: Tue, 04 Mar 2025 00:35:37 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

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

### `neurodebian:latest` - unknown; unknown

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
