## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:02e3b5f3334d51d17c907a109e7baa23a3b6f1efece977e6da220de111919d13
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
$ docker pull neurodebian@sha256:6550c17ae669fe37d08f6078e565a0004d60abe45a2e91105aade65b3fce087b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36183da1e19d84de51ea5809e4159ec8f2107f0b70c8aa80d638baf6b273f130`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1995213564325caf7e52ecd95fe4435c70b03eb94c674ac15706733986b86e0`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 48.5 MB (48494284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e2dba99e5ec29a2897821803f9b24d793a027db51662af3afc8e9f66300421`  
		Last Modified: Tue, 01 Jul 2025 02:28:14 GMT  
		Size: 11.3 MB (11266786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6474565e4f85706c018a8fe448db75bd10446e9317453d680ca2088c90aea693`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 1.9 KB (1898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f48f7bf9a7cf900ab4406a612326c755655184ad87bad410ad08c3644c5491`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4256c9ee1313cf8432071147cfcaf1cf34aaef18083c431134d0d76c1021199b`  
		Last Modified: Tue, 01 Jul 2025 02:28:13 GMT  
		Size: 93.2 KB (93176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b76cb89bd6c797b23f22af82a03567398b178f8a733f169ee5a6cec048223fdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1028bf429c8a434cfa52f7718ced06affeccb0f6f0ec420c0c49d49066ba2c7`

```dockerfile
```

-	Layers:
	-	`sha256:a3239e8e531bb9eb3cbe8ed2e8c93b3bd84ae65295907e1792c4f5348fc26c85`  
		Last Modified: Tue, 01 Jul 2025 04:07:22 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f65a7d9bcec73f81f3d1625604e9081d8bacab46d57a5cccdf9bfe6f6da0b253`  
		Last Modified: Tue, 01 Jul 2025 04:07:23 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:684d5cf2924c0259869782c86482e0fad6a5cf03947551803433f7d28e0af651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59666965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87e615e57fccd37453ac26b2cf379e4ef9a19c09e78f62dc0a56534e920e6be2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f8ab7c4e8b4178f5f2504f6c4b199268151b1fc958cd53bb861d8dbd9faa8c3`  
		Last Modified: Tue, 01 Jul 2025 01:15:08 GMT  
		Size: 48.3 MB (48338785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89c5ba0efb742f26073ffd659a0388e8baf4bccb00e0d04d7b62e987a7790b2`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 11.2 MB (11232604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41477640941442aae5cee7da6735533b9fe3c5ae829c182a1a4b004a0d710e3`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f06fb7079001d13f92762cd5d30daf1c2f43d5f2d45c1f3f82a2a6396bd423f`  
		Last Modified: Tue, 01 Jul 2025 07:24:58 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd28da870c451d725c581a4bff03979bc5383a096e98e9df515d7ba8fb18c9`  
		Last Modified: Tue, 01 Jul 2025 07:24:59 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:98fc1096707aaf619c5bfd33109b22792b8f87cd0bcc58f78e99394d81bf6fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc34afb187651d95ce2ba9a89f16cca65216bf75fa5f2248be8ea5da18f69d4`

```dockerfile
```

-	Layers:
	-	`sha256:89c172bb4e8c24d867bdcf4bfa287c23da7328d77dbc4267ca164801af5342a5`  
		Last Modified: Tue, 01 Jul 2025 10:07:25 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837eb9afd4946b426cc90a905471476d56c51c3b1a5cda9841af37d7fa68cd08`  
		Last Modified: Tue, 01 Jul 2025 10:07:26 GMT  
		Size: 14.5 KB (14452 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:1eab43ffdf27740a4ff6b9871deef4219fc4477e411d7be25d4b22de0d34a9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61261707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8650137fe780d20c2a45a526a978891d45957513364b3407b3a98fce03e70848`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bookworm main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d91f5c279884c41d79cef474ce847b4a02b3539da5109ddb7c291583cfde223`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 11.7 MB (11688896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a27a41894bbfef54041fa4e2ad7a252456c0ea1aee79ba4868f486ddd4f297`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7938ada2d8cfb84599f71f893924e2223be3bd87eadf4d295c40802ed52d3bd6`  
		Last Modified: Tue, 01 Jul 2025 02:25:39 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba7d51bfc7e68a98654699faa6f64431b601c24cbfa96d28e9ddcfa34d67711`  
		Last Modified: Tue, 01 Jul 2025 02:25:40 GMT  
		Size: 93.2 KB (93218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:63b480a21b477fe6d50a7671f7e045fc812577457017b47afab4ac347120b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b42d2a8c7ccbc53dbf7ae36193dd021faa7764f233843b193f035ea43d73d5b`

```dockerfile
```

-	Layers:
	-	`sha256:286cf155bcb80c002a3636d3de56638554a5e2c1bb711b9a7d3f0b855c66ea2f`  
		Last Modified: Tue, 01 Jul 2025 04:07:33 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7327e91c792401ea5471f2c310b5640c40f44a4db82b5d3772b321fda5c46a`  
		Last Modified: Tue, 01 Jul 2025 04:07:34 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json
