## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:f16bc3c501b51c95e9f50acab7cee6865b17ca02a2c2740ddab4bbb1643d90b8
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
$ docker pull buildpack-deps@sha256:e5fc31d8fdca196a8c91485bb49be6dd7b72246db7389414fc18880a0c9d5098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350908175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c365d3e99163fef501f2f274a83f5b5773202d571ce8575b37dca66b5210104`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:12:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e592cd2ed9323d51731ff2e060da4790d904454d4dd8c0f58dc124b12854233`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 27.0 MB (27008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68baee722d285caf3b4327e15b2205e5b417d177e480c8c55a3ed01842c26381`  
		Last Modified: Wed, 22 Apr 2026 04:45:29 GMT  
		Size: 77.0 MB (76969954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4074c68b5df515ef5d60615498c46cb043cf2a5598f4bbe4bc6e038a6ff427`  
		Last Modified: Wed, 22 Apr 2026 05:13:17 GMT  
		Size: 198.2 MB (198232568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:473fffcb83101ba916a9eb56c76ec0f6cee1645f47ec2cf48c2acf0182ca6595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16885861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f33e60c5f1fd2b95979c3382c8fa7e7d995b7d1921b0daa0ca5cb0b78bf979`

```dockerfile
```

-	Layers:
	-	`sha256:17ffecf7a55f0603b7665b5cbf8d2c152cfd01aa7154a7c38803df1a9bd09099`  
		Last Modified: Wed, 22 Apr 2026 05:13:12 GMT  
		Size: 16.9 MB (16875716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723ccb0e04d2df5148ec963c40a5b171c64aee540e77b1afdf0509386c241846`  
		Last Modified: Wed, 22 Apr 2026 05:13:11 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8daf3b4d79d4ca3fed6e52c40590fe745dec5b8536e1d9fdaba8a24c3e531d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.1 MB (296057782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680a9ecba3729280267fa180289bf83a1c090e57b22d8a81a8dbc8c89087371d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 02:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:15:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:616f54f84dee8932180832c344695078e63789301eb12467ca880323e3400586`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 45.6 MB (45622135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970639d217085f63010f6da0cad6e9f8e048924120803b4eb157ac1c2f651a`  
		Last Modified: Wed, 22 Apr 2026 02:18:59 GMT  
		Size: 24.7 MB (24685888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2d4b24b5c349381f6b7163ca764f633bfc2f44c28abd2ae354570db164308`  
		Last Modified: Wed, 22 Apr 2026 03:52:38 GMT  
		Size: 71.5 MB (71474107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b4c4d0d3729ec107c4dd6fda65a1ab42cf6ecdc0c47e064d8a152f4cd1c358`  
		Last Modified: Wed, 22 Apr 2026 04:16:29 GMT  
		Size: 154.3 MB (154275652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9518e0b53e6ee0320c38a6df3d10cde82be30d6f990c2fbef48b06390e5ee8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16639600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93421a98fe0eeaff6cbbcd88348ac99889b22abbb4cb4c4e6c367604f81a777`

```dockerfile
```

-	Layers:
	-	`sha256:cad1e5beb9a6a5bc398b0e2b13f4c4251201cf0c5e12c49c74e2327a93def404`  
		Last Modified: Wed, 22 Apr 2026 04:16:24 GMT  
		Size: 16.6 MB (16629391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:759ead16d59a79c740f65bc748310de8236c5b4597d464e5485bedd975d5cc1b`  
		Last Modified: Wed, 22 Apr 2026 04:16:22 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cfcefe780f8f8e2fc8c548ba73b678c50aa70a7b19ca42b472935eef5a81099b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.1 MB (339075256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aedb9cfd6b81c184f80596271b535fbfeb66d29972261d506804b7d0222d07`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:17:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7406cf4524d3710a69a6e4bbba357df8393b55da990695b89997aa04b54031`  
		Last Modified: Wed, 22 Apr 2026 01:43:16 GMT  
		Size: 26.3 MB (26289212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943416c03b0fa211b9ad3c070b785a9f8b5fea034656c1157181cce52e7b2b98`  
		Last Modified: Wed, 22 Apr 2026 02:32:45 GMT  
		Size: 76.1 MB (76104831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064597ae651da46ed5165c71083726ad4f216943ba9d4ee8d2e6554550ebdba0`  
		Last Modified: Wed, 22 Apr 2026 03:18:00 GMT  
		Size: 188.0 MB (187955109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c55da1d648639c5709ede2765715e6b77599fc4a00c69ceb25454963094bfc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16968328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ec2fe728ac5180b588a8e6f37cd4b48750c3cd3f84cdf0dd06e165f90a5eb36`

```dockerfile
```

-	Layers:
	-	`sha256:678c1569df06023c2607d182bd264e416b928508768f76300f8c2c566e2c5e1d`  
		Last Modified: Wed, 22 Apr 2026 03:17:56 GMT  
		Size: 17.0 MB (16958103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f93aaa5cbcb688ee4427b3b3c760158caa38705d98de0b0ca3ce0b85cf74ae1`  
		Last Modified: Wed, 22 Apr 2026 03:17:55 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:45629870e0be13b15b5e2fe723e8ff520126b5dd5c3c04536450cc11ed06d44f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 MB (358491179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bd1346e88eb4447372a751bc46ba6bd3b71019b445280d0deff872baf5ca6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:42:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 08:19:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c764a369daed85f9b52e15146ccfcd0c76380aeab0914a25d45d32d7e95e4f6b`  
		Last Modified: Wed, 22 Apr 2026 01:42:57 GMT  
		Size: 28.3 MB (28284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7091ca31d67d63360b5bd63eedb35bca55f65b3881e95a9b699db1be7692a36f`  
		Last Modified: Wed, 22 Apr 2026 05:03:09 GMT  
		Size: 79.1 MB (79124028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6374f9717c7e64116279c1c65c129c06bb2b93e2fae6a78205ac879df6a4dc49`  
		Last Modified: Wed, 22 Apr 2026 08:20:29 GMT  
		Size: 201.1 MB (201099731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b3dd0b122d9e89c8b279fc48440877177a7bd90e8308d66cc711dc44eb80525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16853464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcbe68c4ca8317484716bb722926422bdef6628e4c9d9a5991a9dbced6a2adf`

```dockerfile
```

-	Layers:
	-	`sha256:eeb81ade24a69114f61583315bcfb5fc8b58d36d1576a7385574fded6d760563`  
		Last Modified: Wed, 22 Apr 2026 08:20:25 GMT  
		Size: 16.8 MB (16843341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b0c828c8a344174d817cd87eed54b680582866dced4640b9292c6e58b98c902`  
		Last Modified: Wed, 22 Apr 2026 08:20:24 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c7e4c0f8744f905d738eb3cdd7d29fd3a458915b2f0d3c46e1e1aa6bf541a423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.7 MB (358721242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1529f5f70a40d2b33ddf9d096712295526b21bba1446fbd0dfa538bf8e80c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 03:39:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 12:13:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acf335ca95a581f78a61de78111418bda596ddf71257299393203995ee7ea4f`  
		Last Modified: Wed, 22 Apr 2026 00:15:35 GMT  
		Size: 54.0 MB (53983935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d29dcef074d70bcd1e851f17e286abd94e829b11cf89631a079de7a5d724304`  
		Last Modified: Wed, 22 Apr 2026 03:39:43 GMT  
		Size: 29.4 MB (29406037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd57b32a5dc3e8581a7c19ba8dc6ae535a2865291f197fe5f63b9c08c56a590`  
		Last Modified: Wed, 22 Apr 2026 09:38:28 GMT  
		Size: 83.5 MB (83450223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb7b4d6eb6936014d95321bb4d4d17ce4d3d96685a198208daec0938daf7004`  
		Last Modified: Wed, 22 Apr 2026 12:14:42 GMT  
		Size: 191.9 MB (191881047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d8d3126009ed37eb8db9596af3980c42fc21b7c5669b20fc5c718bb113e059a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16836757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95df67720613607f875cdaa155960d24b1ecb03481ddd5a0a5eed9614116f422`

```dockerfile
```

-	Layers:
	-	`sha256:991dcd03267bb488c3bdb8188708a861db730e4a868fe3fd821de3cd35a2ae2b`  
		Last Modified: Wed, 22 Apr 2026 12:14:38 GMT  
		Size: 16.8 MB (16826580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e7192e85925f3e15bd71b7342bedfc18434291451d5762a12d448e7f4eedc6`  
		Last Modified: Wed, 22 Apr 2026 12:14:37 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:58978c1e0e395f32d4aa30503e50eeeee22bb58b450cf4b8750a419d4eb8cebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.5 MB (465537536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a94587204091118de12a06c3ea926154a0a099272036176430a6f1b201693a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1775433600'
# Thu, 09 Apr 2026 01:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:45:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 12 Apr 2026 08:20:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63b5561c308233dcf634aa914acd8af4b95568018df569d4d43c4791c98cc9ba`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 46.7 MB (46698175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d867396e8c8691cbd2e099e7a0d3c7c33eed2261193868cfa5cfdebbe037af`  
		Last Modified: Thu, 09 Apr 2026 01:48:33 GMT  
		Size: 26.6 MB (26580851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d7c78d4e0f683fb07cd5e1493fc6c006352c3197e1c49758dde411d0f9d76`  
		Last Modified: Sat, 11 Apr 2026 02:49:35 GMT  
		Size: 74.8 MB (74755929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32d88f1511eaaca7b7f47f40047169f69f4e64fada65fcfa543a682f3ee25d1`  
		Last Modified: Sun, 12 Apr 2026 08:35:59 GMT  
		Size: 317.5 MB (317502581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4ee4778b4a936c7398b86181dea33be3ddb6699455cd19147c4ed53182f64e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16871754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019e9c71bdc3fabb430f581a2d129fae254a724a8c24c290ac2acd1d3c9d0128`

```dockerfile
```

-	Layers:
	-	`sha256:b5f2c2b51705664af18e232aee9489dca52b42b79e59f21eb442ebd4d25e6a70`  
		Last Modified: Sun, 12 Apr 2026 08:35:10 GMT  
		Size: 16.9 MB (16861577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50b9fb3b4e08782e4266ad2af612bf0d9ba5cb206fab41abf58aba6f0752ebb`  
		Last Modified: Sun, 12 Apr 2026 08:35:05 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d158abe384082127d7debb95ed6184dfb421a9be5380155be414beefe2dffdd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323525945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:652cd9f81980875f00a737810bc6cae1ef810d02a1b18a693b8225687613afb5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:20:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:13:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a1060191b9434ca828b6395f3c2782a999320b4babb35dd20cb17592437fdf4a`  
		Last Modified: Wed, 22 Apr 2026 00:15:37 GMT  
		Size: 48.4 MB (48407607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca628a02ce8552e3ffa145824b47810287e1d695728e354379828ee1a246028c`  
		Last Modified: Wed, 22 Apr 2026 02:32:22 GMT  
		Size: 26.8 MB (26781237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4284620042de7e700765e6cf3d08ae5e2f2bfa319c3f4a48a20ef1a1a7fa7b15`  
		Last Modified: Wed, 22 Apr 2026 04:21:17 GMT  
		Size: 77.5 MB (77487748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ec35d7f52cdc224d8205bf3ea020409c177f179d218b3ff9a5391d71dbd84f`  
		Last Modified: Wed, 22 Apr 2026 05:14:46 GMT  
		Size: 170.8 MB (170849353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc92e3aec97bfac28a1f3715c066d7e95b2ec07278d271c64b76b93248858e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16637539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f7c17f32d377b1b6eec0638583b46d8d080cfb28923e7dea119217a508d7c2`

```dockerfile
```

-	Layers:
	-	`sha256:8a670490aa62f32cae3d4544c960a079f498512b238aa9afb3bc9d081e727b87`  
		Last Modified: Wed, 22 Apr 2026 05:14:42 GMT  
		Size: 16.6 MB (16627394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac5399a45ee65ee5e566f72a0574dddf32fd5c5e3414731c5bf68a0f8edfd20`  
		Last Modified: Wed, 22 Apr 2026 05:14:42 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
