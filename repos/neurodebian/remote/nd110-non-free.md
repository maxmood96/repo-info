## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:1b2d3eb7162fae37bb54559c3bac058da9808476b1876f6027f94729f0fea0c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd110-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:970c3a6ae528525bb1e8ab1ec34a277265ab7d1abdb574832d47e7b4b8c78959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3cb5553e0927f86dbaffefdba643cac55d235a4910d2d479e673633f35f833`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:12 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:12 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c21a08615a577f1cfa9ccc4980ad83b9af3be6520d08499173bfbbb61cc28de`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 11.1 MB (11103504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa6222b3a12994a0a3d2d5aa4e59b93806764f67a9b46108db2375b92572559`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3439e15c014b6ca69436cc53714a5a12b8c82d212bba1d8118567a3fbd3d26c4`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1712a4f29c136e1d7c3f29a70419828d6a06c4f8c0bd8aa2555a88172fd1f9`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 101.4 KB (101392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921683cc3659083392b4ff077850901d45c2fac00ad861af8966aae15ec5a7d8`  
		Last Modified: Fri, 08 May 2026 19:44:21 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:80de42a461bdee72a6de0d2d96c33b96fda58b0f709ab38dda5fbda0dee923d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c6e6e38805523120e40167d506fa8e6fbb1c80532580e72d86225e2ef8685a`

```dockerfile
```

-	Layers:
	-	`sha256:ecf8938eaaae846b52eff960911e1aaeaeea774db94fa0d9270c7ccacacba99b`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97ff8956eacb6b69eead663a90a02709ad62af7970c98817fcf8310f3c26185d`  
		Last Modified: Fri, 08 May 2026 19:44:20 GMT  
		Size: 16.0 KB (15993 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d72cd51fb944fbeefc59dbcfd9207dd62d6b1409175dc0b62c30c20f9723340d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c72a73a81907cd10f4ed9d514fe1d0c96154b13d775360ec1f4e578b4b7c08`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:01 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4d4853c366ae1d8a6092357fdeceb46f1af7fb6971f30fb5bac64d2816093`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 11.1 MB (11109872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0860e8ce6527c5e5eb574f904941f9d5fd1ac72704eec1e19c9667591571cda7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2407a0ee518c92a25d491c4909ce3ed0cb4f84524941a201a7cf2bfd943c1ed7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86985c6bd9a382f6fe79e55952fe846b9dac4b331da91606603aeebec797fb71`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 101.3 KB (101294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a645068ae63614955aa0cce30edd178a25de8ca2dd269f25af6a34467cb6d54c`  
		Last Modified: Fri, 08 May 2026 19:46:12 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e79ba75ecd78047e815efee9fa2ef478d94689d9d1ab9f20fb7ba7bf72a022e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aae72f0e29b5b3a88976fb346afe0082117da0014a70001d64ee3963b586eab`

```dockerfile
```

-	Layers:
	-	`sha256:97a48df79af5e64bcca963ffbc0947249e8e2964559cd3a0216d0b5fe3a662f7`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 4.4 MB (4367557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7ecf2ecbf82b72a416e1ef61bc9ea6fe75d4c000ee213c306b6148414a9521`  
		Last Modified: Fri, 08 May 2026 19:46:11 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:ded0c9f44bfebe4345080e2a4390c3b4fed39780d1353b24e811e6661fba9ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a59c5ac3b1631f24b5bc8d5baae5bb53973e1d0f372a2f088c0314105f17e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:31 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9627add8f31e74417d79a305014794f3cbdfc718e75672d32ef679cae4d543`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 11.5 MB (11502376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fbbd060166db850453937acb417b1629ded3d89e8f175047d313eb4d4ea249`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bda2e809eea5007777365a49ca07551a25dead0adc7cab0981a605143ef59a`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f25d850d54a1638e683ef541be2effa3bca6c0b42442affc13c0b580347563f`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 101.3 KB (101292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fad3e9fd8287dfd51f1b9399e6918557a0ab780529cfb43d95f377c5871ffc`  
		Last Modified: Fri, 08 May 2026 19:44:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84d520f83be769fc2d681e70788d29039c5cde27701f289c18e4bab929ce8d3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24962661fd033444e442b5d8f8a4cce6aa12e5693c6953d7f1bff736b34e166d`

```dockerfile
```

-	Layers:
	-	`sha256:423513329c10f41f709cff6f55c81130aebb09ea250c3f3d837102c1163b7fbc`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4f37060f92539dd9a20f74d6de85a1f15bebe90d992329da9927373d4af4e8`  
		Last Modified: Fri, 08 May 2026 19:44:42 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
