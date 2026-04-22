## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:d67dccd75d860b0cdc67165977678f763ee747fcbd7b04983fb3beea172bafbd
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
$ docker pull neurodebian@sha256:0438bccc7ba65c13d3e3e327154a9cd2374115c4704d3e8795269d86f0646c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59878527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4279b4d5fa39340181ad15329fe13cfe79cdfeaf7cff6f3cf4bbe2316dba283`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:27 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:27 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290faf0d8556a0354ef08cc6b2ab575395ed75f67c1fb090833e5a9dcb73ebb5`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 11.1 MB (11073827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e113876b36cb35bc3449e3275bf2325cf4d135babc8a1eb1aeafb7093ac0fb22`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581a7489b1678da413f412188af43e189558ed028dba4cde7a97bd3748d481e2`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c9798ad62fe6e6987e01644fb45b9578749649d945ee49beaa1fe156eb09f0`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 90.0 KB (90011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3b35ed8b319973962555182b86ee9acb8b47387a161933e48da8776e73065a`  
		Last Modified: Wed, 22 Apr 2026 01:47:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:230277e93b0c55a22f41fe71935f996eb01a41c1741dce3dae8e733a5772a7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde88c881e8e8378e262971e9b4d87678721d7d7c3a1849eef8a074db3155bd3`

```dockerfile
```

-	Layers:
	-	`sha256:5b9eb37b3235558f1c7819837058313695015c6375ebae6365c41d032bf4e805`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
		Size: 3.6 MB (3559975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dedededbb1a459db24d72e128f27c8cdad198b22174403162acfab4a6716378`  
		Last Modified: Wed, 22 Apr 2026 01:47:35 GMT  
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
