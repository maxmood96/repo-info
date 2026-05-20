## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:08712eeb02ae3887d1f25109551263d3b401486dc0a77287955a6447b4becc0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6a72868c208d4a8be5b7b5f612b35ce62e40f3798cf5fe764ffaaf54bde4f98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59698490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de65a63aaa0d111ac14cc8853ffae5cd4ef9156bc96d4bd3a51d226c42ee89df`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb92dddd3e26de8152ea75a9f69a7be5761222e5964f3314a90b2a741df7a67`  
		Last Modified: Tue, 19 May 2026 23:27:10 GMT  
		Size: 10.3 MB (10294134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1c2439c5a41a3f1565849f2bc31ca69db3d67c673bd935365e56e8f32757d8`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd176b7467191c7e24a95efa3ffd50313d148c7ca9ea895d817611de25e2d87`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fcf153616e06880716cf7afc320d8ca5b96a6e7592fdf296f7774cee2c61cff`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:430d60c0f134e218d63b5622fcf67693a4572355671c787fcecc75f6ea05146e`  
		Last Modified: Tue, 19 May 2026 23:27:10 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6575786d5511d37cb45ea2f2bc9a60a73b23ec4b7a846615187b7d53f4c17b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c8c0c8a42b651063403d5abc29b6068a1f0be3c92be2e70cdf69f76f1979e5`

```dockerfile
```

-	Layers:
	-	`sha256:4ad2872e53fafb1cfeb07186d1a983a4d06fb66f95e066efc30f0189d2727f89`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 3.6 MB (3614186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d064af7b145e3a9c6c262ddf2b47d81c9159bb7c8a41e30403adaea836fd0e93`  
		Last Modified: Tue, 19 May 2026 23:27:09 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:7aeac7881d0535bae0e2e617f8315a5761b850d71cf58932bd311d4b4d1f16ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59845840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48ae2a6c99c13fd0de35eef7b88f31273280054664f82606663688cfb962d60`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:44 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:48 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aad82dd52a16af0b9a752ae3c6f52083d005b3f021022ac928e217f659b8923`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 10.1 MB (10079251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3457a9f11dc4e18f12cc7a4005782198f4b79a88a7eb1d887dacf5a49beac32`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864235a4a0107dda08be1df2d9fb91d16a1bf0cb6425d918f3e7f279b47d9f76`  
		Last Modified: Tue, 19 May 2026 23:30:55 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129c1fb1c64d94192c382e701d7b14a904efc5fcf1eb658b53cee6dfe4ae533b`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 91.0 KB (91018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7475df3d2a504fa9557ad54214cead31cf01b3c7ca054fe251c62de736745`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4427b4272236147c7e4b07556d22350ca0313cef9b870e82d94aff1f01e3f590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00250ec6efad1de33c7bad769cf3969b6d6530f417f6a779f0ca83ead0468a43`

```dockerfile
```

-	Layers:
	-	`sha256:724a053293413cabf623432bad27c4826b21bfb9630cc4f131df52bf88957783`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 3.6 MB (3615076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b106f5a48dcae253fb77c7274705db08fa073e24eaf2727eb59817d5105d5bed`  
		Last Modified: Tue, 19 May 2026 23:30:56 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b75946ef52c181c76c2e00440d05d0622edfe6da94570e49ddae38ea079dd3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2b263265c43778c4c1b4e8f75212dc86f2c4bef41fbb14feea9119600cafa0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:44:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:93e493f785bb54571482f102af521d43083373078c8450f7707bbcce2dd2b0a2`  
		Last Modified: Fri, 08 May 2026 18:32:46 GMT  
		Size: 50.8 MB (50825581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4a335a9da7e3093e947b7d57025190b5739906b8bd558a221a15ddf6aa9ee1`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 10.5 MB (10467127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b54ccf8ac71030c118f8ef845986b5523b82fed115f87119415e7d8cc6a7e8`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfaab1b9dbef7720bd0084cf9e3eb661688ece913432774491e5c8964364e34`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a31952666a61c2db472bc221ef5ccc404ecc5d08cea8a1059c7cc6d24e1f2e`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 90.7 KB (90749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9d9d9e1e36df62b6a57b49fb8a76a463da0ead6d8b53ad51fe669976c35f`  
		Last Modified: Fri, 08 May 2026 19:45:12 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2acad64ea16cc709a06d2a5aee32e9877e05ebb94c5c760a32e21c3e45deac9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a59f41855cbbd51dc2e3c593cbaa8adf474717a361518cb3ebb5186e2b4760`

```dockerfile
```

-	Layers:
	-	`sha256:0d1f3edb3bc163776717dfd578079bce618888a806181425e93980efaaffe421`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 3.6 MB (3612092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65cb1f47cd785673497359532ec8428f026e1c4021584f5b6423cb001e8a911c`  
		Last Modified: Fri, 08 May 2026 19:45:11 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
