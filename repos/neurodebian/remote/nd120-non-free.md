## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:0adbbf3acc263c38a3fda0ccdc42cf8697e4ede36efe5e648eb1731a95816754
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
$ docker pull neurodebian@sha256:eff947da7ee0c0852c2a226c66460e8ed2e7871094a295e60df47d86d918c0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59846025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f590833af6f3c5cbfef22e42748a233539eaa90f4f84be131707df1a77ddc9f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16774c3e1d2be750d3953ca5e83dc23f769bb1d02f78a6c07c485238c14eda8`  
		Last Modified: Tue, 21 Oct 2025 01:47:44 GMT  
		Size: 11.3 MB (11269454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd12366c8d784ff1c28323d55888e416313fb285e573d04f1d374304d22d629`  
		Last Modified: Tue, 21 Oct 2025 01:47:42 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df306bf541aff31fa398771c6de75ef12cda5cb2d1894417c1aa6a61002649b4`  
		Last Modified: Tue, 21 Oct 2025 01:47:42 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7f682691eff198620ff118eada891db570184494166b378071627a2f1f4938`  
		Last Modified: Tue, 21 Oct 2025 01:47:43 GMT  
		Size: 93.4 KB (93387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91bb1a76467bb962f37bba034dd1294d6c4044f777a1ac7937b14f4b03cff93`  
		Last Modified: Tue, 21 Oct 2025 01:47:43 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4f356a21f382d33c3adbbdffbc681b27a594c74fbf0df0718a49705519f076e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33110afa117dfe451184587d41c0239865816e9203bc45afbc2e9eb41f3853c0`

```dockerfile
```

-	Layers:
	-	`sha256:4b1dd137af3ff55d9561102d40720aaa862007f7a70e548114eb802e2fcd9330`  
		Last Modified: Tue, 21 Oct 2025 10:07:36 GMT  
		Size: 4.1 MB (4075272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:292ad5df9b60c0b6310200cd4fcef52d543369e78dc5f5702a873eeac75459d2`  
		Last Modified: Tue, 21 Oct 2025 10:07:37 GMT  
		Size: 16.0 KB (16035 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fffa7f527826d62d4274bd238ae84c990c64b9059fcd356db9a4efed02a96a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59708554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d5a6ffbd86c53ea1a4eaa9a95bb80c43e728abdef8d3b213d5ddf4f269bdb6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3266e5c9d4a94667f9955785b8b773051d289aea79afe15e8da8cb14c96af7f6`  
		Last Modified: Tue, 21 Oct 2025 01:52:17 GMT  
		Size: 11.3 MB (11253400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e1f26bdf4280226ed0827bd6d12fe4d3ad9ac9223869a3270d427b17cf9fe8`  
		Last Modified: Tue, 21 Oct 2025 01:52:16 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90372e6a6df20f86e82be80dd8bc1a91f6447591f89a35b5e6c29f3024b59c9`  
		Last Modified: Tue, 21 Oct 2025 01:52:16 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0029ed238a8acd65043c2b42cfb9ca92581768b940e86122b2cfb552016532`  
		Last Modified: Tue, 21 Oct 2025 01:52:16 GMT  
		Size: 93.5 KB (93539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f80c0cabf30eed3f7aa08ddc855175ab90c509ebff9208d7648cb2ce9260a4`  
		Last Modified: Tue, 21 Oct 2025 01:52:16 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5a882e65f15aad15144877546f3b01158880213cd5f8896fe70823c87e360de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2802b796e8c98bd4b47f4d6406367b3deb9c0098ef4315c5fbc675d6b90304`

```dockerfile
```

-	Layers:
	-	`sha256:882c74499f04d01c81b47a5392ed424a0e873a6a6cadbd29d145610c8f2eee3b`  
		Last Modified: Tue, 21 Oct 2025 10:07:41 GMT  
		Size: 4.1 MB (4075514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c81b9794c13baf0502122439f1a1e7a2d76cbb2f04c33f65be920244324e44`  
		Last Modified: Tue, 21 Oct 2025 10:07:42 GMT  
		Size: 16.2 KB (16175 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:74941e6115c73cb07d451afec4a2429fca1334c1bc61070023747b071573f85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61252793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a8ba38df65865835bb5f3f768ad4ae4ea6a3d56ea02ee178802d614b031ea3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:3426ba65368da59a25d050cab9d7713d7873264014ab6dfaa6b0c33f0632cb80`  
		Last Modified: Tue, 21 Oct 2025 00:20:21 GMT  
		Size: 49.5 MB (49466720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05e5acad3a0149d7011f661ce2620d0aa534a4b2f985a79e7fdb722324c55b8`  
		Last Modified: Tue, 21 Oct 2025 01:55:22 GMT  
		Size: 11.7 MB (11690082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d53f4f5cbc892c5c72f8bc953c2c5d314a8306b4e46c0066601903baf51a1e4`  
		Last Modified: Tue, 21 Oct 2025 01:55:21 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f55a74ddc5de469719e6253629bda0873fe34d3c12fa57f029f4f57bec67acd`  
		Last Modified: Tue, 21 Oct 2025 01:55:21 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2455318143cc88a36c9dcc975e5359fa561e0b348cdc0960064e26f4795f455a`  
		Last Modified: Tue, 21 Oct 2025 01:55:21 GMT  
		Size: 93.4 KB (93372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28dc33ba4200bf3f4ec32cdde8604d963d225a41238222e3e92a5a48d697118`  
		Last Modified: Tue, 21 Oct 2025 01:55:21 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a77cd00e4080ae8babba9e00811a35481380039a995dae9f15b1dc9db892a898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bdf29006859dd418a367358bd48fa4e21391990babd580be1cce3ee1dc02f6`

```dockerfile
```

-	Layers:
	-	`sha256:1232b6e52253b7b8d852d2b99a84305742bc8ba6cb2b40a952c3c5f6b2a9da85`  
		Last Modified: Tue, 21 Oct 2025 10:07:47 GMT  
		Size: 4.1 MB (4073240 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4159b78f62f89a26e523df0b57d259dbf42c3ffca748b12baa74b4e321e8b802`  
		Last Modified: Tue, 21 Oct 2025 10:07:47 GMT  
		Size: 16.0 KB (16005 bytes)  
		MIME: application/vnd.in-toto+json
