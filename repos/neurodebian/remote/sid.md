## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:4d0580ec37a345aea46ae505a8dc698ccf008521f93fead14c2140191c4ff05d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:035b7f627535f4f213b8df77e7501d898cb8535b31d3b0ea9ec6190b526c72e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60527446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0620c75bef2ca94f3e2085bef9f7b070219d80eea5f03cb046e443a39f5142`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:36a4985327850927961426bc6fcb1fb8dc1f9b5e7f69f8061c7daf2f4aee58a7`  
		Last Modified: Mon, 29 Dec 2025 22:29:41 GMT  
		Size: 48.8 MB (48821118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2afb24b11b414a91690e2de9e1bbf94e8ef9c750303e10a1f474612a1608bc`  
		Last Modified: Tue, 30 Dec 2025 00:04:23 GMT  
		Size: 11.6 MB (11613260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f117d692e9d33c678c15a431856f5a53a13f3a6dad3cfb64ccb90d53565b68`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3fe440ad283dfa1ff5bc20d76a5aa1943e3a0725babf9323e9f7a8952a30b8`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778a5fe0dc6f45c67af4e740f0b16570ab7430e78dec361704c0dba2c7ea76b0`  
		Last Modified: Tue, 30 Dec 2025 00:04:22 GMT  
		Size: 90.2 KB (90165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f63b8514f32c1fa215e0e8aba690d5e7f4a1973d624c81ae66df879b1946506c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8190f725cf92a2460e1c1a62399edd64257b02d78eb697d0b072a2334c250c5a`

```dockerfile
```

-	Layers:
	-	`sha256:d736499878e3cfd7bfcde74cbf7a0c4d6ab9912f74fe399ac8ede60eacd6a960`  
		Last Modified: Tue, 30 Dec 2025 02:09:06 GMT  
		Size: 3.6 MB (3589915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb93f903cb7d91c8b2fa32e73adc52adb5dc551b0c5b78c36b7ac7d1501e204`  
		Last Modified: Tue, 30 Dec 2025 02:09:07 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:b0cbcd07d5581034cf518ae998bf872b0fa8fc1dddbc5199ead7b0b2e16ce097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60160061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1a53b3bdb4de5c84e64777050843a0aa26b83af4ef0f1bf919ba80c7fd612e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1766966400'
# Tue, 30 Dec 2025 00:04:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:04:34 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Dec 2025 00:04:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 30 Dec 2025 00:04:38 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e81a19d37d9900498b0ca8a841e2e3fe3dfde06146f7d10d1e71e1df7a8ae8ab`  
		Last Modified: Mon, 29 Dec 2025 22:29:24 GMT  
		Size: 48.8 MB (48801029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f99e5f3335c2ff6d9abb774351bfb55d384d817ade2187270b9fe3558779b90`  
		Last Modified: Tue, 30 Dec 2025 00:04:53 GMT  
		Size: 11.3 MB (11265267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4347a2a6ce4512291bdc3028015b54c7df8357a7fdb3630aecd4a3a33d44e4fd`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb44e37c3ff6fd90ab92d83969c35acdcfe3f7adaf5820e89aa01d683814c5ba`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15704ec8aa9e145af8c6e5e21f510adeeed85f82e7d9a5f45154a9b0bf54f18`  
		Last Modified: Tue, 30 Dec 2025 00:04:52 GMT  
		Size: 90.9 KB (90864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:06ec310696b16f7e4166904a3ae30305fd9b5fd8d88454fcca2fd4971032862f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8beb211810ee03db5a4aa15f811c77314d39d61a9836ec43ddda805e26c7fed`

```dockerfile
```

-	Layers:
	-	`sha256:c6d26cb601684ef686b4ef4357a1051102513ec62e85fa194fca69df15f5438f`  
		Last Modified: Tue, 30 Dec 2025 02:09:11 GMT  
		Size: 3.6 MB (3590791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4295813137038125b1d76dbc6634cf4378020e2cdb7ad404da9ecb210548650`  
		Last Modified: Tue, 30 Dec 2025 02:09:12 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:b948fed8f970370d78bb2b66113a9669025c50d49aa0d1814fdc0fd22d488ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61791101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fdf8674537f2abda89b30e4e947dd43ae776cd5624f13562a344fffc9b96ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1766966400'
# Mon, 29 Dec 2025 23:49:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:49:58 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 29 Dec 2025 23:49:58 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 29 Dec 2025 23:50:02 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f17a69092f61f8d721afcb2893fe3fd9f89bff73ba6442fc317604ef6ed50dce`  
		Last Modified: Mon, 29 Dec 2025 22:26:26 GMT  
		Size: 49.9 MB (49939146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6af66be5e6f60f8b9745c1f44a850b26367c40754289eabf69d788b9d32aa45`  
		Last Modified: Mon, 29 Dec 2025 23:50:17 GMT  
		Size: 11.8 MB (11758513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1b455b55e95ce89898726761e4c22a29c4739d213103e6c9b26d934ce290eb`  
		Last Modified: Mon, 29 Dec 2025 23:50:15 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d942f8206b76983527c258f72f848c0b2280a4a183da003426a6d9d12db6e75`  
		Last Modified: Mon, 29 Dec 2025 23:50:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431a9ff949fe43467c92d2483bb250bf120e0655f2ef59bc19e791df3ea9ed7a`  
		Last Modified: Mon, 29 Dec 2025 23:50:16 GMT  
		Size: 90.5 KB (90540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:179b32ec3cc2a4ece82cb8657cabd9e0143b46eb5c8eb9fec1cbf05cea749307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3601748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92689d55ace46f56384d84cc65e769340e7e19aea157a22be1b97747a243b2e`

```dockerfile
```

-	Layers:
	-	`sha256:a90c5d568268b0de4f42931bbaf0dcf9ae4c389853479ef0fbe7b7eeb0e7c299`  
		Last Modified: Tue, 30 Dec 2025 05:08:27 GMT  
		Size: 3.6 MB (3587873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:420efea63bef4995f014ab111a9bc1cf19e0c3dabcb1c2a134be6a02dc90c4d2`  
		Last Modified: Tue, 30 Dec 2025 05:08:27 GMT  
		Size: 13.9 KB (13875 bytes)  
		MIME: application/vnd.in-toto+json
