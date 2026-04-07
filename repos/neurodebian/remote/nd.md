## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:25e9be42321ebefe6ba08a0c5d941df090d2943c03c2af4cbcedf72afdd26120
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
$ docker pull neurodebian@sha256:6d1e2474b98c2a1bcce15b241a355af4da64ec06aa918936617898d29512ac25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60171574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac865a5fabef498174fd27d645f2ae8be8b6b6fde69f727b75846321f55cfc7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:01:30 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:01:30 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:01:30 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:01:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7b208148f3abde07a5ac47cf579ac1ed4c9312d2ae485addb285765d8008fe12`  
		Last Modified: Tue, 07 Apr 2026 00:11:41 GMT  
		Size: 48.7 MB (48710648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9680cfdd3e4129a60748e1904e29c37d431b0b864e26b6cc1169ffebee2cb75d`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 11.4 MB (11368683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d3bef65c117797166ff5ed760c078a32b15b167e32a553a29c940570822487`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330aa0f33df95aecb126fa27d57bb3a070b44e34656956e7fe0264b009211d5c`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d45a5729852586277730461289592c04d0e6dbb72de0e324fbe2aaa4ed9d4b`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 89.3 KB (89340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:963260a04a05bbd3ebd62d35d0e902a265a373f9de3ed9623ecb6cd28dae7f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1362085b857b4acba8f4275e8aac5c6c836e3fe86647fbe51b6e62fa976a2c`

```dockerfile
```

-	Layers:
	-	`sha256:1fe4067892c99e2cf5bc78a6bd50a625130390f8b50c68533758ac6f5af8cde6`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 3.5 MB (3549087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a3533b60c61480c4ae00331be5f79ccbbc42761982e303d6ad716012bf7c297`  
		Last Modified: Tue, 07 Apr 2026 02:01:41 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:31470d05e1cac0a1fc11d2a656a7e2d8dc2144bf2a61a17deef16a5c76919400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59910208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bde8d257c76a0907a0d9b72dc78d5c7e23faafdcd8a3d208dbc5a33e2bfa443`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:04:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:04:27 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ac9c76c00b1b19d9057c64eebc87efd57976d9d3d4373752703081335cbb1900`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 48.7 MB (48744945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17966fa7c8589dcf8dc631f45556cd118e6cfdd3792e0d613548c653c7ba358`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 11.1 MB (11072457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945ff9025edf778838c09cc7ede3fe6e4d78195d9a5d83e9a08d56f48b8a57dc`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5466b442dfef5b49389002c7e3ad8b9c512754b0041f963eb9a349bcd89b8e23`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0177b69925e015ec37347d8c984b1cdac4793c06f8deb29a244711fb3acc3df`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 89.9 KB (89905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:59f0686f262a5e90c82fe3ffcd59f58fdbd4fabde77ccc91b6ca3abec5aa3dbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3569101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9527f078cabafd1d52505d1cdcd3bc968dc8970d9f7b252090e846771bc23c71`

```dockerfile
```

-	Layers:
	-	`sha256:1b37a51526a10036207dc61b7842830789c3a2421a4eeaf39bd1e53632363669`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 3.6 MB (3555072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0362e5d5c5cf674f3f001c0ae6249f64af6a3f8970763d8d641c0b28c56cccd6`  
		Last Modified: Tue, 07 Apr 2026 02:04:39 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:c60db7eec078dc52dc2c3c428344e9aa3479b05011d9d5b163e922dcabe8d9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61688484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a656ef86060ebfca5428834bdfca9780b93a6289decfe8dd3876b08d4ad85a5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1775433600'
# Tue, 07 Apr 2026 01:48:46 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:48:46 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 01:48:46 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 01:48:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c3eef9d9722af9b5785c5725c5b18d448456ee05c327ddf5310134754139706`  
		Last Modified: Tue, 07 Apr 2026 00:11:45 GMT  
		Size: 50.0 MB (49993711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c3a3fef3f09f7a3e83440b35d7d0f2f724470aa7260920183b022678103935`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 11.6 MB (11602235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53125d28144aed0499a184d660c37574f5dc0488d48921247a3954c584682c9`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca2c3c8f62c3c8516fcb39ee0b67f5091ffee2f35935228425aa07bf9763596`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a659b6eeb646760fd0e9d056438b39521d4fbbcfedde6dddfb7eeef1e8767a`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 89.6 KB (89635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5c2f9498331a592ff803623a19243947488e9062f3f57380e234383c343586fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3560918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5a868a104e8cfb4ba4bbc83480a466a971b55003ae7fc8a98d712b25c1e30a`

```dockerfile
```

-	Layers:
	-	`sha256:a58c065d6365faaf3bf8884ca4bf9f13bf2e669f9f981055bbf69409b235f0f9`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 3.5 MB (3547042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be546487457e10b6f2e2f752a781790dd2d55b4764632002fc8e7b752c8b4268`  
		Last Modified: Tue, 07 Apr 2026 01:48:57 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
