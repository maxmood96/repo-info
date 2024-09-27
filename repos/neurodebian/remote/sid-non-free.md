## `neurodebian:sid-non-free`

```console
$ docker pull neurodebian@sha256:731de48ca965761c5f70fc325db8387052984f3c29bee7b25a5e05db163302ac
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
$ docker pull neurodebian@sha256:d6385e1c5bb68d77f40e026ed12ce430380e0e470b79c3f5ccfcaefc931a7b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59631607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e776c45bc6971cf609f11e7627976f0cfe662728ec87d1d886c00188c57a3a0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9932c03d465e07be767be6c6546a5fed0a8b713450009a5ae5548c52bc48a318`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 6.3 MB (6287955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa69fe5d2dbb347bcff9484d062465fb6e89f3a62b98b0ff196ed4d6799f673`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a23af6f8797bbef0455d9cd57276520bb04a5171c6203bc5a5ab3d4c88811a`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7138d16f6eeae6939426514f30129bb8016e17c4b9a24883b9440e1353b605`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 91.2 KB (91238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7203ca1b15919f54f52922c71b014e2624ac6f086d13bc8f501cb8858bbd344d`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:465aeca1f63b6dc525b5632ac6eea79aab7b6e34c2630a00249831526eda91d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3557498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4661d626714f88f865b4ae67b6b9f36d1602de01880fa1be9dfbfbd03c8d6cd`

```dockerfile
```

-	Layers:
	-	`sha256:e3e8d0820b5babfaf76c87b38d941bf58eb80d5250a65992b20ba00063fb637b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 3.5 MB (3542069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a65c24b8306901ac0ef9a25e84ad3f7abf256dc28c444897f5eea6145f6e792b`  
		Last Modified: Fri, 27 Sep 2024 06:01:59 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:61b1335fe95c43cbba5331e564ed344d9a1117fadb9f2d8b7e9cda08ef005df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59939738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bb4b41d27fe8f8f38614f5f9d18334ac64546deb807d9c24f9a8bc2e7d6994`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b8e117af2c2835c43068cfc9561a100b4a2ded0418c44e6deb66f2d0a088ee52 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c86b9ce17f63a085a98e1dec4b1098c61e3e6ddd530e88cc0814e54f39b2ffd3`  
		Last Modified: Wed, 04 Sep 2024 21:43:55 GMT  
		Size: 53.6 MB (53597233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408855a53c5bbe2210b3acb92872348f336eed207c1fd565aa9a1894ae3360d7`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 6.2 MB (6248358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513957bcba9f74ca0a80d4f0d2a013c85dedaca9c3d7851562387b57f917f6d2`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b06fa225e64f5f4e0e613985a5fad9decc48bec4c0f6976a7c73a3096c5526`  
		Last Modified: Thu, 05 Sep 2024 12:38:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda73a6bab6cbe0f0ae9577ec42d105d5e08ef05319ea5926169e01c3432901`  
		Last Modified: Thu, 05 Sep 2024 12:38:02 GMT  
		Size: 91.8 KB (91770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f516d23c8c2424b41423a5203bfe7ee2dc27bf78f1d423bfaec155350b83b067`  
		Last Modified: Thu, 05 Sep 2024 12:38:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:5abfd6e5ca6a2a3a60e3fc06b0a35c972fd31f3d60e35f3768dad4b3d718edaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b783683a14f28eebc05c5436416cd4da84c4587b6c3d69deb4e3b1e9e7997a`

```dockerfile
```

-	Layers:
	-	`sha256:cb59bdc05b436dafa348c7fe82a7d452321c84d9ae796567c4450919ca49b515`  
		Last Modified: Thu, 05 Sep 2024 12:38:23 GMT  
		Size: 3.5 MB (3533538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94fe3d7fc11ba1ba4aaafdb2d86aa83d27096203ad2c8924782d0df67b3d4a1`  
		Last Modified: Thu, 05 Sep 2024 12:38:22 GMT  
		Size: 15.7 KB (15704 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:6bf4e8373e3f6f87febe8b3d0319f5eae2cbcf139f17280c044d49b1e17ee457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60787647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9459a6b567f0d06c3aea1dd09d4385c4b2baaa27e9efbf9cf5d9c421d9fc8f84`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143cefad1d4d9c4b8fd3771c226b9090a09e67f6afcd789097a49ddb1f5932ba`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 6.6 MB (6616300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a977207288632e8201bfaa72034a65eb6f6ec8e61ff6b653d4fb73cf84ccc1d1`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105d3548d214af15c097f1d54ad01ceb9ede39ebdea69818d3e71bc47b2839f7`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769ecbf94961298ff7e98bf0aa70190a17384c3bb8a9f690579e7c6fb520481`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 91.2 KB (91162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9019696d4316f86af9fd804eb7624e648250c6fa998fed26656d8c9a25ff33`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0f672898bb01b946177bbaccbffa0299ab4816defdfd5e2b5087ac9572102657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3554563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32aad4c936608553494658612be8bda4f99b108cea7bf09723c1e5efa39b98e6`

```dockerfile
```

-	Layers:
	-	`sha256:838300a747539cfb1dbc0eff0c046248c8620cf10416eaed02824c77f7b7cf3e`  
		Last Modified: Fri, 27 Sep 2024 09:04:36 GMT  
		Size: 3.5 MB (3539161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0678c291feb069de787e1099a828f38de4639e00c1c427de8e71d86ea3d06b98`  
		Last Modified: Fri, 27 Sep 2024 09:04:35 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json
