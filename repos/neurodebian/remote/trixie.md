## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:7932022e3d8121e11932401783c54eb8a09e58fc0e1488d8e2fff2253734d01c
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
$ docker pull neurodebian@sha256:03f45755a0cbd0fa591dc83b3f174f408ec09689438dd1f600685d2cde3859bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59817418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec1e38ad20d40f39f7b16d2bbf5d3dcaddb31d59c129758a0bf91ac4a087408`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:53:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:53:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:53:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:53:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eff5378ff39f272aafcd4e6eb21f0002984d7ba123df62005a1c72b904f39f`  
		Last Modified: Tue, 18 Nov 2025 03:53:24 GMT  
		Size: 10.1 MB (10073386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7768b0faa974ae0a24a5fc2d6d8ab83d8bfbaac5c1c6b88142e79c4e9331d292`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803b1be5a4e9ea2b53fa1893acd4bfcfcc977b674beb4d6c9df3d231a97eb4e`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239af7ab87748df14555e1392f8dbd23b17160c367fd5fab152ab0d11134d812`  
		Last Modified: Tue, 18 Nov 2025 03:53:23 GMT  
		Size: 90.9 KB (90895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4233619c2439c669dcbd798b18d3779f25a61d90424651cd1a47825c92259fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c67bfaa7bdaea4ffbeca1e70fcfdbd3beb9885e4ede0de846eb219c971de3e`

```dockerfile
```

-	Layers:
	-	`sha256:105073c6ec3e7f5c078d5e10ecdbbf90eaf703f3743f3044afb9c8e051305965`  
		Last Modified: Tue, 18 Nov 2025 05:09:31 GMT  
		Size: 3.6 MB (3614556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfef6ecb903761ecd001f5326ba3ebf4549b1e7fd94a1e645e8f1707779545e4`  
		Last Modified: Tue, 18 Nov 2025 05:09:32 GMT  
		Size: 14.4 KB (14387 bytes)  
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
