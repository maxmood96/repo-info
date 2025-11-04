## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:58df9431de6dac5cace8bca542030e9e935a3dbdd32255741b4a4aaac8903cf9
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
$ docker pull neurodebian@sha256:e8a290457fdcb25fd97add176a89aaf05448fa1604f033e5576c669df662fc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64965323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed0150829bee747c74417bc49a1a7ae7b385f0b3d92929c5e18981faa5aa3e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:33:19 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:33:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:33:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:33:22 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10fd61e59bab2fc94cf6c8ece723b5b01be52abf9287e8ad4a9e0325bbda9f7`  
		Last Modified: Tue, 04 Nov 2025 00:33:36 GMT  
		Size: 11.1 MB (11105086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53069f91061c1664412e1de03713f16511af4421fb26b3cf5c0834cc5e0f5956`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0348217f8861b15dbc928cb9ec299642abee403d4f1c9cdcb54a77fb280929c`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d3db1b8d2466e54a0c98cba6586dee43d21bf61cc29a2d1c31fd2eaf958935`  
		Last Modified: Tue, 04 Nov 2025 00:33:35 GMT  
		Size: 101.4 KB (101387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f2ed622434305153bd8f685c0c5c146c9084bb854c75f81b6c8c0cd8f6616eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a0c559cc49adbfeaa5e73e9f4d74b43be50b2306a5313e2cc008d4ebcc919a`

```dockerfile
```

-	Layers:
	-	`sha256:973ef639fc1a7924a61cc483a9a3391689161787e52c26c8a30c0058f8d90b7a`  
		Last Modified: Tue, 04 Nov 2025 11:09:09 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939958c021b8d787652bb54951123245124f215e3944b7525f94d08aef60a918`  
		Last Modified: Tue, 04 Nov 2025 11:09:10 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ad60d79b65d4ee219870c13df5e5115485fdf0e3a15df30a17b5baf80718b5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63467244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b05d297144c8eca61ed67371e8a89c5b7f8231da7ce81b6293eceadf964fd3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:34:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:34:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 00:34:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 00:34:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a094538342569d02b91d24b808d205b77d9c9fbf852b9fcd0ca7903bad0bf75c`  
		Last Modified: Tue, 04 Nov 2025 00:35:02 GMT  
		Size: 11.1 MB (11105999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dab4fb4d007e63ce04d999f679515216a96e37397441dbfd194691445fdc850`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab95f778dc7d395951c5fc9a7171fbcb2da9219797d0f275f3893baa6d5567`  
		Last Modified: Tue, 04 Nov 2025 00:35:01 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e461a23e42babff2e43e305785bb9d0dee54499c7cf927103041a5d495519244`  
		Last Modified: Tue, 04 Nov 2025 00:35:05 GMT  
		Size: 101.1 KB (101121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:60f3bec73acc99c31f72c306ebce80ea10d53f94d0a820dcfab64f5172af7f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49be1e79f5f06e2b68c2e08d12bda1fac934f3f4cf4597c22d1a2e2f54cc3dd8`

```dockerfile
```

-	Layers:
	-	`sha256:2c77cdcd1f4462f411c49db74b7815b153f938cbf01a2225e1b8254e06291e1e`  
		Last Modified: Tue, 04 Nov 2025 11:09:15 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8a2c5b00b6acfddf7a7463416c74a5f72f5a43c484a9ba8a9b444cdea70f44`  
		Last Modified: Tue, 04 Nov 2025 11:09:16 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:bffad495fc2e10c9ffdace390212b97040d9dd6fd7a3f3bb36b7a41ccf054306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66303623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64afb566d8d555a881c704ad285707871cbed6226050af4b05f957085be2ebc2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 01:37:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 04 Nov 2025 01:37:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 04 Nov 2025 01:37:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e60c3e4fbf8c19df439b90c2a7f7bbd43579378a671c1afe66083570c61159f0`  
		Last Modified: Tue, 04 Nov 2025 00:13:43 GMT  
		Size: 54.7 MB (54699883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11efeb646c81ee09e63cbbd314b45549a0e2d58975c0a2a4d5cf3b176d3a053`  
		Last Modified: Tue, 04 Nov 2025 01:38:00 GMT  
		Size: 11.5 MB (11500313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f18adc21b713d03131791638b3e0e3d1df3afcc168f3a53a98d4642f066adf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de3fdc0a50f5c4807dccba9afe1e063eee114d6f77728b1ecb923ce3a56a8cf`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 264.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:349d451c4654669ab44b9d291f3e6be7912fcf85eb2300008ac567b1bf186277`  
		Last Modified: Tue, 04 Nov 2025 01:37:59 GMT  
		Size: 101.3 KB (101269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1c23e7716c1929c22ce60b5a211c7486a20034efa59e7f82f8172d21695917a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da420932dd33557839e97964af02cd54f6c3ad003782ab0ffa74bc0e4a5426ca`

```dockerfile
```

-	Layers:
	-	`sha256:b6e13c2e37e1a78a39ee3d6fe22eaf77db826b0afa8e4741f6f1d2c1a68b2547`  
		Last Modified: Tue, 04 Nov 2025 11:09:20 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5502ab97137ddc1c1d3d9452d22a75de66d48c5b42f805ec6607488ec4efb1`  
		Last Modified: Tue, 04 Nov 2025 11:09:20 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json
