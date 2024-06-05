## `neurodebian:jammy-non-free`

```console
$ docker pull neurodebian@sha256:5584fe00790527527c5679545c6571b9aaf85345e9412dc403ebf2b27e499fb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `neurodebian:jammy-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:e7abef41958dd7dee0bae8bdc415b40824f92a6d4ec132396486116992b7b681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33268702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d23bccb9a816ef20f98f4d9b63173c11a283b12820991f11f7115d85a7c5d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb43413ee829cc75026067ac5d778cafafb77917da12b5dec6e0a6447a7f8686`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 3.6 MB (3622639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef34d71f1c9345b38a1e54a91fceb7aeda6c3c0467ea3f9b83f5beee6bb28afc`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f7e8f5f4c30e732d2e22abb93e18bdc0a94b22fa7c33725f6be4f02110ed64`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4507960307afaaeb03a72f97620824aecd40f2cb9e3c423b414a6cd862a7594`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 110.1 KB (110053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111b9057540b39a6b4ed07fd7e9a6a01509e0ba6521ca9b08b2d1d4c91393069`  
		Last Modified: Wed, 05 Jun 2024 02:20:48 GMT  
		Size: 261.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:00e298aa5a60fb2c6ad6308605ac14e42df08b2449ddb03dd6710c33e30104e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b82f8e8554ab34024a8fb1f2871a2f17e9c69ae0cc5729ed7de770b5081321`

```dockerfile
```

-	Layers:
	-	`sha256:b22d44f8413e29ed450460bf31f184eb25021178d345ba4ce95411b57fd319bc`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 2.0 MB (2015694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:583e8e5db7add610c022447326ac812279e0a609b548dac8e3235070b6543a27`  
		Last Modified: Wed, 05 Jun 2024 02:20:47 GMT  
		Size: 15.6 KB (15587 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:jammy-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d9af2f3b13b2f5d03bb2fd4b92ecbe81d5f87ba0f8a081966f3aa8448d656b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.1 MB (31067473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693f25b8d1b0237d5c2b0bedc1f77f9aeb399c27850340c8a2296b93687d03c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ARG RELEASE
# Thu, 02 Feb 2023 17:48:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 02 Feb 2023 17:48:33 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:18035d0a8c59e3306bad4219c71a52b03397fc8f231baf7f676287c73024d85c in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["/bin/bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian jammy main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel jammy main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list; grep -q 'deb .* multiverse$' $srcs || sed -i -e 's,universe *$,universe multiverse,g' $srcs # buildkit
```

-	Layers:
	-	`sha256:d5a2ad729c09fbfdb259ae764f92188efc67a615ffde9bb34a46298d1edf3cd6`  
		Last Modified: Sat, 27 Apr 2024 14:45:36 GMT  
		Size: 27.4 MB (27360530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba218d1d7b661878c14487bced886a52a613db7b35be93fd5606033d2ee7cdb`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 3.6 MB (3594346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5cbb193b892b230325e0954e37f9cc5888e4f5be69eac2c00586f369fa71eed`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b9f9da838e49a37d396367d4f8b41a6efa775664ae714448be35174fb50dc1`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f64b85fb3b544ce5bca4e7f032da3c58413de4c1e771a6265988ed8513dac92`  
		Last Modified: Fri, 31 May 2024 13:53:22 GMT  
		Size: 110.3 KB (110337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae1737456c80f50271ee8ed6f2cb88d6f204acd04347df9fc38a7d026250d73`  
		Last Modified: Fri, 31 May 2024 14:29:20 GMT  
		Size: 262.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:jammy-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:8f3634d3cf9c249f686d1d81b390303829e3649bc6af68eb3c442dd9b434c05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2031816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e90c5a9975aa90b4beade40c3f709ac596ddde44b6c22f6cccebf0f8078416`

```dockerfile
```

-	Layers:
	-	`sha256:9a97e8a9a82f6e5319977b58877ecf19396f43b7c3fc91e69f5c2aaead79be00`  
		Last Modified: Fri, 31 May 2024 14:29:20 GMT  
		Size: 2.0 MB (2015953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:837d0f5db9bb40ab8ea99d0fd66ff3f8a7349fa95cb3d5a508ea6d872afc7a7f`  
		Last Modified: Fri, 31 May 2024 14:29:20 GMT  
		Size: 15.9 KB (15863 bytes)  
		MIME: application/vnd.in-toto+json
