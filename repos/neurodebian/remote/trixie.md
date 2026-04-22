## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:ba03f986f1681966bb6cc4ee7bab72c51cf598ce0494a31f8004a1d9af0d12b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:7d39bdb049d63a02c3df2dd7c78552151cd335dfc073402fe68bebfcb0371a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59688225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3841c96179deaba2f3b7dd01df80bc3d441d7468d7f714c9d74d25d9b5f1af6c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:44:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7b07652ba0b5b42398fd9d4133dbf46fc8d5475a7803c682e5d68fae669ae8`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 10.3 MB (10292834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68609610d977281523a6d91534dd2a98a6262c5ce9219fbf52ee5d428d272117`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704da151269ac996fe5183c92901832119273bd56759fcfdcda086da74ca77f`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a0d5c4a276204f2213d846b598ad5d1f09dbb4f3c7b30c399e59c91eda1597`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 90.4 KB (90388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2075e251f251eeba52911348c5d809b65c7de868f4cc0c92cbbdd4e2f92b63ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8af64b9f3ed93290a526738e1cef88ad71e120871908f6f6df96b209c049490`

```dockerfile
```

-	Layers:
	-	`sha256:e671d5b382d3a8fc0a6b85f6fa5b3664ee884f295967583f816d456347ddf56a`  
		Last Modified: Wed, 22 Apr 2026 01:44:36 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd5af09e767338438f7cfcee3f0e371bdf9cce1eb908c3cb0f2ad26adb28fe76`  
		Last Modified: Wed, 22 Apr 2026 01:44:37 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ddf98df98490a30e6516a88dad74c9080b4990b9c2dd7229976aa41fda2cf9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59841114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc0c31d568d638d16c30d49ab66bc22d6d5318f4d29fab71407e077e2360bff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:46:52 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:46:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:46:52 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:46:56 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fae4052bd9a699325323ae792a2e30b9fc72c278dc25917c9a9ff7e234d140`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 10.1 MB (10077915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76798e07400dd767757ec8dfe9435d779d3f31d5250cea5c5ad5936cc22812c5`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70054b902610f6938eb7928791800e9f2a039a25c54d2b3449c512416a689ec8`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d86588e7392a3239165cbb6907456cd15e84c7f32816dfd781734bcee8f9bfc`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 91.1 KB (91052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5d5a814179fb90e34c30b10b430d6b39cf91995c4f927cd8fe9679ec12e6c445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d2f2dcfdf8aea1dd796ecf4aacf7f4a89d722ff014f142a470e282cdfd4e8b`

```dockerfile
```

-	Layers:
	-	`sha256:514f95074e01661cf09b5572aab47cebcbdb61047d81b284eb99088d73f4115d`  
		Last Modified: Wed, 22 Apr 2026 01:47:04 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743fb056862ffb3e08c1e28962e2a9df02acf23fe830e5d5d5920c9dd786117f`  
		Last Modified: Wed, 22 Apr 2026 01:47:03 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:b93692a0d27abf858e7a70728b423918b63b4c28684b86f83619864eb34bafbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61386029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a962688ba052c54db63b75fb9fa483376cf556ba0a010682baca43c66eff9da`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:43:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 01:43:56 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Wed, 22 Apr 2026 01:43:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Wed, 22 Apr 2026 01:44:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:94f4ed96005686cb93e9fa3c8665cf2919ba40f9e10ece9df171f9948eed4c0b`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 50.8 MB (50825357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911b68cd92ec09b4f3e51e44040daa939ffe29ebafb7b3dbe1d070e2a5eb2858`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 10.5 MB (10467016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0273b8fe2b0a620955891d6bd4e97501e44926bfb62fb882e13a16278dedceb`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77cac839167dc6c1253dd4afdc68fa5bdf1ed97b1b3e09b0e47aad451c1c320e`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30f71f5f1eff1e9d1498ffa21b42cdd8089783d49cdacb85c9fecdd17ac7335`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 90.8 KB (90755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bb3de53c6290e3572e8909fb096f8bf06cfc34cfecbbb0e67425ac7022c3645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0d4b4784c953a39e988218e0bd8c6d2abbc3ee0b636b1f2fb27a0550f82b53`

```dockerfile
```

-	Layers:
	-	`sha256:d9d94578c173d477959d8c4eae4e8acf6a0e46cb977d3addb084721bb028a36f`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2f6073c1f07e93781814a1153d3cd5b025a40ac08ae799c9998f6f8305b0e4a`  
		Last Modified: Wed, 22 Apr 2026 01:44:08 GMT  
		Size: 14.2 KB (14217 bytes)  
		MIME: application/vnd.in-toto+json
