## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:87814dab281e862129d3917e0354b26261e3ea24f249fa7bf59d62177f300e14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e94e418bef028fddf8b938f2e13ce6492589f13a237c6f96c1893d648da40301
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.8 MB (311779771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4a705ee51073aee134dae0f28c1b9e1d9b007b6637b42762d5bccd8206567b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:07 GMT
ADD file:d176a72312205fc75b2950df98f4ed25abadd4b053b9d85bea67466a5b30220f in / 
# Tue, 02 May 2023 23:47:08 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:59:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:00:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:01:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a94073ab46f8d565f5938cc345d32f7adda10a2585e39555079da9d4ee595974`  
		Last Modified: Tue, 02 May 2023 23:50:40 GMT  
		Size: 50.4 MB (50448697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f81a21db4398b2051d4ceafd0420bc7966513f9baf20519c7d81761fa4905c`  
		Last Modified: Wed, 03 May 2023 20:14:08 GMT  
		Size: 17.6 MB (17580548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431d5332f45f85796fad1c6f0f23d6efc4cf25b2cb5679e54d165c3c1f1f7839`  
		Last Modified: Wed, 03 May 2023 20:14:23 GMT  
		Size: 51.9 MB (51878971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817c83dfe9f04b43d905535d01115a0bf4d986e95eb438913af163432ea20f66`  
		Last Modified: Wed, 03 May 2023 20:14:54 GMT  
		Size: 191.9 MB (191871555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:91648b9b4dcba93b640e4b50505836963e714a175e8985cd1e5d4089894ce2fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277601936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090072a9e65172b63c84eb49ed096e79e79ced93fdcafb90de35c56ba0904c99`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 11 Apr 2023 23:59:53 GMT
ADD file:3f6ca36ec4fbf50ab85c907c089dbb0618c73393c07a5841b922145b17795552 in / 
# Tue, 11 Apr 2023 23:59:54 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:03:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:05:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:166ef90dbaeab03f451f526d325c57795001e25f10c984c334a82d174b3c554b`  
		Last Modified: Wed, 12 Apr 2023 00:03:36 GMT  
		Size: 45.9 MB (45916201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0100aae2782ccdf7a55cdfc65368dfa31bea8ad211255263c57da584967eb2e9`  
		Last Modified: Tue, 02 May 2023 23:36:57 GMT  
		Size: 16.2 MB (16211233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46e28591afdcb4ab771b00597a0d617f18f15f51dfd82d4c118b9031067fb6c`  
		Last Modified: Tue, 02 May 2023 23:37:19 GMT  
		Size: 47.4 MB (47392446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8750956691654fd451f2b3aa00bfd1f56564b14e1b8ced4d7aa70dbd6be713`  
		Last Modified: Tue, 02 May 2023 23:38:00 GMT  
		Size: 168.1 MB (168082056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a0a97d13d81b34c1f91f29cd9c447e76d8dab421ca2efca3547f114747034068
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302333930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a00b07effe7be235a63b0c6f7f620609e510b93216969728f741ae33e34257`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:22:56 GMT
ADD file:6042e29dcf5e22439cd69873d8960f8d3977abe915ef462aaa84368a7186a3bf in / 
# Wed, 03 May 2023 00:22:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:23:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:24:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b7c5fe8e0ac53c77142bf16686fc01d0d2b1fb2da7be5414cdf2f224ec485592`  
		Last Modified: Wed, 03 May 2023 00:26:10 GMT  
		Size: 49.2 MB (49238630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced623c8f9593ccbdc26a5e9ad9d9ad18aa6a8a3b82d7db591552673ac8e3281`  
		Last Modified: Wed, 03 May 2023 17:37:59 GMT  
		Size: 17.5 MB (17450341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fc649f7c89c148c32767dadfc283ae1472705773920b21ddd2bc77d49b2d64`  
		Last Modified: Wed, 03 May 2023 17:38:14 GMT  
		Size: 52.2 MB (52190435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7089b0cf38b0c4474188c7904744a3a55656697b95a3b5088cb510d0e932ba7`  
		Last Modified: Wed, 03 May 2023 17:38:38 GMT  
		Size: 183.5 MB (183454524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3280e906d62ca9e6030aa17600f7e4f644eec8b06182f0c073315614944d6242
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321202121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6173b5eddfd62b110b348727b60b7e6754b46a5807b4b3e9673496708ca853`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:11 GMT
ADD file:8299e58c7e43af1f3b9fdb9bd37e3f37cf619a97ef1b87d60ca66860d646d526 in / 
# Wed, 12 Apr 2023 00:39:11 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:44:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:44:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:46:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2d15e1c2a3da7d675c2513d7ceab1d0f33ced9a82bed63d9a11ce71f1218d232`  
		Last Modified: Wed, 12 Apr 2023 00:43:07 GMT  
		Size: 51.2 MB (51206167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd99c81a486e88f0f0651f64eb17ab23ef66618d2702b301568e0dedde54f37`  
		Last Modified: Tue, 02 May 2023 23:56:17 GMT  
		Size: 18.1 MB (18097666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb713ce4d6df9acc34bad743fb201e85ffd28c4667280dd9af9bdf5f80f2a46`  
		Last Modified: Tue, 02 May 2023 23:56:36 GMT  
		Size: 53.5 MB (53473895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97e1e4ced90457352bffe63b02b1f7abb90bb492d1d96dbb2f19ddfa467f5d1`  
		Last Modified: Tue, 02 May 2023 23:57:18 GMT  
		Size: 198.4 MB (198424393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
