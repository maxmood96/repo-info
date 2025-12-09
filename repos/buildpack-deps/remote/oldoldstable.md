## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:70ac468e194bdc80c1a9a0842903d9c5c98f6a380e75988a07e2a1267778f9dd
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

### `buildpack-deps:oldoldstable` - unknown; unknown

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

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5a772830cea6a52b85d6284f7e1a5d747c53fdbc90181032c0e1a9531d45eb78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.5 MB (282530947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84c4bc6c9c3dea17f74a72bf0a6d2ab138cf8afe60e66f37ef7de14dc44091f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 03:57:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:22:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:516616c63b11e5af36116ed0b70c230c2287eab3b74b11a00eb299cc4575af64`  
		Last Modified: Tue, 18 Nov 2025 01:14:16 GMT  
		Size: 49.0 MB (49046365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2280342788a66a44d1f2e4bd1eaf8389d9bef9428e09fa0ae948652bfaeee4b8`  
		Last Modified: Tue, 18 Nov 2025 03:58:13 GMT  
		Size: 14.9 MB (14879454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f566f1ab80bd353b42ed837b52fe4ec496dfff10630b53797d35c9eb72bc27`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 50.6 MB (50629469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae163b8147549b72151eb921eaef5a03a6a925fe675fbadbf871e2bfc1097c32`  
		Last Modified: Tue, 18 Nov 2025 07:35:47 GMT  
		Size: 168.0 MB (167975659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d8f6154508cf8b0113f9bce86522e4d3e3f4a4051c2d754d8811246a11fea02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15271749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eedde2be4b647bb59585487e7098dbdf2e356f74a475f0d7e6c74771b3b4590`

```dockerfile
```

-	Layers:
	-	`sha256:9dd18b1fe2c941a444a632347aa4a0eeb153ad5fadc956bc7aaa9c0ff4bec162`  
		Last Modified: Tue, 18 Nov 2025 08:20:43 GMT  
		Size: 15.3 MB (15261490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a537d729a48dccb830b83fcaa27a4018deefc2d3cd581717159a7331690124`  
		Last Modified: Tue, 18 Nov 2025 08:20:44 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:838fb83000d4a50402f612e5a9234170fc27bdb895f621dc28a525d4507ea3f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.0 MB (312974997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8c5cfcf4d82e8e3df4812f3e6d8d32f7629a784703747a547bc7410a57e8be`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1763337600'
# Tue, 18 Nov 2025 06:23:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 07:14:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 08:17:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8dff54e867b76cc09c8e52f48696bb831da283ce2001738567e4185ac2527613`  
		Last Modified: Tue, 18 Nov 2025 01:13:35 GMT  
		Size: 52.3 MB (52257695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf5c6e26abbf2d346305acdea26f4c77227ae8be9882711816b29b75df95827`  
		Last Modified: Tue, 18 Nov 2025 06:23:37 GMT  
		Size: 15.7 MB (15749561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cbea18607285d70f010e2ba402394373534fadffb00b880a34f03b4cba581f`  
		Last Modified: Tue, 18 Nov 2025 07:15:27 GMT  
		Size: 54.9 MB (54865154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195c5566d8037d8b54b239588b83dd1faec060ba39679db65c2b1da016b183c1`  
		Last Modified: Tue, 18 Nov 2025 09:10:52 GMT  
		Size: 190.1 MB (190102587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc7356b21ab2d1bf04fd9f80818394e8a355a33033129ae8275e42264cc20ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15474392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dd6b3e253ec9373387b0b6a2565e048fcac1c0459e544040a64bbdd1be070b0`

```dockerfile
```

-	Layers:
	-	`sha256:9de2d683504cbc09e916d1c4de83c1eed1fff62b0909c1e3326f1744f7fbdbe3`  
		Last Modified: Tue, 18 Nov 2025 10:42:48 GMT  
		Size: 15.5 MB (15464117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686a859bc0ff914f42129a880339c0edbc259189364a9e50ccdd35c5c6c9b25d`  
		Last Modified: Tue, 18 Nov 2025 10:42:49 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; 386

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

### `buildpack-deps:oldoldstable` - unknown; unknown

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
