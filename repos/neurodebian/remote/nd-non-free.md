## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:5f2bb0e6398ae8f699dd373fbe1c7b440e078772f0791b693d6a394f51102496
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
$ docker pull neurodebian@sha256:379dd6cda62c5f956daa4957282d12057faca8d0d2edb10eb00b63aa4b127649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61688954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4690074633fe4fccb4c59a578a84a38bfc055cd41d859f3fe6750c62c03075b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbde13ff2785b11cd70a92d1da45b61ee2c39ba77f505a32b6764e1bb1f3464c`  
		Last Modified: Tue, 07 Apr 2026 01:48:59 GMT  
		Size: 11.6 MB (11602276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8a43f3df2ec92648d7f9cb6ae9b59596ef7550e9b2c0de212a9d5067d70eda`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8292b280ecf08c2a53b62734b37ab925c0596e7c8837ab862f48b6ed13161a18`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4fd33efcb827f079f283388221dcec47472439dd679e48cc1dd8c9c469c885`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 89.6 KB (89646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee066862e919913f4a8149190cef898dcb0dd51f675a1b0b66cd695eab88dc5`  
		Last Modified: Tue, 07 Apr 2026 01:48:59 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:20806508b55568c0a85953b30cecd0be318bf1353380d952b6c350c1f23b2cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58350dbd42299c78510c7b6d6e14c04f9e9925d1c2ea28148368a9e35ce4182`

```dockerfile
```

-	Layers:
	-	`sha256:07eb593648572153e5a66df88d45281816a4595bd6859d58ff20b91cf3e389b3`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 3.5 MB (3547078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e60adcebb1386384577e15e4ca93b84d41693ee7655e05bbf56de36d0fc4ace0`  
		Last Modified: Tue, 07 Apr 2026 01:48:58 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
