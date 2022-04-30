## `buildpack-deps:impish`

```console
$ docker pull buildpack-deps@sha256:bffd4c64746b72a5ea3ff47e9278aa7f7dbab3bb95d01137e2e051f2d505aeaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:952f6b0213b4d63b9f3a36ddd09c044c1660bb0652b69d1f105235b7081b623b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406680969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0fea455216bed7a159018407b8fb77411b664f79aa7280b733225a71beba725`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 23:21:07 GMT
ADD file:e36038a1f6ee02f3f9a7db183e116f58d277e97cb7e71032634097d802654d02 in / 
# Fri, 29 Apr 2022 23:21:07 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:50:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:51:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:51:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:54:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:940122ec7d0c039d048e3bf953a33cd8ef814fd587266a5e732d24d2314af8f1`  
		Last Modified: Fri, 29 Apr 2022 23:22:38 GMT  
		Size: 30.4 MB (30383364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc136e8e3c47f61408398c98287fa53af20236ad2006f834594cc5863aa38b67`  
		Last Modified: Sat, 30 Apr 2022 00:02:21 GMT  
		Size: 3.7 MB (3694309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afad01b9cdd53ebce85092828446a6cd6f8cfb65ca1a433101b71577c8919a7`  
		Last Modified: Sat, 30 Apr 2022 00:02:20 GMT  
		Size: 3.6 MB (3552457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78329ea85bf6353fcf4a155ac7e13ab65ea7844eef65a748048f03a8c64983c8`  
		Last Modified: Sat, 30 Apr 2022 00:02:36 GMT  
		Size: 38.1 MB (38073735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f15eb19915534a58f6063a1e268b8927ee8fae35f3f197792936f9a1950ef2`  
		Last Modified: Sat, 30 Apr 2022 00:03:27 GMT  
		Size: 331.0 MB (330977104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:98472f23ee60d43d3af85cee2cf8faa4d67722d87437e08d78158df5addb4ac9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371093171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6aa3fb17fc565ab34f73e3f3fb940752fdfd5c42abd54d791114110e297bf0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:59:09 GMT
ADD file:98b792cccd674eb149eee0fddc60ebe9484757384fe35630fc361ecfc28f9e42 in / 
# Fri, 29 Apr 2022 22:59:09 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:31:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:32:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:34:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2a09877f6132d465ce4f615f0c5f4bb1dc0e311ce406712beced416d3257e69c`  
		Last Modified: Fri, 29 Apr 2022 23:03:29 GMT  
		Size: 26.9 MB (26920477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4af27a84ac863174a3e2c6171bf9613a188ce8b1b037ddbc4f0fedd477c695`  
		Last Modified: Fri, 29 Apr 2022 23:49:02 GMT  
		Size: 3.4 MB (3444024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a5bb5b4bcc573ab723569d88c431ee0657394bc927acb599d0f698782c366c`  
		Last Modified: Fri, 29 Apr 2022 23:49:01 GMT  
		Size: 3.7 MB (3743731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719bc55e12cdb38d3ec4ef091fb6b61c61f0a27074cde39df57783e5d83dc6b`  
		Last Modified: Fri, 29 Apr 2022 23:49:43 GMT  
		Size: 40.3 MB (40288593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0611332f5c484d6fa3b63c78e918bfb8e3fed5e0d63154619d198df88a1e98d`  
		Last Modified: Fri, 29 Apr 2022 23:52:43 GMT  
		Size: 296.7 MB (296696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7cb723b800acddf293a68669264fa447dc8c9240006fbcc4a917e366d1ce46c9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.4 MB (399359325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ed3abee6e11ab2b6bc2e732c04275127b50095a514200554cc81bc09f50934`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:49:43 GMT
ADD file:d800d571fc22b337baaf45095bd1a303ca66065106c8b943a7a869e145896077 in / 
# Fri, 29 Apr 2022 22:49:44 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:18:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:18:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:19:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:924f038c577f5fb37fec4317d1c44a40bae2f6ee798dc0e31394270b30d69e8d`  
		Last Modified: Fri, 29 Apr 2022 22:51:50 GMT  
		Size: 29.0 MB (29029534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e757d57f9b92f1d537667767d80d964200253f44e0fd0450d481d49710944c4d`  
		Last Modified: Fri, 29 Apr 2022 23:25:46 GMT  
		Size: 3.7 MB (3677922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c053745174b0f3dbc495ff442a2793d0657bdd261a9d160f87c6d47424f4d33d`  
		Last Modified: Fri, 29 Apr 2022 23:25:45 GMT  
		Size: 3.3 MB (3327579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f20934735405fc867dbd7cda932a1436395f40e3bf325ddb688d79b5f0c3c53`  
		Last Modified: Fri, 29 Apr 2022 23:26:03 GMT  
		Size: 38.0 MB (38033146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0fc762af538fa97b6190c26f9751c72a216a46af0198b727e6dc2d036f8787`  
		Last Modified: Fri, 29 Apr 2022 23:27:01 GMT  
		Size: 325.3 MB (325291144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d2ff0cdc961c6379f3e7aa4e2258d97801015acb59a00e98d5a6ce6d3417aa51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.3 MB (414305069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77ba9aa9fcd45cf0ef280b0fc6eecd1b102d8751320ad2177bfa8b52a765f05`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 22 Apr 2022 08:08:33 GMT
ADD file:f7aa4a99dde17a8de92a81187e400ad5d7c8d77f51c5326a58f5ff3b9bde84f5 in / 
# Fri, 22 Apr 2022 08:08:37 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 09:25:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 09:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Apr 2022 09:27:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 09:37:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9679fcb395f86c315849eba78321cd3b3d42168bec93b728e8af50bf74bc3f0a`  
		Last Modified: Tue, 19 Apr 2022 13:20:18 GMT  
		Size: 36.2 MB (36172233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec86ac3701804cbb97b0d974368ed0e361a23b0ba9d44e1d693993f65de57afb`  
		Last Modified: Fri, 22 Apr 2022 09:43:11 GMT  
		Size: 4.1 MB (4146613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cffe7f70cd94d121eb55df172917e21b569060c4fcb4eaf6f171e3a8266c93`  
		Last Modified: Fri, 22 Apr 2022 09:43:11 GMT  
		Size: 4.2 MB (4242427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71bc5c9d1b5a2f681f05f88e1861bf0f644b3c64f05f595c0b1e484cc924617`  
		Last Modified: Fri, 22 Apr 2022 09:43:31 GMT  
		Size: 42.7 MB (42727975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c46aa0868174152c0b5f671de5b684bb5149edccc2b6d656272c47af8e1307`  
		Last Modified: Fri, 22 Apr 2022 09:44:39 GMT  
		Size: 327.0 MB (327015821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:44dfac7f75ecc61f316df3b3517d58f46bb92ddd0a2f9e91ca31c001a644d153
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266370707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b4a901b470ccc76d1f09726fab6725d4b5d560b817e72528a7d55e10095cd0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Apr 2022 23:16:35 GMT
ADD file:bf1fbf364f8a0fef0fa4b4a09345adc1e05055c47d99b0751d87240acaf19201 in / 
# Thu, 21 Apr 2022 23:16:36 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 00:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 00:11:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 22 Apr 2022 00:14:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 00:21:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4422bb9ff39d0068917ac97faf0afb995ffcf3e120e2c72c5948a1f185b17525`  
		Last Modified: Tue, 19 Apr 2022 13:20:50 GMT  
		Size: 27.2 MB (27210182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e51e56374944dbe4502b36fa828f86aa453deb9730c96ef7900ae7788a0a4d`  
		Last Modified: Fri, 22 Apr 2022 00:51:58 GMT  
		Size: 3.5 MB (3490482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05afe80da4939c1390130c76e59671102a5992c02f1438a9426f65d3b9bd5318`  
		Last Modified: Fri, 22 Apr 2022 00:51:56 GMT  
		Size: 3.8 MB (3804443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a0f765d0e8e49388f36472b1ac128c426f992eb323872173b24a75528ad9a`  
		Last Modified: Fri, 22 Apr 2022 00:54:14 GMT  
		Size: 40.8 MB (40764228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0383d76f092ed394e31e7f7a8a7b305c825252174b0ffa99073e647bd62863ad`  
		Last Modified: Fri, 22 Apr 2022 01:00:08 GMT  
		Size: 191.1 MB (191101372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2b56d25b490f0e65453120229a32010f966f00bdad2363caba136ece47b5ea2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.6 MB (367581767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cf47716d0f373f96f5f6882f6a7008f60588067d31d331db405971514b8af1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 29 Apr 2022 22:50:17 GMT
ADD file:1041ef5c07ca82ee2d7f626a60380e731aa09d0d2b9b6877b03abffa280e452b in / 
# Fri, 29 Apr 2022 22:50:19 GMT
CMD ["bash"]
# Fri, 29 Apr 2022 23:12:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:13:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 29 Apr 2022 23:13:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 29 Apr 2022 23:14:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fe0d74cf06c14c44f5210e7c3b5af279f02a1d45707ee11e6afae132344bf765`  
		Last Modified: Fri, 29 Apr 2022 22:52:13 GMT  
		Size: 30.5 MB (30502867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98e5deeb0d7fe30f6c49a20d056ebc1bf7817655a9468ead107eb77a50d8911`  
		Last Modified: Fri, 29 Apr 2022 23:20:08 GMT  
		Size: 3.8 MB (3763492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5616be16d6fad891f5d8a2aa1456063444902583f787bdffee6956e7edc2bca`  
		Last Modified: Fri, 29 Apr 2022 23:20:08 GMT  
		Size: 4.0 MB (3963749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afaf89d9a6b60361801ac73c8a077956ff03b24783c5219bddd6c7e443196084`  
		Last Modified: Fri, 29 Apr 2022 23:20:20 GMT  
		Size: 38.1 MB (38112171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178a64e991df8134d7241eedbb4df21b1678552d09263ca314bbc9fd486a73fb`  
		Last Modified: Fri, 29 Apr 2022 23:20:59 GMT  
		Size: 291.2 MB (291239488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
