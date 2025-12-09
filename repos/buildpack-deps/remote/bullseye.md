## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:6af791007696db413181ce67407b6380a2db508595460f303c9da41f91ec97b8
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
$ docker pull buildpack-deps@sha256:c6bd288cad6643bb262a926d956c3c0e4fb09b072c74c355a3773c46c5b494cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321482063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8153d9567b5aea033a4971a831ea3114fafb9cce5e5cecc5080626eca342f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:43:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291bf09cec80aaf3d13eefc3fba3a6cb13a44cdce91da75e0e2c3d8b72348e79`  
		Last Modified: Mon, 08 Dec 2025 23:07:20 GMT  
		Size: 15.8 MB (15764219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17ff9cfdab33e1021de93428c7968b682c4bb6322df919b3c6622b8ac14ec0b`  
		Last Modified: Tue, 09 Dec 2025 00:06:29 GMT  
		Size: 54.8 MB (54755559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853b40334c538bcc5e2df110b0fecfb8423a3bbe5081982d24d096846277413`  
		Last Modified: Tue, 09 Dec 2025 01:40:24 GMT  
		Size: 197.2 MB (197205872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fae13cb60ee12dff1896ea738482909f952cffecc1a79f0e0f221f60685e98b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15472421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8359a821b3ca584bef89312ebc61c85ea98435d659c172ed24500d95a3f2692f`

```dockerfile
```

-	Layers:
	-	`sha256:9af4fa87ced295358010743d6703f29b6c103eabad89b85bc0178baf29c84483`  
		Last Modified: Tue, 09 Dec 2025 02:20:56 GMT  
		Size: 15.5 MB (15462226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c5b25c8e4d61c24858b053df8a983de2251a7bd2685d0687548bdee7148cb2`  
		Last Modified: Tue, 09 Dec 2025 02:20:57 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:839b6b3b21c746713b315f0e5d854fd689c8f6059b145d5ed77da125e0b48e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282530080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa194e9822a3a48ae7141d5c35c943cdb6e08295708f5b6a1d359c6fb36d48d8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:05:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:33:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 02:15:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4b405dcfbbf208b50f83cb073fc2340dc0c1fad234dcbd26845122feadf5cc1f`  
		Last Modified: Mon, 08 Dec 2025 22:17:00 GMT  
		Size: 49.0 MB (49046374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bbf36f43e54145168310c9263866569faa887bc243d2f3bed9e99c1532e0cf`  
		Last Modified: Tue, 09 Dec 2025 00:05:40 GMT  
		Size: 14.9 MB (14879319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686e406069dbcf32b42bae4ef9dc2c57f02332b4d3e3cfdd9f3d4277550d22e9`  
		Last Modified: Tue, 09 Dec 2025 01:33:36 GMT  
		Size: 50.6 MB (50630265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bcddda7031f4f5f6fc7c619eabba15aad24652c60afd97b83b74d6cb3b067c`  
		Last Modified: Tue, 09 Dec 2025 03:36:23 GMT  
		Size: 168.0 MB (167974122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed0057a0570f6cc4d736c1c36e113700eae180ef714283c5690ea6155c28583e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1613bd5531fc20dd0f1cd84d0412ef92eb8ac35c0ac77f87cfda182e97558ebb`

```dockerfile
```

-	Layers:
	-	`sha256:336ae502e42914717fa131ab016239760cdb3b8c40dffddbb1b33bb55d82a156`  
		Last Modified: Tue, 09 Dec 2025 05:20:25 GMT  
		Size: 15.3 MB (15261544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4fe7f13d6a199ecfc438f446feb244770b73bc4d9176d84b9484974a8e9564`  
		Last Modified: Tue, 09 Dec 2025 05:20:25 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:571444e001aacdf1ee8463eb26097ee206e4a8c490266ade732eec93353f9a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312977511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7809e41f567304c5002e7652d9e1522ac228a09d278a55a2c1b6dd5ec35c1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:14:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b879966726dc963ee08cbddddb10287e93034fcf9e3ddf7a290b1b7e42538c`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 15.7 MB (15749537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9cd25be3019ce9576369c1d01896d355c209a13773e0054363e0e12e57b0e1`  
		Last Modified: Tue, 09 Dec 2025 00:11:43 GMT  
		Size: 54.9 MB (54866122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8012df9f3f9ffe1b4b7749d91d60381788bf2363eb4b53d656bc467a3673fef5`  
		Last Modified: Tue, 09 Dec 2025 01:15:34 GMT  
		Size: 190.1 MB (190104139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d31aca88ca5a3173ac45abf57966c90a3fa7516033eac9944e8ef00e5763d291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15474446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae313dd960992918fd3c210a6dac91aeee7ba20b09b4de1019d9b384d224580`

```dockerfile
```

-	Layers:
	-	`sha256:1e3f91435b41c81f1e46824be254a4790b5abf7071ffcdfeecc59bb7568114d0`  
		Last Modified: Tue, 09 Dec 2025 03:48:34 GMT  
		Size: 15.5 MB (15464171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04599cee7a2192480c862269ce21b93115d4d681726eee809b79a952fa80f10e`  
		Last Modified: Tue, 09 Dec 2025 03:48:35 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ad9e7485a6b734329a376c25aaac35475910f74c2230cd4110c406e3298b86b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.1 MB (327119563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3101499bd83225fe851c02eb60a241f14b1b7bbe81650c352ec146167c81f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:14:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:23:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:16:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:20381eeb836e270b6cf9dd675babbdf823eb79206c868ce7f8ae8aa6250aa68b`  
		Last Modified: Mon, 08 Dec 2025 22:16:45 GMT  
		Size: 54.7 MB (54699532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b1d3bd8e8172de52ae5d3823cd522bc420b102de9f2d204bcdd0b93d98aeda`  
		Last Modified: Mon, 08 Dec 2025 23:14:29 GMT  
		Size: 16.3 MB (16267791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efca8130eda77d172d5308580d8be6986cfcc5e94679f7a976c73a11cc2f674b`  
		Last Modified: Tue, 09 Dec 2025 00:24:12 GMT  
		Size: 56.0 MB (56048951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038937a01f7048871e1c02f1d50fafb67eabf3c0196b963ee8a6bae18ae10e17`  
		Last Modified: Tue, 09 Dec 2025 01:17:45 GMT  
		Size: 200.1 MB (200103289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:70ba5643d565bf93907d4c2ce7ef213cb9b332ffbea1fb83f5b10268b9ddc1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15460413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39eb572baf57eaed85f24a5c80396c1f3700e69213bc78f9480cbb4dc1168f9`

```dockerfile
```

-	Layers:
	-	`sha256:f0b439263dd7c570870c52600ec9f7d2bccea50d4ade5b07fc82a42ed620de86`  
		Last Modified: Tue, 09 Dec 2025 02:21:37 GMT  
		Size: 15.5 MB (15450241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f627c508ca99e103a99cdb659b3c0db3991c41e0f9bf603533b64ff72512b099`  
		Last Modified: Tue, 09 Dec 2025 02:21:38 GMT  
		Size: 10.2 KB (10172 bytes)  
		MIME: application/vnd.in-toto+json
