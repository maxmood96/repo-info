## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:2081610b9e8022a71a59fca2a7af5deda4d7c6a3e930f3667a7bf25e4697e343
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

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e001d718eccad290db87b65fcf567a4ad494cdcde21a3602e633ad9daf2a9430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.2 MB (321155613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58361a4052347d338440aaf4923e9b6b752fd37343a475d6b6e27dda70013b73`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aae550f4768ad83c7dcc1ef8de6de078a33effa152d846f4604ead4cbb1f414`  
		Last Modified: Mon, 17 Mar 2025 23:13:33 GMT  
		Size: 15.6 MB (15558355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a322d21cc1b9c3e86a0528fd885e7483a3b2497c1448256bf87a4493be665ab0`  
		Last Modified: Tue, 18 Mar 2025 00:18:59 GMT  
		Size: 54.8 MB (54752320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6dd983ff133914060200e7c5e808fcdd44c72679c04f55059151aa2050dc87`  
		Last Modified: Tue, 18 Mar 2025 01:13:41 GMT  
		Size: 197.1 MB (197103663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d10c8f17ef8a62ca42c65598b743fa794256b4dd990d93169dc4ad94abfdfda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15081760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d6412856618c1641c0fd13ce1ca725b29fe800bd7332012cd5cc3b5bed6c97`

```dockerfile
```

-	Layers:
	-	`sha256:f7d45408201b790f07f765d636fa643512a452e0bb5976f3f81dd0b1e57175a0`  
		Last Modified: Tue, 18 Mar 2025 01:13:39 GMT  
		Size: 15.1 MB (15071528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806d34d5f038deaef19bddbb7557a5380fb73b8d743b3719f4c36a225ec6b372`  
		Last Modified: Tue, 18 Mar 2025 01:13:38 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:fca4b208229a719ee614dee22186e2834cb085b5ca75d2836223fa99acc00b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 MB (281900655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55b9682e77a4d0b2ace360e551fdb6df2b89081ed54c3566e6caab24ac686f8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6676c7b3b77e9e71cb741c5c04bfd9a595560092d9024884d0ce64c66f48bc6`  
		Last Modified: Tue, 18 Mar 2025 16:15:00 GMT  
		Size: 167.6 MB (167559857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:51252ec8cb3ecd263c0ac9a0f8113d9296619c056581885f7122f1de05b5e378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14882585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ae74366b450e6fbf4f56bd25974e7da57efeb9817c16bc4357bbb389840c54`

```dockerfile
```

-	Layers:
	-	`sha256:f3a927fe4b06476007cbfa975515d7f13fd7834524fe8716410098b62c2abada`  
		Last Modified: Tue, 18 Mar 2025 16:14:56 GMT  
		Size: 14.9 MB (14872293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a59484f05b1c341ee9a292fc5f95c14d03533800117a53a3b2f82401514c98a5`  
		Last Modified: Tue, 18 Mar 2025 16:14:56 GMT  
		Size: 10.3 KB (10292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:600a5ec5a124ad933b7c59d01df3acf8d5fd231b0b2010404572840cde86d6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.7 MB (312668613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2b42cf00f9d12f1803e5cb8307473353b34ebe57c56d3e437ef7b56df2e8cf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:645bc92dcf4a3c806f112acf0724041051eab86b13816f8d7286950facb47ec3`  
		Last Modified: Tue, 18 Mar 2025 05:00:00 GMT  
		Size: 15.5 MB (15544004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96fedce3b84d801b5eec66fa2ddb4a4653be64f8e04188e6e7ab37b6566bd34`  
		Last Modified: Tue, 18 Mar 2025 13:15:20 GMT  
		Size: 54.9 MB (54855429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15780e9924523e788780ac991f29afa248c22b09abb68f8a9945cf272b3dc84e`  
		Last Modified: Tue, 18 Mar 2025 14:12:21 GMT  
		Size: 190.0 MB (190020786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5446eaee0a980322f36b066ad8e77750bf0cab3709eaea1aa72a3757c9b3bf16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15084074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d647944ed499f584b014fcbaa754c92e855d852f75682d974d5507e0850493dd`

```dockerfile
```

-	Layers:
	-	`sha256:b7a5683d817630ebdfcc6902dec82f61d6d1345532373479bae80f956cf371d4`  
		Last Modified: Tue, 18 Mar 2025 14:12:18 GMT  
		Size: 15.1 MB (15073762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f8209538ebf2eb2e3616cb72d35af65984326fc4cd5ba90e83a50b88d97c5e4`  
		Last Modified: Tue, 18 Mar 2025 14:12:17 GMT  
		Size: 10.3 KB (10312 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:28af9da193036e92d8fd3342b37be3e6057ab10966d01936ce3bf9619e531d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326778834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3392056b361f5d345053caefc8babfdff3f7b86e32e54817f181d96b8d96822a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b2bf052a55a1540734073d8a106c4845ec09ac4ac8cc46a275584d3eef876deb`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5503af74d5075005e8a2caef8b6b369ec49cf0d7a20dcdd1fe79d68aa4ba6c`  
		Last Modified: Mon, 17 Mar 2025 23:32:34 GMT  
		Size: 16.1 MB (16062045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfffc7337857c58b61734136d663ca328549ab864bf18f3217e50e3fdc25680`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 56.0 MB (56030008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df6c0e66903ef70af0189af240e3c0623f78105cc07d6d179e9ccce9fb96781`  
		Last Modified: Tue, 18 Mar 2025 01:13:46 GMT  
		Size: 200.0 MB (200008164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3263a9aa1f48ebb8d15d39c05a9b835ad64f2b39484a89c51fd2b9cc8246a860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15070078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2224cd04f66d8e2d213a2d1d33c75dd5c1792e7e68d092c4cfac18a008e43193`

```dockerfile
```

-	Layers:
	-	`sha256:2508e833f0c13079b324f73999dd102d257cb3f3046b604434edc8e7d2a0cc4a`  
		Last Modified: Tue, 18 Mar 2025 01:13:42 GMT  
		Size: 15.1 MB (15059868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:713144375a3728752bb8f2e76cbb9972b32d8f9918864d8343e04a3fd580ab4e`  
		Last Modified: Tue, 18 Mar 2025 01:13:41 GMT  
		Size: 10.2 KB (10210 bytes)  
		MIME: application/vnd.in-toto+json
