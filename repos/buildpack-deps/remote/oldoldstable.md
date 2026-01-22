## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:787f88bc5dadf7f720c7ac347d7ae6d21a34051e53fefb2211464113b8a8ea83
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

### `buildpack-deps:oldoldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:076bb4332e04b3845e4c8a99c011a6c4ffec3ae6b597895e413b5cdccb071062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321494099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbddff2746852e69bc9d9918b2e6b15df6064eed96accf96cf6736c28da51248`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:46:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fccfc62cb15165379a658b98df1680b95e3908f69adc8e7176a095a7b4cf2106`  
		Last Modified: Tue, 13 Jan 2026 00:41:36 GMT  
		Size: 53.8 MB (53756446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24af405f2300f6988a2a2eaae4ec7393c0f9119fea3a400a1864fa5905a9bb66`  
		Last Modified: Tue, 13 Jan 2026 02:09:22 GMT  
		Size: 15.8 MB (15764316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91529b594c86b803d1ccddf4f9d27516e8577c5b27e466be4f89f3a15da8944`  
		Last Modified: Tue, 13 Jan 2026 03:53:36 GMT  
		Size: 54.8 MB (54755833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7faeb084d4ee23cb74164108fc63b81b8d1ee30a494ecc31d02fe53f3fec08`  
		Last Modified: Tue, 13 Jan 2026 05:25:25 GMT  
		Size: 197.2 MB (197217504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a48a81937452fc02c032f3ec8dc652a38bca60c8994477025f43dd2231831eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbdf052abf34fa141e82aec98e1eb83ee08fe7a7991529db86593d5ed34f47a`

```dockerfile
```

-	Layers:
	-	`sha256:5ab485a855c5cd3669ed24b0b1dd1fc314f2bffdbeb610925043cdebabf8a5a3`  
		Last Modified: Tue, 13 Jan 2026 07:42:48 GMT  
		Size: 15.5 MB (15462226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb043aab655aaf406e96c045c8ecfc2fec6cc7dbb5f587a04e25781d1417e889`  
		Last Modified: Tue, 13 Jan 2026 07:42:49 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6f9a2e4e9ed9af5147715434b0019e9d02f8974bf818d0e50f54204e64dc3302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.2 MB (282200090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac2161adb2146d09c586556caae20c4897edf2616d9e08f4b0f8be7708205e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:57:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:15:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d86a038b54ede2ada385178a3a13e9fc7833f9952c07b251c404c3aa117dcd4`  
		Last Modified: Tue, 13 Jan 2026 00:41:24 GMT  
		Size: 49.0 MB (49046458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd38532089c34c92931050565b084061d36d5f2907633b524122c2d6f089b42a`  
		Last Modified: Tue, 13 Jan 2026 02:57:35 GMT  
		Size: 14.9 MB (14879656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e704ca674385fc92cb2832f27a6cfada2b1b4e440bed4c77bded017641bb11e1`  
		Last Modified: Tue, 13 Jan 2026 04:25:10 GMT  
		Size: 50.6 MB (50630568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fb78f7d484f57f4d1e2674d8385a6277b814bb5c23d2592e3dc2290d02b25a`  
		Last Modified: Tue, 13 Jan 2026 05:36:40 GMT  
		Size: 167.6 MB (167643408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9c0b32cb55832eb301319ed91067f3cb883a8727c490328a9fee866eea9a56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bcaa292f60f1022ab94d1428b4340d6b71dc8e7857f4579662f879903f4b6d8`

```dockerfile
```

-	Layers:
	-	`sha256:21bd7325767ba3030655a821e0c84b8d2b6f4b12589f5b6f525a70f9d605627f`  
		Last Modified: Tue, 13 Jan 2026 05:16:10 GMT  
		Size: 15.3 MB (15261544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2604e4dbd60431515262b048288b80d00de5194b6c0b0faf93a65f9383a45784`  
		Last Modified: Tue, 13 Jan 2026 05:16:10 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:de837b66e6835407886d4c6f0ea21590ef3857a198a70aedce433cebec8b8df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (313008721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65029a5a9235b10fdc0aba7134f7dd657ebc55e72df5f2ba8298002b8969a091`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:13:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:56:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:49:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6280b099c5251ca1a2b55e8af5af4da252bad1f89325ba7a8344f2dea14e67`  
		Last Modified: Tue, 13 Jan 2026 02:13:33 GMT  
		Size: 15.7 MB (15749667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:735b68aa807ef231d58e7459ca83cac377da9d7f71d24a498190598a342d5bac`  
		Last Modified: Tue, 13 Jan 2026 03:57:13 GMT  
		Size: 54.9 MB (54863508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2705808e73b5ce7c5ea71a03de0f42c7ecdec94b51ae96443064253dcbeaea6c`  
		Last Modified: Tue, 13 Jan 2026 04:50:04 GMT  
		Size: 190.1 MB (190137777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:943f95df8421cbc06e1ccea0aa13cac7d01f32f78a81a4d94ac85b2dc90082c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15474445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c514675cb7c7b601f6be73ecd12035dd7b3ee2c8f8ad891406529a698524ea`

```dockerfile
```

-	Layers:
	-	`sha256:49281b0d42729cce10338c6c976a22242f1460efc455f33243f29cc81f295f12`  
		Last Modified: Tue, 13 Jan 2026 08:20:42 GMT  
		Size: 15.5 MB (15464171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffe3feb7a3685c03c08281f8d2572d7bb6ad44a6c6d62f2450b378926e775491`  
		Last Modified: Tue, 13 Jan 2026 08:20:43 GMT  
		Size: 10.3 KB (10274 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a5ef1072653db25e396cfc0d685a4819b0c22e02cd579ed834f33d895e168b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327129462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a06d72fbaeb914200ef467b3dd4110e4c2ddacc8d2b4830ab7a514dafd3049`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:53:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7e115d265636fc6da528c1f4977e22baefb0bae7061ada6dba677a290e83b246`  
		Last Modified: Tue, 13 Jan 2026 00:41:26 GMT  
		Size: 54.7 MB (54699638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ed43d5d71f701abde2a62df95258edf0ac9ef3046d49ca25c0f30e57af2985`  
		Last Modified: Tue, 13 Jan 2026 02:02:38 GMT  
		Size: 16.3 MB (16267780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50309e354294a6f81ebf1bf80c4203a79bc9374449993f7fb52ebf0640408262`  
		Last Modified: Tue, 13 Jan 2026 03:03:46 GMT  
		Size: 56.0 MB (56048907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad7ad875273afc9f1824115dad6d50ae84fba747da8a0b124f82d730bcb8bae`  
		Last Modified: Tue, 13 Jan 2026 03:53:40 GMT  
		Size: 200.1 MB (200113137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:637b9b6e5d83e02b33457d3a28ecd2d70f215fc1bcc96de03f2ebbdba40be067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c7f9e72e7b42ec1b2549ba1ea8f167d0baea66bc0494d87afe735429b777f98`

```dockerfile
```

-	Layers:
	-	`sha256:0d5dbd9c424a60e680a31a2550374d9d74c9e1cc3403249b5e17546d3b1b5856`  
		Last Modified: Tue, 13 Jan 2026 05:22:50 GMT  
		Size: 15.5 MB (15450241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a97f7cab03dc1f50f6ae592ccb5f186296b7cf75d0a4ef3fa85a6bfa854cdb8`  
		Last Modified: Tue, 13 Jan 2026 03:53:33 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json
