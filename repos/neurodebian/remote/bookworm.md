## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:df5704712e89286ed529ff4d47cee89766d3bb8980a44a083873ba28fc874572
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
$ docker pull neurodebian@sha256:c57b2f6a3d83e008a8374833294d64d7ea020d3897f07d9f96a317dc6fd4991a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59666969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4bbfb7b8a510cd8c1e4a88806bae413f872423387041274881d9013419584c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5c2d6b1d7d5d28d02e2f2cac517a8cdde90e21e5a6e67277ee7cfaad9cb254`  
		Last Modified: Wed, 11 Jun 2025 12:09:03 GMT  
		Size: 11.2 MB (11232526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:765bba7a7ecb589546d86353bd0d94577c74fca3b7a96a17b6372db8a4d46d17`  
		Last Modified: Wed, 11 Jun 2025 03:35:42 GMT  
		Size: 1.9 KB (1903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bea4e39b1faf52aa6e75eed7c4e67851e88e15f1bad433741dee64f21654ac`  
		Last Modified: Wed, 11 Jun 2025 03:35:46 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571ff130ee2030768ccbdde40e0b0cc38a55d68706e2e115ed72ce1951bcdbe8`  
		Last Modified: Wed, 11 Jun 2025 03:35:49 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4679137c067a99ee683dafb2ae9637e8d984373475ba2b9a1e53a0348dc51f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4551441a3b710c67f67d9cc1bbb001da8d9eae63a4fd372983e21d1130db4563`

```dockerfile
```

-	Layers:
	-	`sha256:07e4af5e11e836ec2abd0aadb072181bddbbfb39c26ca8b3637d8dbf44a467a5`  
		Last Modified: Wed, 11 Jun 2025 07:07:22 GMT  
		Size: 4.1 MB (4069025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c617b20fd66a64f64960a9acd7ef713f9b71c70e48a8da4d309e9a240261359b`  
		Last Modified: Wed, 11 Jun 2025 07:07:22 GMT  
		Size: 14.5 KB (14453 bytes)  
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
