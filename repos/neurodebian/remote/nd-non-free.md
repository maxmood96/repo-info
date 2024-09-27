## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:ba48eba3960765f9ccfea266dbdcdd86d7969d5deed37f153a35fb3c3222ec48
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

### `neurodebian:nd-non-free` - unknown; unknown

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

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8405eb81d4fb50f2e0ca8052e64751a2166bc5f44bd91dfd5f8364928076fca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59959165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789b6fc36a6afd9830924df899db96464eff91a08d2fd009cb9b3d1088a5325f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
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
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1707618fa9372fa7563234001ca06291da815e7c963e11719d290dcc36218024`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 6.3 MB (6270740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9f92dac85afbe3987da72fdcff7499ef9a4bef39d0ea83f70ad579e421b2b1`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560ef25c1ef36b5b05dc1fd297de1698589349e5c080811754da6ab61635771b`  
		Last Modified: Fri, 27 Sep 2024 15:30:28 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c67a14658f20791e7bebae65768af2451f13d17e95b1fa2ffbcd886802abb3b`  
		Last Modified: Fri, 27 Sep 2024 15:30:29 GMT  
		Size: 91.8 KB (91783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed1a0ff889a3d19ad950be2e4cb5a585ad9f69009887c6d58da8a5f7bfb5ed`  
		Last Modified: Fri, 27 Sep 2024 15:30:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0a0fb2b4c94881a145a88d8cc5d383cc5abffb8759ae1bbce2a56aa27dcc36e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fea4b5d7ea7ed8b0f6ce474f3f3263dd4b2b04738558dccdd3a704db4e1b350`

```dockerfile
```

-	Layers:
	-	`sha256:0b580fb68668f72246a5b77f9ceab789100d2ab9171a59039e674ffc2dafe1b0`  
		Last Modified: Fri, 27 Sep 2024 15:30:51 GMT  
		Size: 3.5 MB (3543111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37ccb2a5d05b136f255c231e5f7370718d916c8cee58b2a409d354d4a1fc598a`  
		Last Modified: Fri, 27 Sep 2024 15:30:50 GMT  
		Size: 15.7 KB (15703 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

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

### `neurodebian:nd-non-free` - unknown; unknown

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
