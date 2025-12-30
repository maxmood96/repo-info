## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:e21fa53efda88c069dd1c2878a1b2f28855ae3ee762fde42098e7d168170874e
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
$ docker pull neurodebian@sha256:8f5cfc00500cc0d446db7aa634f75cf84b12afe95e95ebdb31af23e36dd652c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61813318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574cb528275d8e08c0c2aba8f98ebea411e3d9e83b8666ec032897e9890a4e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:15:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0266c0513022413f6a42ac8de173ef0db6a7fd70a6d1859fdaee0ff7c1f1a52`  
		Last Modified: Mon, 08 Dec 2025 23:16:17 GMT  
		Size: 11.8 MB (11771438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54d5b89513ee9aefb4cbaeb149aac108b65168fa8016ced6820617134e33cc7`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44066a3eb12e5a62aeb429ee8e2fa4e039a016510b0053f5b6d5a21937982b57`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469a39499ff4a4700821efc8a4595a0a54ee4dd2c440d4d7d1bd6a635aeb8f41`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 91.0 KB (91009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:683dbe22bfe3d344489dcd587c30032ec24bcc1eec3ddd9dc64298a5a3b44fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d30d3a82ccd78c8e1f82eefd7dd5e1a1c671e68a0c3acffd7baa9d15c330adc`

```dockerfile
```

-	Layers:
	-	`sha256:61532c3563e04ec54407712519658270da6406a9e32a333a448571a3a74f36e1`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 3.6 MB (3589161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce849a1ac7c09b2ee06fbd7089981ce600c9dc4944c42e11cbeaf60a93c90dbb`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
