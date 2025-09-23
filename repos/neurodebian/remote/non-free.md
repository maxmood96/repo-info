## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:460e1eab04d26ad05d6e50658a9413041784a1a17d8aa759cf1f5c43c5216d1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:6f43ef7eb07bc7c20266846a1c98b55a22011567a05f2ac5eff2909071eae0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c172ba0b81dd8f89238b22511a3d5be1d5180c0258e9e889a6ecb01624a3a2cb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb3e3b92bc6482e0df10b8b95bf25efd483c108ad208a60664cf5f1d1e77be1`  
		Last Modified: Tue, 09 Sep 2025 17:33:49 GMT  
		Size: 11.3 MB (11269552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e96c4ca1ae8d9db1d4c02f9c3d0652e417622ed05ff6eb736432722662ccdb`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4541b568aaf9f21e14e1425e4fc093a5dd0496df3829b6404b3ad6c41efbbbe3`  
		Last Modified: Mon, 08 Sep 2025 22:09:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c1b15bdadbbe93287ac427ea3a8620f5b0157a4e6b13f7635f592e3bcc2708`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 93.4 KB (93361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c38cbf257c18774f93a43d3e807c5ccb87233a46bd639fbf19fd1391531342`  
		Last Modified: Mon, 08 Sep 2025 22:09:05 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a2a94de25facf95724b2d16ca71a72d99a2e112b2d316cd949056412564d4d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206e4e0e5813d979635e9c61374bdbc88d22a2f82bc265b156b17600d6bdbdb3`

```dockerfile
```

-	Layers:
	-	`sha256:6d1673c322c9fbb37ea05028f45c19a0ce42f508639ca61a70c7c7f98a8aa319`  
		Last Modified: Mon, 08 Sep 2025 22:07:46 GMT  
		Size: 4.1 MB (4075584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae33da5884a0a82ad883b93e19d26853d993626f9c39065efe0d9f5aafc836be`  
		Last Modified: Mon, 08 Sep 2025 22:07:47 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1eda3906e3d74753dc6108406609474e17922bc4473c0650138d2a71e0bb0a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59811107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1c0ab49c63ddb928d1ea6152bce13a56e8924cf87b59b98426b5735b06a017`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8928402f9240101fa8045309f2d1f99869f404958b90ade93c18a6fdd5103b`  
		Last Modified: Tue, 23 Sep 2025 17:39:21 GMT  
		Size: 10.1 MB (10073166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc260bea759081fbc813dc13e45189e07a89ad889eb04898b83095ebe8e46f6`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7be6fa450a008c0111b995191dcbebe968fec4b2291cb9f77b640b8d90186b`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c083f97f9134022f86c20007997675be9039bd0cd5b261235fc0333b295336`  
		Last Modified: Tue, 23 Sep 2025 17:39:20 GMT  
		Size: 90.8 KB (90839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c02e6d484f97370f3d3a31c333d86ab85c56434cf062ec9db96eafa89afbb58`  
		Last Modified: Tue, 23 Sep 2025 17:39:21 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:67f19ba1c382f706a6c0546d668de36db5eb279435eb55be0b971d0d1d6e0d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41fa20712a0c042f42ad63fb2ad11b46db8ea8e4742bcf4d3e9369a094bd33f`

```dockerfile
```

-	Layers:
	-	`sha256:072889b65b38c27822eae4197991fe09aab464f059df703c0ad31613b64ffe68`  
		Last Modified: Tue, 23 Sep 2025 19:08:17 GMT  
		Size: 3.6 MB (3614548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfa28fcb3ba4cc4a53499f985d3803766945bb3f97081ac0415fd7b7b58a8a4`  
		Last Modified: Tue, 23 Sep 2025 19:08:18 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2685dd7fe3afbe2157a72c212a66ffebfa1465d998490f39ad7fcda33a6079de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61351708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcff7d47fc0d643368953858e2e160918fd389ce7a8454f06445f8f694148b92`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb41c38efac3c3a4e479715bbfbc2b0cf2daac281761c6f91ffab849e5c8190`  
		Last Modified: Tue, 23 Sep 2025 17:35:05 GMT  
		Size: 10.5 MB (10462867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500ab29cbf1ed8b8d382ae37afa2d978700800d7f839dbf340f2b3573a7e131d`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351373291dcdae77241331e750e91a9d52b1632c6ef73f989f1801a1126abcbc`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa920d26fee157ad165e0eeea4da5aa8faab9500938265f152c6cd6b98ec089`  
		Last Modified: Tue, 23 Sep 2025 17:35:05 GMT  
		Size: 90.5 KB (90535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31df9627b83b4bc4a24ead4a19c413ddfa015c8dd02d315d050d11654445897a`  
		Last Modified: Tue, 23 Sep 2025 17:35:04 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b8294a8060dfa8487b4aabb007bdb278688245077d6acb64e69b97a41e98e2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb7094164a2f8304232900ae7771326641faafedada4ae34e3f96b23f4b435e`

```dockerfile
```

-	Layers:
	-	`sha256:464f2f4ee7c536a30f535caa5b810a4fe3b192a5ac0e163b2bbc250ebe2f6f77`  
		Last Modified: Tue, 23 Sep 2025 19:08:22 GMT  
		Size: 3.6 MB (3610970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f90069b14333bca50c5c0537e5a3deaf9cb3036ecb495ff5dd8610331168857`  
		Last Modified: Tue, 23 Sep 2025 19:08:23 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
