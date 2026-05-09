## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:eabaa9df6e6f28acda269868f36fe6b1ef1678d2762119d6c77c78b5d87b1363
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
$ docker pull neurodebian@sha256:5334a29a1f0fb4835758c1b388e322a2348ec3032da1a4e6572e98134532a498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60186655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b064c3891de8ce33ff0e4fe108f5171b68727f60ddc6590af502f8e0281df2af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f85957d69d501ec6d0cc38c388d29b67893409a599a0fcd2b22af2a3660ed4cc`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 11.4 MB (11391676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d154e7fe6720de57e32775de2e5bdeba041c1cc8be9924ff6250053bca50a1e`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01de64d5db46c87cdc4f28638e85cb1ed77837b8947122fd2a37dbf6a2f7b87`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfcec0b2aa32503cec752f39c7a9b0c88eef9c3672f941e3e83f08087d90a4d`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 89.4 KB (89417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93eceb2733233ea0ba023ae35ac2b50c8272e02060ead780922c8d64837d456`  
		Last Modified: Fri, 08 May 2026 19:45:20 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:83338b9dab02c5e892d7e4c04216af3417a35050a3c6a89f5679c02580d0fbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d211b3029e995baba17d24b26293538cc7ca7cbb4c686d90d9282b1952bd0328`

```dockerfile
```

-	Layers:
	-	`sha256:489a9f86bff40e3acd067530f627ebc463f581180e26ef866ff20945dbb69aea`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 3.6 MB (3556270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9842aa3c21dd529e05422a063872ac17852062730e02604d63b250e85fae24ab`  
		Last Modified: Fri, 08 May 2026 19:45:19 GMT  
		Size: 15.9 KB (15931 bytes)  
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
$ docker pull neurodebian@sha256:fdfa585524dbca77dc88c79d28594b439056998a1873b0734100d0fbfcc4983a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61725576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e746d8a97559c27eb06570b8eb5bf7fd0656d5f75194b377aaefd9ce7fea3f94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:29 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60950ea8f81eeb40f4ffd4c9eb5344310a3d3b4a3ba10d8636c3e11c143743a`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 11.6 MB (11625857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e999e91d392ae0fef15aeed6175ba39d08817b5593d30f26ef16d1565d28f379`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208859bef58c08283e7c0113598e89b5851cffe3ad75ec5cbe4f8826bba0007`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ec1337df25fa89a088252f15b64bba7bf8f37501ac5944f7352dd621c52673`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 89.7 KB (89684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354222966e2e2c36cd8e4d1a765f5ce435c85024a44468f4c76ad662da8dbe34`  
		Last Modified: Fri, 08 May 2026 19:45:42 GMT  
		Size: 417.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:efdcb503bdb440864d0bfd5fcf11ce13a5bcd3ca870806e08019df74f241815d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77f0b27c9a0833de49273eb014ec6b6900a97b4265c8339e9c8422a12a57f18`

```dockerfile
```

-	Layers:
	-	`sha256:d3ca879e53a051396232cc6749a325b48a90a77b314898d6642ff4a75b84707d`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 3.6 MB (3554216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bf0aae2c3093143415998f808232246df063b6a5a9ac0bd9e4a9bd97ff539e`  
		Last Modified: Fri, 08 May 2026 19:45:41 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json
