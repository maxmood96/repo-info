## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:d70ce4038c2f2be6f5cd739ab937f6602f0cc3d3c3a803af2ff38aa82371d5f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8254b96416c8ed428becd6efb7cdbc2a3723a8848c7832b166e8d11b0e9afd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60132721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142695fdea8a00a7f5e049cd7e3d16d3f45c60ec3c83408e71540e5afe7425b2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee90c31e0b15f4e954828cc2f0d46688fe82416349686f56dec0c166678f5638`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 11.4 MB (11369466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e4cb1c64ac9255bf58f619be961961ee174ea76890f76f7618aaae17d36ea8`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1e9d2b4d9826d726772bce260874a2643d684a679d886c0261c13de59f8488`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92e25aa604374b2020c0332b1b6dc98904a02655ccfb3ed6f6f811a9aef26c6`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 89.4 KB (89358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fea64fe3bebafb63bdbd3ba66eb0e5464d11fb4a8d75e97934c70c7ed99021d`  
		Last Modified: Wed, 22 Apr 2026 01:44:42 GMT  
		Size: 416.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5bfff5564e0573ee9c4d10642f18ff643d102ebd4d9912360c21faf5362ca8eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4ea5287434c12cbe0d87060dca1b8110c2968791cdba5c3f94ab8fda1a6504`

```dockerfile
```

-	Layers:
	-	`sha256:524e5639afe25e0ba933e92eed8a89dad80f88d9ef7624eebf1cdc79bb7fd552`  
		Last Modified: Wed, 22 Apr 2026 01:44:41 GMT  
		Size: 3.6 MB (3553990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a93ebe9eccb230ade1d8700be8f427026ffdb634abf6a5ef474b0208902b13f`  
		Last Modified: Wed, 22 Apr 2026 01:44:40 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bc374f952257e26453ff7836ddfaedb60bcb7b8567066896a59a1dc6235eafc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33147fd5038a8f3c7854dd92f9f80f55966afc35978f38770149742f5fcb876e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364834fc8139dd37c03942d4ae776f1690a19fa2aadbf6286e0c696c77f02654`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 11.1 MB (11093047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce88d73a7e0fe050bda503e936cec378bffa4e11cf99f44f3547a9bb9550e9b`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042248e359b2ca8c613f492ddea03664e1f5545d422f89ca2eb579ec4fe36cf8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d05b1b5889373a2ff082dcc562fe9b6c87f4dc954311c07a9235161b5b8348a`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 90.0 KB (90047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb1a6769325f550371ea3eda25df8162e96ffd9d1e724c04e9fd6a53a5b15d3`  
		Last Modified: Fri, 08 May 2026 19:47:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:38f1246a7857ae16f1ee50ce83dd99f709d82307b1ac48db4580cdd4ec7ea6ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3237ed235baeb7082f0151c28c4714dc3f510674f4b363afa9a12ad73cdc2a00`

```dockerfile
```

-	Layers:
	-	`sha256:d51df37178d40b9b383e7bec1cacfb104cebafc298e749ac1e0fe3566149be4c`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 3.6 MB (3560975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fef56e4295a87c65f8c4cda5532f9cef3a17c374c89cd048b622e0afe8df15d8`  
		Last Modified: Fri, 08 May 2026 19:47:02 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5164af7768687649b18fe93a5992d4a0024df733a66f8b02596fde9e8dcda1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61674235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a5a6ba8b32631c0e82985b0c51df6185372015fb3e8cf77b77ee456d1a75ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:39 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:44 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a68ed28706ac755be40447c885e7277b571939be826b0bcf8abd61cb9be646c1`  
		Last Modified: Wed, 22 Apr 2026 00:17:10 GMT  
		Size: 50.0 MB (49978211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880bc6e7d430abb8a6ef2d8705a91aa0e43894a1c630b37d5a10b23cd36b0c70`  
		Last Modified: Wed, 22 Apr 2026 01:44:52 GMT  
		Size: 11.6 MB (11602999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d87cf4bc4f5fecdcdfe3a6a62fb1b07da675a417909df6d6a6e1dca26cccf8`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0781201189a8dfd0b453ce46cce647390e66eb32c4311f35e87bccd757dc2820`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e4c6b35978a2d1f7aabfe5b6e8eb013ce3eeecb0d5b21091356ba3b8ddc893`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 89.7 KB (89705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7400f42191ea101aeabc19397e96f4aa24e7c153d04899e4e5971b3bf435fa9`  
		Last Modified: Wed, 22 Apr 2026 01:44:52 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:78129261531fb1c60d6bd44f21b001f3c940728bc776e8e3c61bcf3a3210c3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8cf5872a91f89295c3884443f2c314ec3d0648e920c08ab2fc034a0d03122f4`

```dockerfile
```

-	Layers:
	-	`sha256:d55e913d71eef96fab9791a630c39238eff4ee5e9ace508b97b4df1c24716e67`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 3.6 MB (3551939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:942f6867a08a89dac43be49a8d7c02797c05dda7bbd9ee3ee17ecc3c05101c3d`  
		Last Modified: Wed, 22 Apr 2026 01:44:51 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
