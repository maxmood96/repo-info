## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:fedb002c513c97e457b10f050e6bda121ee4d0fcca23d7872533283eeefb9f51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:cc67b09f7895ff3925f71081205a61e074956d54256bd70e466dd06e7481964a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.3 MB (347294744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af2dd3707f0817fcc3b435a70868b6a30037a9ebee853846727ee6c6e5cb0c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:45:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:38:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1869079ab5cc3b00301445717c112f3ddb9424b5d7b2a41713bc70d9482ee85`  
		Last Modified: Mon, 29 Dec 2025 22:28:05 GMT  
		Size: 48.8 MB (48830058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9becdec1844ece10920454e52e9f153d35fd872e9ffaceb5593016edc7486d22`  
		Last Modified: Mon, 29 Dec 2025 23:46:16 GMT  
		Size: 27.2 MB (27164425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c878fb0b7aa23d581ef5f8169f99d577505c3e94f8550d0f4a0f4615645735c9`  
		Last Modified: Tue, 30 Dec 2025 01:24:01 GMT  
		Size: 68.4 MB (68443537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de232601e501186235833bbb4a8991cbecf50342302883bcc4f16f9cc610599`  
		Last Modified: Tue, 30 Dec 2025 10:17:35 GMT  
		Size: 202.9 MB (202856724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:658b8f1cfa9d3b2e6c997c9a69412126d4548242dba1aee6beb7e2ab4909d0a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16295416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8427df7297dc36a98557f0310c62823d9bb22c2d4b507b7f556ce459a6afeea3`

```dockerfile
```

-	Layers:
	-	`sha256:0a6f8954cdac797887957eb82fadc992189b4ea42e8e92ac9583e22f34ae209f`  
		Last Modified: Tue, 30 Dec 2025 05:21:17 GMT  
		Size: 16.3 MB (16285271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ad8eff0234eb59e8791639a98bd033d4a6f9449451a524b09eddf1637f7357`  
		Last Modified: Tue, 30 Dec 2025 05:21:18 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4f4761cb2f6e9f74ba56385592c7fcfd43157693539b56130ad35103c3314b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.9 MB (294866280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1687cfff4c37b6779e88c4658ccb76e845da315bdc5b45567c9f90cbf6c63cfe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 00:34:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:35:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:241c7878eb5bbc21e3d5116dd5ea31832b2d3bc7489b0d564310ab3bd542adee`  
		Last Modified: Mon, 29 Dec 2025 22:25:59 GMT  
		Size: 45.1 MB (45129806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cfe0fcd77ad4f32a187bf7cc2a756d93850a1250b0bb64207ab8263c6fe614`  
		Last Modified: Tue, 30 Dec 2025 00:35:10 GMT  
		Size: 24.9 MB (24885689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d9e7eb1430fbc458f5de067624571165f4d9928add27333f54b491748689b6`  
		Last Modified: Tue, 30 Dec 2025 02:07:37 GMT  
		Size: 63.3 MB (63344458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382c73bf82b14c2604707d35c2cc7a74f7d70a4284ac3c8cf71ca7b836d6f4cf`  
		Last Modified: Tue, 30 Dec 2025 02:36:00 GMT  
		Size: 161.5 MB (161506327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fa94a1135d758814f2674947474a2ef1957bc0183bc49244eb1d1355406cc78d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16051167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae3f5433830de7a879b7dbd7e3981bf9d88458d001a5df5ad4b51fc9728134a`

```dockerfile
```

-	Layers:
	-	`sha256:8db56e3ddf8cce5c53ddee0b56ab42aea60601a589f30df07537478ac297de9e`  
		Last Modified: Tue, 30 Dec 2025 05:21:33 GMT  
		Size: 16.0 MB (16040958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958da71ac6fb23c9dd33e5518ccc111bc6cfe0e88d15630a9f136ad7fc2456c8`  
		Last Modified: Tue, 30 Dec 2025 05:21:34 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:21ad2eb503e3ca2e85349f9549b7e8cedeca19187b922db0463ef9ea0ad0494e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336507755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10988441801ae79bbf6e2a95b26a1235170dbe614486b1a7f19effc73852718e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:37:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d6ed83950a3f675536ad8634cde3cf4c241d5faea11ae3192ff5909f826256f2`  
		Last Modified: Mon, 29 Dec 2025 22:27:42 GMT  
		Size: 48.8 MB (48831993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf6ef9ff46c8cdd87f91591a96ba850200dfe34c376dffe91134bf667ddfa22`  
		Last Modified: Mon, 29 Dec 2025 23:46:56 GMT  
		Size: 26.5 MB (26460878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7c23095ce6398eaf80110721fa38c4bf3ba716dfc692946b69f2bf36a47248`  
		Last Modified: Tue, 30 Dec 2025 01:26:10 GMT  
		Size: 68.1 MB (68141330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7148c5060db5c03a2858e3b201d691d27c164edfd4058e81ec25d3cd2ad5595c`  
		Last Modified: Tue, 30 Dec 2025 02:38:07 GMT  
		Size: 193.1 MB (193073554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6429b3d7492e63ffe510fa9a9c5c45384faabb16271e99758fe5f7ca4057ca7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16370046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54195e419022429a930f48399a1b15a8be0bd450fd46e4723c8e27b38dfe52a`

```dockerfile
```

-	Layers:
	-	`sha256:b6253560e9b74a617dbe27dd23c0b3c8c6385d4dbd4da2c573d0d4cfbcbf6922`  
		Last Modified: Tue, 30 Dec 2025 05:21:48 GMT  
		Size: 16.4 MB (16359821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6df94c21fa1b86dc6d62c1354cd1811e9bfb2230ea1ec13a7ab08f7fb6703b9`  
		Last Modified: Tue, 30 Dec 2025 05:21:49 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ff11e4376eeb76ad954d553b3b16346d075557000f646d8234bc508f6d2ae907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.0 MB (355045015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a21e2b8891f485c0d9d6bb7663f9bdcf89d2dbd7f76f8f370828477147392ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1766966400'
# Mon, 29 Dec 2025 23:47:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:33:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:50:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a557815b7e39210fb0b4048ae58b1ffddbc8cf0f656a5974b6c3b24f7bdafed8`  
		Last Modified: Mon, 29 Dec 2025 22:25:28 GMT  
		Size: 50.0 MB (49955836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5e10cdcca6f1b0c95acb93ab2b6af2d31550b8756e6b5bae03f69991891b7`  
		Last Modified: Mon, 29 Dec 2025 23:47:37 GMT  
		Size: 28.4 MB (28412777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637f9908731534f4dd3db9b4b7e9719543000812fbb5ec06ac1443d1521a0d94`  
		Last Modified: Tue, 30 Dec 2025 00:33:31 GMT  
		Size: 70.4 MB (70407533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39a2c5a0a5ea7d4039b859f5b2fb45da590aa9aa959564bb42e296242b95437`  
		Last Modified: Tue, 30 Dec 2025 01:51:12 GMT  
		Size: 206.3 MB (206268869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:61ce177ddae815f467fc9adfcf7175757f15527008913592ed21488f178b8e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16265141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e9142eb7508440c4f9a02e7041ed25aa40d452f7268149913532c168577ff2`

```dockerfile
```

-	Layers:
	-	`sha256:d960b22c4ad30dc1a654648f5a32669ef97efcfa1aae6075134e019b125fa08a`  
		Last Modified: Tue, 30 Dec 2025 05:22:04 GMT  
		Size: 16.3 MB (16255018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fe456d4cc8d786dc056f246343ad2153f72775f8e83ddd91a64a0b25ca0e17e`  
		Last Modified: Tue, 30 Dec 2025 05:22:05 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:06da598fc830fef93b55da1e701e30655bd5e38cb8f4d723470b35f6519a056f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.1 MB (348069384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac23131226002a73ac8e35b3a88454c646efffad8d35af955596a0e95302880e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:30:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ca6b6474de59c13edb40994c0579d1471aee6a7743baa1f84bd96cf0fbd414da`  
		Last Modified: Mon, 08 Dec 2025 22:50:05 GMT  
		Size: 53.4 MB (53413786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16460d60e48e0172db82e752033b5336b64df38a32ba4e288da4b3068cc402ff`  
		Last Modified: Mon, 08 Dec 2025 23:21:53 GMT  
		Size: 28.9 MB (28864526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff96e6fb6ec2cfd3a984712824e772995b886f15a30aa9cd1af807a917dc615`  
		Last Modified: Tue, 09 Dec 2025 02:10:10 GMT  
		Size: 73.9 MB (73918725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b880315cf5eaec75e10d96ba6701919d98564258fcf9a603b0c818441829cfc8`  
		Last Modified: Tue, 09 Dec 2025 10:05:00 GMT  
		Size: 191.9 MB (191872347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:984087b97c358691a51f2c69598415113f1ae9f0291c8f2628f71c9d5a2e1039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16250875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754717f2e13092c441fa73adbb3ebd33e7867b250739833a54a0dcb75822049b`

```dockerfile
```

-	Layers:
	-	`sha256:d74fa394cc4acd86bf7024e421e524c247f362110bf7015dabbfc0ca5676f22c`  
		Last Modified: Tue, 09 Dec 2025 05:21:31 GMT  
		Size: 16.2 MB (16240698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c8aa5f285a80173f31e107e00243d4fc8181db16a3c99bc304a2dc32dc70ced`  
		Last Modified: Tue, 09 Dec 2025 05:21:33 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:07a5079cd86b63163f526d7d6225e3bc814a772411687d3631b01bcc45dac4cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.4 MB (455373372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48110a4c6f56c2ee341804a467245cc1209fbcd73c32238fbbb40e2732d8cdc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1765152000'
# Thu, 11 Dec 2025 08:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Dec 2025 06:01:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:002664050c13ca9d4571d9c24b2cd8235785825417d0a59db3d16cec4b277530`  
		Last Modified: Tue, 09 Dec 2025 01:49:57 GMT  
		Size: 46.8 MB (46840355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79762d676bf44b71b19af2f5e9bf3520032115760ca18d18b1e487b509a74b9a`  
		Last Modified: Thu, 11 Dec 2025 08:33:56 GMT  
		Size: 26.4 MB (26411155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899e9bcb2a2f2dedd16603a638381275feefb5833c5f56fd53977194d927e781`  
		Last Modified: Sun, 14 Dec 2025 08:38:25 GMT  
		Size: 72.4 MB (72429817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbf6f859df9d39b71e55095171de1ab0e019f15b8eea9901570eb9dcfea6a05`  
		Last Modified: Mon, 15 Dec 2025 06:18:31 GMT  
		Size: 309.7 MB (309692045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6363b6878b619892acb81b77cdc3d1580f1c00ac9125fc0aee4fc9b63e7d6e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c7f3ed34fa0d601c155980803788e85e0a63f8d846a87213b42cb02cada1dd`

```dockerfile
```

-	Layers:
	-	`sha256:f6aee94621a200712b5a2e2bb7d0fdfc2d2e326881cf10b0282f14767ec5e1d7`  
		Last Modified: Mon, 15 Dec 2025 08:20:51 GMT  
		Size: 16.3 MB (16321486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc60d85882b91adad72bdc91cb0c573612f41d7bf763ae4150f59945bac2479e`  
		Last Modified: Mon, 15 Dec 2025 08:20:52 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c0f7c4763496ca83a86b9f277d975aafcb1254198de86b17a67795c03aadbebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321115529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2823e324f7dc04084c0936998f6c166b7db08f697d087623fa4a6dfb14a011e9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1766966400'
# Tue, 30 Dec 2025 03:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 04:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:04:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ed754f864448d0e594994dc11148ccb02da6ea309851c997288e88ce4fa4e08`  
		Last Modified: Tue, 30 Dec 2025 02:08:24 GMT  
		Size: 48.4 MB (48397553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d28917da9bd93a97bef96b25f92932fe3babe10b8325e0cde3317e7a34eba7`  
		Last Modified: Tue, 30 Dec 2025 03:24:40 GMT  
		Size: 28.3 MB (28270771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0cf5f751d0c65a3f9d4bfed3f5391773af837d7f314dc3df35eca86c8c1ce0`  
		Last Modified: Tue, 30 Dec 2025 04:14:08 GMT  
		Size: 69.2 MB (69167734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba6528e977b701a6ca8e6a10e57118508dfadd0b4e4df9a01d485225eab7bf`  
		Last Modified: Tue, 30 Dec 2025 06:05:10 GMT  
		Size: 175.3 MB (175279471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dc879526ac5002711cddd9b01f5e8adbda99716474ce54c35c7b58077717544a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16072586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600de32321885c8ff19c9cea4f75ec62a61816da42d1965f44a73347e312ac59`

```dockerfile
```

-	Layers:
	-	`sha256:f7fc355f088156d502cf7f946691413ab1fc11f1e6ba1eb56a4cbd725d080954`  
		Last Modified: Tue, 30 Dec 2025 08:20:49 GMT  
		Size: 16.1 MB (16062442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29ce8fd13d77d6dd11340a976e66766cb735d410361c695641d642e15d8c159a`  
		Last Modified: Tue, 30 Dec 2025 08:20:50 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json
