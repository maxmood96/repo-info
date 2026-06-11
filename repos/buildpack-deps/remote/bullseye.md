## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:52339530af0d8a799ec69766d5ff8ab0462346586a934fb6fbfe6b5ddfde8540
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c95cd77f441a5bf79d0e52ef7de12351a2ef77ca98f821fc9f817debb7977b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321639496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5935d39f34e1145f66bbfa685b9d30b329cea86cd53dbf6dbf80b0a21ec26fd1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:16:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f53a3a71a19cca6d8312e9c60a5428b23742024a0057b1f0e46517df6ae4a9`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 15.8 MB (15790824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db6c46730caf21fd1b15e0e84732744cb5a66e6931cf2c3753965fc32257fc`  
		Last Modified: Thu, 11 Jun 2026 02:24:52 GMT  
		Size: 54.7 MB (54743048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e50d0d82f87937c72206c32f1786576fb4549351e09e2d42f4b08196308d649`  
		Last Modified: Thu, 11 Jun 2026 03:17:29 GMT  
		Size: 197.3 MB (197333855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b5c810e22dd095e6e4b81ac4ef1ef5a0d1822cb3dbd0885a3b622e05492556b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f545d6a8aab807da9a595d1118ee88cd2fe55412012b57bdc7ef02579711d75`

```dockerfile
```

-	Layers:
	-	`sha256:ede9179da5bbd85cf9bb4417ac78df3bfb140999eb62d3016ea7664a77e93dfe`  
		Last Modified: Thu, 11 Jun 2026 03:17:25 GMT  
		Size: 15.5 MB (15471585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaedf11f9b68f29dec7a86b4fd29f881aea186d9749c17fee3cb7e51d9b2d0ae`  
		Last Modified: Thu, 11 Jun 2026 03:17:24 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:79f5cf9987753894efbed0260efdd3f0066d1c19f3826727485d09d51137ffcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282401087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890635f4f4af426696fb9bac28f947c27ba74317ab360a61d24b7fd60f409930`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:43:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:20:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:057662c04791d47966179d44811cec5af4565f7f7a6a4690c7d8e834d0ba3bd2`  
		Last Modified: Wed, 10 Jun 2026 23:40:48 GMT  
		Size: 49.1 MB (49064004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa240a68c3059c2e50ee1949050052855111d59f6865103a70421028ec0d924`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
		Size: 14.9 MB (14905396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c8d826bdbb6b8ffba198124f6ff94c9cf241cbd4761c9ad97d0feb1a0f3333`  
		Last Modified: Thu, 11 Jun 2026 02:43:52 GMT  
		Size: 50.7 MB (50658997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:703cd3e4780ac097023e574c5d70d53caf447530af3ef5f584975e25bc356179`  
		Last Modified: Thu, 11 Jun 2026 03:21:15 GMT  
		Size: 167.8 MB (167772690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f4a39582683de18263125e88d8a04b27372698af2d321c82216820b8185771f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e436029e3adc5cc69bf67caa26890a62cd3c7d461326f5c62c2c0188b3a7b33`

```dockerfile
```

-	Layers:
	-	`sha256:501167339afb87a31f688ec78cdb1dc2e162cb3c3deef799e8ff44a4a0b7cfaa`  
		Last Modified: Thu, 11 Jun 2026 03:21:12 GMT  
		Size: 15.3 MB (15270903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ed66c3083d0ead2b56d3a8caac2600859467c0b6c70b7b8d251941d034457b`  
		Last Modified: Thu, 11 Jun 2026 03:21:11 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:652d3ff3fb558dbfa4f256baf29849394d8324e23a60306b83324b6230dc9726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313151314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1be494ef64b1a0e15f0f6e73cdec35e9dd3913aa3fba3a7e460e894cb0ac5d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:16:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8698eac281c2783fff44c0d5a2c381eeb273791e12f4dc8b407db26260bc3b85`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 15.8 MB (15774833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd4791f1a451400cf59328cbd4f4f9bed438b89f7103b59dc50338fd2ac9293`  
		Last Modified: Thu, 11 Jun 2026 02:24:59 GMT  
		Size: 54.9 MB (54879555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b9bf79c3a8f4b5133b62d2b5a7a2edf601167140ded4bed2e77325e6485cb6`  
		Last Modified: Thu, 11 Jun 2026 03:16:52 GMT  
		Size: 190.2 MB (190232812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:47b9f53928d34f1b7b9b773c19472ff41c1081960d07ff5656ceaa8b55dd526a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7bc88f8c4601ff3f59b36a6b321c725cfa22cd419e1fc33c32159712dbe700`

```dockerfile
```

-	Layers:
	-	`sha256:cd4d4c6da67e633a9902bed636fe71890a3e81eda03fcfb320a137a7c458957d`  
		Last Modified: Thu, 11 Jun 2026 03:16:47 GMT  
		Size: 15.5 MB (15473530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d81b420b23dd582f474ed074b83c8356fb96f43aee0c1072477b56ed0baf7a37`  
		Last Modified: Thu, 11 Jun 2026 03:16:46 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:658a35046770cdb498fb61461129eaa41b7897d9ef3d6758bb7525c5870057b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327282305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4e22f56456355f148c9510bcc5f56e89d90fe073015c5171254f8b874da8f7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 03:16:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7baf1917f31dc6264a068963cb19f53c4fc1fb3df24b85fb7b1a7235134b9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 16.3 MB (16295657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c66634bc3fa0a0bcd10bde2aef17a8a2d29d8cc303406e191342fab9599745`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 56.0 MB (56047555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680b9a9afe383985f9ac5e211b845598224d8c23f97d9980d6e264b6f15c0345`  
		Last Modified: Thu, 11 Jun 2026 03:17:05 GMT  
		Size: 200.2 MB (200226236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7183299fd5008aa0f969854fd6736b66641116bb4fb8036da68feee6d03821c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f136eb8a9af2872217a33c0ef3bca9b227eb914349497d577faee907a1e7471e`

```dockerfile
```

-	Layers:
	-	`sha256:7dd50882a087f0c99ab8bc00fd2b2bc9a924ade68173cfcb2fd2e9b31f358be3`  
		Last Modified: Thu, 11 Jun 2026 03:17:00 GMT  
		Size: 15.5 MB (15459600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e273d6f97d543790875da38cfdf30e0c94d46433d9f0c57662b18fe2a8d9264`  
		Last Modified: Thu, 11 Jun 2026 03:17:00 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
