## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:9abab9d15da6cb0e42d51e53fe1c1dc42aaf01fd04d882c13a28190851d6d3a0
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
$ docker pull neurodebian@sha256:48b978dd2f847654f39cd8f1776daa4aa9df89f142414d40f5676f7b97bc8370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002d5b89a4707f51717893785ccc02875837ce31f701bfa352334058bda856c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:17:47 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:17:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 02:17:47 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 02:17:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c72d0fa0f448323831012892fcfa3fcab666bcfd3f5dffde9845c3fcff1a5c`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 11.1 MB (11103538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f9437b17831a4574865078d6d6f2735530dd5df4d98bdf4cf80ecbe1eacb9f`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a07c90585c91a04ece397b0b7c2aa7103ad950e701ca4fbc90e9031dc945452`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9e0d3d2c3d046339e5eafeda28eb07678ebf29523f1cc7311ca0f4366b5a69`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 101.4 KB (101428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:11f07afbbbe928a378281a2e4e9aa71232f720ed8c10015d2a68898a8f42f783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ac64d62683665c45e0891c0b9483a646131f67f43e3d7c13640436e90407b`

```dockerfile
```

-	Layers:
	-	`sha256:8c4be9b8444a505246705c3f67d140f0953839be0a6106ab4b93c9696fb8f504`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:610c4abfd3a816fbc742987c537a656800f8939c7bf19bab75263e3fa00aec50`  
		Last Modified: Wed, 22 Apr 2026 02:17:57 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1506b5eb3c91ddfabe3ce15c625abcf4f6b173160124ef880aeb1fe3f8922178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb07d0a1c67220cf5e80417b476a42f6ebd083909935aebcc88121647cad5635`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:46:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:26 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:26 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:29 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ed6df39abc7d594f94814fc149a6d12ce8e09d24460ec736a00c100e19ffdf`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 11.1 MB (11109727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec667baba589573605c133826701cab34d84f096e1e91fa94e543e149924f91`  
		Last Modified: Wed, 22 Apr 2026 01:46:36 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1013b0e0636c96189cadc6bf6decbba384ac6e9ed98ff455d06ba7bfec473993`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e5cd02b66d7b76cdc68bc6d1df382e683332c7cb55b4e15f19e3d0dced161c`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 101.3 KB (101300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:54754071df71e040c8597ffaf6d760fe6be1cf9654e900cb74e49b322c7ae893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa89b23b03758493f1a04f87e158c59b1ef50d412362639d02e2b68e3fcea16`

```dockerfile
```

-	Layers:
	-	`sha256:4b8233d3d9b8a4e9a9923daab5c738a9ffa0a8add3097ab0455b285fd73cbe69`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39277cbd5fc62794898776a591fe1fc0bbfa2a1d5de76eb732de8469593fc4a9`  
		Last Modified: Wed, 22 Apr 2026 01:46:37 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:17793f7beceb2301200093eaa872899b8f20ead35b93dbedfd981183f89f29fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66308360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6cbef88dc1871fd829472d420d8aa6a5b9e2025757991eb9a1fb169244756c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 02:16:12 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:16:13 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 07 Apr 2026 02:16:13 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 07 Apr 2026 02:16:16 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:17c3ebdef14b8265937ec7a01f6bd551a86fc0903b2144405f77b14942f88fac`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 54.7 MB (54702589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f876b1db5bb9c9255bea19ae18fde9747fdb0c02be464e9379fa51c73d2f5f`  
		Last Modified: Tue, 07 Apr 2026 02:16:24 GMT  
		Size: 11.5 MB (11502348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5368ac9a74843c95e70f77bbacac35d2162ffd6aacf13ada3d871c8775775d8`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d920dbb8d782826431dc24219d719874db195b5c3204623b900bed68910d5`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f782acd2f323b11fe0ded7a1fcb099c41b8d25183157922c41891127243c5875`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 101.3 KB (101265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:18247538bfd3db99a32a3758e7d03994c39a2e2ef1595d508fa2dba7ac77fb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302c2b4c9cf24812a3a1862a60bc8b7b80e60f7881845d9fc04d388753327acb`

```dockerfile
```

-	Layers:
	-	`sha256:e04f46240354956e7214563f94cd809be7295aa5e1d169c9b958b714fec79ab8`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fb8255945b9e668090fa3ec96598e2849651c55338c00303b5b49d1bbeedd94`  
		Last Modified: Tue, 07 Apr 2026 02:16:23 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json
