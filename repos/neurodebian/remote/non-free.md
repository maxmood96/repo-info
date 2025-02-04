## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:55d0c6121aae7cf9a74c27c05bebdc4bd5867092bdde45d061c88215b68411b2
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
$ docker pull neurodebian@sha256:0675849061bda1b38185c2e1812d727d5b0d1db5ae8f3c09181d39f227ca47b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59635086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d0eb33669da82633d048e56398d2ee12cca1688105f20aaecf564a63e1f25b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63297db49aa1fee77d18a7f692b7b36f85214cbaa7f8a77e111f638aea5edbd0`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 11.2 MB (11232397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30096a8bba85c4ddea6082a5ae4d246978818eb34e1a6355eb305dda4439e502`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9ab318aba0ec0653df3f41df8255bcf221a39e34c2e6e6bcc9f0b537063e7`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986c7651cc110568cd8c25742246a21c09c882a240da263ec1da9e18328d304f`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b55876296936d652efd807c401513a3d8dd9ac97cf2648dbd96a596ef9b97f`  
		Last Modified: Tue, 14 Jan 2025 07:30:22 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:639b93a3d0a313aaeb9b27ca2dcc439bb59d78547e5f285cfe9414b664382a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ab937b993ca5d9b3bcff1bec8f89c63b742ee19d86fe582f2487dfa6468594`

```dockerfile
```

-	Layers:
	-	`sha256:fd87584336d0bf806432fe2e706599ae36e1fffe26cd0655465d6c421edcb895`  
		Last Modified: Tue, 14 Jan 2025 07:30:23 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702c5a800583ddff468432d35aa75855a0c9a8bd4961e8158cf542f3b265fd3f`  
		Last Modified: Tue, 14 Jan 2025 07:30:22 GMT  
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
