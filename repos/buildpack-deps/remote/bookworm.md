## `buildpack-deps:bookworm`

```console
$ docker pull buildpack-deps@sha256:8c30a94b4fb5caf5bd7d24f45791b590a56c1260191876b06404692a507f366a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a9ee5a22b083dfb713fa536b4f5bb44209c7534f837ad29f806ff8e21b5806ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.3 MB (348252857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a210310b5851693a3478c27a0cee7e1c173687ba37b6395c419618fe8f06206`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd32ebdd0f2fe46fb720e197c4b837800d63f944a89569b03e24d7c92663b11c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15479171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d78bb7f67ef8a00ff64776d87e0c9c275aef937b98767836daa1c95b04e49e56`

```dockerfile
```

-	Layers:
	-	`sha256:f0ecc11d0f916e623f0b7ce305540399a71a1e35b152c06422349804e05c368a`  
		Last Modified: Mon, 28 Apr 2025 23:12:17 GMT  
		Size: 15.5 MB (15468631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d305286508cdc02e93b91c3172d535ccfd58612d2095a8233b4071e4a03fdfe7`  
		Last Modified: Mon, 28 Apr 2025 23:12:16 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f6d0affbe05ce3a92cfe70c9cc7a73a16f4df51765e163e4fe0cb853a228690b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315378187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e293fe1b9686654e664f1de4a256ca4bc556967f3275b2d391db9a87ac7254af`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:41b62f0ff831a6d9573670f580122f67e27137902fa02ca0a3faf11fda42603f`  
		Last Modified: Mon, 28 Apr 2025 21:07:39 GMT  
		Size: 46.0 MB (46026796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933aa71bcd4cf4d4ade7e455a6a748ec9d00e74ad6f8b2dfd8f9c9b70593ba3a`  
		Last Modified: Tue, 29 Apr 2025 06:01:08 GMT  
		Size: 22.7 MB (22689607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461cae6835e6d9e4c238b202d114b5fb2f2b659479fcad91acee966b7bf3bcc9`  
		Last Modified: Tue, 29 Apr 2025 06:21:48 GMT  
		Size: 62.0 MB (62005790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfb6286f141608ba5fe6c6ba2dc6eccf0574268a7436cd81d4de08cd3894433`  
		Last Modified: Tue, 29 Apr 2025 07:09:54 GMT  
		Size: 184.7 MB (184655994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aafea3e94fd67c0f29eca348404165f572ee0d02f3a40ecad129339777bf5eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15278157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d49b1e7cd3b0304d2c3723846169836f739c99682cb2cf5c9908958b3cc609ff`

```dockerfile
```

-	Layers:
	-	`sha256:bfebb6796989ebb6d9bf151e1f5439f64131042af7eb3cb188e1d9210ccf4891`  
		Last Modified: Tue, 29 Apr 2025 07:09:50 GMT  
		Size: 15.3 MB (15267549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:369a8401a72834aa4a53d910ca98b0ad1f47b3ec2cdcbc817716e2c793c7526d`  
		Last Modified: Tue, 29 Apr 2025 07:09:49 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:76e47282845f8f503774acdc0280fb335ddc983546e7450410d18dd8ed32714d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301071852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305fae71b846aa1784d2ad04bbc2a785bbe99b4bac6e66f0697fd5b68760ebbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d55cc6c59023a65c15579520e32553ab9f1e2d6377e8e4dd69393e113713d3`  
		Last Modified: Tue, 29 Apr 2025 16:44:12 GMT  
		Size: 175.3 MB (175316182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:77b1a7bf5febd0f87f61cad4c46fd1b3ffb48a512d802daf1dd8f92e21fe25ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15283631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dd0c205e9f4716fa8a65266c37cf1013f74f6a60406db65ae80509e3882a2a`

```dockerfile
```

-	Layers:
	-	`sha256:4425b6aea5b2b0c8894140cd2df077f86121e1cab65b92e02788ac0ff53d1a8c`  
		Last Modified: Tue, 29 Apr 2025 16:44:08 GMT  
		Size: 15.3 MB (15273023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e375c5f8ce4d4008fc64e99a82b75832d6e752bdfe3c127a3415188484a83544`  
		Last Modified: Tue, 29 Apr 2025 16:44:07 GMT  
		Size: 10.6 KB (10608 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b71388eaf7e01ef4d2e69592c1f30e94df49e5d422289cf201657a89ed8610f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338975816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e7972d1201ae37a705096e14cc05fa47576b7935c36d8f84748bf3afbe0d129`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d41c7623f41e51939686bf861fe89538ae4dc84481ff4136b55524e770d2603`  
		Last Modified: Wed, 30 Apr 2025 02:16:31 GMT  
		Size: 202.7 MB (202748227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1b3213319a09c519d65301bbe02cdf777c464b9d66bd821164dbab01e8b83420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15507776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f68436ce2dd94a1824df8a80f1094bf8e032a18f592b4b8d218a66c53c737c`

```dockerfile
```

-	Layers:
	-	`sha256:f39ca6cf709374fbe5b717d0053e3a751bbbdc666725f582f1f9f04142009b2c`  
		Last Modified: Wed, 30 Apr 2025 02:16:25 GMT  
		Size: 15.5 MB (15497144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e2c734854a952beda78fb4e235834932b91ca70e1cec1eabe7ae590b0f9d16`  
		Last Modified: Wed, 30 Apr 2025 02:16:25 GMT  
		Size: 10.6 KB (10632 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:65db65f2f41c4a11b716d0f5c036bb2246d560e1a393365e0d249efd7ca5f564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350847733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:027307bd43d16b5aff5186883fd40160becaf978d824b640b234c8b6e6906d1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1528cc13747bb103866d00332de43f9304156fef5a2f396b15d9e173b1365f5`  
		Last Modified: Mon, 28 Apr 2025 23:13:00 GMT  
		Size: 210.3 MB (210293092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc13b5ea82deb4cfbc028044b4b75a31768b2176038234806f4949893f52a9ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15457737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d28c3eac07ab74d752c7679d8b5b699f7e3df1a93e21e80208ead07f4c4117`

```dockerfile
```

-	Layers:
	-	`sha256:405bbc44ab704610a7966ac3e632aa3444e9eb9c20054a9481cbff7591ba4ca2`  
		Last Modified: Mon, 28 Apr 2025 23:12:54 GMT  
		Size: 15.4 MB (15447224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b15065ab5693fc1fc2bebc1535fb49a0ad735e21e4b906e9db6f8e1b0b4998a6`  
		Last Modified: Mon, 28 Apr 2025 23:12:53 GMT  
		Size: 10.5 KB (10513 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:08fdcacf05a6d09ba0af1c9ed40d6c7ded9e14c1a4707dcc59732ac655d0000c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325621344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0f0af9aace3d6ede2d178a49792dfc5484021cb54373caf48c617503842339`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Mon, 28 Apr 2025 21:10:59 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Tue, 29 Apr 2025 12:43:07 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1d30b00e6e88ef455123e625951481f519a50849cb9e967c590e851c17b408`  
		Last Modified: Tue, 29 Apr 2025 21:16:09 GMT  
		Size: 63.3 MB (63308148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d3c73f9a369d68121002b85e15bed118b5f9aea42d9fe654c6ac01aefd9236`  
		Last Modified: Wed, 30 Apr 2025 03:16:35 GMT  
		Size: 189.9 MB (189942024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c7ff18cc9905da2e2bf1cf55e6cb8fa1531dc37c9c8e9a6fef8edea8431596bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 KB (10382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4857d7ee3e83869e8458ee1e085f9722fd71f12805b0b05cb4058ec78467c662`

```dockerfile
```

-	Layers:
	-	`sha256:c9dff1746316c882e9ad30506a9f0764abeb7d1e67bea38cd5b0322a62373274`  
		Last Modified: Wed, 30 Apr 2025 03:16:18 GMT  
		Size: 10.4 KB (10382 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dd4024fcf3f0db626442f6b34a0692e9c0f9dc9f14e8c6fb9c1b235fa38bd619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362231906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3c35e6d9f31722ac35bbddab3801300e10aad40b9030a055ca6f9c1d30fb65`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f7f895e65e8530bee082db2e14aefaa34547b4753e60990faca2b691714e63`  
		Last Modified: Tue, 29 Apr 2025 09:10:46 GMT  
		Size: 214.4 MB (214409240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c45db60cd40c5d109aef1c44e35b1f355cf65877247a2cb3e57f2a5501926e0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15455581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2295905217caab8ddc9d0ad05a12a332c6d8f816fcad1e78200403bd3ec893ac`

```dockerfile
```

-	Layers:
	-	`sha256:38cbb9abaaaff415d42057d340d06512740a632e6ab0ae2d7fa52de75a6fe283`  
		Last Modified: Tue, 29 Apr 2025 09:10:41 GMT  
		Size: 15.4 MB (15445004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402793c2fdb920562f02679fbb3b011a29a5fb63384fd4980e4ae1678e37f700`  
		Last Modified: Tue, 29 Apr 2025 09:10:40 GMT  
		Size: 10.6 KB (10577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c0e0270db5f78eb94fcee89863dba68b288fbdfb259aa7452c411fca04099cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318062483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8552272ac4b5a26feb1cf73a3d7dd3222cb821e3bc4232fad49d9176133f57`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfe8bd3e826ba76e4ad73b0a5ce638276af95b860bec9b25c2754c5600c5a61`  
		Last Modified: Tue, 29 Apr 2025 05:34:00 GMT  
		Size: 183.4 MB (183405963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b75d1c2d392663af7af0bc4105b05dbc1a3b7772530a0eacce11873f91f975c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9593e4d960fe43bc8a9dd5e166873127dbb0ebc845801eeb648c4a8da358cd0`

```dockerfile
```

-	Layers:
	-	`sha256:87ce056f10f0f89331e22aaa7645300fd36812b0dc5f827ba4ee4eedc189401b`  
		Last Modified: Tue, 29 Apr 2025 05:33:57 GMT  
		Size: 15.3 MB (15281321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e311022d94634b9f268613a7748ab83f692f55cf7a581a4664867b0c37434111`  
		Last Modified: Tue, 29 Apr 2025 05:33:57 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.in-toto+json
