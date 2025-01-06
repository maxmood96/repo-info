## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:7b2d7509820d4a42460b76c04196e03ad8598d4e9c545867ec3bc8a018831079
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:75dc470dd481b34d8d3acca65d9917f1e05d3a32de788b96b61ade181176e948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88889e709d3de477a06d2a8aa359b158db5f62f8a903fd365b5ceb5abd719a09`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096d5194d130e490b02f9eed837f199ac0d1abb923e345a62f61451a52a2cdd4`  
		Last Modified: Tue, 24 Dec 2024 22:29:02 GMT  
		Size: 11.3 MB (11266794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063a5616cfa155fb951bd0c9cf1dd0f9322ec8b3d98dc600700cce46c3e435cf`  
		Last Modified: Tue, 24 Dec 2024 22:29:01 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f06dced8f7c7fe5dbfd8ef9650f54793d5d6196b43078f72fcd64b157bb6bc`  
		Last Modified: Tue, 24 Dec 2024 22:29:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7ce674a7b52e38abb4f78fa7e02c121e59eb3d7399264a95f7f1ff5c52df7c`  
		Last Modified: Tue, 24 Dec 2024 22:29:01 GMT  
		Size: 93.1 KB (93148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a37183ccd386f80afe02a6835a70753e0e305681a417bc3b629d708ecd2b62fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c09a24876501e8b0b66414bddefa4bbeb57cab12f109ca753bdcf4b0cbe9fc`

```dockerfile
```

-	Layers:
	-	`sha256:d2a5e209b448748f04cd11161ac5faa84de19427c70ac95191a2e9304b6e29ef`  
		Last Modified: Tue, 24 Dec 2024 22:29:02 GMT  
		Size: 3.9 MB (3932810 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b9c6e22b9e5d5e04a6a3154f8982d932a9b712803427f7e631ef24edccac4a`  
		Last Modified: Tue, 24 Dec 2024 22:29:01 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:734acc47d42b01956b35d079b765bf472ccb9f50dc09f98cc2e40b1c9d51e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587cf8611df7fadff75a9d555af44c9e48df19f1c7b3cf2f2c57f9257665f68c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0367019e15543f02a69e834f1c24024f42ff4a354dc1d505f1fb3f7f641f344`  
		Last Modified: Wed, 25 Dec 2024 02:19:39 GMT  
		Size: 11.2 MB (11232347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91a2c5dffa6242c8635282e5d3644e5542d4d3fa55a50296ad77f135894427`  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f7a3036299a2c5f2be4ab8d3c47a46eab3f06d55ab60826cc639ced1d6c067`  
		Last Modified: Wed, 25 Dec 2024 02:19:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06582c2036bcbd28dd303ac041a31fa9d209a44ef50795590fe9abd81bb38db7`  
		Last Modified: Wed, 25 Dec 2024 02:19:39 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fb147c9de766d97770096590ec67c709e95e8595ed8c7e57b834e7557fb79de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46257d3c532f95254cd1e43b2d6a8989b741560933f1991eaef270f97e14547`

```dockerfile
```

-	Layers:
	-	`sha256:b7e98d96c97512e8b334ed328f0f3aa31def722c686e529de7d30412a2589c06`  
		Size: 3.9 MB (3933064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1250350dd844645b4aa3d7037f20c5f201967cc18ae3c49aafa8359ee8204a43`  
		Last Modified: Wed, 25 Dec 2024 02:19:38 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:8ef813151990f62e11c797c4a697acd88310cfd9382109f16b994da4581a140d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1062244cbc6e51d56db28c694d788c0fbd996974b55d996af2e32b19ed635cda`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dd322311a74f01b8b9ba5bb8502c37125af9fcf12a3c2deee1502f4932057adb`  
		Last Modified: Tue, 24 Dec 2024 21:32:22 GMT  
		Size: 49.5 MB (49475925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaca672024ed12d88e75ba076209f8fed3b1ae0f09abe209abab63e05d1de5`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 11.7 MB (11688955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ec5dd23d75ab6db4734b22603da43811c6888c5c636e667e08b27510b5ea5d`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2174eee6044b649d5c653f77f0cc8a18059a445206abfd699bac6449a22bb86d`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73be09a6e46ac65260dbd2eee179d5f83fadcd7ae71a737ff16ecdf1aec9909`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 93.2 KB (93222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5ae97e8d1b6021245600711e96823345f9c4c21abee5c2e7935c8a05f9dfc2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fd4bf6ba2c8dec58aa62a53b48218a992689df628a92629f63abde4fc3a7e5`

```dockerfile
```

-	Layers:
	-	`sha256:58d6fcff4a60871926d33a53162c63d565fb63b7e85dad0e4590d21e4133f716`  
		Last Modified: Tue, 24 Dec 2024 22:15:31 GMT  
		Size: 3.9 MB (3930727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd86357ccafbbed41a80187fec3260dca24b1019cfe1907149f9d44f6aa8d1d3`  
		Size: 14.0 KB (13967 bytes)  
		MIME: application/vnd.in-toto+json
