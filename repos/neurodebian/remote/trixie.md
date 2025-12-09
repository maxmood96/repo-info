## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:a54aae46b16c331a05bff757ee11082028ea18b79820286779856505a51702eb
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
$ docker pull neurodebian@sha256:c23f92392fa77aeebca1b0a2689a4e578e17d4db31e0a5a2fe20d2c8b5153951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2be741bd1c8e15dc871536bf9cfd8156d00af00cc1e3b3afcc359672ec3a1c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:13:34 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:35 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:13:35 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:13:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a21b328f432c2695ea418e2297d8683d94d0bb34719cf2d6e49046ee3a9fd`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 10.3 MB (10289981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a203543b43beebc00f8552d5d91aaa670918d0e232f30045aea459e846ccf100`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6ec7525c679f2e38d78c4471fdb657268002ac43e22284bed0da6fe15f9696`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a5a989b999caced1a948390e2bbb139e07fc1f68d8655fcedde22722c43e07`  
		Last Modified: Mon, 08 Dec 2025 23:13:51 GMT  
		Size: 90.2 KB (90240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:314610e28f3b29d6523bcebaeac38c91814020fd60b71e6ad1f7c31d9313b7e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bea8db94b3244b38aa08c189bba0b80d7c1c5bdecc9efe190f9b40ae1aad4b`

```dockerfile
```

-	Layers:
	-	`sha256:1e4a942f26826cdb1948d06038cbe951dbea0eec9e0c4dba4a3a2f9dbe58673a`  
		Last Modified: Tue, 09 Dec 2025 02:08:22 GMT  
		Size: 3.6 MB (3613029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a850890e8cbc9aab65555284e02161613f6aa963d4d62a6837ab437ea9ebde`  
		Last Modified: Tue, 09 Dec 2025 02:08:23 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:faf4b547f7d7261320c615a3a50a999d9f2dff96d0543d2d98ca11f1083807bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741e466f75c36e8b1284adeded02f3d6485dd0e57a07ecd409001edd08af953f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:16:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:16:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:16:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:49 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d485c0e048dd206b424d1c6a3b6e2b36ebe22afbb9481571a1571537e9584f70`  
		Last Modified: Mon, 08 Dec 2025 23:17:02 GMT  
		Size: 10.1 MB (10073401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eae35cb500120bce8b896df2da017729483613409fcb341776489b276201f4`  
		Last Modified: Mon, 08 Dec 2025 23:17:01 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71a453da5c2e1611357d08e4d118f29bc16422cad6b5a3b7ff8d8bb9466b8c3`  
		Last Modified: Mon, 08 Dec 2025 23:17:01 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbc9f1c1dbe62134830b36022f3bc833615c0915bb5ceb0fd92c9ff6009f21a`  
		Last Modified: Mon, 08 Dec 2025 23:17:01 GMT  
		Size: 90.9 KB (90914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e8b088e86370dba4853ef563d6677d3a2f76c7a40180fa95c0b432dfcf833da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b523e4191883f408d23929529d592dd12fb066f8dbe8181fef212411782f4a08`

```dockerfile
```

-	Layers:
	-	`sha256:6862e0c468997b58a23be2cd343405a4d21114b59676066bf2ca5466b2c1ae20`  
		Last Modified: Tue, 09 Dec 2025 05:08:13 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bad477412afc2f0f05918ed8cb680255d5b58ff6374a00f8db2cabeba00640c`  
		Last Modified: Tue, 09 Dec 2025 05:08:14 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:c8dc1f5965291d82532beb930b4b8dd9d2857dcffb348f41946ce7525f9d1868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61358183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4224f54fb533cad2f8b9b30d2e785eb1fd843e4fd63e905343da0c070c075d03`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:15:24 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:25 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:28 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e964d190139b1aba3de28d11b605a95f92489da3beb9d80e9099db336eb72530`  
		Last Modified: Mon, 08 Dec 2025 23:15:43 GMT  
		Size: 10.5 MB (10463020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ec584c96f35b189d796255e99284eb2b5a60beac79d3aa5e9e38511057c721`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9b780ecf3cdbfe9614a0f6fb11f3ac440968fc9859f8381cdd325606eb10d5`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e72d44ba44c44786256e5c59963306628e9bc4225d957dc3c3f88b69404871`  
		Last Modified: Mon, 08 Dec 2025 23:15:42 GMT  
		Size: 90.6 KB (90608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8feb71ee0324566413295afd412d3e8536f97cd4923d4b4e3a66a630eb6b5e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f48fe17c7803c7f0a740da48d64460f0e14b205e6ef00e468dd25f6d417492`

```dockerfile
```

-	Layers:
	-	`sha256:6565d47d0408e99891700b9f73772b468617ffa2decbf66dd47aa2f3825e0c46`  
		Last Modified: Tue, 09 Dec 2025 02:08:59 GMT  
		Size: 3.6 MB (3610978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:928694ae3cbda82a9b5864d3bb2e6e8cc4bfd721706dd53996bd42268ab412db`  
		Last Modified: Tue, 09 Dec 2025 02:09:00 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
