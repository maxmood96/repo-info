## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:e7c6f8577a483db6d30fa4a4bdc6045b24e9ad353ae5a2eb8101477da849134e
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
$ docker pull neurodebian@sha256:b16595e63ba04c7e0841c6967c6836bc323e3a4f5be5775016b435463d05f118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59722181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3bcb7fbca38c758f45c29940aa0046dd2fb52c05d76557f8965ad6d75e7ec9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:c6dd4b778062640e2abc4c889c6db9feecceff7f28c2100dcfa570652558218c`  
		Last Modified: Tue, 12 Nov 2024 00:54:59 GMT  
		Size: 53.3 MB (53319444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04acb53059fdb56a81917ae63844cdc7d1347befaf6268afc454c8f14eedbe1c`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 6.3 MB (6308926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849966c7cdea3eccdafc1d6f151deceacbe76414ee9110113000a38ca53de21e`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26889570a7c30127539f0f09b14a7a97160478527741986bb26dc5cbefe5d9ae`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dca83d71667f3556e88dde7a6b401f7d3161e58440d39fe177b3e08f509230`  
		Last Modified: Tue, 12 Nov 2024 02:39:31 GMT  
		Size: 91.4 KB (91430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7adabfd3ac898c58a22effd512bc9f3414a90bc969291ac6bb76d624c77642`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b7bbb2d989aaa50bba0d13101afa86023116fc26198c91c5d7650b59a33f3483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5171bcb6e91aac1dbe42a490166691bded29cccec6ccc2b3411ad3adf080d95`

```dockerfile
```

-	Layers:
	-	`sha256:c8e7df85f0ba147ed47c2f2de77ce911bbb23317845db0121bebbc88b3b1a936`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 3.6 MB (3566734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf55523d3adeb0ad34254cb09aeea051639378dc2450e32dfe5fe84e4a49b96e`  
		Last Modified: Tue, 12 Nov 2024 02:39:32 GMT  
		Size: 15.7 KB (15653 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e9b1dc92def9b23d4147b701479a4c0cb4287a99fded2945d0f6141c918d1718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59997190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e1d085caeb9723f2e7d1685e044ddfd1251b756793da9068dc8ef89912c923`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:58acae53f12429504dea737cd60eba46c5f2eea862974a8d8fe218c17d285565 in / 
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
	-	`sha256:d246237d395a465ccb5ede6b1a321d43a78766a62bc93015a0368a88624aedff`  
		Last Modified: Thu, 17 Oct 2024 01:15:57 GMT  
		Size: 53.6 MB (53629485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c4d641255ff6bd7b8ce630c8cf947966d1ff05bdf86f951c687f989e2f5e9`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 6.3 MB (6273546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c25f32db1b1126487143c75b9ce0d496e410c5bae14e76068c7767c3979041`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1aa1fca4ed404a2dafbd083628f990869ee0dd7b253df1199afbf67da6e338`  
		Last Modified: Thu, 17 Oct 2024 13:32:40 GMT  
		Size: 239.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4cc25b7109f5af55ff37456e9f7fe94f979dff175b36667bc066bff22439`  
		Last Modified: Thu, 17 Oct 2024 13:32:41 GMT  
		Size: 91.8 KB (91781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376ca4ce57be9758785676dd94566197e97b56e273d0d68b507106d5fb088f89`  
		Last Modified: Thu, 17 Oct 2024 13:32:59 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dbb9f5c6a73482e60b6f663408c48da9384405cc218fc0247429a4db9e0a0c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3546522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f10c7d37e9b03e2031feb3ef71d8d1bf5349441266305f933b01c78e258c35c`

```dockerfile
```

-	Layers:
	-	`sha256:ae362c8599903d2c6f23db6caf041eec1d93bdbc004c5115130317bed59a413e`  
		Last Modified: Thu, 17 Oct 2024 13:33:00 GMT  
		Size: 3.5 MB (3530921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857190c4726e7bbad6a89b69d081e58436891e0510c537d4d585edd56bfece2d`  
		Last Modified: Thu, 17 Oct 2024 13:32:59 GMT  
		Size: 15.6 KB (15601 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:8845c7ed5b6d8416f9855b7bfe27a19c7d30aa28d292315ceed1208b3ba010be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60922100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2cac8eb5ab9ea391b78bf58b3009c37226156e61983dfa3bd713767973d918`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD rootfs.tar.xz / # buildkit
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
	-	`sha256:266f316e766c7029b1cbb65159b6d9ea1da28d00e28cf109ea069ce95b082ac4`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 54.2 MB (54192046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f05d044e3c2e56e20b7d8664005a131b7f0db158a0815b6ce0e963cd6fc766`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 6.6 MB (6636013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86351738a6ffd8a98282b090108718fd6e1ae2e9844a2af0c0b0b965a02b723`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41ebda76b66a81c0a7173531a24d7eec966e7980ae07fe7c2a526d7a84a9f4e`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8339bbf5071f7546c5f224a122b1523ae558568d2167e052f3abc925bee431b2`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 91.7 KB (91668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413c486f7d7508fe28152d1b0353e06c91d1945ce06dbc30755b3ed9bd998394`  
		Last Modified: Tue, 12 Nov 2024 02:39:21 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ed502b06a74350a876c7e6c61711adf51a489f6579f09b02125da12abe3671dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3579592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efff5e3a11aa6528b0e441f116da4e6a7ea7cfa2b827b2ee6bf07ee16edd5c2e`

```dockerfile
```

-	Layers:
	-	`sha256:4cfa1d9dd39b3ed912815c7fab75213e74f763e42cfa2c1a7046c7eee356f07b`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 3.6 MB (3563970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16276af2d35957766d2b5863e3a7e6f54e9ff3d186ef0347471d7e811660d184`  
		Last Modified: Tue, 12 Nov 2024 02:39:20 GMT  
		Size: 15.6 KB (15622 bytes)  
		MIME: application/vnd.in-toto+json
