## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:d767f4c150fac95b8d78241bea39205c24160bfa465b6a45b00d197da0379306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:4579804f9c875206d578d7270319dc28a643d4aa34b4a2367fc01971c611b3a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60132047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c41acaf6f627e96a8a6c80d06069c338667c22f85a7d97f1e84ef7a31090bdf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a10f86d641494b5e6b1c3b8b85409baab7c4d325c9d6b292a94180331dd6b765`  
		Last Modified: Wed, 22 Apr 2026 00:17:03 GMT  
		Size: 48.7 MB (48670580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3323d1feb76ec39412cdc7d5e6f45ca2ae177c89aa55e93ac5b44a2b6d906a5`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 11.4 MB (11369205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c437c44f17b74c9f33cf3e8e09521e142cce4eca24916441e07fe0bb3c6761e`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdebad56288aa68c2c0d31e441aa24dc3377cb17a75fadca678055d5a9b8037`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595eea0b749305f483189db566fdd77c036708c287c2826ffea185e7ec4aef28`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 89.4 KB (89361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5416e419aee655489a1463c82274d016822c2e5580d33624857a086b5efa2e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3567858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d239d728c5941ccb90be7991659b301e96754d13cf2e657566205ab9865d2930`

```dockerfile
```

-	Layers:
	-	`sha256:e113e9ad631fc85d20909c5fe6734ab6769af5809a286fde81aa8eddfcfba9fb`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 3.6 MB (3553954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b311560e14d5ed28de590f0d425f27f4f3767dda4686161f9a858af8bf7073af`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0abd855e4cff87a36e4ebb8f40dd8654974639604b5b088d0fdc0dc03594cc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59878213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d58153bb476604bc2d7ad9631aa75339f5babe9720a507535e9efd3ed33ba69`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:47:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:47:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:47:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:47:23 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f7ead27882db0d1de6eb6e496d384f406d278f217abdf3e3c50a235ce7737146`  
		Last Modified: Wed, 22 Apr 2026 00:16:20 GMT  
		Size: 48.7 MB (48711371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c29ad565b922827657ac0f33a186ce40a940510fda76beb2d874d1d5b7030b`  
		Last Modified: Wed, 22 Apr 2026 01:47:31 GMT  
		Size: 11.1 MB (11073925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511be1a46ff384a862d72da9d2e226e22fe4006d712de763a4d58c7ef0495a`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e85e5c905988a736f792021239cbf29a8923446a7b545160bb4951fa705bc6`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d36acdff774458323d42437f75ecd32b46defc5c8138e7523766659b6add11`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 90.0 KB (90013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:803f87020fee5bfd46a8f93d177b3e8185c32d355677bc1398a8f19ee75bb438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2fad5403d40e355b0bdd69b6359195e04117ce9736be23c09e479169d238a54`

```dockerfile
```

-	Layers:
	-	`sha256:b14618e60abc7a7b62b9ae414e94d2e7ac1773cf504b8d3d5c3393cb4e59f7be`  
		Last Modified: Wed, 22 Apr 2026 01:47:31 GMT  
		Size: 3.6 MB (3559939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ada421d2dae55a1bba91151296ca8a6dcc4778247e367b54f5b9d54c99244784`  
		Last Modified: Wed, 22 Apr 2026 01:47:30 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:044f83a3d7eb0b8c55409b58a1f42685deca14fbe335dd8caa00f5f372d9bfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61673915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc23870d7b84a7c15f4e2f712545287a06f7569ec1c73fa77cd088f2bddcd7fb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1776729600'
# Wed, 22 Apr 2026 01:44:23 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:23 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:23 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a68ed28706ac755be40447c885e7277b571939be826b0bcf8abd61cb9be646c1`  
		Last Modified: Wed, 22 Apr 2026 00:17:10 GMT  
		Size: 50.0 MB (49978211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd6f22b6390e0b2749fca38f9bb2fd609f4420f88c6ef086f4d2a6c3c71c7f8`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 11.6 MB (11603049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5abcee47f182db20cd39e6c87b5f6253d17d004ca4cc49437e874b1331770`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3352681e10ff29c43254c025849efec18d6b5dd5ad9f3031cd9b43ed4f1b4932`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575874e7db5cb895159b72c29b91e0ab22a06e4a74312556d1ff14e5925bbdf0`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 89.8 KB (89754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0c30220cbd31e8748b077b77cfc95c1630d8f2c4dc27f35c5c089a9a36bcee31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25903a975556a7d320dfd4c4b4ef0fe89a1b7f9e5f9a10269a8520fe75b6ee3`

```dockerfile
```

-	Layers:
	-	`sha256:60a8019be1efe3a65435f58733997d2b65f94549ca8d9d7b5364942ced6e9904`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 3.6 MB (3551903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c745709d65d1864c614cdb8c10c0a67e3faf129b909cc387e1c03227688a1344`  
		Last Modified: Wed, 22 Apr 2026 01:44:35 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
