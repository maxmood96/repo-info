## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:8441c97a8e198199f07e5a76d645e70806fff1908f494ff3ddec0d444f7ebe52
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
$ docker pull neurodebian@sha256:43852c13486094023492093d1debf80eb35c72d63a9ece7e046323c60a5e227d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8557567cb0aa131beb5a5004ca576ca408d37ff2ac4aa19205bf4b5b2c0db17d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:29:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:29:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:29:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:29:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:25 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60469e509d0db0a8b229a64c66febb355a8cf43de76e0ce7b698340166607f1e`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 11.1 MB (11105087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d9c9f86602982491d439e62a677afb463694c0b1bc57e50d08347d6ef88e3a`  
		Last Modified: Tue, 13 Jan 2026 02:29:52 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5043a9fff3300da9bb6e22abdfda0cfa3de5a76ed7c68608348c68b7c634101`  
		Last Modified: Tue, 13 Jan 2026 02:29:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2364ed7d3cbbdc21509804a526b9d7357b52c813e5a0f97fdd14aa5f803f30f`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 101.4 KB (101367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183f5f0fd07e138f2d622e5e46a79e3681174f26740a24f3dcc6ba9b9c9c6ea1`  
		Last Modified: Tue, 13 Jan 2026 02:29:58 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6f6c0ff5acbdeb75814a080ef01605770da928414eaa93d21149e8d166889fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660955ade71b3e4a77be848bf34643f837a7c771f0b78fb67a80467ea0f3527e`

```dockerfile
```

-	Layers:
	-	`sha256:18ad11d013327db0cfeb37cf2958c48784e34c9161110ebb3cbff0070cb04ea7`  
		Last Modified: Tue, 13 Jan 2026 02:29:52 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3c5af0c09bfdb2cad7723af5a5dc2497ad97bfdd9dcd6c0137b68e30daedc5`  
		Last Modified: Tue, 13 Jan 2026 05:08:17 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f5f7312c945b60990fbeb6fa3ac154b799bf2d959560ac8209d2695e35608669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e996b679012531510d226df25700fee8ee8d09cb53e5037c113b5b6eef393ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:33:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:33:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:33:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:33:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e852e98585e0086932c28bd104c90762c999c879f6bff631b9dfd3e5e027ad8`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 11.1 MB (11106067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2012f775c3a0b7db8ad8b6a741fce6bf1a3bd9e7285301af6bb8c74aa205a210`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ebf6dae5f8f124e7deca8a99d38275f3c415952230053da6203eada6d23fb4`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198ebede9dec6dff5f729071cee117718742f091332b36e1a24dc261bb2f4460`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cbc978f4e18f291d148dd2e8b50e3720b87f256894ab7ca9ee5548ec476ec8`  
		Last Modified: Tue, 13 Jan 2026 02:34:15 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c162acbfd1be1a7b6057738ee3e0f7eeed018cbbfe6384cde8bd6a7aa2fd6ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26227bb96753fc94da015678725c714ca85ed6bcae28e4cb9e8efa8f62ca3f2d`

```dockerfile
```

-	Layers:
	-	`sha256:fa0ebbfca159885e51eeec2aa8d9a49786b1ca5cb94a7e95879a740e9c917d61`  
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3c2220f93de37bff4c79e226a29ae34c67448e82152cfb4700a608af0f01c27`  
		Last Modified: Tue, 13 Jan 2026 05:08:58 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:b4387c5264e12a316b565ed6d7b792e8b38229f38956eeb5c8b8f7deb44931e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d488196570b9678d5d15398ea3a5a56144e7e2fc7f6b24ff3e53a9760cc2b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:08:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:08:53 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:08:55 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:08:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:42 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84f7876b97c9cc558e3b682faffaa05ced369d3a1daf0097395a92379a1e56e`  
		Last Modified: Tue, 13 Jan 2026 02:09:04 GMT  
		Size: 11.5 MB (11500374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0706ef71ceb0b289ae294621e19630c33b44b79fd2a4700c9bfe91af88f5e09`  
		Last Modified: Tue, 13 Jan 2026 02:09:10 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93d15594c1a09687f963a46a767fd98814ce5068a9a92bee4d01761a2547e5`  
		Last Modified: Tue, 13 Jan 2026 02:09:10 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685f5a198b5049eb844e3225fc405d497e7a828788b0b2d3a99315e1c89872d`  
		Last Modified: Tue, 13 Jan 2026 02:09:10 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2935e4ff248fbeb6449435fe4391367a3ec04a837788d04f2a5c950f94815f39`  
		Last Modified: Tue, 13 Jan 2026 02:09:10 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ccdbc0018d01f9e14a406dc7bfa3d3e22843a63b2183a16fb9268e2b2f13f988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b44cf07798c40a6ce78dbafc09692d3ecfb06394249c498e5874b19421d30a4`

```dockerfile
```

-	Layers:
	-	`sha256:d08560fbc054319e24e443e931ae6376f40ec35a6650d0c9a827ecfcbefe1fe4`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de584fcc7e6273fc33f29b39b5ea37d0141365526c22b1438baebc0dfcc34719`  
		Last Modified: Tue, 13 Jan 2026 05:09:04 GMT  
		Size: 16.0 KB (15963 bytes)  
		MIME: application/vnd.in-toto+json
