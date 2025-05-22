## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:0ab91160929ea8f620201f714422051504bdf3c80fa2e25b59c160e144d9fa68
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
$ docker pull neurodebian@sha256:246a6cea29bf1e53a63f2df1fa30567895cfdd762588b7a18d23e8f9ad82f454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64958971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e7f339bf19897ed357c21d32de33023e06c814327decd8cea75737758fc620`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca25855464c362ff5b431ed1c58bcac1d3074d341dfbe0b69db0c4b7b06ddfb`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bd852d80e3b0c678ae63bfb3948aaedb9a85ffee30335e3517dfdb5079959d`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755cd40c0c29cc545f889321eb72bcbd161b6e91d0f0b1b7e45ff98558c28ca2`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4067042efe9918fc632e3430f0139557b52b74d633b305ae3271d19e6436a4a6`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762595f10379f52572d8fd283315b81ce1b9219d0093d67e34f012a23d953ce0`  
		Last Modified: Wed, 21 May 2025 23:34:07 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5c68454aa7e6353c94c501e6d14d0fee25f41e3af967fa9d7929a1fa53c2d33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4275455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00e6656fe42ba476e7319395892b61dd62ce9e32b70cc90b728550196d2864d`

```dockerfile
```

-	Layers:
	-	`sha256:f0af86d5157ce7d3378518d30607cc486e5a125dce2db026e7967a909b8826da`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 4.3 MB (4259418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2d960478801780d84e84a55651c3c2b08d38fb5d627fa32b2e14ea9edb0c29`  
		Last Modified: Wed, 21 May 2025 23:34:06 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3cda06f8fb6326d7aff37ccf966a10e15f1e957e7397892ed65ba00cb7324a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e866f9690cb93c903552d461eaee74e9538e29d9e14eddf6d9fa64f8f3d735b8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9753e330284da1899fd231bf33fe62c0d83e3f17a233f3f30f504bbb6fda21`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 11.1 MB (11106062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4499b0e25845d2e35fdde74226cf5901ec7e9be9382eed98b9a3eb02064d539`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4039d5ee1ad977691de6bac1fb9373ed9749a1f33ec81bd570216e56c21b379`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea557c3b7e8fb6dd8d91d49cae4f0e43f2c39dcfedf77ad960408c3552376f`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb5394c6c7df9c157ef89060c5b3728c4569afb6f29aa90099a6604e7b5a5b2`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3900a4f64cf6c27e536fc131954fd0c5e09bfeaba76a2c956de2b194626b4606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf7a90d529ff4e3867c6ee1388eb4da4b771cab6312d7727d44a0862d829e4`

```dockerfile
```

-	Layers:
	-	`sha256:d1212b901568e21393d035b08d640b468c1053363d014e1f3307ed7ce8c051e7`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 4.2 MB (4234407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d1348aeb4ec99ec3692b6fcc8ef4d9de310223650528f78e204440ac3c50b`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:354b07db5d7f3f3ccf58d06ef3859976a429f941a35da01c12412d09a93f90ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66289634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5dfab42d2d147736ab665221a26bcb8c9cfb8de220dcd99ae2e231a180902eb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb82b38255af376127b720c3434c7588d795cf564324a00430b2e96651baa61`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 11.5 MB (11500246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829d9657d4d662f0da64ae1af4cf6886eff04007f3845ed03cf24b904192bd79`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d687c2c1ddde860df043e0a7972ca660e64f07726254450e3b965eb4c222c8ed`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3157e5a3bb34d5c229b87fe8a5f4cdbb169c5ab8176a02ad6a7b54f6cba873f`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 101.1 KB (101061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d80bac826a6ab24fbd286405cff47489bdf4673594316ec5e86c17c2c57e061`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b86338e7e377c60cdcb2dc43c9fa4b78c0f552887e78cc5b614313337dee915d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3d014f6e237e0cd1607930875f138176cf59c131019cd3fb2e0a02ef049b0c`

```dockerfile
```

-	Layers:
	-	`sha256:a64b7f8aae914ada58530ee812e30cb786ad7fadc5ede081b18a88a6fd946e85`  
		Last Modified: Wed, 21 May 2025 23:20:16 GMT  
		Size: 4.3 MB (4255937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92565edc49b85cf72d56f5a48654518b0c5ad31ce49b271befd3cbacbcc166e5`  
		Last Modified: Wed, 21 May 2025 23:20:17 GMT  
		Size: 16.0 KB (16007 bytes)  
		MIME: application/vnd.in-toto+json
