## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:e104106f660546d667426a24f12ea3c97aeca1793ebffc238c73b16197ce61bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

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

### `neurodebian:nd` - unknown; unknown

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

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8d042e0c6b2b0bdc7bd6088a54197a0062b4e77fef4e334f0b514b42ce76bf43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59920057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca4e48d28afe7d23765196f54fdea60741801af0f6b198d4f1d7aff164ec43b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:46:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:46:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2a6841249cc037385aca9cb88bc26e07cfa8ed2a3f883ffdea8ae1be354b5a`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 11.1 MB (11092978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938906dfc842f7becc351af1835f05072b61776a354569f75a22d1f1e6ac299`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0668f71f67e7f7a552b9af4850f0941fb6afd56c29cadc4acd358584bd8a7518`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c06c9c91f639614d4952e3ed20b59bf97c833709c3620987f812909d74f82f`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 90.0 KB (90027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1515e7f8ac45bd3a4a536ba87d58574f9beedb409c59fc72752b88164c944056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3574968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36672cedf692ab9b354876cbf435214d90917c05080107060f25e608acf9f045`

```dockerfile
```

-	Layers:
	-	`sha256:1aa37ce6e70e12258b02b458c1845581d86ecdd450c40a6a59c724b75463cf93`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 3.6 MB (3560939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da2b316ca48ed77a2b1aa0ced2f3d8e67b58143d8135f7f24e5168d05f49127`  
		Last Modified: Fri, 08 May 2026 19:46:58 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

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

### `neurodebian:nd` - unknown; unknown

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
