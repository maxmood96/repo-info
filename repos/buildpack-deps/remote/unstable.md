## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:e1ce62040838d6ed5a5b063a04e463faaa5c377725bfa87603649230a6394b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d06b9c9a0b43d5cf9ba185cb98902d5d006604d7ae912e99cc49e2bafacfbcbc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344986510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db522652278aba4050aa04755035020098e12ee7f98d0b89e685ea61d8c582f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:47:42 GMT
ADD file:6261ecb921e04d2b3f6fd44e5dcb5683154bc0beee4f26913c2be9395a060489 in / 
# Tue, 02 May 2023 23:47:43 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:02:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:02:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae396e350f30e1defad1bfa67a84b97389d42cf3442551e39a0e2bab6b53a50c`  
		Last Modified: Tue, 02 May 2023 23:51:56 GMT  
		Size: 49.3 MB (49299270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd17d28808409b147a3bf1ad99b0f7837c93556c98e22adfd32391f10cd514c3`  
		Last Modified: Wed, 03 May 2023 20:15:05 GMT  
		Size: 20.2 MB (20241988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c7fc303564e2f5840c7571b2755251add439e9c918e410cb9101bfa2d3e540`  
		Last Modified: Wed, 03 May 2023 20:15:22 GMT  
		Size: 64.5 MB (64511077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa3739c6e2e043a0c968190dde8dec2ee8d9a1e0a1666a9312f3b1e250f9aeb`  
		Last Modified: Wed, 03 May 2023 20:15:56 GMT  
		Size: 210.9 MB (210934175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:180d8eeffd2e4855879295bef76d87fc0065a5e92dff0612cec766cf61502637
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.9 MB (312893740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46a8f785150a4178943cd376f1059156023a03f694b66fd444df28444d0efb4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 22:49:00 GMT
ADD file:2228a07c6ec82db1e0719684d77cecf448c3be947c2b1b48347ba5de9e5b57f8 in / 
# Tue, 02 May 2023 22:49:00 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:00:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:01:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:02:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:90d5a5fdc15637fce928afc279fecd9adb82fe3c476f174458fc6bdd7fb4b57e`  
		Last Modified: Tue, 02 May 2023 22:51:47 GMT  
		Size: 47.2 MB (47167062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d5ead8dfbbce713a49ce8b7288e71d62ed89f8fe7bdc5a9a3601fedc95d026`  
		Last Modified: Tue, 02 May 2023 23:05:01 GMT  
		Size: 19.3 MB (19334073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7796655abf4f2957cc5d94738416e24552291e28456a70d36d096584ddeccb6e`  
		Last Modified: Tue, 02 May 2023 23:05:21 GMT  
		Size: 62.1 MB (62136786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a4f3e185a4645892a788b689cd8ac1a7c08d0dc4d3bf9bc87518b63e0cee71`  
		Last Modified: Tue, 02 May 2023 23:05:56 GMT  
		Size: 184.3 MB (184255819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0d58cdc6d536b4a378802edac6aa9d93a1b79ddf2afb2f7ebfd859bdb829bf57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303756849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51696134895d029f4d6a524e3de33e23304f5e7007e847e6daab405439b135d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:00:33 GMT
ADD file:f8bcd71f10e7adad706b3a1685fd5c4844e3ebde65bdf9a7c004d7b9dd3520d7 in / 
# Wed, 12 Apr 2023 00:00:34 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:06:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:07:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7b0aac501774f41dc4e46815077e011ed06b86d9469c6ca28755965123669423`  
		Last Modified: Wed, 12 Apr 2023 00:04:46 GMT  
		Size: 45.9 MB (45890234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40f36cc9abf83398d26c55cfc4ca06cc31dcf06c33d2c7da24b80a00c57a974`  
		Last Modified: Tue, 02 May 2023 23:38:12 GMT  
		Size: 18.6 MB (18602339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd64b39b95dbe081b6e8dcc7962f63ba1863cd81c23a43d9e0bb856367a18b8d`  
		Last Modified: Tue, 02 May 2023 23:38:34 GMT  
		Size: 59.8 MB (59763827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce08a78dd1d654a91c92b403658db9f111a9bc0ceaf486f2a678b64a0e59b52f`  
		Last Modified: Tue, 02 May 2023 23:39:19 GMT  
		Size: 179.5 MB (179500449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:df0cb9d60f4a3da5222e962cd051f69148533e796b8f3af25c2a97b06b33b0f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 MB (336236536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab8e2caa840a09d8f8f064f8a000843b7b59bb81d7852282c29262353a3313b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 03 May 2023 00:23:28 GMT
ADD file:cb107aa90220a9fc72fe1e3aa26878752691d6e9eb04696738920b5834c6d9e2 in / 
# Wed, 03 May 2023 00:23:29 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:24:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:25:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 17:25:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:77a3c1a83d83f65ef8fd579d19879f09a4018e384f42cfa55f82d426f32ff840`  
		Last Modified: Wed, 03 May 2023 00:27:15 GMT  
		Size: 49.3 MB (49345262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc449f3c80cded292a5c3da27ab253ce49a715e2cf061c906852d4c1361f3bf`  
		Last Modified: Wed, 03 May 2023 17:38:49 GMT  
		Size: 20.0 MB (20040094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da391adbd4b39ccb3f1529dc541725ebdac9583cd6dfda7d044de008344827f`  
		Last Modified: Wed, 03 May 2023 17:39:03 GMT  
		Size: 64.5 MB (64494432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6960ac9526339e863318052de3e69ca28a7d55e6aeee2891ac1e15a5105765c`  
		Last Modified: Wed, 03 May 2023 17:39:31 GMT  
		Size: 202.4 MB (202356748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:62d0f4b24d16ac947bca11c80a65e3913a125e283d64f0d82500d8f8a596f6c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352922802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce356751cfea2133f993f5c29df94fd6cd84ec698fb6ff6619339c1b86885cb0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:51 GMT
ADD file:31710a830769b5e1f2612e1cd05380f677714bf52f61a54adbc7424087fd1378 in / 
# Wed, 12 Apr 2023 00:39:52 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:47:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:47:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:48:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:35e4af56b8bda58bf958814bc36c8e3a9a1d719c8582c0f33d7d69cc5b416211`  
		Last Modified: Wed, 12 Apr 2023 00:44:24 GMT  
		Size: 50.3 MB (50310899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499e0d2794581c0b3fafbc9ce91c00afe10e1d6704447fcec0b1b4ff6df41bed`  
		Last Modified: Tue, 02 May 2023 23:57:29 GMT  
		Size: 20.8 MB (20818586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8f1e71833446e567aaacbf83081ffe5a7cf93453d6d2ed37d800c0b89c7013`  
		Last Modified: Tue, 02 May 2023 23:57:51 GMT  
		Size: 66.3 MB (66331473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e721b0407dd26332a080ee9d1131b27b6e735fed1529800542230c5f722a6a7e`  
		Last Modified: Tue, 02 May 2023 23:58:37 GMT  
		Size: 215.5 MB (215461844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:16c248c6fb4accc346278bf80ed6e7322dc44f69c1b7128b034c7264821e0307
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327813054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d839e31d67887f2f4aed62d5471f0cbeab4bd4cf154ab7ce9e87bc058deac18f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:10:29 GMT
ADD file:60b5ce2a691448a1aab43387ba9337b8cc193a2cbb2a01ac71f5f0cb083415ff in / 
# Wed, 12 Apr 2023 00:10:34 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:29:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:35:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45f3dc30e8865982b1af34a4bd64597aea34350dd1bf817342cb2901014ff9a2`  
		Last Modified: Wed, 12 Apr 2023 00:18:10 GMT  
		Size: 49.3 MB (49296248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf4b724cd7bc4b197cc5156622c80e9b57f3b3c9185058f2ddc799d3f4b4cee`  
		Last Modified: Tue, 02 May 2023 23:42:14 GMT  
		Size: 19.6 MB (19554260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f568b715afffdc8179b7108b5118ba8037058e2a10fc275f68cfdcca38bb4c`  
		Last Modified: Tue, 02 May 2023 23:43:03 GMT  
		Size: 63.4 MB (63412774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1048f6225eb53a808f4c9fc764a9e12e4902fd3b055234e77f3ded422a46ec39`  
		Last Modified: Tue, 02 May 2023 23:45:09 GMT  
		Size: 195.5 MB (195549772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7be3a1df130305a61833eed7ca0d362b05e8dbb98df2c6fb4ff25df3b74d96f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365649986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84175a5fe94e4f13f430ad3b56301ddd05e300185b63a05b0a1650c4c3922023`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:41 GMT
ADD file:8700846eefa6ef0670106ef8055671479d597d057ee34d1d248dbefa5977753b in / 
# Wed, 12 Apr 2023 00:08:44 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:28:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:29:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:32:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c14c235d79599f644d6f952e975871669fe8a00e0434e5d26966f11cfb3820b`  
		Last Modified: Wed, 12 Apr 2023 00:13:39 GMT  
		Size: 53.3 MB (53291710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f7fcb97c8afc6c0c2224ad25838f0b2c58a23b8b1ea868b93f7b075fdfd416`  
		Last Modified: Wed, 03 May 2023 00:14:32 GMT  
		Size: 21.6 MB (21578703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726c71ee2f84a020202671d9a1b2e9064700ac60dcf19b2b863286996fd0ef79`  
		Last Modified: Wed, 03 May 2023 00:15:00 GMT  
		Size: 69.9 MB (69948607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d84f3b56f72f9033414cdd956d3dcf71b42c12dce5384f82b712b6616c52664`  
		Last Modified: Wed, 03 May 2023 00:16:01 GMT  
		Size: 220.8 MB (220830966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:12adeb17b70a35c1c949d02fd340381a96e45f3e1357ae31e6741dc4b203d8a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356278392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8edc6f31938e2300aac23d2456cb5e56e9d5f903b4c676136993b343ebe82932`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:29:17 GMT
ADD file:4e365b380d9cfb77573624c399d3376d19fa5c7028c44b681071b426fb1c6db0 in / 
# Tue, 02 May 2023 23:29:19 GMT
CMD ["bash"]
# Tue, 02 May 2023 23:51:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:54:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 00:02:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:29b183cb384ba20db9a991d4213be72a43fcec3d5fc87f259bd5719d35027d1b`  
		Last Modified: Tue, 02 May 2023 23:32:35 GMT  
		Size: 45.5 MB (45510102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93940bc329d1d971861f44e84f01d2bf1b1b0075644023b2caae44992f0e70cb`  
		Last Modified: Wed, 03 May 2023 00:03:11 GMT  
		Size: 18.7 MB (18656704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d9b13ea8a5a6cc6efb43a7b1b940dbe6a4cf4e6dfd3a66e0d926891398ac6c`  
		Last Modified: Wed, 03 May 2023 00:04:32 GMT  
		Size: 60.0 MB (59957056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65751e6feb8ebfc538ee01d19da0c0de0f28112bf667890c6565039d166b71f3`  
		Last Modified: Wed, 03 May 2023 00:09:49 GMT  
		Size: 232.2 MB (232154530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5ba16f608e548cbb31e81d699527b911b6bc0a5e68c526003f3e3c69fb56eb8e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.1 MB (319082934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5f03d166ebf8301dbc885715f55a8e97ed27b662089f2033824f6357d3b7ce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 12 Apr 2023 00:01:19 GMT
ADD file:0593fbca11f3d4a9b2b916ee99bb70651af04ea1275262f12e9b0e5c07e81f0e in / 
# Wed, 12 Apr 2023 00:01:29 GMT
CMD ["bash"]
# Wed, 03 May 2023 03:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:10:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 03:11:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1844a6b5cc32e25703d3a6ac2115866157b1f856d7463d0dca8443fea51061f1`  
		Last Modified: Wed, 12 Apr 2023 00:05:31 GMT  
		Size: 47.7 MB (47665068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9bab29a40052387d03edbfdb2b9e7cf4ea1697712ebe40519c4323ffdb7e3d`  
		Last Modified: Wed, 03 May 2023 03:34:45 GMT  
		Size: 19.7 MB (19733832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d728f596a0f5f94054c6338c0f5475b7fb39affc7bae86597e1c8f20adee19f9`  
		Last Modified: Wed, 03 May 2023 03:35:00 GMT  
		Size: 63.6 MB (63595522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba78898922e01bf65ea017e86ada94d1a4f71c5821f7ea1d3f2ae50184bf45f4`  
		Last Modified: Wed, 03 May 2023 03:35:28 GMT  
		Size: 188.1 MB (188088512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
