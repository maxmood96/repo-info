## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:d8499e8b46e0655ce15feb736d6646f4c0a2128e80279004b66f993ad841db46
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
$ docker pull neurodebian@sha256:73aa7beb900b2b857f3c4e97b3768980b2e079cefb4fd543c9ca356573ab6caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64978762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbf106e61f2132667a8e9ac996027d6929275f246acd22030c0255eff5946b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:40 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:40 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:40 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3a4f7cc0717582c2f3c6148a1e85b8dac860ba9d316c50151e8fc2dcf24e33`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 11.1 MB (11103447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16f0eefbaae0196bde0bf762bda663256e23157799b4e3139952d3cc719550d`  
		Last Modified: Thu, 11 Jun 2026 00:45:50 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789b4402e52242b672cbe6b5b1a6387c64225f3e55c7450e3f117d1d68f9dec4`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e70122fd1bac8ad54f5ade4c5092064824cb18e49265fabdd64d5cc7e546655`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 101.4 KB (101389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a16eeb6ef64d1a380b22a910ea4466843a9d8e0f3b95a548601375bbac95335c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe56286e7a99287cff1ae93f70f0f65b90bd59b20187c884659a3c9f2e62b003`

```dockerfile
```

-	Layers:
	-	`sha256:178a957cbfb1c5b27a4238fdac26baba7e17da0c95f747fa841d4bbb582e2b7f`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 4.4 MB (4367918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725bab1b25497fd016971b729a2493af95f6dfe7858e00793b91ae2aaa7bc0ed`  
		Last Modified: Thu, 11 Jun 2026 00:45:51 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0964dc7edd5968e5463c8d308c19bc81457bd15b028ad513be5b3ec1450b1d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63477463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbb8774384c869137df0894a6ace3cbb906552911f2524f6c7421c055e7d476`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:47:18 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:47:19 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:47:19 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:47:21 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2478139d0786de2aee4b1dcaa1cf029f85acd978f95dbfa7a0aacc5c3057f1f2`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 11.1 MB (11109904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286b2901c8bad4d6c2369e254e93ed71f6cefce38556113f956fc7fc4fecc1b1`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4971bc72e136ea404c0dcf45d3e13567288c6c38674c9bd86aa34eacb2c4570e`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9ece72ba9b9f5b1452547498613d7bfa4b34c414087b11fa187117c2bc2818`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 101.3 KB (101286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:a82b1f17237127ba4ca6fc91917e6549e7c67760c9982aea3d9ad90906584677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:971afaf909e83b24a05309f9b3a950507ee08ca4c48135c1a0ff7bb0da5c5931`

```dockerfile
```

-	Layers:
	-	`sha256:14a53dd714448eace56b3c2cb11cd120d635a97615facfdfdd8073942f9a591d`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 4.4 MB (4367525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946581dc6b334d33c918daa2c33425c1e15a95bc39d3352f86420a0c7d647450`  
		Last Modified: Thu, 11 Jun 2026 00:47:32 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:177001282dc54d461853f07708f22f134ad2ba848f6605cb73a8bcf511cdf9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66318635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfbead96266eabcb3e6dc47637e716f6c315f017b4a198c61f81202ee285ab0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:45:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:45:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Thu, 11 Jun 2026 00:45:34 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 11 Jun 2026 00:45:36 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de40a8efdbb710eeeb369826e1a843a9c7ca4cedc5830be54bec9a4c04821d8`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 11.5 MB (11502372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035a7ead740086997dcaf6944ceafe496330e0f19f6dd3b1c5da4cca8c1c93c1`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0bb1942aed2f10b661ee389529e90a2c3382ee9b8352495bb9f8e15036bafa`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e1266b6a8fdb893c7711ff9efa76426630140426fe129839b84e775d9d6321`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 101.2 KB (101249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:c5016b6665cebe115adc388bf52b0f549711f8986423f177ed551138732afcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574b0780e44a485315b1a3b753bd3604de4cca26a68462267b4fcb172f659235`

```dockerfile
```

-	Layers:
	-	`sha256:3ed797e12ca446c70d177753899e05649a218c9caeafa78589ab38aabc867c83`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 4.4 MB (4364437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73493f351af6e15279a38dcc882e04149790290a41966ef74581934d4d7dea0b`  
		Last Modified: Thu, 11 Jun 2026 00:45:44 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json
