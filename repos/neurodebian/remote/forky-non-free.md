## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:0dc2f773daa7d22adba6aa7de74836388e88697d6fe3a215830b29a8913137bc
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
$ docker pull neurodebian@sha256:dd5bc7f6893df426625b44e21543155e38944c72365cdde75b136cb1114f3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60182055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac711ac0cf19ff39eec3d6b93c2c44ac71263b998019c8ce6d6c3151688edd5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:27:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:07 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:30b85315dec2d58f35c416abc0e468c9a5fb485e83af8c76ba1b33292e721633`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 48.7 MB (48697206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8034887a0bbbfb1d67831fbc844720a3b006206b9e49f7870fb5005bb3c89001`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 11.4 MB (11392061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e91ec5878091a1da281fc06f89966a5ce781d30d1cdadb3534b96138fbbca5c`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f543c19bffe03075382a45dfc91388da45cf11bf12ec5be4f33fb84234947212`  
		Last Modified: Tue, 19 May 2026 23:27:15 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399ae341c4077520a588253618e8c4225e95ff6ae9bc4b9e1633da51a6a75100`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 89.4 KB (89436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5bb7d619a42df196180ed8bef0b5f80176bf6f00f546b800c1c31b10d9f9e9`  
		Last Modified: Tue, 19 May 2026 23:27:17 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:044e4a207e873752dda35d4d8cfd81e45c7bbdb7989a0ee0d4311fa09acc29ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e367fda5e18a445afa9fc71877870628f335e4d71a337fc4bdc50de917ca7800`

```dockerfile
```

-	Layers:
	-	`sha256:15a08b05785f1847bd3d3df55e8443c0d80c779856b0862e24ec6c38169d075a`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 3.6 MB (3555669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7dd5aacc2dcb6133d43b785423cf00d00309871d85a776360ceba20e840ce0`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b5343f56c1fb31218429053ffbecc0cdb55062fcd20ecfe9d728041c5c01d50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59906536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c799133513afa7f756207bde3447643a51b965c35cd88008e1a6556f3ffc8999`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:30:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:30:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:30:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d4360d64f4e71c17817e39372cada00ee239c7d2715cf79f6e6cdc602a7cd46a`  
		Last Modified: Tue, 19 May 2026 22:36:44 GMT  
		Size: 48.7 MB (48720031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec98f49d5e4fa11cebafb79bb6f58fbef7023c8a19fcce5aa94df4a4e7496f9`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 11.1 MB (11093072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a7a448cc8b0211eb9bef63518a33e6ab21d9096e89b4d32e81161f1b4437b`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e100d1e87b39987108ee142e1e682902047cbc3339a12200c2f6773805ef3056`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c32e23cd1e65b98407dd7e7eb4196697bdb064b3446d752955286f082a89bd2`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 90.1 KB (90077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf9bc2b2cf57a5d3f81b2da41573718da95babb252453b4969fc2bfb79f25f89`  
		Last Modified: Tue, 19 May 2026 23:31:02 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8ef9c7076cdb1f64991964c59458038a88cd5185a2cedd92eb15cfe92ddd0946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3576473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222b74591ff62cec5f61294bba8e63539d6d288cbfd0767d3ac7f827ed20a158`

```dockerfile
```

-	Layers:
	-	`sha256:5abbd613c8df3b55c925c540eecc65c824e5574b6fb95d4311b7e67d29ef7735`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 3.6 MB (3560374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f0379800346bedbe8114baa2a2a59c79880f928a6875b195fcce6d11a9d4d17`  
		Last Modified: Tue, 19 May 2026 23:31:01 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:03a1a328bfee5ff0a2bcd6a694bf094d95381b9b663a843aa2e3ae99924b758c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61606220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c3c7ade491f697623eaf25c70f50f5a71cfb7bb1d3153121edb8caadc6b964`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:08 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a99493d96d6f92ea6d88890fe995d3918a05c9baec0b84c6e9d10b95007a82`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 11.6 MB (11588918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a0c33e147fa59d9124cbf1b02679d5996d94f20e43a0b0dcc7bac0c76d9bae`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a895ebfb8de9b1aba761e3f5032daf08032da3fa41c4770fb7be187e4cf0`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d22eba06c949e34b02517b4968779ffafdb8e6ce52c51cf497c682389b154`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 89.7 KB (89726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2616c3f976bfa74ec623fc4792a7910f4ad8177ed3b117a8e270087f0510a539`  
		Last Modified: Fri, 08 May 2026 19:45:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8c75c21cbb9fff8f22041a53794d1631c30d371e24e4a25d431e1c649eb7fa77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7075d85a25976a8e3bcacbf0a99c3a51ddb29e013c5b42c7da1a973f852c1ea0`

```dockerfile
```

-	Layers:
	-	`sha256:7ca33354efa5a678e18c52598a002e0f989c7bb096e45147472c2b5788c43e45`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 3.6 MB (3554226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53d2a0a43649d8f679119161461ce4dc60d130a0faefe0533fc5173dbdb17353`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
