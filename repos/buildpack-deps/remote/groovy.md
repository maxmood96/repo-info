## `buildpack-deps:groovy`

```console
$ docker pull buildpack-deps@sha256:8b9dd797ab377aad551abf99f39d1532b08ff376f827d9051cd63a66b98efcde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:groovy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2bcba59f9698803f44506a42514d9142d80f9dea57f6c983c520d280805c8f2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246116642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:498cc230102a994eb71da70b7f4903e9c7e2f854cd6bb1a1b95612a6a56e17e6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:36 GMT
ADD file:8fe6bbb03392c41fe275714978bd93f4c94d64366217e95415b50aa7edc3b7c8 in / 
# Thu, 17 Jun 2021 23:31:37 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:56:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:57:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Jun 2021 00:57:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:00:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0166ff847fb08131d71f07d323c9814e7b7a658fabac8a5c3f07c7aa6e645460`  
		Last Modified: Thu, 17 Jun 2021 23:33:17 GMT  
		Size: 31.3 MB (31341655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594260cff16d25c6707fef3872a8e69ca46132c30853f5f0f6b5cb903c277169`  
		Last Modified: Fri, 18 Jun 2021 01:08:55 GMT  
		Size: 5.4 MB (5405111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67fe17eaef54d2ecb4512176cedc37a936eb3a28daaf82bda1ca71c603335af5`  
		Last Modified: Fri, 18 Jun 2021 01:08:55 GMT  
		Size: 3.7 MB (3664253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfcf02a042f2b82c5bd140dfcb312927b31037dcc204b22a05333f7062f45c0d`  
		Last Modified: Fri, 18 Jun 2021 01:09:16 GMT  
		Size: 55.5 MB (55472673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac175df73a944acb98baf1c7d3c31baf4c642f64b147f20aeb0523e9956c1804`  
		Last Modified: Fri, 18 Jun 2021 01:09:49 GMT  
		Size: 150.2 MB (150232950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b0fc662e7a872ca9e4a4fdb0ffa0c307661cdc62a26559b0986f93f1c00b7b47
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215464151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e69437eee10e96ce95ac352d786db00c52bc3eb7b6d3feba03fd6c404042e14`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:19 GMT
ADD file:738456ae96cc12db6ef2a0447b191ed4ce32521c1a9e750b62339e7b180e6660 in / 
# Thu, 17 Jun 2021 23:32:19 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 06:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 06:04:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 06:05:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 06:07:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:db4b059f7335fee291ba5065aae186569688129caf45e6c65fa8ec8949f82209`  
		Last Modified: Thu, 17 Jun 2021 23:35:24 GMT  
		Size: 26.3 MB (26308558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9cb217d71241fa34b16b6f0f1fc7a8531994c1ec2f6be90b06b58845905215`  
		Last Modified: Wed, 23 Jun 2021 06:33:06 GMT  
		Size: 4.8 MB (4840577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d91c77e77ea02fd7d118fc368b926aa635e191d49ffeb54decdd467ce9500c4`  
		Last Modified: Wed, 23 Jun 2021 06:33:04 GMT  
		Size: 3.1 MB (3140475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19dff25025bff08868cb8c8db852e704e017efdf88fd9c174bba52f4ec01e0e`  
		Last Modified: Wed, 23 Jun 2021 06:33:55 GMT  
		Size: 50.3 MB (50281599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23da62d2490e36c0420ac038c9dc58f832160b9f733661fbc9a8d549e8f7924`  
		Last Modified: Wed, 23 Jun 2021 06:35:29 GMT  
		Size: 130.9 MB (130892942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:72ee14f9b232b5bba32e3fe83352c95aa52cb91a7bf86274840826f0eecac7d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237131141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4654ba63c89af5b2690e0169dcfd7121687110b18812cdacc7eaf71b57dd021`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:54:07 GMT
ADD file:3516eb7d802e1e7619bc080a65a13864ba6a8ce052c2c7b6b8f27e291ebb0543 in / 
# Thu, 17 Jun 2021 23:54:07 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 00:17:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:17:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Jun 2021 00:17:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 00:18:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e83729d16232f8e27d4bab42e00352bc57b53f07a423fd5316ecce65afec97e`  
		Last Modified: Thu, 17 Jun 2021 23:56:26 GMT  
		Size: 29.9 MB (29875719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2547faa05511d57cbd6f36693ce0e24a28b06c527432f09d1ef05a25c568c9c`  
		Last Modified: Fri, 18 Jun 2021 00:25:06 GMT  
		Size: 5.4 MB (5372219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9993457c5d745f0e31482101bce3176bd919190b356d53510fc883fe841bae72`  
		Last Modified: Fri, 18 Jun 2021 00:25:05 GMT  
		Size: 3.6 MB (3634521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18db5c413d02b16d84320a142eaf930e413bc9be34388078741ee45af2dc8804`  
		Last Modified: Fri, 18 Jun 2021 00:25:27 GMT  
		Size: 55.5 MB (55461373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685655db60b32078c31c955d5f7b773c15a58d23d4fb7b4153e6aa7991866649`  
		Last Modified: Fri, 18 Jun 2021 00:26:03 GMT  
		Size: 142.8 MB (142787309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e38dd9565098f72008014e98f83e28da0982b51d5879c49331decf8348561e2f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (274026702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8a883a671d9d98334c454fd4b05a940c447718bbb3cc4b1607ef898f343795`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:32 GMT
ADD file:5b3e0dae91824102eb438ea2d8c1f1190ffcaa623f93c4e0e96004e1098cacb7 in / 
# Thu, 17 Jun 2021 23:25:40 GMT
CMD ["bash"]
# Sat, 26 Jun 2021 00:54:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Jun 2021 00:55:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 26 Jun 2021 01:01:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 26 Jun 2021 01:23:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f3c6e346cb79378eaa11a81268da2aa9fb480ab376c060d5cb48380f3754b37`  
		Last Modified: Thu, 17 Jun 2021 23:29:02 GMT  
		Size: 36.6 MB (36561549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf3088338753aedc77d485ca99aac63dc4bc2bb88f766d066e9a92385a5ce31`  
		Last Modified: Sat, 26 Jun 2021 02:18:29 GMT  
		Size: 6.0 MB (6040721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432b10ec98757d1b5f49aeaf3288c25955f16a32ac6a74b66cd627510ceb29c6`  
		Last Modified: Sat, 26 Jun 2021 02:18:24 GMT  
		Size: 4.5 MB (4521737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e5cbe30721952aa4eba97d67389e491f056e856cefb4754ddb778c7d02cd3b`  
		Last Modified: Sat, 26 Jun 2021 02:20:04 GMT  
		Size: 63.7 MB (63741631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7cb6b73304aa2ea32bec80b97ebecbf60ba14199d691fb185f3e4f03ae96028`  
		Last Modified: Sat, 26 Jun 2021 02:24:02 GMT  
		Size: 163.2 MB (163161064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:groovy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b37a3799e81ef1c400751ae41c25a99f079003d81253052a683be33c62645320
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250222467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4b0fced329f4d7a14a3c2593fa996c3b6e1a3e46c209c0debc9171179728fa`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:44:10 GMT
ADD file:3cd751b8e50fb2cd9ce918473bd8f686a840c79094b5d8616cfcc9a8a0051f17 in / 
# Thu, 17 Jun 2021 23:44:12 GMT
CMD ["bash"]
# Fri, 25 Jun 2021 21:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 25 Jun 2021 21:34:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 25 Jun 2021 21:35:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 25 Jun 2021 21:35:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:37d7d8f44f985bb1d5e8f0c5d97987e4fda43e7715162c6e919f6ff767121465`  
		Last Modified: Thu, 17 Jun 2021 23:45:44 GMT  
		Size: 31.6 MB (31574525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ed46897f50ae361e4ec2547386f38b442fc3a02982e9ed1f0d3a5a9d5ede6a`  
		Last Modified: Fri, 25 Jun 2021 21:44:26 GMT  
		Size: 5.6 MB (5629604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee158479835dc8922e4cc3026d1e8023d528013ef4d0c6b5cd4b4255a215e884`  
		Last Modified: Fri, 25 Jun 2021 21:44:26 GMT  
		Size: 4.2 MB (4156598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2e8b33cd0551400a2c4c85925e24571ae15414922841a61adf5e943faef79e`  
		Last Modified: Fri, 25 Jun 2021 21:44:43 GMT  
		Size: 60.6 MB (60648750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f9d9d716526b4151f8be6515798dad06ca1e28885c21e6cf48f781f131c159`  
		Last Modified: Fri, 25 Jun 2021 21:45:10 GMT  
		Size: 148.2 MB (148212990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
