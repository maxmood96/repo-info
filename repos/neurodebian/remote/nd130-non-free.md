## `neurodebian:nd130-non-free`

```console
$ docker pull neurodebian@sha256:2158a62a0b10708aedda37492bde2d288292fb01bf748f974a3015ee8f269122
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd130-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:9b74c3202ff1d28a9bc492b31b8ea9e8c9b9be6b63bcb68e0aa15fe63e173047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59704925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733c6cc1679ff8846e1c2db00fdfa0a14c44d7830f4ddbc5241391dc645b802f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:46:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:46:11 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:46:14 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9443e90dd36b4d7df0ce4d2bd3a9f86ccde7df420c85200869452e1d2c310a3f`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 10.3 MB (10294066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b311040279a30f28e966f2a5f173993093cbd64887ef01d6e4aaa7d6c49715d4`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8afd3a0920f39400ad7fb5ad3a3d14689c9cc1c7252860a938da81870f71c5`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118da0436bfad5757b22eb7483dfb8d4caa8dce58fda3d5e745f38892404501a`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 90.4 KB (90387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaade245ece996568fb7645f92a893e7db0b8361b850a93fccfd2a9d94a7675c`  
		Last Modified: Thu, 11 Jun 2026 00:46:23 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:28e7c75fee510a7acd4fc200e0d667d9cfd91e9ab8cca5e946e378b1b1e4ec9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2eca42e82561b2771d46a87c47c776316b6e839cd802e995555cbfc8465b7`

```dockerfile
```

-	Layers:
	-	`sha256:36cd5b6c3434365f2cf71c0b9bd5700b02ac52aca67b173355b3f58bc1f7948c`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 3.6 MB (3614204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4b92efa6ac90e31135660a7259903bca1ded723e7162654d117bc591dd1faa`  
		Last Modified: Thu, 11 Jun 2026 00:46:22 GMT  
		Size: 16.3 KB (16282 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:4f735a295bf56114dc844067c8559b447376008a394f05dc7bfa19b3cedb5fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59851751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1fe4fe93d83961ba13a917f6bc125e566db9df7f299c05d3b878ae060062c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:48 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:52 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607d619e0dd73deeb9db2b25df205732643c98352d9d7155abdaa4c445585b7`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 10.1 MB (10079193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f03c6928c07168f2bf548e6930872e19baf37abc1cf0af526897654a7d8b4b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac685d980ae5b64951b7260afeea4aff7557f31fd69a01a970bbbb9446a664b`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0675ff08b6519b01acde1fd7cae45036ddd625bd1f8ad29726f13b0c2d8e9550`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 91.0 KB (91040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf2d6bd6dd274b0fc66d385da6ef377cbbf87c7b53b2ffd1d82140014e913c5`  
		Last Modified: Thu, 11 Jun 2026 00:48:01 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a992e0d49e73cfc21fa6db8235421e67f6a92ebdb3674d279e7dbbb82500f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472593d75487081cd96f86808b920d371d5794341e8330a5b48716f70fa189a6`

```dockerfile
```

-	Layers:
	-	`sha256:e942ca8eb7f884ac336651d2badfbba2ae0e1c3b2707ceb693a8dafcfed43268`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 3.6 MB (3615094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36a70c74b7bec526e65bb31fe6513941cd08cd11448342af81a777e368b4903c`  
		Last Modified: Thu, 11 Jun 2026 00:48:00 GMT  
		Size: 16.4 KB (16434 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd130-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:2a596ddb9229467c8474294e2e7fa84b37aca64758f2e82a66a7216074aef32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61391860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a3b151ea42db43a346e8d6b49db21ace20626081ed4e9127c0bdaaf47a98cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 19 May 2026 23:26:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 19 May 2026 23:26:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:26:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e6c7527b1ba130a7fd028db4b4f53fe2952922685a72d987e0bb45aba2d459`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 10.5 MB (10468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac79af1a4117eeb379989c2a6fa268003cbcc7d525c61702842e54d57e9dc65`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37824e2171f8bcb2f390052ce2fa9cb0f979c1030b16c7aab208f7ab72ec972`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b750bf144b8fe3a2951d8c7acd97d5afb0704bd216e92fa3a311ab128669845f`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 90.8 KB (90757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822259b6e0e53e9f7d48de30ad4a457448625709e9bdcb8900c1f585458a3b94`  
		Last Modified: Tue, 19 May 2026 23:26:54 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd130-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:571389a940bfcc86c5c176393870c94339e1c9c4addba68adca4fc69aeceb89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fe2f14ca78dbec2a02cb0190f6d6fa7ec0db597f47cd9517ec5e4f34f24303`

```dockerfile
```

-	Layers:
	-	`sha256:03d12e0fb081073377307046634158fe58b2600b735ce815ae52909707755842`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 3.6 MB (3612134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18610647bc1842a68384e807f0184ee9984e617990bc40de96da84e376d8d4e`  
		Last Modified: Tue, 19 May 2026 23:26:53 GMT  
		Size: 16.2 KB (16247 bytes)  
		MIME: application/vnd.in-toto+json
