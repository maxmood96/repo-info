## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:a1e542ac7b2c45a6c308f62ebbb2e935d31136856d6955d5411697fc560f8578
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:b687f95b09bd33f1d6fc6023c50035210c76b090d4452ac589b1e16943d40dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db85053dfc60633d33e2da60411b52b36da568192c2d368791a87635521e4477`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def3f2dad6b1f604ad4c07c3db4985365f97269cc58f5920dd7a1500f2d8c8e0`  
		Last Modified: Tue, 01 Jul 2025 02:28:02 GMT  
		Size: 11.1 MB (11105129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ccba64b24515e9839769851aadb7822e51d08f355407c7c41beef62b118b99`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776611f363aab3cdb88c94e560b83508c59dc3fee3c8587fc4ed0adaf8dddfde`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcab2dd3be6f48e07a2160f3534a114758725b772bc038dfc4410214b453f7b`  
		Last Modified: Tue, 01 Jul 2025 02:28:01 GMT  
		Size: 101.2 KB (101197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:6665a43de60208538f9220729a73928e3a9740302d4281e2a13f013115eda085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9217b8643e922f9471e290337d3f5d00221866205eb1e925f53662a166ffe8ef`

```dockerfile
```

-	Layers:
	-	`sha256:514144ea2bb344684170ef2aa30ae5c85a2ed7a4f8ed8a9635b6b0c163f1de56`  
		Last Modified: Tue, 01 Jul 2025 04:07:39 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2540c5f8cc2d3e0620d788d859493e36fb4b167fa8116165969ab865bec5d66a`  
		Last Modified: Tue, 01 Jul 2025 04:07:40 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:c6226c5d1bbcdbcdc4bfd2a736a30090d07676fc9f5183fcb03747c3dd45d7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63461606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8dc659fb58bd17842f2b2b0c03ff062761bdb5aa47446d67cce71e8088094ae`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3704fbfd86a89305a8a4d0556a88966db2c9ae3b7731e49335164c93b49ba182`  
		Last Modified: Wed, 11 Jun 2025 03:31:02 GMT  
		Size: 11.1 MB (11106051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bcb90956441591df9a1f5f32b74f21a6fc4b2efa523a109f5c567befc57d05`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 1.9 KB (1895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d5133fe164372190e333a26acb1669673c83c44225e9c4bcd48cdc24788087`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473514cac34b3a0a9d0a408fb13bb9096b3c088423448884d4944cb5a73eecaa`  
		Last Modified: Wed, 11 Jun 2025 03:31:01 GMT  
		Size: 101.1 KB (101095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f47c60feb71e1a24026ac69a15c67138420dae31da3c6ff87cd0acfd6383b01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e77babfb6209d17309a5a4dfefbc6ccfcf22478fbb4127264d046b98b027c01`

```dockerfile
```

-	Layers:
	-	`sha256:fac044c3fa4a5f3cd2da938d094a023035b08124113a81a01dde2d020ee655db`  
		Last Modified: Wed, 11 Jun 2025 07:07:30 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff065860ec4dcc9bc48e62a6fe3836c570b1852f1ed47af72b56cc3f6a4ddc1`  
		Last Modified: Wed, 11 Jun 2025 07:07:31 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:6e909d6c7fa5cf372e8b4abe17f50eeca0e00c630503cec88634de534003f725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60d0d301ed5a1ddd3cf737fc8c7772446f55e1d7d79d437fdbe8d88e08089cb`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7813ab6958459e0b769c4eaa51def1096dfab337ff7338a6ea28a8bdd9011dfb`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 54.7 MB (54689934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cf048cdcda148f850e2e923337e3401fbe1b081347cb68f105fe08a801e7e1`  
		Last Modified: Tue, 01 Jul 2025 02:25:04 GMT  
		Size: 11.5 MB (11500286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d5835ff83f8c042a185d3cba1bca9295d92658f244e9cd26f2b20ac9c1d1fe`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc86b84a80b36b0face148287be1c965f3409616a10ed9eb7c1b614634fcf52`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b3f1d3e2a2136e743e345a3eb6fb67b18d9dee013e83dcca7096e289dde428`  
		Last Modified: Tue, 01 Jul 2025 02:25:01 GMT  
		Size: 101.1 KB (101087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2ccb5caefff2f66c642dbd34b4502767433f033578d678c313a27b4ba11d62b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf33f0ef895cbc93d99d36f202d2ae4942e8025fd3ab6e2c9eec54ce9f5f6cb`

```dockerfile
```

-	Layers:
	-	`sha256:eb2bcb20d589d3cd3dbc77ae5b266f8179020929c01c37afdb660b839c24a802`  
		Last Modified: Tue, 01 Jul 2025 04:07:52 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7136ffec7778c0aa2729a07697c8ecaf5aa45fe1a01ad817adb3d3f20e5e6871`  
		Last Modified: Tue, 01 Jul 2025 04:07:52 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json
