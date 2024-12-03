## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:81f633276b9be30fa1dd00b0723598ca82c4071e30da9746fc744a70d1d430fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:f0b826db0485d7e82be034c6c5e7edf87df12d265d6677d054029eca4e93eb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7686c9b19aef29cd8dbd901aef411bfa8220e559879f8633d2b8abd2cc429f7f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3cc0f98744a051a1a5f2afd9efb44ebed4fa17eb3c1dddb60d9c9400c80ab2`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 11.3 MB (11266780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ba287ed08d01881207dca39c00528deb3fdc3f2d81914037be7b1cfdbe874d`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150a6037915fb13285e5895a6a1c62c6afc1704844f3fba6208d25301de77e56`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8683715aebd7fa532f695293a9e651f0864ce67665530642a85014fd00d60f96`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 93.2 KB (93152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9738867365afce7f70b32c401344176aad5e654c99fb07a9333af858e584b4e9`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5ea80b90c3a2e9c97601511fd1dc77bf211dee1d51e558aa1fda464ca36368ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc33c8834e62878218057544094ea5fe3dd9746688832eccb7832c6c514dd2f1`

```dockerfile
```

-	Layers:
	-	`sha256:7bf28a7d462fb022e11d07e4097edcfda51808238332b04d7be6307f77970fb9`  
		Last Modified: Tue, 03 Dec 2024 02:31:50 GMT  
		Size: 3.9 MB (3937271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2408a1585fa162bca505495ed4028662a915c5800c5ec73c3024bf5a965ac6d9`  
		Last Modified: Tue, 03 Dec 2024 02:31:49 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8727cc1156f0afd9f41a4c982dec32a7669106b1396116e3bf6adae8aa7f4756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f52ed086311e71cb3ca17d2f26956adde08dc02a426a23d623a6b6b455dc26b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d6f082b94e725149735aff5f39abf2a5c1faa04f4f35829c2b04bcf36fdb0`  
		Last Modified: Tue, 03 Dec 2024 06:16:59 GMT  
		Size: 11.2 MB (11232475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7164374defb4bad306066d94c7dac571980f047bf262c550c04b585b492527`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1000d937bcfa52ee6cff54a54a79274765aab42bb61041dba4d40c8ea00a`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab49634abc6db7b16ad6e4f6d1bd12260c9a0555ba2d16c5abca22782e40f3`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfadfcf78518bb3680188a8aa8e9b4e03dd0606fff44a59bb7c8d5499eaf1b4`  
		Last Modified: Tue, 03 Dec 2024 06:17:11 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ff00f65b3308cbfe02001d7be3d5101574bcafc13cd2ed12fb2c5ea4a3f904a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88092ab67db4a2a365b3756e65b7129bc9d0f9970f46cee3556212d286bc0541`

```dockerfile
```

-	Layers:
	-	`sha256:5196f61854393e3f4bd1507046c2519f7c7085fc551d84440d34fc98c60437db`  
		Last Modified: Tue, 03 Dec 2024 06:17:11 GMT  
		Size: 3.9 MB (3937524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfdbf730785a3a5e3830386fbec8ccf928bede15706f942762a042e778e73df6`  
		Last Modified: Tue, 03 Dec 2024 06:17:10 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:8dc7482bab5a6e73520137dab2efc0ea2e1cc8fc7b00a55bed98c1f0f08d9b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c795e80457b17a40c2f0ba40bb9b3c56514d9bd56e840230b6cec3cf737c4acb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4351f3571feee02247d67c5362a4118390ace6f8c203163c4f98131c109f39`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 11.7 MB (11688949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47502da2499b6aa6bf2b0b61829d4882722d17064ba80d8bb48ea95f18de4d5d`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807895808115d1d32826306aed408a2b386e021fe7a1a16f92541a7466a2bc9`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ae4b46bcce38d9c1ec20a3d33ac2e841511ae54438cfaafe1d94b487dcc6b0`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 93.2 KB (93220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f86ac460bc7c2375830f2b95cf8a012950443b99acbd0fc9bfc962541710a1`  
		Last Modified: Tue, 03 Dec 2024 02:15:01 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ddd3208bdcab3b163d0e37e9f5c42ceb55651e14db8e8389f4adaa1ae19865fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a502d814818aeb638b6714649752b3a5f5ef284ca7087a822e7014812d9e26`

```dockerfile
```

-	Layers:
	-	`sha256:1d21298306b6c34fabffe2598c235ed691faa6d0a6279c00194aa06ecb984533`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 3.9 MB (3935188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ebb9243e1a48616e3d08d94ef366bbf4796762ab8c72db1e88b6d07afdce1d`  
		Last Modified: Tue, 03 Dec 2024 02:15:00 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
