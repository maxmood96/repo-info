## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:7da0da4f0cbe841089f33c105fc2eb378eba082a878a3102accec83b22b23370
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
$ docker pull neurodebian@sha256:97a9b47d46ac52b75308963511789fed73668a70ebf9cae0988f1815035e1c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbaf972a26af8b6c046b93c68527b022680f6c76ed6a1d3c973ce3ca0b3b3f7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:26:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:18 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:20 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff46ee5f51abf7e5c759522ed9dcf0a5f5b2ec464fa632d56405b96254b1dfbb`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 11.3 MB (11273406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f8ff7d4d348b07f5a336cd39456ef6e1b6fe312df471f7bf66ec73f7601735`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5e1b61cfea69e2da3c4dbc64fb5c3f02cea34a5a5802c264392ac150afa2a`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585bb0b08038e32fe6c8d0bec19cc500c0d3d79edb1321a1bbf38f5039efeb84`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 93.4 KB (93375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:19bdf24a96f9561229e50d1c27a79f51962f942533333ede87e3f322b3c2a654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd397e9b8639b98a2f8a5b34a7c72d37bdde5bdedcbf087e90371893eb03167a`

```dockerfile
```

-	Layers:
	-	`sha256:f1c063a3b65d43aacf26150c57110c0ba52b44a9341e57979b083dd7dde88610`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 4.1 MB (4075879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b21a0f70fb07b2b7df369389e2b19fb1d183a19103181d75e803e87afce3b3`  
		Last Modified: Tue, 24 Feb 2026 19:26:27 GMT  
		Size: 14.0 KB (13965 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1ff4cfddc9ff89453b1a9f03d1e504ac913f8ac54328229b3c52987ad14fb699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59721929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb46cb4634d0fdefe1fde8946ef0d02431408f474346b668e5b1f2a97d496f6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:31:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:31:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:31:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36254904a1a9b2612da0a07f6b3f730c2a2cf793ba4c8666f0e5023ef0d952b`  
		Last Modified: Tue, 24 Feb 2026 19:31:21 GMT  
		Size: 11.3 MB (11252977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a69edb662b1eaa3f9871d26aced9707417502fec45aaf3327e0974865e293f`  
		Last Modified: Tue, 24 Feb 2026 19:31:21 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fb248e4754516b9d3ddb8e0ce91ac4aefc2df417f18b920eeed914808b2adb`  
		Last Modified: Tue, 24 Feb 2026 19:31:21 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1067fa1b1e9dbaa518b34c3733e98ba6dd90067fe050af634654d300cf445d`  
		Last Modified: Tue, 24 Feb 2026 19:31:21 GMT  
		Size: 93.6 KB (93569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4f505eab4792fc2a76d28b2e4172539702c95b9203a321f011d41e38bb44305a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4090210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cdec5db136dee55755c5be5a0c9cbdfa75eb929760222f303661bac811560e9`

```dockerfile
```

-	Layers:
	-	`sha256:fa7b901788b47018302e296537cdf4f6d4b277b2f9c5fd54528946b96abbc07a`  
		Last Modified: Tue, 24 Feb 2026 19:31:21 GMT  
		Size: 4.1 MB (4076121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:678e3d33f6e526ea0f8fd85865bf7dadfb56580d9d6d600c7878ba851040ff2d`  
		Last Modified: Tue, 24 Feb 2026 19:31:21 GMT  
		Size: 14.1 KB (14089 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:48c90f7b145968d342ac3dd1eb409dd70eb3a31bf91a7d6310a7e7dae64a6504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fc7bed47523fae5c05cc98d9ed786b0373d1d06e2967a7d645736ae16a7e6e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:25:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:25:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:25:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:25:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428a319f5e787075f3801ee1630c12f41c037a3202d1cc63653c44aa3ce7494f`  
		Last Modified: Tue, 24 Feb 2026 19:25:50 GMT  
		Size: 11.7 MB (11692926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4eea611746f4432d9c94e63305b464ba05adbd479914e27826a481e999a0b7`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9e8ac80819200996ecf8de8db3b75d785db78be625a4b7edd91d9e5b3e8a8b`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd519a2fc8608d8657d5aea4ac6a60024763292d30e75b9ea20c597db8ea928a`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 93.4 KB (93400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:586b8716c10d6eb176ba6c4fa5b2c17a4ab0962a1496f051366f28d4d9540ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529c8b487a50159111bfa4a3348518256aaffc3e038902a01f9a416c590e6257`

```dockerfile
```

-	Layers:
	-	`sha256:ff8aee6cfa7794a7219a3cd1c6cb34c293c2bcb8665d1ab465c0e3c6064425f4`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 4.1 MB (4073846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07193c976114f60f52cd7f6afcc9086f7069e797b0498a23cf480050aa0035a5`  
		Last Modified: Tue, 24 Feb 2026 19:25:49 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json
