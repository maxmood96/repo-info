## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:adeee7665a100d8ae114f76573fdf2804a9950abb8d6f1af6580e0e87a1ddad9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 5
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:5238cfe08865e6d220ee2e441d2a11b4dd3876aebfe8934d3ae847a062d39a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (60049648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5fd9cf60415cc4d6a2e41b0ecb799b45050a2b735d4684059251269f304fcb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
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
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e371f96dcd488dcca9b548ef17888a30c45ce4185fb64de3935db57cdd0f075e`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 7.3 MB (7313276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663cae23bb39c60559275df0410ebcaacba26c9c421222281f939ee17f70d9a2`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf7d3a1037ce374991daccf4e28eea64df1abe8c4db782678a283235875aa22`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962fd9f4dfaf26a175b8d9be95478724907ec51e80476cb047611792164825e1`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 91.1 KB (91096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a48833da318e61e1c29dc561a729bbdb2297e59817a9dce4d792c1a03cf48dc`  
		Last Modified: Fri, 31 May 2024 00:57:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3932fe7a10c4ef043d4b16430814bb2f7593eb20a6a5f9e64f1a2ce9ca2961e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300a524f0ae3b5ca164f2d6494e49f4b28b5c83b20dc6b0e9e4e0b63d64a34b2`

```dockerfile
```

-	Layers:
	-	`sha256:d3daceb491c6e32ec20d264ba220ecf8d90a01111f4e1ef6b3395d3f0ab10f05`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 3.6 MB (3592195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce8579bbeb70277e1ebec780493f9a3677213b182e3859b373d3843ac4fa3485`  
		Last Modified: Fri, 31 May 2024 00:57:02 GMT  
		Size: 15.4 KB (15380 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:a1ee8d1689c95e098753ce53088f14e6e9c3b37cdbdb33ac55da81b428cac8a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65424251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368fd79da7031ba430b0e81529a14baa87001b24dbacde5eb4ed4355922155b8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:41 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Tue, 14 May 2024 00:40:42 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:16:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:16:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Tue, 14 May 2024 03:16:22 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Tue, 14 May 2024 03:16:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:16:30 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d28a39104fd5e32ed412e20d214a05f37a1a4ec16fb97a9a449a83e52258347`  
		Last Modified: Tue, 14 May 2024 03:17:55 GMT  
		Size: 12.2 MB (12203403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e345603e50bdc3be68723503e6942f8482e09b422addd688b37650872fd3d672`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429d4647eb3dc1619353f3cc8078aae3ebf270c3f47cb280e016725bd6fda0aa`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c81171b646346b09db33a14c3712df0f0f1ed3e82d9c5186dbf349c927fa9d`  
		Last Modified: Tue, 14 May 2024 03:17:54 GMT  
		Size: 288.2 KB (288160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c8f72e79a9004504393febbe104203e1e6c31e0a2de069ac2d6593e422a142`  
		Last Modified: Tue, 14 May 2024 03:18:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:7c77d4afec0b7c9e461398593995b8ed5e5568a016cc6078ea918d9807f54d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61373014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220c4273ea358e21916d7f610f12604cb7577ce9f0c4040b350753aafdb5dc4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:e7eb6b079b0eae2716a306dfd153c88de0766961cbb0cbc2499648abc3b7bb7d in / 
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
	-	`sha256:241b052c0f57772eb9a56c460c88c133545f781291832042a8e20e0fd5b01591`  
		Last Modified: Tue, 14 May 2024 00:54:59 GMT  
		Size: 53.5 MB (53539918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb2f8ec404cffd4f14759ea97853a3b5a91ea6fbf30cf868835b5d935963a8`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 7.7 MB (7739743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c87467765b5a37d61c04f087fa4e848e9329b99d686598d39b5116fa5232719`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d437e53f6c88aa2bd8a128238d49ffaebc152071e70ee972cb11c32296bd7ae`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146d22fc98dfb67b9d330aa518112ef1c4607a6de2bb6f141381e9e11e29a3c6`  
		Last Modified: Fri, 31 May 2024 00:57:05 GMT  
		Size: 91.0 KB (90976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fffba9e15e6e6d0aabbd140cb4989396f341c9e95c75a92351b7618cd4ce97`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:2141972320a5e82e7db799456ca50080a0768896fe467ee27f51f8e233a19398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9773ae4175cc1dd62c870995193ee697ecd39082c7150f2361a00f293dd566a`

```dockerfile
```

-	Layers:
	-	`sha256:80e582e07e65a4fa60ede91236fea9e79fe11d0ee18ddc17a633163467b170d9`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 3.6 MB (3589291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f5c095cba44c0904acbdb19051fcf2ad4e495b03d4c1153340fb84674d9a8b4`  
		Last Modified: Fri, 31 May 2024 00:57:04 GMT  
		Size: 15.4 KB (15352 bytes)  
		MIME: application/vnd.in-toto+json
