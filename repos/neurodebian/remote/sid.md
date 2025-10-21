## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:f591c935dccb57159313ee72ac44661491ebec3a9a4df492bbfee3c5b924f38e
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
$ docker pull neurodebian@sha256:cae72feb0d6fc71607d86ee057d0c2c290440406b82aadb6e728057aba6c6e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60029909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb37d8fe96189424494e5083598a38ebf59d0ee878a2cd9d25e5c7e47011130`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:767319f7ad72179f876946bf5b239f862d2d5ad761041b6e449acd3ce4c0bdde`  
		Last Modified: Tue, 21 Oct 2025 00:19:58 GMT  
		Size: 48.4 MB (48383307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada264860038c9dcde7a02175464bf0468f0638c5ff2352483072ccbbd44f8c3`  
		Last Modified: Tue, 21 Oct 2025 01:48:19 GMT  
		Size: 11.6 MB (11553976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160595488c3b8bf91696f3563c9ee88afad2d590a134017c8aa9225194a9f86d`  
		Last Modified: Tue, 21 Oct 2025 01:48:18 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110cff31911969e06b17a0a847556b724b7dec095996f10f92b263d82c1a4eec`  
		Last Modified: Tue, 21 Oct 2025 01:48:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a6b0a54577245caa029047c1fa6f4230b8280f4301bc7cab33d1ab5cb2dac`  
		Last Modified: Tue, 21 Oct 2025 01:48:19 GMT  
		Size: 89.7 KB (89723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f84ad5c370bada65a0ee8a23fd89011fd3145da5512f273ccb26cc783aefb295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3589912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee70f0e9db9d32cd8a31f6cfdbdd606613fccbca43173d824b5b29e08bc019fa`

```dockerfile
```

-	Layers:
	-	`sha256:ea2e75c89c7b58b64e2ba8baaa6aa27e2441d6f95339919d486a30c6c1802436`  
		Last Modified: Tue, 21 Oct 2025 10:08:46 GMT  
		Size: 3.6 MB (3575965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf78c13db3e61009e34cb65954d4327c3c36c1d2557b015d3bb80d35d70d7e7`  
		Last Modified: Tue, 21 Oct 2025 10:08:48 GMT  
		Size: 13.9 KB (13947 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ca4b3a696c33b76e72e884890fcf3e463dc9dfdeece2fcceec113c355311314a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59891732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffc7ecd03e2fc9c5cfcd51131980bc4f133b802b62a6bf3a0bc729fff76b53e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e43e2837b589215836966b2f88d71f57e2c4d5e8f8cb435d19f6ca010856531d`  
		Last Modified: Tue, 21 Oct 2025 00:21:19 GMT  
		Size: 48.5 MB (48506031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b1302c061342c184628e6ab129002defbc7051e1fb78537751dc24b2a4d0a2`  
		Last Modified: Tue, 21 Oct 2025 01:52:37 GMT  
		Size: 11.3 MB (11292308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d943228d57b3e2d35b8f42a65768fcffa9ebf08a97769d8cf10110550a8c0`  
		Last Modified: Tue, 21 Oct 2025 01:52:36 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7014668b5b2fa5ed2a845f7ee65f4ebc9c1f3a89b14ee703299a4eb79939100f`  
		Last Modified: Tue, 21 Oct 2025 01:52:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96697d24b36ebb6d9ebb7614ed6dce19c78faa924818b3458caf9442c8185d48`  
		Last Modified: Tue, 21 Oct 2025 01:52:36 GMT  
		Size: 90.5 KB (90489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bab1d46293c7b21b6ad8667ae2aaa29020330220f0351707cf9932fe6a0e0067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3590912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd079b81c0b172deb61ad5e074140aea7ad8f2ab0cf0a663896aa534003f4d7`

```dockerfile
```

-	Layers:
	-	`sha256:99513a38d8ee92ce7c02274ea76632ef756f39cd01ffd97c71e79653642ab8fd`  
		Last Modified: Tue, 21 Oct 2025 10:08:52 GMT  
		Size: 3.6 MB (3576841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:add3e05aca8026e2ead7788582e9ec90b2f8bef62b8cdf057bd20decb335504a`  
		Last Modified: Tue, 21 Oct 2025 10:08:53 GMT  
		Size: 14.1 KB (14071 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:283bfd51b4eba0300acb532e0548590e24ad2c72d403800f1f6ac0508580076d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61537240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f670507753ecfc22c6377b66730e46efc61f574e2eae908b356b078ba9a088db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1760918400'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c10cb3338a430a2ff28907bb8e87eec0d18b9eda310d3dbee0b9f6e1108bcaaa`  
		Last Modified: Tue, 21 Oct 2025 00:21:24 GMT  
		Size: 49.7 MB (49718167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880de937fe0daa8b9bf0b74f74f3404a7c7fdd98938a21f001d9ba517974f3c7`  
		Last Modified: Tue, 21 Oct 2025 01:55:47 GMT  
		Size: 11.7 MB (11726049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d01b6ee9f8032cac7c0d5e17f2febd49d55e145f37d1086c5e17709b9e33bc0`  
		Last Modified: Tue, 21 Oct 2025 01:55:46 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257d037cae06693a398e9161aa1f82fa60d40614aaf45ae3102d59a774d103d9`  
		Last Modified: Tue, 21 Oct 2025 01:55:46 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e0e37356e8b93e351fd74a317ba735fc94c6371feca671ea9d433434dd24b1`  
		Last Modified: Tue, 21 Oct 2025 01:55:46 GMT  
		Size: 90.1 KB (90126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2dd28a8e9100b90ec217250f4fdd4af671306956746c75f74b7d14a051550e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3587847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f60635734aa507f0cf6475035dfd0d7efa428a0b7d7375d3336838b7614f720`

```dockerfile
```

-	Layers:
	-	`sha256:d3dd834a8d10637eca4eb4d1053049cc0404bd38d80a2112292c857beb55e7c4`  
		Last Modified: Tue, 21 Oct 2025 10:08:56 GMT  
		Size: 3.6 MB (3573928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bfcaa1dca5ee3de58c8fbbb6f6d731be2d8c71ea03c34e5d53323f6531e288e`  
		Last Modified: Tue, 21 Oct 2025 10:08:57 GMT  
		Size: 13.9 KB (13919 bytes)  
		MIME: application/vnd.in-toto+json
