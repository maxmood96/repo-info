## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:67e1b7ad3c369bdada21478445f5ccbe31ece37a139d266d78c06487848f60a1
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
$ docker pull neurodebian@sha256:3e546a3eedb271a9eb8c8a3fd359cc34aa309cb0f055384484db71a135a5a035
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60019399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452d59ad840fbcfd81c522c18b87369321b77e10537e7abcd4be040eefd0fcf2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:edd38bdf09a62ab44ffab2a10058156dc336ea087cf3a73258758d9bc541ff85`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 48.4 MB (48376965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbd61395bd6666c015e62c5fd23a5924635a999daa18e84a1346004e8e1a3fe`  
		Last Modified: Tue, 30 Sep 2025 00:16:35 GMT  
		Size: 11.5 MB (11549370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39194b1de3ff41fb77cf0e8d5c69d997b6d0ca8d0a35c644b1ed207e9ef0a8c`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a410d8cc2f19fa3ba9214b113c6f21d9fcf24c60ecacbc24a8352834dba93dae`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1abee6b364777d5c62b6c23d22cb7f9c3d6718362d6fedc11ac022176f6a032c`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 89.7 KB (89745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87144e73ed6f2011ee26137d4e17657da8fa9cc9fe23524733fc900fc0c488ce`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c56ddafef222795b2c3e6d957988422562cc939522972b2cb37df0c29252914c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3591195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1397b37b2621de8dd3b31e24bb65583e05fb53d4bed8e7250620d68d1ccbbc83`

```dockerfile
```

-	Layers:
	-	`sha256:de1436e767210397db0ce0822cdab812243cbf01b60f76a691141e21d30f7036`  
		Last Modified: Tue, 30 Sep 2025 22:08:32 GMT  
		Size: 3.6 MB (3575221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fa86c35f97f132f3e730b9933892b76c47a6fa9c0a40ba58e5fdbac4999fde9`  
		Last Modified: Tue, 30 Sep 2025 22:08:33 GMT  
		Size: 16.0 KB (15974 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:9191edad731c3777239ab7a6df02e8c3cca27fd39f070d3a9f2130a27b286529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60205498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed9d6ab91c97c1ce364b776c074b575641047e24efa1851b32dceb9d3e43f91`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:00e024daab2d43f36749bffb01f2b299b405cff0659a8e4f4f00bb468dd24c27`  
		Last Modified: Mon, 08 Sep 2025 21:14:58 GMT  
		Size: 49.9 MB (49934721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81efd0f0dcca0cb336b828640e6827714cf6b6db92f89cd82e323f6982d7f4d`  
		Last Modified: Tue, 23 Sep 2025 17:39:59 GMT  
		Size: 10.2 MB (10176977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603959d5699befce3d731668bbda6ef5af594a431dacdcd4f999328e185fbf82`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e002eb0aadc14a90478115b718f1549b2e972b9c8b9828cfcf24af8768e48b6f`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb7eb4cc610f644f057f5935ee9846750de3ed5aa29b6b4626721d2881bc3`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 90.5 KB (90473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f379b3fb391ace6e8169e270dfe80ba47aa454ebabc6a261938b427e9ba848f`  
		Last Modified: Tue, 23 Sep 2025 17:39:54 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:84290dc5531ab703d1ea0a46c4080e9bb469fb5ffa14f513534e950f69ab9aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b99802cb1d850e1aa7fdd8c934d54b5c43752f6d208c43ddb6954d3353ab6b5`

```dockerfile
```

-	Layers:
	-	`sha256:3e46be236b4284404936a8f6998febda1ad729b8427e99900db52dfd85f23c32`  
		Last Modified: Tue, 23 Sep 2025 19:08:01 GMT  
		Size: 3.6 MB (3611491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a6e5fd5021e1f648ebc119ba8cab091880a2c17c44168587834ec61baf52878`  
		Last Modified: Tue, 23 Sep 2025 19:08:02 GMT  
		Size: 16.1 KB (16114 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:83aacc7fb7b5c65ca54a080818e9df1beb9e2835d71400afb8c936d0be0596c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61496540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d626ce9d4f2fad6eab9d8e779976d51889a33cfcdd0cdf4d001d569d28c47a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d00269cb73b9e4cfebd155b431da849e0072689663a0a658044389a50f9d989d`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.7 MB (49686171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e44f7b83abd8b70cd2ad8be2342045f1278f361d52d006293b6138988a57d04`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 11.7 MB (11716994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e53eb5296e1a4de069da153195c7ba4f193ae52135e2fe3e4f00df0a32fabf`  
		Last Modified: Tue, 30 Sep 2025 00:23:17 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f65dd046c1052fda8eb42005bccd5b42eab0bb6d48a74c2ba1fb663bafe25`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55663231e76515c4e6592b762a96895630954a6b668a4b634aba4b9391b3dc6`  
		Last Modified: Tue, 30 Sep 2025 00:23:17 GMT  
		Size: 90.1 KB (90053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46582ec95217b2b184925612b84924c68c5346b759bdb1ab3841815dc207c91`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:cb6e5622e428e267adef0d79727976efc8d4b353bca077aac7912d8c1e7d8390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:519927b36064e015e1e86af0b2f1d9ab668b2d6045b87467db30fafc83bd1b8a`

```dockerfile
```

-	Layers:
	-	`sha256:73cd775764b53a6df1791f2a63e44e371b862cc68aa1b9f35d6e5d6dcbf5f8ea`  
		Last Modified: Tue, 30 Sep 2025 16:08:29 GMT  
		Size: 3.6 MB (3573184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1dbad6618782fdb70a1e53631f2316732918e54a51517310778994fd40f091f`  
		Last Modified: Tue, 30 Sep 2025 16:08:29 GMT  
		Size: 15.9 KB (15942 bytes)  
		MIME: application/vnd.in-toto+json
