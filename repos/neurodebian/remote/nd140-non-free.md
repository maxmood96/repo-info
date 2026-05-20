## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:fc692782f71ccb077da8611789c9d51663053488c1e1182d5126e93dfda29f1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

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

### `neurodebian:nd140-non-free` - unknown; unknown

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

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

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

### `neurodebian:nd140-non-free` - unknown; unknown

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

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3b0d1d02630a55a6c377fac8567c347cb626f7b41b37009486d26cc4219a707c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61720915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a46cd04684649a857887b5148ed9863726fbeae7e8cdc8a0c3af9b9e4fb03f8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1779062400'
# Tue, 19 May 2026 23:26:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:27:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:27:04 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7af1962edabe3d58af5fbd06f3e345528b78b672a4b879b72fcf2e0d92549637`  
		Last Modified: Tue, 19 May 2026 22:36:57 GMT  
		Size: 50.0 MB (50001944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b022792ab90d17b19c012791d704160e1cb4d9c1094ed5126b1ac93056114f`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 11.6 MB (11625868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80680d0e09afe77e520bc718136fe080de719a24960af381889b5325a007ced5`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049a2f99f1f32136fec89aea3b0aaf2aca4477d31c89bde845d0e723a40a5695`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56352ba5cb0918dea97f161038dfd699afb0529bea66b2ba9e35950d31b10132`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 89.7 KB (89747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1ddd8e31b744cbe0b5383cca53cdbaf40687dfc7261d3a1015473b4ff07ac0`  
		Last Modified: Tue, 19 May 2026 23:27:12 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:042aab238d53837875e53c16a3e8ad5d5d5c64f13e80e00a71a6262f9605782e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899c13bc48fc716a0d53b364d858095d8a5fae3ea53f1452ce1e5c91a133f67d`

```dockerfile
```

-	Layers:
	-	`sha256:cbce9fd25812137d4aeb6f43af2ae3016ac0cdc0b3a8a78ff505c25198869c80`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 3.6 MB (3553615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:104654a631070bbc809227ff13dd24c16337baf2e2d63f359da294dad41790f9`  
		Last Modified: Tue, 19 May 2026 23:27:11 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
