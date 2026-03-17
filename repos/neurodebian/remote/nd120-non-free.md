## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:d85a1c76c4f664ed04bbac437e25e0737e0885dc7e8c920fdaa2d885be3797b8
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
$ docker pull neurodebian@sha256:e20510eb85a49c92b795fab0d13a6d603c8409302a5c27850e354e4ee2d075ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59858026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da05d84add778f43b34c90e4eb213783d2c3b318a820b3ff886321cb4dd4d113`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:37 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:37 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb4ab961a252192c5be9e8c63671378611d52d0f34724109f6e629836bc53d7`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 11.3 MB (11273414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71cb2ca05722ac51a62f208f0db98f75733c1869a7b970b3d6e9728e6d7b6c0`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d5d1fe0dac7a522ec964bbd579a3b0357f6eec985f44cd5636d3c0cab7e7fb`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017d0fc0f54797bd2aba2050d3afe8b77d26b55aabfacd01a99312e7df2ff432`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 93.4 KB (93408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9358e6a3e29c05f7244211073d6120f0badb79b3c9ee205e705a6704a50bd`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:52993ddeb92f56ec85fbb569cd9eea5ff7b06d4150243ca04ac399dda36744d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4091907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d343663e9c398ee23f9a095c3bed5c1214d4b233d609fce3cb69d63b1f1a0544`

```dockerfile
```

-	Layers:
	-	`sha256:98001a2072223ab569f56d119e4012edfe4488e5826deab8f16af1e0ab31d25a`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 4.1 MB (4075915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26aeea9927fc53e73b9dd0087688c3a82279f1407cc38f5e5730e4d86255f5ab`  
		Last Modified: Mon, 16 Mar 2026 22:44:51 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:3679b10ad0265c286fe8cc7068ca88e407f282182e8032cf327db1187caa55f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688b188efc48999b9fb300c96d92b1a18961afdae960c7c4b544fb15dba1dbf1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:46:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d8b009f63f40fabbf62b60a8f36907161db1ec174f241c48c828d1146a4198`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 11.3 MB (11252967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efa4181c0f41640b93236856c6e171cd14af6ead409446252a8729f96de12c7`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7170d9480708eb8e65c37d81ebd0f0f0249ca85f420c027bf87f22d36f7972f9`  
		Last Modified: Mon, 16 Mar 2026 22:46:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f754ac6996f3755689ea24ef32042440f61bc620c7b4baca1b94aaa4e11daffb`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 93.5 KB (93550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a25894cc7c550827691f700d1c89634d25ff883e8732d06f5e611905a3820e`  
		Last Modified: Mon, 16 Mar 2026 22:46:55 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:711a3828e487b3c898c3848819d398337511b76fd48c38eb53bfebdc59e34b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6484e97b3ad88ab4b5e77b3cd1d740588372cb67df2e30ff6d0a402da4360dc8`

```dockerfile
```

-	Layers:
	-	`sha256:ba413f86b373ddcb50bf9e59ba53cd49381e972f4184a6ac602ae96f7302b323`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 4.1 MB (4076157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05392ad75b16bd0e7a41bd30945205e4723b6d7f97b7c4ac41f80c24eedc9bb4`  
		Last Modified: Mon, 16 Mar 2026 22:46:54 GMT  
		Size: 16.1 KB (16131 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:784656544058292447b93e94fa60875fee7b4f9d332636b5c325ad7b8c8e838f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61266629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5a6e6d20a87459719fe2aa819e14feff590478d329837eb64e7e969c3a448a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:44:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:43 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:46 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:46 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:400234fd447028a685a307ac0360522f0cd83d85515ddb6a2bf38049ebfe1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:35 GMT  
		Size: 49.5 MB (49477654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c6743caba6d50541b062d9790addb6ecce85a4c2baeceea8f6548dc7cacbc1`  
		Last Modified: Mon, 16 Mar 2026 22:44:54 GMT  
		Size: 11.7 MB (11692936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76faf673c44e016ad78b4539dddd5832ff382ef7c8ce58fdd6ab08fb13188900`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e040d877e32d0e2211999898375fd545e15f72c45209a01e4336d4c8131700`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a633250fedc942f435168aab78b16d80bfbb5c995601098e8f5599d585a48d`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 93.4 KB (93419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e72f4af573ef43d21fac89dfbe526a4e2d98e7c1e3e7ed7857cb6aaaf4d344e0`  
		Last Modified: Mon, 16 Mar 2026 22:44:54 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d085ce204c95503a0a63907fcf810118c90ab52f1f3da4eaa97ed45beb8831ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd4cd459241aca69da0575888e08971d2480f995c6f985d07e6fc75b137fa0`

```dockerfile
```

-	Layers:
	-	`sha256:0099bc1cd9bd0c2a571c2c804a366023fb81ddbb6913a77746c1820ba406a749`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 4.1 MB (4073882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8ef2b64859296ee30fb161693c2082ad9ac5309e7e3b6bf80cd58b6a83f211e`  
		Last Modified: Mon, 16 Mar 2026 22:44:53 GMT  
		Size: 16.0 KB (15962 bytes)  
		MIME: application/vnd.in-toto+json
