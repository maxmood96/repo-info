## `neurodebian:bullseye-non-free`

```console
$ docker pull neurodebian@sha256:c1e8a9907c9692a2d8eb4d928f1aefec63938fbf94b7ca14a5ad9711a18a93a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:8f9ff1ebd5c472b4426d607cc07971c22e2bf5bad4d6d606de40b2d890e46a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64979065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd98d76f08c16ec4990e9f61a3ac3caa3ec79c409488e00695d7810dd59b477`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:53 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9981861713d98df05d7f547a36e5538556e8acbec7bd877edc0dd7993fe81863`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 11.1 MB (11103365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678a8c2c315d7c2004f34b79f34d5a5dd42c5e3280e38124979c08592da36437`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7faebae933191c95abaf487d33f1eb63b4d96868295eaa6b233e3646b5a6edf`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e33875f4ce4b42c4b83282de288a8b46dbc815d4c91b75fc67496c60cc50a9`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 101.4 KB (101385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4af7eabcef6f6d21f23d675c0f72d225daada2975c5707e1005847cfb81e26`  
		Last Modified: Thu, 11 Jun 2026 00:46:02 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:be4f972c9d26a3670c1eaa5c57cea6b5c2ec00f243e8e90eda928e119fb1b7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0740d9f0a724b025b94ec77233003ce1f313a1a044642fee83619469e38315c`

```dockerfile
```

-	Layers:
	-	`sha256:67725c13a7747a2a89253b7bef171a279d77536b72fefee7e6d066ca7f17e0b3`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 4.4 MB (4367954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c5f799e9aaa132fa1f8e59a2fcfbbaa3acee314b7dfeab533ccf376747870a`  
		Last Modified: Thu, 11 Jun 2026 00:46:01 GMT  
		Size: 16.0 KB (15992 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0f6973a526abfa5aa64033c68e2339dead9400d7d3583214eaf9b67dcfecd1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63477866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7fdafafad7f39ff6339fd0937d939fbe1254c6a002d4db291b5748f7d36015`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:47:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:24 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:25 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9b5af5e4a2d9cf379b3845400efaac90cfdcf08652cfb47e8eacd1b326cf38`  
		Last Modified: Thu, 11 Jun 2026 00:47:33 GMT  
		Size: 11.1 MB (11109924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118c21db13adf2a7275b56854f237f9a0ecb6087b823d8ae0b8b1c2fda19c649`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17306412c7fd596ae38e8a3f5953b14a9ab1ba0c1407f778b807e3dee8f7f02`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97341d516dcc446e4e57b1e6d23781a5287793340dbf15b385a694230a24473`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 101.3 KB (101279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bc0d75d6e94011362e701158a8fab375ced03d20c5bba23e88ede331f4bfe6`  
		Last Modified: Thu, 11 Jun 2026 00:47:34 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a55fea1517b08a1a7852b99d3e895beaa4de0646af1d53784b6bc3aaa442b60a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4383695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7933225ad3f8c35c6b1af8b493b8c89edae9c666c21e62d4cd3382ccd4d696ba`

```dockerfile
```

-	Layers:
	-	`sha256:22f1d97419c0a41b97eade5795164af3b34d7e54b1001df4f3298cd26f3b80cc`  
		Last Modified: Thu, 11 Jun 2026 00:47:33 GMT  
		Size: 4.4 MB (4367561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d3e96c9f17ea483f929a4f340951e4e6caddc8c891849704255c24b5ddd1bd`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6898e68eec990afef9e8e941ae475a6e6ba9a7c89d1569015326302fc85dcfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66318901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b96db0eb400856d9b433a74f7ea4a06d3bc9652109f52f9cae74de43474f6c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:42 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5431d75034b78174b62a23408161498c4408116fec0cfbafac129d42f0e94cfe`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 11.5 MB (11502228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c7da2715bd36e224998cfb7872b10d6ec78a79f0ff89b70efe80caa5d71fd5`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a37c05c9b88b6b246537e6834721e590a62a7b061add25adc0166d822938ac`  
		Last Modified: Thu, 11 Jun 2026 00:45:49 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbcc0a810f7dbc1da929c8af13f18de2d0e9a1fc46fd8e93e7c421885f6f78e`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 101.3 KB (101272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69c86e8eaf936891d2d5bd628df1f381fc68d3f61b41070615e12cead6ce08b`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:572913f9f8b3584a32002da1cd705b096a86166c536eeb2e5e6bc1a1b85673b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4380437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe8627f4038e578e722de05074c970b82764f21a2849a92d2c1129e91bcc9b5e`

```dockerfile
```

-	Layers:
	-	`sha256:38b0af99d61a4f4256208de3c94529a49ad3a3a726f68f0f188ff7e8b195e752`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 4.4 MB (4364473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2479089dbf204ece3399229ee5fa2b425ec9bb713e627746b2311062b5e6cb`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 16.0 KB (15964 bytes)  
		MIME: application/vnd.in-toto+json
