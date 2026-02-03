## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:6fa71149b39566a9b40b3e31620da4b02316e38d01a7c2f408f94252367bdf46
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
$ docker pull neurodebian@sha256:c6fe056761bf624c48323aa68b1a0f5d713c4d0b61832e061ca1ea7ecda933c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21627ce4e7ec3d7e88f1abe7fa4bc41c147db83695ed04258bda3a7b6dc4445b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:32 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:35 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1d633e2bc91aea90973516b45752d540db2ea3cedbfabefc881c030ae1e19f`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 11.1 MB (11103524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5bcd939835f01a3b851bb6cd334c3fdaceae44dc5ad0b2ff9983495d88ad0`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 1.9 KB (1889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0cc5228ca7eca77a2a40283d1d9ae0330aa87b2d01ff8cf386e2e04e296e29`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b465d2202f2a38722e786a7c0e5bd9671a551c9ebbcc46d3929a4bce2970a3`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 101.4 KB (101429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9cdf47e555c97d954a83f3afa5500cf5b0c917f7db57b2737a13e136b200a8`  
		Last Modified: Tue, 03 Feb 2026 02:48:45 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fff433a0c16911f96bb25b6fb337a61b0a4c392e54d963c253c382e94f961fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e6144505b81e88e04ceec7346c279a36e30e6c8747e2c29b4a53bcccf0a4224`

```dockerfile
```

-	Layers:
	-	`sha256:83904257f196bddf92b45b7631562668036000f57c2d47b653b38066e4e63f45`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf75af788ef139571dc1aa51a678c8b24d5627b132e55c158d9d084f744edd4e`  
		Last Modified: Tue, 03 Feb 2026 02:48:44 GMT  
		Size: 16.0 KB (15994 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 02:34:06 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:34:05 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:41:26 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84f7876b97c9cc558e3b682faffaa05ced369d3a1daf0097395a92379a1e56e`  
		Last Modified: Tue, 13 Jan 2026 02:09:04 GMT  
		Size: 11.5 MB (11500374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0706ef71ceb0b289ae294621e19630c33b44b79fd2a4700c9bfe91af88f5e09`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93d15594c1a09687f963a46a767fd98814ce5068a9a92bee4d01761a2547e5`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5685f5a198b5049eb844e3225fc405d497e7a828788b0b2d3a99315e1c89872d`  
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 101.3 KB (101277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2935e4ff248fbeb6449435fe4391367a3ec04a837788d04f2a5c950f94815f39`  
		Last Modified: Tue, 13 Jan 2026 02:09:04 GMT  
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
		Last Modified: Tue, 13 Jan 2026 02:09:03 GMT  
		Size: 16.0 KB (15963 bytes)  
		MIME: application/vnd.in-toto+json
