## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:1a193e68a4415058ab3acefa5a8db0e457fc474a71a356ab610b0af8174c42cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fee8f0c94f00831d6b4bb800d7842480d81edf044ea6b932d972aae6a186760f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321704733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8243fc789f239b1164dad645dd56bf1dfe3559dec769972fc10a6368b9c29e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:21:52 GMT
ADD file:719f8702f6aa56e8ad69f574e924fdf062e8fdc72584f70aaac387be5e1d4a51 in / 
# Fri, 12 Mar 2021 02:21:53 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:51:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:51:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:51:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:52:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:78c7a03f25ec710f7b6b9ccc0ee40eb1871016252eea6df272c68389f18d30a5`  
		Last Modified: Fri, 12 Mar 2021 02:28:37 GMT  
		Size: 54.8 MB (54840531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b278fd0013a1b4473879cb9b2035cb02c05fa6d0900c208a8ef34a515c8b3aa`  
		Last Modified: Fri, 12 Mar 2021 03:20:36 GMT  
		Size: 5.1 MB (5136354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d30451e23b656b5f6aacafba452dc7ed84b576095192b81dad42df280fb244c5`  
		Last Modified: Fri, 12 Mar 2021 03:20:38 GMT  
		Size: 10.9 MB (10862407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4779737acd0d5488f0a4dcab8aeb64d803bab2c5c57ba1db53efb60f1172d5f`  
		Last Modified: Fri, 12 Mar 2021 03:21:08 GMT  
		Size: 54.5 MB (54549036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdfa2eb0d13d69bcd34eee48bc46831e66c3bd28b1437267ce527210289e387c`  
		Last Modified: Fri, 12 Mar 2021 03:22:00 GMT  
		Size: 196.3 MB (196316405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b34eba27332b47da22dfef3e8605009ff6df7e486a7a5f7d6fa2c96865dc5d10
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294821183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074e340851ebdca9b590a96aa3ad4df55530e79195d1581d75f0711b7d3e9f38`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:55:11 GMT
ADD file:a1779c1f149525491eb986605ce34dfd0564f696efff3fb2ffe72af7ec4c77ca in / 
# Fri, 12 Mar 2021 01:55:16 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 04:07:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 04:07:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 04:08:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 04:10:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:177cf6a27ef5c990e067555516777665a0919d69d03f92e8e1585fb62fc1e547`  
		Last Modified: Fri, 12 Mar 2021 02:04:30 GMT  
		Size: 52.4 MB (52373683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f538e256be329fedd7f020e741cc9e7bf33d3be2d4805f957ee220e75a5bf4`  
		Last Modified: Fri, 12 Mar 2021 04:19:25 GMT  
		Size: 5.0 MB (5046198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beefb21b2f6f80d57a5c923e17c4c63da87a1360a28ff998cd75a0904f998a21`  
		Last Modified: Fri, 12 Mar 2021 04:19:26 GMT  
		Size: 10.6 MB (10563828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62099b3283eadad2e52ebc5135b78c1a3fa96d311fb6697a70dc07117f6663f`  
		Last Modified: Fri, 12 Mar 2021 04:19:51 GMT  
		Size: 52.3 MB (52301278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a481afe3883dfc65e41f6ea623be208df9e48f3cdc9372224aae98571e29acf`  
		Last Modified: Fri, 12 Mar 2021 04:20:47 GMT  
		Size: 174.5 MB (174536196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d1191fcd498575db7d5485e5fa2e6a787a9803a5a3bbf7b2f24e6808a57b6ed5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282283452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3514cec5c62ce1076061f9e45e8553ca459786089bb475dbe34347caeb106d9d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:03:15 GMT
ADD file:14dd8de951fe825db7d388033d6936d3035ea22c36f61cd84e564b5c97ae4fb6 in / 
# Fri, 12 Mar 2021 02:03:18 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:35:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:36:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:37:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:39:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d53db477f7b952a423ea709246666b7c318b3cced3843682efc6d4a208dea579`  
		Last Modified: Fri, 12 Mar 2021 02:12:47 GMT  
		Size: 50.0 MB (50045565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4025818d1b6987e6fb293a834f790b3ed687e5e51f4f134fe506031c6ecd71df`  
		Last Modified: Fri, 12 Mar 2021 03:48:39 GMT  
		Size: 4.9 MB (4905677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71de73a4f3386ee5720525d4d312ada7f5eee4cbce9ccbfb448f73714f705238`  
		Last Modified: Fri, 12 Mar 2021 03:48:38 GMT  
		Size: 10.2 MB (10210960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebc13ffa9b1d558ea38d4e7624dd489218e518de49c7099fee76119503d799fb`  
		Last Modified: Fri, 12 Mar 2021 03:49:01 GMT  
		Size: 50.3 MB (50312744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c056d576889311d885c002faa4b9913c0d74f77ea1cc16f190f58a4594a3ff12`  
		Last Modified: Fri, 12 Mar 2021 03:49:55 GMT  
		Size: 166.8 MB (166808506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:087035c9d1e11bae21f397ce58c5517df3e08c1623a70ea5b03786151bc33b04
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313368799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0efe7f9452afdb83dbfd15015cc17907aeeae7a3eab85478c741dd69199dd7ee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:55:07 GMT
ADD file:e98b46fa08e28b488d04d4429e536292413d7b6dfbd8a34310c44a6b65b421e7 in / 
# Fri, 12 Mar 2021 01:55:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:32:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:33:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:35:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:443483bbe5c8ae014cc3cb8df57a0b708d2b55560844a100ea84ee50c9b1736d`  
		Last Modified: Fri, 12 Mar 2021 02:02:40 GMT  
		Size: 53.5 MB (53528745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9595d36f863c2eedb478cac05b443a7facc8fbe6215c6ea34f6e78566d92db8d`  
		Last Modified: Fri, 12 Mar 2021 02:44:57 GMT  
		Size: 5.1 MB (5125646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162a05b96d3ad03a4a6a47488547154bb54acaebbb89c3308feb6fcb9e7182cc`  
		Last Modified: Fri, 12 Mar 2021 02:44:58 GMT  
		Size: 10.9 MB (10861159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b880467de79cd98ec113e06c6c828640c57a302ea1e7ba3cccb897402a301c8`  
		Last Modified: Fri, 12 Mar 2021 02:45:19 GMT  
		Size: 54.7 MB (54654979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf701b98490cccd4c5a7472f7f346d4170c5cd7a885068f3c807dc6c9d6c9a1`  
		Last Modified: Fri, 12 Mar 2021 02:46:07 GMT  
		Size: 189.2 MB (189198270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ed84bf5237a72053d8796ddfdfb124cee77546a23c6386b6826b95288f636ba4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327527979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7e8247d2c4f57bfc05ab82d8b15aaf50f20beb3ec5d19a521eeee11829bfd8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:45:58 GMT
ADD file:f2f05e5770523445c3d58c38661c24400d3d13e8d89e5e8b361fe9b063862930 in / 
# Fri, 12 Mar 2021 01:45:58 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:18:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:19:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:19:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1d51db899b128072895ed240852af0ccc606db1f5e0eb5b88ceccc9b8bbd2876`  
		Last Modified: Fri, 12 Mar 2021 01:55:02 GMT  
		Size: 55.9 MB (55863208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5781e963a9335b9df072e412a0ebc745f84d8ae613018e2920170ccbb48bbe6`  
		Last Modified: Fri, 12 Mar 2021 02:37:56 GMT  
		Size: 5.3 MB (5265307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2312f71f4fac8cca17e63b3141b7ccf40bef38b47724251c13c3b2550dac6dd5`  
		Last Modified: Fri, 12 Mar 2021 02:37:57 GMT  
		Size: 11.2 MB (11241384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5cf5f38339f2b296734f2442c2b8ee1147c6695bea0407cab5d7f8f567cb0c0`  
		Last Modified: Fri, 12 Mar 2021 02:38:21 GMT  
		Size: 55.9 MB (55895993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae66d617a9313d2dd4fcd72206cf245ff1efe6b0a2b2fdcd8132c8e49e45562b`  
		Last Modified: Fri, 12 Mar 2021 02:39:09 GMT  
		Size: 199.3 MB (199262087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:13e7ecab6ffdc9c19cf7e0c795e94cb8c66b283218873fb31944ff0388b2360c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301133550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2800cc1addd10afbd8296a440b9642d71bb4d9656b6f4e235358ef47bf9a7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:10:32 GMT
ADD file:05c36efb2a1cdd3e19c1c92b44025435230be4ef1d6ad0368a35841611aa0b1c in / 
# Fri, 12 Mar 2021 02:10:33 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:13:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:13:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 03:14:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:16:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a02bcaa9a66e386c33b8a384f0128e8f3c09d4fae3ecd414b165ed57c46c73e0`  
		Last Modified: Fri, 12 Mar 2021 02:17:54 GMT  
		Size: 53.1 MB (53099214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c432c77aca766d470bb76933642682cf43076808ff53eb201d733630878d19f5`  
		Last Modified: Fri, 12 Mar 2021 03:23:52 GMT  
		Size: 5.1 MB (5098099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97822413d3936f802a61681a5420dab88509f39bc24caa7ec14f56070b2dcef3`  
		Last Modified: Fri, 12 Mar 2021 03:23:54 GMT  
		Size: 10.9 MB (10864854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81853232fea6e8b4ba2921bb5d3b504e0e851614f50ce166ced770c074ed1085`  
		Last Modified: Fri, 12 Mar 2021 03:24:47 GMT  
		Size: 53.3 MB (53285920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528fdc99aa9f3e8aaa1cb55ae85532bcae9dfffc2c479023ac5c6fb453f5a99`  
		Last Modified: Fri, 12 Mar 2021 03:26:56 GMT  
		Size: 178.8 MB (178785463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9881608f7a11ef376df710390951aadd05716bdb8360a6ba48e4041e3095c403
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.2 MB (330209249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6758d57621e2d6708761d72a13f1d5d0b6f0218ce9090896f0e797f1e83edf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:33:07 GMT
ADD file:976d560bd7f7860fcfb64f49aa1043a087bc71ae5099f0cb06a93ac6051ac5df in / 
# Fri, 12 Mar 2021 02:33:25 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:25:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:26:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 11:30:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:51:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45911da2c88811278c7ef0cc34bf94d713837727d8059f205da3332e2aba2766`  
		Last Modified: Fri, 12 Mar 2021 02:47:13 GMT  
		Size: 58.8 MB (58753842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea21134dbd57e532f752628fc40c5d7fb196f24a6a7c14d87635986a6cf0bee8`  
		Last Modified: Fri, 12 Mar 2021 12:06:51 GMT  
		Size: 5.4 MB (5386609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe41bf7ec41499507285e048756dc75193e211029867c6225e54a5a4f4becbf`  
		Last Modified: Fri, 12 Mar 2021 12:06:51 GMT  
		Size: 11.6 MB (11615129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99fb492c43b83df8b6f9daccf9e7df4a2883b6fe988b796a394b45b30c63b23c`  
		Last Modified: Fri, 12 Mar 2021 12:08:11 GMT  
		Size: 58.8 MB (58835209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e16d0f708b407612a47815a09b72843176e8148cc3ae2b0bae18456bd212f5`  
		Last Modified: Fri, 12 Mar 2021 12:09:22 GMT  
		Size: 195.6 MB (195618460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:04c16fb11d28456c0d2af61536dd1cd327d230ce9421de483f09e807dcee1327
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295358174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2adeca3f81ac9d3ddeb9b68263940b75f4159ab61887c7eeb5b0ec836f070ede`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:46:21 GMT
ADD file:0ca8df72ab8a25212bc85ec53930c9285a0c63ea73409a2e42e8749af8d051be in / 
# Fri, 12 Mar 2021 01:46:27 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:34:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:34:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 02:34:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ae111c7645dfe78b7684eb4252c76f987ecccd3b0e2f8bf675e007362fec66fe`  
		Last Modified: Fri, 12 Mar 2021 01:50:46 GMT  
		Size: 53.1 MB (53116371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab6e9aed411053c58f4976ffb587937afb07a3caf34682be859f3e490c4e450`  
		Last Modified: Fri, 12 Mar 2021 02:40:31 GMT  
		Size: 5.1 MB (5121396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737e596c1c60857e5f5203de639f8591e441767ca10e8f3d18691ff699891e6`  
		Last Modified: Fri, 12 Mar 2021 02:40:32 GMT  
		Size: 10.8 MB (10752914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41e2306a5ae6da4bd562d74278b91b83080405dc11b7d1e3a98923c5266d7b3`  
		Last Modified: Fri, 12 Mar 2021 02:40:46 GMT  
		Size: 54.0 MB (54026091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6c02c6a94dfae92a7f13300da4db8f1f3d2e1a05a69d60317021ef4c046c1c`  
		Last Modified: Fri, 12 Mar 2021 02:41:16 GMT  
		Size: 172.3 MB (172341402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
