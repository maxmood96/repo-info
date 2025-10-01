## `neurodebian:trixie-non-free`

```console
$ docker pull neurodebian@sha256:0d9a4c13d4e7371ad64078f0d671c6383a8f7afdadf6df21e6ea836acc999891
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:2503ccc01a731af5b2d3d92f7327d9e31bbcb1011139a72879f223a379d18068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59667538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b4b50aa0579a74bdcbb49a498d7315d494e61327bc54deff97aae76e3b57c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f805df92352cae0a0a2836745a1bb53b364d8cccb0a97b47b625e0dde43f3f`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 10.3 MB (10289390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc43eb24082631f3aec7eb229fe3fb1fd1008d98e03bfbd5a612e46b23ba1e2`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f3328b63a48e14a4f9831671d91841324f4446ffc7c53aba7cd267daa4b4f80`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b20b675e05429ab3c15103ae9009614f1f3725ae5cbad4733ca582901965b1`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 90.2 KB (90174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daee8250ea7ba96eac71bc0e2a8bbd64222f6a94bb432c8cd8623a6760f3002`  
		Last Modified: Tue, 30 Sep 2025 00:16:33 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52e009a03c07d287b8712a89275cf62d910e6f735fb37cc5e7bab8beef1bbe66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a745821a65d66b1aa0f33a69d19c1824d420dbebf69bdce4aa51155bb295fc`

```dockerfile
```

-	Layers:
	-	`sha256:458676c72d3376b2e2adc40b027530e16649d7cef3dce4f466fa9eafc5e2602b`  
		Last Modified: Tue, 30 Sep 2025 22:08:44 GMT  
		Size: 3.6 MB (3613021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d73401dfdc2638617c66e6f3c897b4abcb9fd9d44e04be80396ce82befadec0`  
		Last Modified: Tue, 30 Sep 2025 22:08:45 GMT  
		Size: 16.3 KB (16325 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bb8a1f91ca3dda2b54c613358a3f2f2945bfc5deaafc4eeadb6eae89d044f6c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8008367a8e867e3902e67f9754a14d41e1c86f389a5a7ecb27933aff25207f1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f827ec068a53d186059453e246d57e837a733af80e5e8a439634aaa8010cbc48`  
		Last Modified: Tue, 30 Sep 2025 00:19:31 GMT  
		Size: 10.1 MB (10073018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f2c0c542f12345a7b0b7332a3c30fbef3e0f06cb41dab53840a4e12b39a669`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb99ddf347a9b9633f0d8033fe5a42e37880b4b2ddaf4bda2922f2c4bc504a8`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7514b6a6ce06d47e1c9a211e6c9baac0edbdef4aa535d618f6415f0fbe994a`  
		Last Modified: Tue, 30 Sep 2025 00:19:31 GMT  
		Size: 90.8 KB (90837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a6f3450e33d6d3354fde8b80a122a9643f6244d174f78222de5bd8feb1a930`  
		Last Modified: Tue, 30 Sep 2025 00:19:30 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f0d1fa2842c899d239f59156bb06dcb2aa6b4017485f5d1418867ab3b772ea22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3631025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc74683096734fe8a7282c0c86a4b90695de4208566bde26b768822394849ba`

```dockerfile
```

-	Layers:
	-	`sha256:8358e4867b6f7d30ccde76e14fd6bc289cb71cee56a711c57179f8b40eda4b1c`  
		Last Modified: Wed, 01 Oct 2025 13:08:20 GMT  
		Size: 3.6 MB (3614548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7daca65ee14aa6ed1264b3293452c903db18d8777d168fdec82a6219fa454ed`  
		Last Modified: Wed, 01 Oct 2025 13:08:20 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6f5f51db0117943740d24d6272ede6d385cf0de736a0a87db476f1cd373ac423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28287d3132e454889d0cb4278309fdd1c117e4946ce49dd56a41083c2539181e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b43fce213f96af9285577072bd9752768a9c65a727ec564297271c4fb3dd675`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 10.5 MB (10462626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e2e09d36685cd8530477135a922a156ccc8bfdf81e79a088f5c4b6bae27c7a`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77747ec32ef9084e7a31f53e4895625940080c905fe34a4b4a1518a05da0be5c`  
		Last Modified: Tue, 30 Sep 2025 00:23:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe8cd32135ae5186a68422d3154e344abce87331d1c80a54f49c008cafa3754`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 90.5 KB (90540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ade42626c18876d4e066d0491d60ce433a6f3f35060ac999555d4904dbba5`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2e53fda5ed32d4582af0d59a52f6053c693f45de5a8593022784d862534f1272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff141d466be7fd3841ab7f3fdd7191cb53a6b2c3df26fa213fd731f4e39ea16`

```dockerfile
```

-	Layers:
	-	`sha256:fac33ea0fa1e517ae03eda600bab1c7ec5b8189b09fe01c651a4f7d35b69e1cd`  
		Last Modified: Tue, 30 Sep 2025 16:08:40 GMT  
		Size: 3.6 MB (3610970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39422b45dea80b7340f8112c3c76282ecdcfd55ec0cbdbbdbf5570d78a2d4128`  
		Last Modified: Tue, 30 Sep 2025 16:08:41 GMT  
		Size: 16.3 KB (16290 bytes)  
		MIME: application/vnd.in-toto+json
