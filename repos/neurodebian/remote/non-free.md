## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:2d7188de13759391a284f061e3db0f4e06ec535f9208d8084c7e13bb94e0f6c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5c667bad9f0331d8d1e04c8543c9f933714a78a6dde5c14ee356c97b5cb3d6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59842100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d92edea6f76f954dc63a9ecc22376ac5f4ef7000b9d31f4c11e582f0deb887c9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 01:36:22 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c624e4a384ad34078bfa6758d673f603849df0e861e8a500d469cb00188f7b17`  
		Last Modified: Tue, 04 Feb 2025 04:25:25 GMT  
		Size: 11.3 MB (11266841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5fb56a342c339fd7c5892a2a8416640b92bdbd82576e1855ab59c7cbf84f3c`  
		Last Modified: Tue, 04 Feb 2025 04:25:25 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee6d33d3878b23c3a2b65595f53a3aaded314694f19344ce9e18ef3e77f50c6`  
		Last Modified: Tue, 04 Feb 2025 04:25:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653d1a9c76eb8778002403eecd83bda034bc3cab2c78bcea682cba2490063a68`  
		Last Modified: Tue, 04 Feb 2025 04:25:25 GMT  
		Size: 93.2 KB (93159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601898ac19aecfc8074819331796ae72b0cc5536ce1e6bb35e8a7d264d794ab1`  
		Last Modified: Tue, 04 Feb 2025 04:25:26 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fb2e463193d715c2f18a8b8dfa04ae4c334fe0dba9444b8da092e70a04f7b427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15653a5e95238fdce1e9d051c5b08f1254fcfb08b44bf24d0f5b91aea41040ce`

```dockerfile
```

-	Layers:
	-	`sha256:3f1c03f180c8b671064428405d7bca75d874ca3e90b0fe826c82fdb62ca7ca55`  
		Last Modified: Tue, 04 Feb 2025 04:25:25 GMT  
		Size: 3.9 MB (3932850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca674673e56372c8739f1f2c3834e201211376b1bcb0a79718ff787835478be`  
		Last Modified: Tue, 04 Feb 2025 04:25:25 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8cd5e6b7bec8b2fb545404fa4ef6bd502469cf4951c316d6e6279f2853160096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59634890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4830671f1f42f572e6707b244573102e521ead223e96423ff85026ae06f25297`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 01:37:39 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0890be792eb8cf2c454fe7c038fba6da83a8ef251447a532fa6d4f3108c2f7`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 11.2 MB (11232504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f99eec1b3a608d28ef329abdd58a2e25ee524c0453b1269a4668003e0983d49`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86127ee86de4c4cff8e4bdd5c18c3f9d3021d01a9a46fb1e63a786d3c5abab3`  
		Last Modified: Tue, 04 Feb 2025 10:14:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cd76384f78a868cb30bf0b964090aebaad99664c593dc1fcb7897c3ca2af13`  
		Last Modified: Tue, 04 Feb 2025 10:14:53 GMT  
		Size: 93.4 KB (93414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04417613519d31f6f792cca8327cad6db9d5664fb6531c5c94f92801518ff51d`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d5ca00e53e65addbf1adf8782ccd07719cda0df67061120dae1afa0773d8cf40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6e6e0a88411798e9de89e740aec9110aa51198ec12d4d77b9188f3b5d0ab85a`

```dockerfile
```

-	Layers:
	-	`sha256:2c9e1237745fd9d27f596daf590b01f333c1e6ed5054993d33f0533e77edc71e`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3978024698224d9e7ae7a49ba553a6391e10f049df270264dacc9a5d2e8d971`  
		Last Modified: Tue, 04 Feb 2025 10:15:07 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:5c12c4e75d70fa5dbc1c1fa0e10fcc38f47b86b84ff3adc777952012f2a42634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf2bd1bfa500e74cfdc4ba352d6f2156d4464036832326ae63d951ef4368c18`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:d6abb78404200438eb560450e089a4e7707a23d5ec913df260500d902666670a`  
		Last Modified: Tue, 04 Feb 2025 01:36:35 GMT  
		Size: 49.5 MB (49457456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0fc3eb9cbdd38cd5e41219f2cf183331f8ea286674a684bd89a77fcaed6e16`  
		Last Modified: Tue, 04 Feb 2025 04:37:28 GMT  
		Size: 11.7 MB (11688906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3bbc19666d7b9185379a9ffcee26785019dd6a0f8528571079622b8938a80a`  
		Last Modified: Tue, 04 Feb 2025 04:37:28 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e195c9a5c37aba66e546e538394168c90623235ca50fe3ef13812aab6d698f6`  
		Last Modified: Tue, 04 Feb 2025 04:37:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e781d700c8d03ddf1679900081fd8019c6ce99420528c2945f27aeca34a434`  
		Last Modified: Tue, 04 Feb 2025 04:37:28 GMT  
		Size: 93.2 KB (93225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa1de705767adf458c047c12be1bb52f838e88187ce6a3393ec5c3071e8b01f`  
		Last Modified: Tue, 04 Feb 2025 04:37:28 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e0e7bf9bcd29ebb50166b0a6b2958aeff2806670d7e329437fdd616e5a44bc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e84440d7a041fe4921dd6d730605a51682736fc763580090cc7327b5dd9ef2`

```dockerfile
```

-	Layers:
	-	`sha256:81083588bda8736adfef4644ce3066300d6aa97735b45c258ffd8c178a246754`  
		Last Modified: Tue, 04 Feb 2025 04:37:28 GMT  
		Size: 3.9 MB (3930767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91a41c92ed09560de51dd2b3bbdebf9df757878b6e5e174821082fc7e3855c66`  
		Last Modified: Tue, 04 Feb 2025 04:37:28 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
