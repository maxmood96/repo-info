## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:c2072d99e5e834380b493b8d747258276f4d98b855f7052bcda0108ec10391c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:efd26f70b1aa846fd63041bbb9d89b12074377739e7a9e8c64ed51989cd5e876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60534589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3059527f0fe40aa75b84a855a2d3aca39b621d4f439c2be95b600a5bddb7b48`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:14:01 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:14:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:14:02 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:14:05 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:14:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:490e982b5e2060f5a5ea7e5f586ff8bb98bb61a953b4473631a9da94fd85fe11`  
		Last Modified: Mon, 08 Dec 2025 22:17:59 GMT  
		Size: 48.8 MB (48817523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbc453549aa375b6e8656d9e28470deeb2ae7b02a4c71529ba81bc89115b66a`  
		Last Modified: Mon, 08 Dec 2025 23:14:20 GMT  
		Size: 11.6 MB (11623061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180a2f2456c270668df5c04b7601cb8d752e5625286c109402075a7b17df4413`  
		Last Modified: Mon, 08 Dec 2025 23:14:19 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd313d1fcc1ce2bb201d45252b0c0b5191ea0f1cbb3c53e31ecc9161d156c13`  
		Last Modified: Mon, 08 Dec 2025 23:14:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c7baabbd226f823fb84288cc86f08255207ebf5050eb7c6be5ae1e7bfe6d01`  
		Last Modified: Mon, 08 Dec 2025 23:14:19 GMT  
		Size: 90.7 KB (90680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd8a38b8bfe624e29512fd82d44ba68e4806d486bc7a21bf6dd30affef76565`  
		Last Modified: Mon, 08 Dec 2025 23:14:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0bffb23545f365bfd4d611ca12939434299d19a9df7491d9b70f94b980b7fc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10ccdaf70686b74918494dd0a28ae73e1d36c899494b19db967af360a94f3fc`

```dockerfile
```

-	Layers:
	-	`sha256:07fcd1f0d128fd78af9a45dff8d8d0bc329a713326f77a68d454934a41117272`  
		Last Modified: Tue, 09 Dec 2025 02:08:40 GMT  
		Size: 3.6 MB (3591243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e55f3c2e004079dd425d73a54471221d87d82e485eba27d889f3d385ac4dfd`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9c548a571e85b70b292b96813cd00941bf3e96b959057db5b2572c2dfee4aeca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5c33d75154b40af5a4e2ed79dfdfd6a916e3cda19c539fe5f34c6f4cf23f76`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:57:13 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:57:14 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:57:14 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:57:18 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:57:18 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1473a9ef112b3354ecb8ad37437881c07c1330a179af790e6197afe69d118085`  
		Last Modified: Tue, 18 Nov 2025 03:57:32 GMT  
		Size: 11.3 MB (11255640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7b3173ae7900350aa0c13fb1183ca91219d5891202b3cff35eeaf1c80b7d5`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9797247299d9f83b806b73618e195baa0f95d2ddc9b81bb9c6cb69852d70360a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305d3575bebd85f0bb2b4936522cbfe2058213f281cf396211a6dcaba921569a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 90.5 KB (90533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07a8228ced17f46f7ea430082bebae91f27757072506586bc99ec87f75f6d0a`  
		Last Modified: Tue, 18 Nov 2025 03:57:31 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef97f524e0b4f5a6f8fbe1cf7cc8862b248979d93944230a0e6ef10ce6a2bc5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a332782142e357fb40eae518f5fc9a7ccd220d630e0da1481cedc4f1684377e`

```dockerfile
```

-	Layers:
	-	`sha256:6cd1b21fff2d2212e067d9150271763da862a313f3c4b2fcb4e5fa0c42f1f4ca`  
		Last Modified: Tue, 18 Nov 2025 05:09:49 GMT  
		Size: 3.6 MB (3578307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581ffbae3cc89923c70c60e4c5b10f6337934afca176aedaec8dbb8f3f4fc942`  
		Last Modified: Tue, 18 Nov 2025 05:09:50 GMT  
		Size: 16.1 KB (16071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:49afcad16d105fd19bae60cd14158c11b083cd49993f77a1b4f650c6ab293be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61813645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23040b5c36dbefc61179d2d7deeda5abfc71fea09f198c632c1abe65282f03b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:16:08 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:16:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:13 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec12c3df770257e87a24e89f178be2debdfa70110f149c64f33fafe3e06b0bb2`  
		Last Modified: Mon, 08 Dec 2025 23:16:29 GMT  
		Size: 11.8 MB (11771378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d9aa372e7ef553d58fcd21aed06e967b22c56495ff93ff4db7ba9cb7dded3a`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1a6aa5a510c3bbd9a734f2af4a0f01c08b189f9964f11c3f81c91174367bb1`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca5f7bb75d5cb357f3cf6974aea0182f5878e2b95b614c8d4f0d1ccd309cd70`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 91.0 KB (90977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137b22bdee3d72723ee405aadd32bb53c6338c92f8ef80e18f5a70cd443b75dc`  
		Last Modified: Mon, 08 Dec 2025 23:16:28 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3da97abc8582eb66115af61c24725caeb2eb08ae525671a2c9180458e24c5623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f369991e4501a6c1095ea76a75182086694a3acce7d86fbe1e9e5cf75cf0e27`

```dockerfile
```

-	Layers:
	-	`sha256:807a054d1fbda6da8789823823c4862f08b246f336bc67bc357a9a4fcc45dfdd`  
		Last Modified: Tue, 09 Dec 2025 02:08:48 GMT  
		Size: 3.6 MB (3589197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e54569f675797e675d8e53c2f3cbb7f2e4ed87ed2af17c0cc005af7d6f08535`  
		Last Modified: Tue, 09 Dec 2025 02:08:49 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
