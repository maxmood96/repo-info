## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:c9e446fe77a5f4b1edeb17c325a74e4030d3fda4ca2982fef4a1c64127bc36f0
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
$ docker pull neurodebian@sha256:ef8358828e792416074f063df036d264266a907209af1b61b671255996634e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64964793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f1bf797a7a382ce7d0a660da43e6277ca9e7b7e1bb2d7ca77cca82320b9c15`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b6f830cd306f01980373f1e0120f2d00018fbe51a9506b7262f5d9e4bbda74f9`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 53.8 MB (53756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8316c89f4f0a7409a24d7f7d25255773ca831765776c5cdaf2019bd226bed583`  
		Last Modified: Tue, 21 Oct 2025 01:47:25 GMT  
		Size: 11.1 MB (11105102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf39199172dcb55cac1f868727f84f159b960857d951e4197e99947dae9ec08`  
		Last Modified: Tue, 21 Oct 2025 01:47:24 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f77eb06813bbcc75d2037c39a42087604c670cf1432df1d5d1383d08c5d4c6`  
		Last Modified: Tue, 21 Oct 2025 01:47:24 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2442abcf0dc7c9180a53edf89d4126d36a788a09f57b139b9a610c005de847`  
		Last Modified: Tue, 21 Oct 2025 01:47:24 GMT  
		Size: 101.4 KB (101421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:094de7440ceaabc3e38bcc48ac140a751180ecc8de575fc21480830f280e2d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82adc2621748ca37dd1fcd949b3c76e0d80e443a723ff69165c9c3c087c402ed`

```dockerfile
```

-	Layers:
	-	`sha256:827997d73d36a59ac083bc74f8f3b20b468a4fc42bac9e97dfd3eb0d1e7c5e48`  
		Last Modified: Tue, 21 Oct 2025 10:07:46 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7097e0cfb3688c168c65128de6f56077381f45a4629e589157d01907fd06c6a`  
		Last Modified: Tue, 21 Oct 2025 10:07:47 GMT  
		Size: 14.0 KB (14008 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:efa3452804e9587f5722568e6ef29abd1e23f0d1cdc585a1a83cf098a40887e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231413620ed5b6136e902902a07b95f4db387daaea76efd1fad29c6e265c603a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a72c4e347b74aa6a0086cf3d1d928528ab02577a17bff4e22366a7df681f564`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 52.3 MB (52257444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f0e0b7ecd33bcdacb8ecbf9c10cab8490fdb1c156de83a37c8fbfbdea01287`  
		Last Modified: Tue, 21 Oct 2025 01:52:17 GMT  
		Size: 11.1 MB (11105996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d29d7c791e73927623a94053de9a0570ee62aa007a4d08a409a06283062c8bd`  
		Last Modified: Tue, 21 Oct 2025 01:52:16 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba5fd6cb7eb6d8abd869b775589288e900cfceb9c4eacf0c3d466bd722811f`  
		Last Modified: Tue, 21 Oct 2025 01:52:16 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b62921de093a8c4019930b9ea0141277176701b041e82f48b2a2b04334ea2e0`  
		Last Modified: Tue, 21 Oct 2025 01:52:16 GMT  
		Size: 101.1 KB (101119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d93c7112ad90e301996de6e35770b84c07e37def67c76bab4062f4c9a84c5065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0930242fa92b5c369d4c2d4032bd5b9fb4ff3fecfec9e5140417cb1a5bf08bc`

```dockerfile
```

-	Layers:
	-	`sha256:faec4fe93a5935c8df733e0bc6acd4d02c1ccbd329f75d6b4917f8d2d9a00162`  
		Last Modified: Tue, 21 Oct 2025 10:07:52 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66882d1bb43dda49072e5042986cadfadf4d8b7e07f9876d258463a3cdfb9fa7`  
		Last Modified: Tue, 21 Oct 2025 10:07:52 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:38eb5ee4e668fbbdef525dd25dcbe9bc0de045ce8dbbddcb5e09eed0f61884f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3628d1828d0f455ebfbd89e90f7d06d5910c071cbd71bad55b567064d0312449`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10d430deaa3d2ab4898db053e80d62403503897839bf6efd17ed5412b18d7973`  
		Last Modified: Tue, 21 Oct 2025 00:20:39 GMT  
		Size: 54.7 MB (54699294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bafb03c492417d745fe9148c731122a53e1f35f9af2e8df8bf69ac48cb9b43`  
		Last Modified: Tue, 21 Oct 2025 01:54:45 GMT  
		Size: 11.5 MB (11500372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73ed3fa36e6e8124959f4c297f50987f6f26142fd6ec0135d10cbdf5dc86fed`  
		Last Modified: Tue, 21 Oct 2025 01:54:45 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87760869e26f5be49f48136d1baaad65f589b757cbb756f3f51cfbd8230252`  
		Last Modified: Tue, 21 Oct 2025 01:54:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9f7cbbfd83d93b1c49793a29f52b7346dfdf69670d3f245e2fe6578048aeed`  
		Last Modified: Tue, 21 Oct 2025 01:54:45 GMT  
		Size: 101.3 KB (101268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:951e697bd736658cba1a98afffb154fb17378d6a5eccbc7fed7a26758327d1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8bdf91e3fff18cc1b6ceb4bbaec5c0012dca48a9eb492c45565e93992e0cff`

```dockerfile
```

-	Layers:
	-	`sha256:95cc7fcddb91205cfdc7f1b7b0d366d03c072911cdebfb55516c875cebfbf7dd`  
		Last Modified: Tue, 21 Oct 2025 10:07:57 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8c33457908ff99ae075793d0f2074318e9dc6b1f96e12527dd2522f8911452e`  
		Last Modified: Tue, 21 Oct 2025 10:07:58 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json
