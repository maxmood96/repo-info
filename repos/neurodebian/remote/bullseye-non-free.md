## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:77c47c7668866764a9122387e7419916c7c8d85aff7f5a1ce83c1e3364195be9
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
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca25855464c362ff5b431ed1c58bcac1d3074d341dfbe0b69db0c4b7b06ddfb`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
		Size: 11.1 MB (11105060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bd852d80e3b0c678ae63bfb3948aaedb9a85ffee30335e3517dfdb5079959d`  
		Last Modified: Tue, 03 Jun 2025 17:40:40 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755cd40c0c29cc545f889321eb72bcbd161b6e91d0f0b1b7e45ff98558c28ca2`  
		Last Modified: Tue, 03 Jun 2025 17:40:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4067042efe9918fc632e3430f0139557b52b74d633b305ae3271d19e6436a4a6`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762595f10379f52572d8fd283315b81ce1b9219d0093d67e34f012a23d953ce0`  
		Last Modified: Tue, 03 Jun 2025 17:40:41 GMT  
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
$ docker pull neurodebian@sha256:35cfa864205249d1d4e82504829a5f5aa992c2d184e55290bbb0d1af4dd05023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45c8b2299769ab81320368fa621d518caaa4dd7850a06661e4a8369452622c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Tue, 03 Jun 2025 19:33:33 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Tue, 03 Jun 2025 19:33:36 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd4d56a7262cf9c7a1b114c72ceb3299228df837a1640a8ce90628bd5c963b1`  
		Last Modified: Wed, 04 Jun 2025 16:14:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7c666df1009a09dcd1bbba24ba9169ee5ff609d9945c900d9b868ca55e8fbbf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4275202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f951394aedf3782b624e9bd05e62a2d1f23bf36f0a4d9531db99d61cdad249`

```dockerfile
```

-	Layers:
	-	`sha256:007a6fcd8d32772a7c49365a7cb79a2f7def3249337b36bbf7b5868f48c256bd`  
		Last Modified: Thu, 22 May 2025 03:19:32 GMT  
		Size: 4.3 MB (4259025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec65fca109040eb81ff69488061cea5448ab551ff306c257491499a58e6bd282`  
		Last Modified: Thu, 22 May 2025 03:19:31 GMT  
		Size: 16.2 KB (16177 bytes)  
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
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
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
