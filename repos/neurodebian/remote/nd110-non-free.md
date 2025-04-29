## `neurodebian:nd110-non-free`

```console
$ docker pull neurodebian@sha256:a209a003fe2cf739a06a10bad52dc252cb0b03dd16c3e7218481887f240c5bb9
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
$ docker pull neurodebian@sha256:d81a476a0c0a5200917c0c098955ff67c2dc7163b6722f5b9009ac1d6ce8f87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64956557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51bb2c6517b71cad4d4531fb28674813bdd45eaba155b3f1383f1f066bf9f978`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3805948ea0a099f128fd1590cd09c7deba13a775bf11ad6652a65dee5e7b3307`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 11.1 MB (11105099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4bb79503e49002e87fadfc3687fcb6efa56f7c94788a32dd04842147ef637e`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e782051a7146746e97fd5dfaa52270bcbd5ce40d6c85269dbbfed17a02a624`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3633c4afe5e0e441d7aae2bffd0f2374b68698367bd08804f4fc636516b18`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 101.2 KB (101171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e5747c9ed81a4fef65a55f99af17f7db3a478c7d5d65e53369b2aa9e584969`  
		Last Modified: Mon, 28 Apr 2025 21:56:53 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4454b45f35b9696e23c0d5f895e9c28c8463b5888c82e6a557714df5e7f6932e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cbf5bc16f0f074a4177db482f4899dabc0752ee21ac58e4fafffffd3839615`

```dockerfile
```

-	Layers:
	-	`sha256:7d6d60dc20dcc8be5f866b6763476be367a685777bcf709a1813368e566f6ac0`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 4.2 MB (4234800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:984001af9a5f710a9a82b5c0fa141ddf03a8717e933fcda115e031f021df0ab5`  
		Last Modified: Mon, 28 Apr 2025 21:56:52 GMT  
		Size: 16.0 KB (16037 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3cda06f8fb6326d7aff37ccf966a10e15f1e957e7397892ed65ba00cb7324a2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63455704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e866f9690cb93c903552d461eaee74e9538e29d9e14eddf6d9fa64f8f3d735b8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9753e330284da1899fd231bf33fe62c0d83e3f17a233f3f30f504bbb6fda21`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 11.1 MB (11106062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4499b0e25845d2e35fdde74226cf5901ec7e9be9382eed98b9a3eb02064d539`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4039d5ee1ad977691de6bac1fb9373ed9749a1f33ec81bd570216e56c21b379`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ea557c3b7e8fb6dd8d91d49cae4f0e43f2c39dcfedf77ad960408c3552376f`  
		Last Modified: Tue, 29 Apr 2025 20:17:58 GMT  
		Size: 101.1 KB (101116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb5394c6c7df9c157ef89060c5b3728c4569afb6f29aa90099a6604e7b5a5b2`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3900a4f64cf6c27e536fc131954fd0c5e09bfeaba76a2c956de2b194626b4606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4250582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9bf7a90d529ff4e3867c6ee1388eb4da4b771cab6312d7727d44a0862d829e4`

```dockerfile
```

-	Layers:
	-	`sha256:d1212b901568e21393d035b08d640b468c1053363d014e1f3307ed7ce8c051e7`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 4.2 MB (4234407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978d1348aeb4ec99ec3692b6fcc8ef4d9de310223650528f78e204440ac3c50b`  
		Last Modified: Tue, 29 Apr 2025 20:18:11 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd110-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7fe93975c6b8bef6ffc276b4ce7083e14497561f5596eaa3c2c3c77e70ecc0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66287038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed0c0c22ad836af99126ccc8f2c1699cc2253963005fb73df0ccf1dde0ec19b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78a375722d52fe5ae5287838cde6a528a6e3614649ea4486c6a6a04472f8b24`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 11.5 MB (11500331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4961efc6aaa6e0e2fef51fabe26b021418deb491dd1ce5250e97ebbdaf940464`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799be99c522aa1a27ffd172f171bdec808f16037cbd4c44d8b4f32adac7e7cb`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef98689bf88067a5b7bd537640dba1d3e41a94c92bd39a54a5ba69819f82ced`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 101.1 KB (101058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa2462fc78f51b305bd074cf1634f3470150f9b2f1b82f4e1107b93bc57f047`  
		Last Modified: Mon, 28 Apr 2025 21:54:45 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd110-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbd5d38b5fedf86b44de1a7e51c7dde5402528d2aa0091a7f87f2ef16d9ff987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3f2ff430ba7fcd8d76f2f2cee0bcc459bac956d411110e7af8a975f6702b5`

```dockerfile
```

-	Layers:
	-	`sha256:99ce1363ab1e2a5dd36fb177e64e2dc8d8ebc1104b228a1f43e0c06d241aeb44`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 4.2 MB (4231262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe1745ae34a3bf2f421654efb60c5db9c2254eabba488faed4ab3d800519c0c`  
		Last Modified: Mon, 28 Apr 2025 21:54:44 GMT  
		Size: 16.0 KB (16006 bytes)  
		MIME: application/vnd.in-toto+json
