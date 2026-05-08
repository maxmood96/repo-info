## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:a3cbd7ca8039c13e7eb7e557f96439de19b426e31ca2d13b56dde94b07020624
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
$ docker pull neurodebian@sha256:555440ecc7c6f655a1f24cb37b25ac77f16f360a99049d9ea7a9c5c136dba234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38937761e563f02f1a8d4ba92e24ea94cdcd83de4203265bb370625eeda2fd05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:44:00 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:00 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:00 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0802b439ba506ee42b40891edfe6f9b4eb3055ea7d81ecbc3d1c87a08b141de`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 11.1 MB (11103547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42ee071305f1b461b88de5416fff15b4f7563a181be72046ad6dcbe2c446b02`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f9afea8b6181ada18a56edd636f0726aed91cc8382c81977739411f231524f`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386ec5b98b370be832b747e784e7effe8e6a952f7ce138c4def942bcc243d7f1`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 101.4 KB (101353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c47ebcb0a700e2b6652dbc7de864c41d2126d949ebd0bca7ed3acfc9d8b614a`  
		Last Modified: Wed, 22 Apr 2026 01:44:12 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ace222ba3da95f703da60158d587e1157e099ecbbae7f02da2f2877bb04ba743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54135d0cb4cdfc7dfac0b8beb5954939cb79280fe680f47eec5643ad0f6e7346`

```dockerfile
```

-	Layers:
	-	`sha256:e768aa59b6fdb62033d29df462af080e0ce18d30ba88640f432b6cfaeb7aa0eb`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 4.4 MB (4367950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b29bfc03bd2c77e02f21088f2cda163050d8f828320dfa8b1d23037ce926f25`  
		Last Modified: Wed, 22 Apr 2026 01:44:11 GMT  
		Size: 16.0 KB (15994 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

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

### `neurodebian:bullseye-non-free` - unknown; unknown

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

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:be20e7b0e215c4deec6aa2de282c6b428f0d9d78dfa2e9a48a21a04aa1309aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271902e4ce05784fc0ff5d6e016a0845b149c59c943cd5951bb641ac145378f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:43:29 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1516c79839462487ebf969fa4a5a0db19d5af6adf507a4fc9cc33e702e252f68`  
		Last Modified: Wed, 22 Apr 2026 01:43:41 GMT  
		Size: 11.5 MB (11502096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc24b7ff3fb59cab3e8b089d3e98f3aeeeebc1a716fe7e4b4710a8f2c57f89ce`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ed96c6739d01a12337c6c9b40fe1c07118326d0531824658d69a8239253bbb`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff1c6f719a9e92fa099ce6018f4fe86fc6cd03baeb042f11c1d662042c50bf9`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 101.3 KB (101271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4755ffa1449a1b0999111b69e5bd22eb4db3b4de5dd016f94f99c635cd80148f`  
		Last Modified: Wed, 22 Apr 2026 01:43:42 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8d9b3ca1ff285715b70ca7072ee3070c4f5c341311035c12b90f3bacbc8db176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d03e6338a4f4cda9497f14486e3ba04f901974153fba8b8ee489b3574a9899`

```dockerfile
```

-	Layers:
	-	`sha256:06c69fd2a19c9907618c9ace118aa384a7baf2562e3fb8fd3747926c796f47ae`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 4.4 MB (4364469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e13d9295d1f7ceb76e6efe645bb726797d1bbf0ea08d285d5bf4fd07015d0ca5`  
		Last Modified: Wed, 22 Apr 2026 01:43:40 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
