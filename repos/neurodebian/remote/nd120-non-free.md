## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:68087a05a6a7fb01e26f490193b166ef26f3b943d68e912500b8b5a34622fb73
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
$ docker pull neurodebian@sha256:2c4cb4e49d32e0800ccab1b383c4df2c0507d6232aa910100bacae012ccc80be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59857959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a98c800a04fa92beeebb45cece13dc9a5a2bb2afacd3fe6b49a6af4c345f54a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:44:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5c6f68a47f6aafe93c229c3fa17bd8f9eca8dbcb82026f265892037a7e7ca8`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 11.3 MB (11273308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d79daf0cf6757e31a1107175cd1e7462256549e1d3d30fcce502bd6b523440`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acd65166e3ebd350cc72a3012913c626286396db1340b7ea63e94bf18f645be`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddccad9b7d786b644e59a626a14638210a2ea9aff44f74ec61dbf6eee0101215`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 93.4 KB (93400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e4d2762c39b83ebeb647c5d5a01a7535bb73003d5cfdc730cbd58dda43cb37`  
		Last Modified: Wed, 22 Apr 2026 01:44:17 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a894ea750272941947bceba5b021cb9f1323c9effce5f027b01b101eaf12b7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7391f965c78c1414439c34110a9ddf1fc2954c0ab321306169ec35348f65b3b`

```dockerfile
```

-	Layers:
	-	`sha256:438e2af1d3add7733f1e2b743bd1418519d72549264d12b537bed012abfeec97`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebde2f39b24d1676597cba7a414b48ddb0418b77cd09adc479774d0c97715acd`  
		Last Modified: Wed, 22 Apr 2026 01:44:16 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9d1120aaac014085ce56a331d7ea575340d210fa6cf6bb93d8dd48b01bde2707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4aa0f2d93ab5a0ef749e44b75fe66d1d98716e61a59f33ec6b37262e1eaf99b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:46:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:49 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:51 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1419a29641a382bd5d008c79413b7a0d7f982afcc54d158356ebf834d777985f`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 11.3 MB (11252881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c3250ae94100eccecd5ddde9d4ffa62ee2b825e07429f002e2df72bb84619`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6291e28edd6e8f08470374ec8879c087c0fb691bf9c8dcec73c4a7d89a442520`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511dcf0a8a93bc3c8c53587e7a674accd45ee7dc685cc3c31336ef424251476`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 93.5 KB (93514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89100960aea92e7ee71badc7ca255d4f2c6989d01f183b99c05d15a3f884e142`  
		Last Modified: Wed, 22 Apr 2026 01:47:00 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:65027bce3976a61075bd0f1ac2612aaebeb740f1f6f36c9db5340623ae6d2736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be843c3b23cb464a4fb68f900a751c67e0bddb7d266bee20b02a577d9d7f918f`

```dockerfile
```

-	Layers:
	-	`sha256:6ee6b5b3e6a0e40998662f831430bde4d01243d416c3eaba5e287204740ac7e7`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca90bb44921d010c885d204cb6665ada1449816de5bd1a1732874889f0de829`  
		Last Modified: Wed, 22 Apr 2026 01:46:59 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:520ee5a44ddfe1fdc8c29908c80cd33fa4b80e61e0a6a7fea2236f8acf57e63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39b44109263a95adccf888e8d1877cb1c7e34ee47ad75e1bb7a63abc65c9a72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:53 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:54 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:54 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:43:57 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:57 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:1f607c56991d572a9c9e62692330777522b959fe17a14367be35d12959214fa4`  
		Last Modified: Wed, 22 Apr 2026 00:16:17 GMT  
		Size: 49.5 MB (49477718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c950f45f1a3bfc61a9c1480c4ea9fde2a03316cd953138ce00699c9f7a3b045b`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 11.7 MB (11692996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06407c79badd50171efc07c97a8e73ce7ea48d39d2677a386a47b60804ab9c00`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed8f9d4838a2b0037c69af61b838c7a681ec221f106d08be8c0d589f82cefc8`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b48decc6dfccfbac4be598308637f9bd32f75d105fe1a9e2d50ddaad525978f`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 93.4 KB (93406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d828cfd13f00eab171bc955be08af42ecb017a4fc01a54804cf008f7b9c0a95b`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:12a5b425515756459b282bc12e754da5d18f9654f7f594d3ab5fa131fccddcd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d688f4c176cb5073364ce52b334f75aeb3cacd7da06b77e3e2e68fa02a1b7b99`

```dockerfile
```

-	Layers:
	-	`sha256:7f4fa81df859d5217bb07cfb2ca3a6026136a42f1b4d5beb2b7d4ee8d75117c8`  
		Last Modified: Wed, 22 Apr 2026 01:44:05 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be869ef59e935c1c52547a4769be7bb9ba422296f6d77f409abddf7bf2567ce`  
		Last Modified: Wed, 22 Apr 2026 01:44:04 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
