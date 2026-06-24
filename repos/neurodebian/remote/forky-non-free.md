## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:3c73e8072ff1cb876e746900ad9a809bf38fd10ecf6c073c95d06eb1eb5357d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:b78bdce54ee430234c62067fbcb93af9068329a16b67c969fd21d23614fa2fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60246474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7fa70c620862ca20b41e0af7a9a30a323c395007f8462483d249bce7afaf7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:45:17 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:17 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:45:17 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:45:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:21 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:447e2db1403dde86cfbb4e736a0555036d98321ddc327da9305db2a007cde1f2`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 48.8 MB (48757790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12890eaea259d4409d91da63bfcd1e0aaae501c3a53bafd56347d5c779c79a40`  
		Last Modified: Wed, 24 Jun 2026 01:45:30 GMT  
		Size: 11.4 MB (11396024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1de09fad6ddc4c6cb957e238fe980ea45672539306dca6e18e0e55fe2e1581`  
		Last Modified: Wed, 24 Jun 2026 01:45:29 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23c816b72aa6f6a8af8d9faeddbc2bacbeebc6cbb2300c96cebf31a9b96bde0`  
		Last Modified: Wed, 24 Jun 2026 01:45:29 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a2dbcf242f2f59901224ecd08402a8b5cd1aaa8c93a56e28d7af6d3e5c2f8c`  
		Last Modified: Wed, 24 Jun 2026 01:45:30 GMT  
		Size: 89.3 KB (89313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66a2b9a728c5ffa5bbe9b53ffe2d2964dce3b136fbee5f0bd07e727084c8cbd`  
		Last Modified: Wed, 24 Jun 2026 01:45:30 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e047c03fb080b3a053866f0be814b7760826d27643d2a2c4ac5733aff7c3630e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f0108c4e46a06cef12fbc70580b74a9a34b82074fa477d2255e1b366d61be67`

```dockerfile
```

-	Layers:
	-	`sha256:6ed5d1b0e4fbbbcaacf5e8b69ae85fa5bfb21855109d950d6fa01e07eb57cda7`  
		Last Modified: Wed, 24 Jun 2026 01:45:30 GMT  
		Size: 3.6 MB (3559357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe7623aa7dbcc057038f9f485ec12e929e65c05f933476add30f8ccaa9cc14c`  
		Last Modified: Wed, 24 Jun 2026 01:45:29 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e355b2aabfedf7aede8b74a034dd9055fd513ab80c85c2ffd5047a5519109670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59954853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986ae5a30481e5eaab366199b32717ac5e684665a168311fb16d921b9188b6d3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:48:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:48:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:48:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:48:58 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f5991d5bb2fa21186c9152bf0a9fa1c9c73892f68235c440c9967628fa5ecac9`  
		Last Modified: Wed, 24 Jun 2026 00:27:35 GMT  
		Size: 48.8 MB (48768712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e01d74273ee9f96a0289d4d9ed0dd60d7dbd12507f1208c11e6f72111097850`  
		Last Modified: Wed, 24 Jun 2026 01:49:07 GMT  
		Size: 11.1 MB (11092824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e684f87a6be888a633181908b0e6359923379831c1e1ed3621cb3e3d90a1f6a`  
		Last Modified: Wed, 24 Jun 2026 01:49:06 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec11d1fcced0c3e2cdeb1b9c4a767164b303fadb93a0ef6efd79bb71de136d4`  
		Last Modified: Wed, 24 Jun 2026 01:49:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a78a3f3527131ae5e35c1964d1de45ff075cd2294fe53fb52d49376ceea812`  
		Last Modified: Wed, 24 Jun 2026 01:49:06 GMT  
		Size: 90.0 KB (89968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22186f3e48cdb66e822ad747e504769a877e5c2520669e70e8bff4bbb4406322`  
		Last Modified: Wed, 24 Jun 2026 01:49:07 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5ba037caa2fea4c3597207c5ac27d8b9689b4e4ca8a159a67335b66c24f1f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b748eb52b849f1882a2ae9e6c72acd725cb1b4b3934d58d51a1d22f3082f54`

```dockerfile
```

-	Layers:
	-	`sha256:87b321f89c659ff01a4a8b43e11598739a7e42dad2365bc49b0bf7365d25330d`  
		Last Modified: Wed, 24 Jun 2026 01:49:06 GMT  
		Size: 3.6 MB (3564062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3d8912f8883c0232675501ded187935c537e100b5cffedb09fcc9d72ae4807`  
		Last Modified: Wed, 24 Jun 2026 01:49:06 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bfaeee17908403cc02ae0a3499cedabae1311c1e04218bdf82caefcd8e3e3b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61771264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a2cd80f90bfd1af51d32c58bd18ffb098a9a5b38e1dfd077d8952dfda16215`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:45:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 24 Jun 2026 01:45:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:45:49 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9b65e2e922e5570b1d72c057efc4f398b0b14051ad2a0b581d6669e50195e288`  
		Last Modified: Wed, 24 Jun 2026 00:28:28 GMT  
		Size: 50.1 MB (50051032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7336ec1003969be0143bc9fbe3c31e0ff036a32d586b032ebce59c60a6335d`  
		Last Modified: Wed, 24 Jun 2026 01:45:56 GMT  
		Size: 11.6 MB (11627244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca48798ebf6c29aa4ab183e938fe9d6e7d5ac20966647ca4f12f47edc562214a`  
		Last Modified: Wed, 24 Jun 2026 01:45:56 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85af424c5e2456bcd07e10905ea8eddda380c464a9579571fac01b7ef7b2f455`  
		Last Modified: Wed, 24 Jun 2026 01:45:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4561b9efc49bfa9823dbcf0aec676d080fea2aef163503c1df0bb7c76a5dd202`  
		Last Modified: Wed, 24 Jun 2026 01:45:56 GMT  
		Size: 89.6 KB (89633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe6964634b01a0d18a4bf64af05927c0d748d662fae42dfd86efa3435ea3d85`  
		Last Modified: Wed, 24 Jun 2026 01:45:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8700a5402396c84af551dd89ba0d4dc3abfb23ece249cc5e4b00324cdefc173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c30becd5c02a35b8211bfc91746193837dba4434850f0b953a89a3c55f8ea413`

```dockerfile
```

-	Layers:
	-	`sha256:7b2fef64f41dad56bea4a7df849cb1220a659fda0a0a2cbecb5b2efef61debe5`  
		Last Modified: Wed, 24 Jun 2026 01:45:56 GMT  
		Size: 3.6 MB (3557311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42b066fd18c7e2259707c59e98d56dab1eb356da092371471c50c29bfa4c1425`  
		Last Modified: Wed, 24 Jun 2026 01:45:56 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
