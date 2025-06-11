## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:91d03c12c24727945c18a1d0698d199518d9e0dc379cae634172bb617cbc1e81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:51870411e6cfb59409d593f72a2355e59ace517258dd08dcca5fc19b04e12f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59856403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e74521593afa5574af921754ef044568d01babe316919d0227ce0ee2ef2ab3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfbc9b299160c1db312e7b95d297e3a72795f0e0cd3629f99ec0b5d5074f482`  
		Last Modified: Wed, 11 Jun 2025 01:26:55 GMT  
		Size: 11.3 MB (11266798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b92ffb97d1ab74a8c03abd5bf067a7db8b6a98535222d4198d2aedd42e704`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 1.9 KB (1902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9905efb8849d4ad84769703bb6462b7fca532c145a9f3a617ccae66f5cd8178`  
		Last Modified: Wed, 11 Jun 2025 00:04:22 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c5bccddef1ea7c90a3f83a629491790fd61738f12e0b059ffe29fed6947dca`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d7302e39b4a84ec236cc63f200ce5cd12b25857b6860d8aa9b4f2c630839d6f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac74c06d4f5af96295d348e5b88a26551309b48c3fd3aef828768699b17b3778`

```dockerfile
```

-	Layers:
	-	`sha256:330ba10e15b4eb2d882fe878e073c41b4621dba90fcb4a15242608a79e5a0d55`  
		Last Modified: Wed, 11 Jun 2025 01:07:21 GMT  
		Size: 4.1 MB (4068771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57969539b0d4a6d56f45d33a21186e47a269fe3eda38459de47c1bec3c4b99e2`  
		Last Modified: Wed, 11 Jun 2025 01:07:22 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

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
		Last Modified: Wed, 11 Jun 2025 03:31:13 GMT  
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

### `neurodebian:latest` - unknown; unknown

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

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:aed52e4c3cf784e520efd607e8de956432f1649765ad50445d121a3edc376564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61261796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49497c214bc44fcc564f62c485f1aa0ebfc134858d7316f94b89ac733c9191a2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cec3206abae9af7504c3ecc6fc1d7ad93234636734cfd15d6641ce1fd2ef19`  
		Last Modified: Tue, 10 Jun 2025 23:36:46 GMT  
		Size: 11.7 MB (11688919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9367740ef16aaa69f189736ee3e947d62834ff67146519987e1bcbb86e6eef45`  
		Last Modified: Tue, 10 Jun 2025 23:36:41 GMT  
		Size: 1.9 KB (1899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a82ec3d2e8e2d3698f3fd68d39a22f2192cc781a4413841252b837f3c5c52`  
		Last Modified: Tue, 10 Jun 2025 23:36:41 GMT  
		Size: 272.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3adf80d23972c5a2315ba281040ac8889bc1cb52b4052b7d3533d1941ee436a`  
		Last Modified: Tue, 10 Jun 2025 23:36:42 GMT  
		Size: 93.2 KB (93232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:16ecefc0b3d1030c4e5e61a12393de7a5d30cd21667f71b9a8c0c1c8db03acc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4081022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3d9b8214b88c9677b119d3d04eb71b7b2042ef0890334ab265f462ec690e20`

```dockerfile
```

-	Layers:
	-	`sha256:a0a953cc95bb74bbc501c537cde161432dba83f9bc9fdf30642cbbff4589ccdf`  
		Last Modified: Wed, 11 Jun 2025 01:07:34 GMT  
		Size: 4.1 MB (4066739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b54b0972fbc6c4a305521a5c2070dba0fd26c33d2cd58ea932189117f34493c3`  
		Last Modified: Wed, 11 Jun 2025 01:07:35 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json
