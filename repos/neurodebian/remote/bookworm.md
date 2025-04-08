## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:e7653463330c9126ea1eec402d23989d49b28dea5be93237f2efcded4bc2ee75
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
$ docker pull neurodebian@sha256:a0dcbdd5d33f6b4ded90721e79214b48eb07fdfb81a611bf00f38b84d6732433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59852653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56702c61529f652e18e461b9d975da1b918fb642b0bcda7dc99adf61b3ca13c8`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51de7fc88f83bcd2ca272e9807479a820de15d4593a3dc968f48b4d1a264a15d`  
		Last Modified: Tue, 08 Apr 2025 01:26:18 GMT  
		Size: 11.3 MB (11266816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c97f36fd4e9a7f0a6099eee5422210349bcceb3ada17c5b6e372b193e1c53e`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9bb8e081d93848263d5c8ff20270983c16677528d3cb8280bff02ad12ab3c0`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738450aea5f8426606d81f919575dd5d096b41723b21d3907e88864249d8944b`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 93.1 KB (93122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3f958aa19a0cc84caf4443c0a5262b383f914a113a69501f1067faebeb388fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b65e7f8c4f9fe56144b3b34843001eef2fc8ab312552bdecda43286b373e72`

```dockerfile
```

-	Layers:
	-	`sha256:c9dcc5dde5954616e94ca09bc8d97aa97919cf2de5e71636e27304a17d7859f1`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 3.9 MB (3934172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8b0e321829f52c1752633cdb98a97311dfcf9f59962d259c9bd20835c9e0310`  
		Last Modified: Tue, 08 Apr 2025 01:26:17 GMT  
		Size: 14.3 KB (14316 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:316e85d6b21524cdbc0ad15080e717847fd5073eb7bb75d67349765ad063d86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59655700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60e8af420ec5da3048814d4cbb202aff23e79ea370511fbaf0b7b066ac993921`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce08a29378b322d580a290ac850ee07138f732ffb563fd5c9ced94337ecfadf`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 11.2 MB (11232654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c994ce850f986eb5546d5276357b320b7bde68728c6257f9f77b9539290f72`  
		Last Modified: Tue, 08 Apr 2025 06:36:08 GMT  
		Size: 1.9 KB (1901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c982b1954d94fe6ee8540f3d265491f3cf0dd395d3534a72e93c4fad36fbd9`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e1367d165818a29284a9956a4df5e0769d1e2307631fc56bb05d36b69ca141`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 93.4 KB (93402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29cce2b5a259f9c9f056e1510d143b2bafda8f596db6f9057a1b5f855d7450bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2d09196cebed934f4fefcd0203e85074211214122b021911166b08d731ee49`

```dockerfile
```

-	Layers:
	-	`sha256:f3e113528761941f55aee8901be4568a28106af0dad374fa90926309dce2b06f`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 3.9 MB (3934426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7c22551460781337ed41c7327a05b21f15a1c30f17258e6ec4776b3c7f7379`  
		Last Modified: Tue, 08 Apr 2025 06:36:09 GMT  
		Size: 14.5 KB (14453 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:b89bfeab4f715e94bc3700d8663421acdfe91d53470cbebc93731b319e997d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61262486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f166a586e8ba988278b8e797306d03e139439505e284834af0e9ae2d0a87b4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1793e288819ca8e5da81164fd3b0b1d24868aafe1d8a9d34f091a2f21c58d474`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 11.7 MB (11688962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157d1e1ccb587dd93d76e563527e79db61a20ea5a68a6c403990dfac4c4afe2`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 1.9 KB (1900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311b058d618e974504bbd6d59732c7adb9d6ae51b0e044e6d23722d4d75dd51e`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cc6e969d13f9c2cf36335348948dd286883e74afa777719fca45c5b7494b71`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 93.2 KB (93220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:1a3a2e7151462913ce91f40d07426091dd56d0538e73a5912341dcb207dbc1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539f5b686c724a08c2290236cbb9eb0a22a1720be1314f8cd5295968526f47aa`

```dockerfile
```

-	Layers:
	-	`sha256:4fafb8b7f5dbe92132a656924115da59d568b9a2d25df7c119e69607f36496f0`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 3.9 MB (3932089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c3da41f1e996b0bea791a288b31615f5e252addac9255378820496817694b2`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 14.3 KB (14283 bytes)  
		MIME: application/vnd.in-toto+json
