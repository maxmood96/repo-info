## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:1c42386984b67c6027e4d9591d99937318f073051462836e8c63f133aee34ad2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:fa8d0e64ddf2c1f1524b59c687262eb2f390dffce21e35e655a09cde8c897585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64963207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93a0c67e1f5a7d1e6579a77a17cf0f61e311848eec5f0fef8948e5888ddd6ef`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12161ce65f3f2f3d708a045c4fa86915abb98817b1d113b48df410dbd607979`  
		Last Modified: Tue, 10 Jun 2025 23:39:48 GMT  
		Size: 11.1 MB (11105046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c78d6484fd08234d24ffd44b1cf75253482d44f61de3b4d732c1a875f0482`  
		Last Modified: Wed, 11 Jun 2025 00:04:43 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfd68787eaab78b42c559ed7924a86222fd0f360803250914a6e3c1273bce86`  
		Last Modified: Wed, 11 Jun 2025 00:04:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d48b5c4c76458905e76732ba51f0d84c7705618ac8fb3edeb54cac29cb7cd85`  
		Last Modified: Wed, 11 Jun 2025 00:04:49 GMT  
		Size: 101.2 KB (101220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7a662ddfd8f8e1115e6dde91224cab8e49b8a35e368a288dcc5d02bbfd3bda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d1cba6ed4f2a462bef52d228bfe3d825f7d55944b76eadf532a001b7e97a6c4`

```dockerfile
```

-	Layers:
	-	`sha256:d0979e886eef455999223006e6d1e1b32a15df13b9a2977627e6c89d85995bac`  
		Last Modified: Wed, 11 Jun 2025 01:07:37 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d06cb507a902e6a58d9b540dfd6b4044211fe8adcda2c8c7f5aaaa3ef804e53`  
		Last Modified: Wed, 11 Jun 2025 01:07:38 GMT  
		Size: 14.0 KB (14009 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1f6ea5c2d91ef0725d4a5ad5cd7125f80b3fc78ff261238fa7c4d9f75b37e1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6873213ee173fc0021a00d8b7d220c1d2216db447ef3644e158f2a2b05e69a06`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238ad053354067eb964dfd74d01bf6f0ecfc281d685820bcfaf985802b572115`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 11.1 MB (11106083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba42217ddf0a827733b7c068083cef07d73d3618fc68bbf995d444c5e4878cf`  
		Last Modified: Tue, 03 Jun 2025 19:33:33 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fabb9921d93c301fc7f92c8070dfc175a2cd99ceb458f5e0dee60781e06ba5`  
		Last Modified: Tue, 03 Jun 2025 19:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f9c53b5bda4d401bfc0a611f23cbe35208ee1fcdafd404674325c07feb2bce`  
		Last Modified: Tue, 03 Jun 2025 19:33:36 GMT  
		Size: 101.1 KB (101120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:61a931e647ad16337d4f09e239754e94547af9d7946cb1869572b5ca182da3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4273123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea337907d2f184a758c15db149c8c91fc3a44aec85d6a4ee0b8617add242f04`

```dockerfile
```

-	Layers:
	-	`sha256:33d48daca7db678746999e040dfd483fd2b62b4a311c170482f61deec548557d`  
		Last Modified: Mon, 09 Jun 2025 02:16:09 GMT  
		Size: 4.3 MB (4258989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dc3b54ca56f986bfc00993e3cf39fcb4d7301bcdcac2156bef0c4f29bd42dd`  
		Last Modified: Mon, 09 Jun 2025 02:19:41 GMT  
		Size: 14.1 KB (14134 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:e7246e0a58c8da6ac9c975db63e6584dc267ff91c2094271417bf61cd6baff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66293643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55d1972e505207c201182536b8203b6addb6ba7474d3f976cf07b1f8d8dd81f`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Mar 2025 01:29:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Sat, 01 Mar 2025 01:29:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74216023682d3b31d84de0ebaeff59619d56684e8f5c8c4a19cf9794f79c8d50`  
		Last Modified: Tue, 10 Jun 2025 23:36:26 GMT  
		Size: 11.5 MB (11500388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954648ca4b374873e27c6cb4db5fcac429b6cdb75d89592ace61f69f58265d84`  
		Last Modified: Wed, 11 Jun 2025 00:04:19 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c27a1b518834de55ce4678d5c5ef7a81d8de304747378c297306ab52c279f94`  
		Last Modified: Wed, 11 Jun 2025 00:04:21 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ff93ddced19b93a0a2b7ca0ff36215d59f37be24b4512a0752abbbca5355cb`  
		Last Modified: Wed, 11 Jun 2025 00:04:25 GMT  
		Size: 101.1 KB (101085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b51d0516f8e8ec87176aa063c2397f6ac06e922b0d2c3973b10de1c41e1b2c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf6fd4a2d7d454aaf3ca63f0c8db6452e0b510c18c1d1b6ce8f12187deaddff`

```dockerfile
```

-	Layers:
	-	`sha256:b8a880c26a89691b0df62c5aa9d221f823f338c4bd2ced185abd430b56b1cbc1`  
		Last Modified: Wed, 11 Jun 2025 01:07:50 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a5f114021b4fa20ebe17faa78be8de615a0e049329eac6a9ae8cf6c037477b`  
		Last Modified: Wed, 11 Jun 2025 01:07:51 GMT  
		Size: 14.0 KB (13981 bytes)  
		MIME: application/vnd.in-toto+json
