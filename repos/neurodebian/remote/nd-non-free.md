## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:a4aac978f348d599f92c369be37445b4130f56251e5cc2f05f9cae767f2e3fb0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:cc9ff12f4b5c3d5ecdfd1b48e3c6b47017b76e51207fc9b7fd6b869c68ba0833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58743619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862822be5a8d104ca7e83bf6e033220ddad5d73fa1af06fedecf7e124b7b9682`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:06cf5b56eee98058acc2138b22939b094380deece3b7569cb8f72001a1b1ae81 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:5d01f86c265bdcd9ad24686bfb950b1af7886771bc1e983efedb66d6751451de`  
		Last Modified: Thu, 13 Jun 2024 01:28:09 GMT  
		Size: 52.4 MB (52429606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488d6102ee6e2900c71b9c591ea4c218f6a32d1272bd6da65bcbc599bc9a863`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 6.2 MB (6222070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3438d4d4458889db590cc7d2cfe76d021c278e615917bae61ee1ef90da2cf30`  
		Last Modified: Thu, 13 Jun 2024 18:29:07 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1665df950e2dd250967fc5d624ee4c22dacc5cc0086147ec53e62c6eeb2680b`  
		Last Modified: Thu, 13 Jun 2024 18:29:07 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97487b731367d59935e3a898e7186d98bd489b9af72989dceb07689c18e6ecaf`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 89.6 KB (89566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ee1d2c9ff452a433dcd1e416e8781c25075fac9ba5d7ea84abd8e4dcdae1f1`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:24df50af7abd2b00386c7caca5975b2e4315bca816f5f876d091236ad223b0f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd535e3dab140cdf82d3d810e1271f2a0e8a77d648b7528d8feb3f39c6b2e1b3`

```dockerfile
```

-	Layers:
	-	`sha256:3355f373b4915eee06f1f5aac77709ff6974d9729623384ce5dd7d0aa89cbed1`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 3.6 MB (3550050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea2a244515150a346bb9e850b807524c86a2e8dddd67298726cba5b66de21d71`  
		Last Modified: Thu, 13 Jun 2024 18:29:08 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:afc79c7055d268b7a9421be92cad87792fba1ad94968d4946ccfbbeefecb0b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58995481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27c47d587fed9542a94257a86bfe482879229c5d5ca96d11ecb73508339da2d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012a9a0c6fc8e14dbae0dd211be74c76a40a0bdfe55e8fd25532fadc68dea49`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 6.2 MB (6219805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46829409c0895984dd0c82567ac3a739a6cf8e121453008052b2e558d75b2ab`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08328daef7cdf76f8df8778afcbc4c476fef35cd256705e6c768b9ce1033d6a5`  
		Last Modified: Thu, 13 Jun 2024 19:37:58 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99980679ea6d0b863dc5d985d23bdce3df45e1f095ca22b3c2e45a70dbb5f47`  
		Last Modified: Thu, 13 Jun 2024 19:37:59 GMT  
		Size: 90.2 KB (90185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab908a816558985f15055c195cbb0d376fd1c6714e7e54daa161c41e0894a7e`  
		Last Modified: Thu, 13 Jun 2024 19:38:17 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b36a2d46a5120d388857f8ed4c930c3519384b84bd207f5d2f40b62de7c7a8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3566795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02096d9c06f0272564cf0a0bd536a43d85e1ea75de2987b4c6ff82a563329ee9`

```dockerfile
```

-	Layers:
	-	`sha256:1dd93fa599412c7ab21640af88ebae609db25942ee5b55918960f43879886c0d`  
		Last Modified: Thu, 13 Jun 2024 19:38:17 GMT  
		Size: 3.6 MB (3551091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9412b2354d62582e459d224f5786a6e9889640453840203358bfef864104f562`  
		Last Modified: Thu, 13 Jun 2024 19:38:16 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d4bdf1159b48c2ecabc30bce4f3ea3ae73a8a2325c1326d2fbe45e7939f168d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59947750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b40502da47f32b5a185493da2779d36e20e7f4c4747590909e51d36de4b97d6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21de92121739d4fa9675f02b90861a34f4574dc9e316bb0802285d92e4ac9b60`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 6.6 MB (6551627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf96fff31007030f5b9515a1a6aacbd32612b1d07ff9f3c78c1015183eb77672`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62789b7063d2d62b9591fffcf6f696ee77c7bde371b15b61b45647cc1c4139ec`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731f1ad43b355ce70365191a317496e08b26eb26184ca25bb2fccc05ede567bd`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 89.4 KB (89448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9d9e3bebf592f069cd34952600f4fdab904969c316ff205ecbec5fd7e4d7b8`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b8023242e636bf70cbbc9a46cfa11df011120a169a23c971e7b816b8727c27b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3562551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a40003dba26a551eb5404e012d47a3314c68829113f7442897d4a58fd15670`

```dockerfile
```

-	Layers:
	-	`sha256:9116b10c7dc54220fedacf31400461ce9e8ecc63e2359d29a7cfdda20ae5bdc3`  
		Last Modified: Thu, 13 Jun 2024 01:59:28 GMT  
		Size: 3.5 MB (3547149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e85ecd426065713204ad4fcd588935afb2e9b8a8a114098388115cc0ff4755f`  
		Last Modified: Thu, 13 Jun 2024 01:59:27 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json
