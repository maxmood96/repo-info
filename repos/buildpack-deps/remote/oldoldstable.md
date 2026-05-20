## `buildpack-deps:oldoldstable`

```console
$ docker pull buildpack-deps@sha256:a7b21c9a3c0a68b8dc7e640568d0066ad2ac614bbc5bc80e2309b615007c953c
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
$ docker pull buildpack-deps@sha256:869e63da9cd7cadc2638ca1e3c29bdc21a945546a129f20a61342e0e0aeb9fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321610846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7618c60dcea33253b1ab6e456c20e61c02e19e84370179ee4b140f818568fe5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a725631376ff1c8c144d62e01c2dd134ff006899cd43c1aff2afbb3141faf91b`  
		Last Modified: Tue, 19 May 2026 23:23:13 GMT  
		Size: 15.8 MB (15790858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5942943df443b1bc1e709676d52a57b0a7ddee0c58a1602ecf5e2e8b271916d`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 54.7 MB (54743262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecc88763ad50d1ab5c41218bf6aa5893d2c739925d42b6eb8f2c52823019e44`  
		Last Modified: Wed, 20 May 2026 01:16:23 GMT  
		Size: 197.3 MB (197307874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd001f72702357b820f362f078abbcb40c93af41eb3e6f3b15ec5499635bb400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15481772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb6dd0838f08d71c3c45a932d9d025896414e87bd93a1ed783389c2874ec80f`

```dockerfile
```

-	Layers:
	-	`sha256:4d9fed555e6da8c4b07ee9a71bcd1c1b6b561b61420834a146fdb67b84623514`  
		Last Modified: Wed, 20 May 2026 01:16:19 GMT  
		Size: 15.5 MB (15471577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11be2bfedae0c89f51edd24b042a4398236c2e14f2a130a9408735f9cd2e087c`  
		Last Modified: Wed, 20 May 2026 01:16:18 GMT  
		Size: 10.2 KB (10195 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1c981c126bc325087e2aa5241def421ca3812b728ffba72d262912eeb26eb7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282339957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8225cfb58f2b7b26daf8773b79bee36a45c46aa8120eba5a7db4dc3753ceedf0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:03:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:34:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:14:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c303da1bd3f277cef3c251ecb02fe6ceb28404700c2776e5e52078361e0d5a63`  
		Last Modified: Tue, 19 May 2026 22:36:43 GMT  
		Size: 49.1 MB (49059808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6159604253fa0b585197db46cb3703cf956f0b1a4d8cb67a661c9f449e5220b`  
		Last Modified: Wed, 20 May 2026 00:03:11 GMT  
		Size: 14.9 MB (14905378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb581721ec88241b5b5ab6b082d3be5546d7889197d205126a49442b917bbba1`  
		Last Modified: Wed, 20 May 2026 01:34:28 GMT  
		Size: 50.7 MB (50659222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9412242c111ef7d371b4d7f9d3c50953090d140db79f045fca66bbc462846c8`  
		Last Modified: Wed, 20 May 2026 02:15:30 GMT  
		Size: 167.7 MB (167715549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:10ee47f45bccfc5ad8537e57662494b5d12333fbe9b46636fd3bba5083b14d83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15281154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf91cf15d19c53d787461ca976f1267d173aae3dfc433c64fa4b2fd497655377`

```dockerfile
```

-	Layers:
	-	`sha256:f663c35fe6460282230352c99554e8814263384b59fbeda9d2780e79d86e8b79`  
		Last Modified: Wed, 20 May 2026 02:15:25 GMT  
		Size: 15.3 MB (15270895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29945754e8b5539e4586deadbbb967306f30e9db022ed2dd63452641120832ce`  
		Last Modified: Wed, 20 May 2026 02:15:24 GMT  
		Size: 10.3 KB (10259 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:26c36e784e2b5f3546d8cb90416d3a2fa4b7efbefcc74d89ab5824c5f29eb05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.1 MB (313120706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418dd129beaf45857674a4f5de88131963aa46f7dfc2cf5768d1a6a94ffeae5f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:26:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b862d1986560a28dd19f86c2aee630b1502d7f508a9266ed7d99d6f03a48419`  
		Last Modified: Tue, 19 May 2026 23:26:59 GMT  
		Size: 15.8 MB (15774880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522a0e24f23d039a1a5ae21822bccb045bfdedf83da569dc13fb1992e903bbcb`  
		Last Modified: Wed, 20 May 2026 00:27:11 GMT  
		Size: 54.9 MB (54879862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5578d03844480631fb598cecf497312529f7e21642b612b605246de4df178882`  
		Last Modified: Wed, 20 May 2026 01:16:01 GMT  
		Size: 190.2 MB (190209386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:94c21ce83c9c4fe034410c59ae199cb8a846c42c8b187abf6146858b78bf2bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15483797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e4552c4b87d0b8c48e8f162c7c54a8ea982c1a004f7079a5dd6c9f8846a86a0`

```dockerfile
```

-	Layers:
	-	`sha256:4e837effdbd916da129cdaa30a605477511dba0b92f48d3d0dba8023fd77768c`  
		Last Modified: Wed, 20 May 2026 01:15:57 GMT  
		Size: 15.5 MB (15473522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b122d72ce44f2453fb8a8b019a574b51ef23657163c257415b5eda358c671dd5`  
		Last Modified: Wed, 20 May 2026 01:15:57 GMT  
		Size: 10.3 KB (10275 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:611a27f2250571fdb6ce610e09a87a3db73f86a5d1d2d329165801da616d5bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327206447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99281432eba15216bedaad0e5f584c4a0abf87045af8ab769e8dab40e9a7a27`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:25:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:02:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e09eb609a6245c10b9cb43e597a7ec3d9e4224f925e717a38f2fb36787a4e7c0`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 54.7 MB (54709050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638a100a514adffbab3ef3834e4740a809fc60c49ad1b434f56a2d8254524b75`  
		Last Modified: Tue, 19 May 2026 23:25:19 GMT  
		Size: 16.3 MB (16295788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927f642862236d0c357dc4ae576bafd5ea8cfb669f7a55b517fc7627c3283f4b`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 56.0 MB (56046808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db8f3fbeb17a8bd13e4eb6de659e76a8e6c76fd6b0fd0a16a26b1613dafc13d`  
		Last Modified: Wed, 20 May 2026 06:02:56 GMT  
		Size: 200.2 MB (200154801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bfd6835f2822871ef8c459cd8792429069b2476f7d3e640d7b985902eca2a7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15469763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc5d0a3a1fed00e5896cf5a21c7239d45615cb857e313394057049d4328767a`

```dockerfile
```

-	Layers:
	-	`sha256:37c47c26fa21367601dbbb9c2495eb8ce02b9c0aaeba9befc207fef756b96193`  
		Last Modified: Wed, 20 May 2026 06:02:51 GMT  
		Size: 15.5 MB (15459592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:685152e717f8126e7230b8b0ab1ed5f4b02297ab8933469473aad30b605bd60c`  
		Last Modified: Wed, 20 May 2026 06:02:50 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json
