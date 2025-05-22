## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:4f61a2ae007b0cf3e383439bcebbdc6f9b535fc8ea709473287039834b7916fd
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
$ docker pull buildpack-deps@sha256:ecad7f4cee212d977ec6723ebb6439f3a30baf21fee87a2dadd4f35c907f4eb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.4 MB (321406272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b47255adb10573aad27547e97fd5e160bbdef7c573c3246c0e512127c1d55b3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Wed, 21 May 2025 22:27:58 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6c820e694a6c19c297492ef4009391c7dfc83ecae735895f31a89e78b31fc`  
		Last Modified: Wed, 21 May 2025 23:20:29 GMT  
		Size: 15.8 MB (15764874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a69a02035012d2783a66ac7ecc549af09c1718d81affa5f9c39abcf969da971`  
		Last Modified: Wed, 21 May 2025 23:37:39 GMT  
		Size: 54.8 MB (54757308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94932625c5ab18ebb7640ecd70dd33061ba90cc7666b7ff06042a8bd7cf63fb`  
		Last Modified: Thu, 22 May 2025 00:12:38 GMT  
		Size: 197.1 MB (197133895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b94390f64ea793c8da147528138bcc2e4276f2cd401c284ea285b64716e2de77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15183304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6be73f0ce111365c0b6c9e14fad510d50ff0998473a972ee4cfa40ae864f067`

```dockerfile
```

-	Layers:
	-	`sha256:b9773b66ecb208a1e098a31ebd427e9cb3e056a66827fdf758d364713f7b881c`  
		Last Modified: Thu, 22 May 2025 00:12:35 GMT  
		Size: 15.2 MB (15173072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd66f6b0dd79a36d5af130bf11d85e6100419122c9ed1098083346cabd8d7c32`  
		Last Modified: Thu, 22 May 2025 00:12:35 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:02e270a0de32434b8fa5d60f55118eaa99dce5f16637e9eda194c7e95bba75be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282103121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa0ca967f37c366b073a31c75fc3e08bd5309c06a255019b3ad324d96c7c322`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34362265f33a06975f249d19b3ebf3e131e052b1333868e863a53ee816bc45`  
		Last Modified: Tue, 29 Apr 2025 16:46:09 GMT  
		Size: 167.6 MB (167558886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ebcff6643cd1ad112a344ab9a7922d66e14cf0db6ce70cd2454eac2f7bb6b59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14884787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78a935ac0f258b1431d64f26e91f6f02eff561dfb521edda9d52fbec853b572`

```dockerfile
```

-	Layers:
	-	`sha256:9d024394af90fb08c546db0cf3486c6b71f7e805b0b9be512e630642d03ead86`  
		Last Modified: Tue, 29 Apr 2025 16:46:05 GMT  
		Size: 14.9 MB (14874495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3a0221c3adb5e6a06670201a38a9e1607b68a9e4d21db620269a99deea2be9`  
		Last Modified: Tue, 29 Apr 2025 16:46:04 GMT  
		Size: 10.3 KB (10292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0eae89394efabd51cf47053d0cc746ccf4ba95dfb984fd52fef04d0000612911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312869416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe3674ff282d910fdd55e0c61370c37f59946611a8b34f6f023652796bd33205`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356545a2ed16b26897f2a271b3f4a7d7e64a9bf9bc0c78fdf4f1386401e37428`  
		Last Modified: Wed, 30 Apr 2025 02:18:06 GMT  
		Size: 190.0 MB (190024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4396b4ce4d4f1436172c8148d704250143ca6093d8b9094e4280d28ff117d6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15086276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e758a8b173226712a332819a547debd03ffbdd5111c90be0143d51a0340cff44`

```dockerfile
```

-	Layers:
	-	`sha256:12122eaa9993e469b1d05ea734c8e9c81df77d16d05c62c7ce972da393787d8e`  
		Last Modified: Wed, 30 Apr 2025 02:18:01 GMT  
		Size: 15.1 MB (15075964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd32e95cf9243b835298775747643922f0da3aca160a81d2b4167cb96678d37`  
		Last Modified: Wed, 30 Apr 2025 02:18:00 GMT  
		Size: 10.3 KB (10312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:57f2435c2f5c0db232af12c168b7f47f851f994ec580d8397779329ea3451ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.0 MB (327043385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e59bfec70aa6923c2c2e71b91be322c7eed605e6d18d72f16b77e5774b307f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bde5c2ebb13d7ca154f5cc8b4e26e7e3a669b8bac689ec15851b65e299a0fd6`  
		Last Modified: Wed, 21 May 2025 23:19:38 GMT  
		Size: 16.3 MB (16268487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e052669a7dd77fed659f1b6d3fcf5171929214e8821aaf28744160fb71f4f1`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 56.0 MB (56049779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f06bdedcf2f8fa5a0d52d346902f8aceec74013af364956265940521230002`  
		Last Modified: Thu, 22 May 2025 00:13:14 GMT  
		Size: 200.0 MB (200039337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4e1ab1ae61aca4422bda744c8ec64c649961805296528ff34b2e9001addc32e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15171299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bbf4e188cc8030758bd3829bfd3cab204ecbb15ca09c09bf20595f33f5c286`

```dockerfile
```

-	Layers:
	-	`sha256:4b746b3f01ab58ff608e79e9a208e1ec80fc3a0711f1732ceb44d20e651f3a71`  
		Last Modified: Thu, 22 May 2025 00:13:10 GMT  
		Size: 15.2 MB (15161089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ab254f84c9e2e0d7bf6a711427a28d0c44a6f9d00ab991c227eb76fea608252`  
		Last Modified: Thu, 22 May 2025 00:13:09 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json
