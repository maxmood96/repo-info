## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:2868f82f73ee102ba57a440e81abd58d9c14c646da48495717c3f07d46e0cdda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7ecaee8c4a64d3c75ea1db7fc133ec0d606fdc0cdb94bd56a724d2ae5dd033fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312627759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef0e2a2b02c630f80258eebf0a8f4ae9d28e0e5ea4dff01896648eefb681c31`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:36 GMT
ADD file:2f32dd3ef1e51a4d2d6dcf55fbf766434df5b3ada802b087d5761f2fa0cdebf5 in / 
# Thu, 23 Jun 2022 00:20:36 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 00:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:51:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 00:51:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 00:52:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ea267e4631a981caf2841a7e9a1faf29cef9d020c4378fc64845802d17586531`  
		Last Modified: Thu, 23 Jun 2022 00:25:38 GMT  
		Size: 50.4 MB (50440811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a014c92148934973210d840dc7cfed53e0afba38d839afaa48ed5150eae19af`  
		Last Modified: Thu, 23 Jun 2022 00:59:51 GMT  
		Size: 7.9 MB (7856631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ff1be7001d642a624409e2d5f90e7708ef7e6f1a75f4eb7362a9296e18d20`  
		Last Modified: Thu, 23 Jun 2022 00:59:50 GMT  
		Size: 10.0 MB (9997231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e42533e7311ad0a85fe19e9bc5fe3138f608853eeaaea70ee08b2a631b356c3`  
		Last Modified: Thu, 23 Jun 2022 01:00:09 GMT  
		Size: 51.8 MB (51843778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56e70ed0dfb39711bca67c13b10e546d3d79ce4a6b0fa528c1d1bbfc5b9d02d`  
		Last Modified: Thu, 23 Jun 2022 01:00:43 GMT  
		Size: 192.5 MB (192489308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:9fe6815cd30caf922ddc31c74ee828b62ce7c4b68fd895502418d451424628d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286258277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867712a4a48466e56ce699ab9c333bc7c6e73e502c6aaee5d6de8c8a863f8047`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:51:06 GMT
ADD file:29a86a4b70e0fb7454a1325b875ec05d02fe02c2dd72a61a0b9476e7f1f3fb78 in / 
# Thu, 23 Jun 2022 00:51:07 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:41:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:41:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:45:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad2005e84922efa5686f4921c83f828452891153e5fad381514bbdbd3b2b8fa`  
		Last Modified: Thu, 23 Jun 2022 01:06:27 GMT  
		Size: 48.2 MB (48160705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540e32e30ed2717efe58bd73d7a7469de69e97c528d2402897d3f6d326ca6af4`  
		Last Modified: Thu, 23 Jun 2022 02:04:39 GMT  
		Size: 7.4 MB (7400800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd283a4314a89d71392745ece238ed63888f508f2dd55f513099cfe5d8748eeb`  
		Last Modified: Thu, 23 Jun 2022 02:04:39 GMT  
		Size: 9.7 MB (9687650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8287fbf741a3acfdcc7dae55783cb6450c99e052448a3e31549e333a036e58d`  
		Last Modified: Thu, 23 Jun 2022 02:05:28 GMT  
		Size: 49.6 MB (49584208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bb322c614ad37b396dba51871f5c11d8a7861abe552cc770c617d31cc10c22`  
		Last Modified: Thu, 23 Jun 2022 02:07:24 GMT  
		Size: 171.4 MB (171424914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:749cf14f8fcf613facb06451911f93336972a34ede39ec4ea452b0eff7a513a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278450310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceed07940bd0ee8119b52dcb56cbbf841b84202dc8aa547e98cc44a25266a086`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:00:14 GMT
ADD file:b8401862d74ac67a61f764c5dcc54fde231623bf55d2299665eab35dccd25114 in / 
# Thu, 23 Jun 2022 01:00:15 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:50:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:50:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:51:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:53:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0555d003e6ef528480fa5625ca8ff9a45d899a62b5c20ab7547a42c64d7c1d4c`  
		Last Modified: Thu, 23 Jun 2022 01:16:07 GMT  
		Size: 45.9 MB (45915761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d67b659cf86b06bd457cf205d2cfded55fd9654e275d3ec128f15fb94099c21f`  
		Last Modified: Thu, 23 Jun 2022 02:16:11 GMT  
		Size: 7.1 MB (7145400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6da167dadbe348ebfc7cbe4152eae80fb72e14b28b417ffa2bc6adf87034179`  
		Last Modified: Thu, 23 Jun 2022 02:16:12 GMT  
		Size: 9.3 MB (9343917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034ac9bc2920b12499948ed10c17ffdc5b34b7e5bff76a6b5735dbddcd25233f`  
		Last Modified: Thu, 23 Jun 2022 02:16:49 GMT  
		Size: 47.4 MB (47359583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460fa2a517792e189f8bcf5c8720fcc36670999648783f68e21e0aa3dfc2a43e`  
		Last Modified: Thu, 23 Jun 2022 02:18:27 GMT  
		Size: 168.7 MB (168685649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f0fa1a2f21d7fa686a9875a3ba896cfc7d2b41766ee9e07e69d5ce5be34df38b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.0 MB (302956368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86aa00ed4cea47da15a23bdb9a364174f18dca1317caf839a4b294e4793e2f3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:54 GMT
ADD file:a5e3c0ffa9f9754a6d77fafd8288e699a70f7f6ff7c5912a065f1c69f1393e99 in / 
# Thu, 23 Jun 2022 00:40:55 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:12:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:12:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:13:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:14:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8d6f1451981514e25c21542f5c7ee9bb90052b8856b484ce47294cbf1fd5a234`  
		Last Modified: Thu, 23 Jun 2022 00:47:46 GMT  
		Size: 49.2 MB (49229092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccc9fb4baf6e7f2e6ee18ed689c8ee1171c6751c8bbd317d580a193da27a5f1`  
		Last Modified: Thu, 23 Jun 2022 01:23:09 GMT  
		Size: 7.7 MB (7719858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620d55693ed5943ab298346d9ccafefdd6d6f33994e6820a857737df89b65f3a`  
		Last Modified: Thu, 23 Jun 2022 01:23:08 GMT  
		Size: 9.8 MB (9767307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dcb0fa2b6020cd95c3972ec0fe03da38862f57574fe03a49360713d6f415d6`  
		Last Modified: Thu, 23 Jun 2022 01:23:28 GMT  
		Size: 52.2 MB (52174988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75d85ab89337b32fb8b4e0454a157fa71a765a1daf512255323edd5f3f0afe7`  
		Last Modified: Thu, 23 Jun 2022 01:24:03 GMT  
		Size: 184.1 MB (184065123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:41d319389aae28e1b0dca69e00d508dd8b2ed0216be7950ef10fca5b275fd37f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321803929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c65a723c390037d146f2369f60f74862dc32d9eed2bdb860fe2131d8129640`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:44 GMT
ADD file:6437b7652a12d978836b6d8c12403ce48d71210a2944ce96c0ecda8dfd89af2f in / 
# Thu, 23 Jun 2022 00:39:45 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:13:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:13:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:15:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6fd723f5696212bd76053aaf0e4dc9c090f488b14b41ae360bafb5574352e90c`  
		Last Modified: Thu, 23 Jun 2022 00:47:04 GMT  
		Size: 51.2 MB (51204247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4827b8abd114ea1d70c6fef5972f989dc7d81f662c584282f4aa12d20703936`  
		Last Modified: Thu, 23 Jun 2022 01:23:31 GMT  
		Size: 8.0 MB (8022623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0f822c867b6ac88f38f1e895c670c32e86a79dd0f62ac9ec5afd6cc3b5eef9`  
		Last Modified: Thu, 23 Jun 2022 01:23:30 GMT  
		Size: 10.1 MB (10122040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49061b906506dd5e7d3e4beaebefeb6ca6446bbdcd913432122e484aadf4dbf`  
		Last Modified: Thu, 23 Jun 2022 01:23:51 GMT  
		Size: 53.4 MB (53443635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea593fcead79a04a733db35dd59f436a81c556a673b60db48100ac15374b12b`  
		Last Modified: Thu, 23 Jun 2022 01:24:30 GMT  
		Size: 199.0 MB (199011384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:ab6893bbeae8ec31411bc00aa91e005bd0f4be45ebe74de6dcda747390789706
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (297023520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3502cebc89c16230d6058b0c104485e8673606cd7301d9777df550e8309e31f5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 01:10:55 GMT
ADD file:e97021cb9347cc6233316e4e1f31dc6728791c819d5c4f472c2e9009df33ed64 in / 
# Thu, 23 Jun 2022 01:10:58 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 02:00:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 02:00:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 02:02:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 02:07:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c69f93f35e40f60566a2c787b9d7a1e4ae3c026d480bd089de24eaaa432ffab6`  
		Last Modified: Thu, 23 Jun 2022 01:21:04 GMT  
		Size: 49.1 MB (49073169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8064d03bf4d62d6d286faab208b26248a41ff122c53e3a1cc34d98fff9698faa`  
		Last Modified: Thu, 23 Jun 2022 02:23:21 GMT  
		Size: 7.3 MB (7272853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11d44e638ac6c53724b0eefa08dde59c4fe2c7cb51801bb214ab56c4f8634a5`  
		Last Modified: Thu, 23 Jun 2022 02:23:22 GMT  
		Size: 9.8 MB (9800300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0c8148d6586ab0843c3316210a98b1355a7b90e58c7f09e81feee93e27bcd0`  
		Last Modified: Thu, 23 Jun 2022 02:24:08 GMT  
		Size: 50.9 MB (50862080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709fbe1cd666dac5a125c19c825efc54bfae83acc5d33cecd0326c2a23a7ff8e`  
		Last Modified: Thu, 23 Jun 2022 02:26:11 GMT  
		Size: 180.0 MB (180015118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2667c0011fbaf54d18807e2fbb537a39a8e17fc76812eb51a73c01e3b1897ee8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.0 MB (334027228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0cf45e4268f52c51d935bdd891ef5ef16e7308665981dd65eea7daff362f1c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:23:18 GMT
ADD file:111395200ed598f754f449a2c278d0de3716fe88c66495506bbfba93a1be60d9 in / 
# Sat, 28 May 2022 01:23:24 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:15:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:16:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 03:17:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:23:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a84717e4877770b3a8a9f0eb6890cb457d0bf1ec5c2013b56c1a2353beb5cbc0`  
		Last Modified: Sat, 28 May 2022 01:32:57 GMT  
		Size: 54.2 MB (54176994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34161779331d3aba2a35660a49ce70bb924f430f55cd87d24c4a93a50735456`  
		Last Modified: Sat, 28 May 2022 03:37:04 GMT  
		Size: 8.3 MB (8293525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daa1667acca77ec8c0a28fe3d5e8914209d4ab7d21c9ae4f44667705750e5a2`  
		Last Modified: Sat, 28 May 2022 03:37:04 GMT  
		Size: 10.7 MB (10727643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54afe3a1ca9ebf47897da5bf3470187988793f427ac1efc94b7f4d1d754e7db`  
		Last Modified: Sat, 28 May 2022 03:37:27 GMT  
		Size: 57.5 MB (57457968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d33c72787f5105ae2ebd54d1a426d819f48f61fa4c9b6d1351266d30635844`  
		Last Modified: Sat, 28 May 2022 03:38:12 GMT  
		Size: 203.4 MB (203371098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f973d694e23672877ab8665cf6e53bb7f6847e57ef7ff14f2aa407e1546da7f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.7 MB (294665604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93f5ed7f2e0d638854f4d41a4ef02b1a54cadf47974e3a68c15949f31574494`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Jun 2022 00:43:34 GMT
ADD file:2fe0c2724221ad2af3b740e4e2da8c4e883777f2e4466804951aaacc7472f0b5 in / 
# Thu, 23 Jun 2022 00:43:41 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 01:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:20:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Jun 2022 01:21:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 01:24:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:977fe4047366375c4e256a32fd8e196b4ce6a283da397aa1ef2dafa150c30190`  
		Last Modified: Thu, 23 Jun 2022 00:52:15 GMT  
		Size: 49.0 MB (49007215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3205fcf3ff7eff52355fbdc242f38950a2bb1e025c8c3f0d6c952e2a36295f60`  
		Last Modified: Thu, 23 Jun 2022 01:35:59 GMT  
		Size: 7.4 MB (7423836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d1428cca6d47f3c2edded7af8b465dc3457d6b8231f1f691b2e5b7517fcf31`  
		Last Modified: Thu, 23 Jun 2022 01:36:00 GMT  
		Size: 9.9 MB (9883348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692a5bd2de9979006c276a4aeb1301534893d7d38e77ed09cc3084b5b0569e60`  
		Last Modified: Thu, 23 Jun 2022 01:36:15 GMT  
		Size: 51.4 MB (51384085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36e764f0a052c49f9bb5a9c5850ea48f067614ab25e05778a29c545f2a0deef`  
		Last Modified: Thu, 23 Jun 2022 01:36:44 GMT  
		Size: 177.0 MB (176967120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
