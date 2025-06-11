## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:bceb8e4ed0b2e8eb3d51c87c2b67b5426c694a9ea62406bf4a879f2e078f8917
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:df6f98d131c4b4bf650a51a1c7cb8ed75f6b077109089524861bcda54b09d0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e761c4b19cc195da8d2855cb566359243e2c2282c9d400eb4c1e84760f913924`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09446529b39b6e747011c65127756ea8c59f2b0b9dc3096e7f48c5de96ccc8`  
		Last Modified: Tue, 10 Jun 2025 23:39:47 GMT  
		Size: 11.3 MB (11266854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301fc755d8ade11aeed0a053875ca7bec42da40cb0a5d13ecb4b84d6c554fc5f`  
		Last Modified: Wed, 11 Jun 2025 00:04:20 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0288b274dd2c371bfab2859b2d1cde4581488f737485247c84dce92e4d2b7747`  
		Last Modified: Wed, 11 Jun 2025 00:04:26 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88f0c71750a0635a612ed508c265aec03154a9a165ac80f4d16644bb162d486`  
		Last Modified: Wed, 11 Jun 2025 00:04:31 GMT  
		Size: 93.2 KB (93182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b082f19682f2b486a0c80b855625ac837ca40d6474e312afe94d9358a943e0d9`  
		Last Modified: Wed, 11 Jun 2025 00:04:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a59d18ee99e44947f8786dc60e2eda4f1ad2dcb9e52f80b9ff75f6f0503c7b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4085158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dcbea1c292a0676d2e7427bad68077d67903db9500a9c57e829f6c4376720f`

```dockerfile
```

-	Layers:
	-	`sha256:190e185693c59b487307682a32db421010423d06f2d8afc82e125fd629a46f57`  
		Last Modified: Wed, 11 Jun 2025 01:07:29 GMT  
		Size: 4.1 MB (4068811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7352e7a8c0e8bdeb2fbdde263e76d108e097cf91c47f04aaa19d2bbeea69cda6`  
		Last Modified: Wed, 11 Jun 2025 01:07:30 GMT  
		Size: 16.3 KB (16347 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:f0b21e9a2b1d87e8e9d1cf617208198e10c617d9f80b1339ff54ce27ee66c91c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36204bccfc429d1ecc0ab3e4cb4d125b9a3f7594aa42d97f2f51c173dce13323`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2ffc1c9ee11e35bbc8d570cbe8cecbae9658b61781afc52d70080ddae7411d`  
		Last Modified: Wed, 04 Jun 2025 16:16:03 GMT  
		Size: 11.2 MB (11232707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93401a734aa5fa03346b425f587a1e2d185b73fc18e7217a63a017c0a9e7b85`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60235f1eb5d671ee92cd25fa8f034e60f95851e22653011334140922c4f8bf9`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9addb204274723b9dfc2bc35a1fa12c9b517f82e012207157d445fa00609fe59`  
		Last Modified: Wed, 04 Jun 2025 16:16:02 GMT  
		Size: 93.4 KB (93443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd89280029104abf21945b59b054a3eedf9f7b23e94999b1aca58011419c300a`  
		Last Modified: Mon, 09 Jun 2025 00:55:36 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7e6da63402e4b1eef862b0d8a3f101017276aecf02c60186b794120fd687915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3971615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107dbd281f4baae96d89cf725ff834951638204a9503b9812136446b2ad9caf4`

```dockerfile
```

-	Layers:
	-	`sha256:b4f000b0ebc61fecbc86e06e322d07a3aca6d8fa3ed3c9d7d781d5c75cbcf560`  
		Last Modified: Mon, 09 Jun 2025 00:04:53 GMT  
		Size: 4.0 MB (3955116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73550faaa5db727c23fdf4536980baf5f17f7a89739abf435a3879571e512a4`  
		Last Modified: Mon, 09 Jun 2025 00:11:16 GMT  
		Size: 16.5 KB (16499 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:bcef4e130e048631d0384f4d3a205fbd025912b2c22c4ddb4b379b316643f789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4925bc3778b6b9c6a745172c48b31f0867a1d496d392da2e5e6cdbafb8a59ae9`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b3e3e6e2d9340b30d10be9677d2a91088a9651305d3e2814d24858a5d1767d`  
		Last Modified: Tue, 10 Jun 2025 23:36:55 GMT  
		Size: 11.7 MB (11688864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847d2ad000b61b2f234b9980ea545edacb02cbd88ee3f3f90bf6fe2daeadb805`  
		Last Modified: Tue, 10 Jun 2025 23:36:53 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994203a98e1d20fa0b1dd98832c1f6f178640a9cf5f3b357e7fc2dae27c25aa`  
		Last Modified: Wed, 11 Jun 2025 00:04:16 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4912929dd01f693d2d50ccabad470fdf08e88e1602d5cc27d7edc7d2de7f05`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 93.2 KB (93219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33efd2b24711ab06b45a10963b4b06e468a842e81d32c38d9e6b08cbd957171b`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff720c8e4f114b36fb3ba27756e87d0525c45d132bfcdec8b951db47adfb27e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78957fdb65a2c4183db08aa3428de96e661ea300304ac4527d7c61ef279719cc`

```dockerfile
```

-	Layers:
	-	`sha256:8f7c40befd41400cd338eee56f9ab359489ae226cb16cba8f1a7265fece184b7`  
		Last Modified: Wed, 11 Jun 2025 01:07:42 GMT  
		Size: 4.1 MB (4066779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b39234998b303494b07caf4110461e1fe5a4a40b9aa15d920f390887c601e67`  
		Last Modified: Wed, 11 Jun 2025 01:07:43 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json
