## `buildpack-deps:forky`

```console
$ docker pull buildpack-deps@sha256:f789ace602e85bd7c4126e07fed4c7081bf46629b940f2950b89a54813db79df
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

### `buildpack-deps:forky` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:bb51e0333b4881f6dc46023cdb49294c0d25157e2520d25917db2febb0c55c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.8 MB (349790543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d8f210977bdac2275f1fd2079d9e193c049310e4f7626d0ebd3e0ffb153025`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2544a38ddd1390105762bdf349d1e32b7cf1a9f82dddf930c31b8042b03c6965`  
		Last Modified: Mon, 16 Mar 2026 22:37:58 GMT  
		Size: 27.0 MB (27048499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60232b2b35a4cd7a3c869ce028715219f655956cb40f5462e6fb4439cc2e05f3`  
		Last Modified: Mon, 16 Mar 2026 23:25:44 GMT  
		Size: 75.9 MB (75947432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ecf9ee25a68bf8b76aee8bc662aa505146e114f6e617213bdad99978d47f2c`  
		Last Modified: Tue, 17 Mar 2026 00:20:49 GMT  
		Size: 198.2 MB (198169521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88bfaeff4de17eeffa6d08acf0bb95273c1be80337f9e99de986f8414e4c6828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16802702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74299d89a21acc3f7c951e7af0d5807ca675163456490c556bf860052d6f4eae`

```dockerfile
```

-	Layers:
	-	`sha256:c20a6957753a9cbd0e0dec07f9743ccff13fc07c568e69c73b234e2973aa9835`  
		Last Modified: Tue, 17 Mar 2026 00:20:45 GMT  
		Size: 16.8 MB (16792557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c6a69073fddb90e06d62b2ffd92c49b2fb5ed04b882259b6a0f555f4749eb40`  
		Last Modified: Tue, 17 Mar 2026 00:20:45 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7382c484d0934679d3ba6d226e6d735c81642dae6b3a6a3dc90e93c4272255e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.3 MB (295280485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c84411ec05687b5d2b696700f0345fbb383553750f94d828fd96b03440f3dcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 23:20:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:51:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:16:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e808829cfe5315cd67981f1a90877f9ceed482400b0f64a9a61a5068bf2e2381`  
		Last Modified: Mon, 16 Mar 2026 21:53:22 GMT  
		Size: 45.6 MB (45555225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3a3183174d50dae2f383480aa0bee03715dc30a220abfb476587db07c5672`  
		Last Modified: Mon, 16 Mar 2026 23:20:29 GMT  
		Size: 24.7 MB (24735775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8188e372c017c494407b24b2b30e203daa280d4883793d18b074e8e8f15361b`  
		Last Modified: Tue, 17 Mar 2026 00:51:48 GMT  
		Size: 70.5 MB (70514894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28851adaa73f50eee9bc8100aca7536523aaca0c67dd896db114fbdc19774408`  
		Last Modified: Tue, 17 Mar 2026 01:16:36 GMT  
		Size: 154.5 MB (154474591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d46a6122a4806714127235ea8da3734c3a3297f804cd38bbbfaf23596e3432f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16557807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375eba9731e121d7a2bc9a84dc8adfc0082426cc668a023bd019e209815843ee`

```dockerfile
```

-	Layers:
	-	`sha256:047107169648f6af575d3cd41eb1ebfbeba0c75c4db4c51428d63bd546f2ac60`  
		Last Modified: Tue, 17 Mar 2026 01:16:32 GMT  
		Size: 16.5 MB (16547598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b17fa0ed476acafad6f00c01e0a01447f8549bf231072774014edb0d494901d`  
		Last Modified: Tue, 17 Mar 2026 01:16:31 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:811dc8e8d9aaa58446119d0a6b45366caff1cd4ad796565a8b05a82e14090be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.0 MB (338020783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891c237582fb4c9051be3eca7743624b8feb09791781a83584102123cf3a89cb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:40:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:19:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873916964a227a18ebb04ec1f407f168a33886e300682cbd4848c61bc623f448`  
		Last Modified: Mon, 16 Mar 2026 22:40:19 GMT  
		Size: 26.3 MB (26344588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4fb7d902f3cb9bf3e0daa77ba127ee8230f61ba12bbb5d9f7dcefc084f7373`  
		Last Modified: Mon, 16 Mar 2026 23:31:17 GMT  
		Size: 75.2 MB (75222389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6719eb5de4a05a7626a3b66f236c500c85db4d56169bd8486988d9eb1b4c289`  
		Last Modified: Tue, 17 Mar 2026 00:20:34 GMT  
		Size: 187.8 MB (187794745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b3866399cec38aa5f1d5e69404273d8cf5488a394e8278c09cda1a02bab24182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16888337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda236def5714df193be53360a84c8f8a18fe9bbf12457a2e3da282f2a919803`

```dockerfile
```

-	Layers:
	-	`sha256:4cfa768cb5d711b96b2e39b5c31f6c21b0da048a43ff1cdb1b90dca962d5c06d`  
		Last Modified: Tue, 17 Mar 2026 00:20:30 GMT  
		Size: 16.9 MB (16878112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0634033859063264c581959d881d1855a0de90fc6247b6e3af17c0fe135f06b`  
		Last Modified: Tue, 17 Mar 2026 00:20:30 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cd7409d7abf16f56af908fafddf55934fdc507c14d4256b34f3fb681840bee6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.2 MB (357226204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36ad77696485d1b2f977f4ee67f683387d90c8ea16d3e7ce55018d173602859`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:44:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:41:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 00:20:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63597877e9ce45a8d644c87f2edaa1b6f60b392c0f8a5049196e27710801057`  
		Last Modified: Mon, 16 Mar 2026 22:44:13 GMT  
		Size: 28.3 MB (28310412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b32036cc7858dc14c7d8b709498aa52c52147bbd4f9cd24a39c522f264cf55`  
		Last Modified: Mon, 16 Mar 2026 23:42:04 GMT  
		Size: 78.0 MB (77964507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6614020f7ad970a65a6139fcb8b9913066a1c5f4945ad804e2c0c2271693d3`  
		Last Modified: Tue, 17 Mar 2026 00:20:44 GMT  
		Size: 201.0 MB (201031414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6523270cae55b10f237ecbecaf56491648d9581be8eea24ec942a396977703f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16771749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1346df970287a83a9ddc7d0bd89b952fc96465101bf77d399a78851138f2b09`

```dockerfile
```

-	Layers:
	-	`sha256:3b690647eccb3ded83f61f9ba7e63c5f83158bb53bcdf19d2850e32350bdc561`  
		Last Modified: Tue, 17 Mar 2026 00:20:40 GMT  
		Size: 16.8 MB (16761626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b3291abcf222678cf875ee14f784288200fb3e5b132ab21d5fbccc7a842ce8c`  
		Last Modified: Tue, 17 Mar 2026 00:20:40 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bb1d87111f2bd88d096d27a77279b8b5a95adb50edc21b2cd9c37691cb973a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.8 MB (356839033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b8e575940d6b72da96ba93f2587b24ce98740afc0b4896e8e6fa48c921b46e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1773619200'
# Tue, 17 Mar 2026 01:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 08:20:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:75936ac254db13d0215c75f5fabecfedea28136e3ee0cacb89bd8884668a56af`  
		Last Modified: Mon, 16 Mar 2026 21:51:49 GMT  
		Size: 53.9 MB (53863314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e0924d7ad541b2109556dcbe1d5d7994260b154430061685df2536f4aafd6`  
		Last Modified: Tue, 17 Mar 2026 01:50:07 GMT  
		Size: 29.3 MB (29334407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9adfa45e921c3124cd11880041b79cbc945f57ca5ff667ef09fa57d6468ae2`  
		Last Modified: Tue, 17 Mar 2026 06:04:44 GMT  
		Size: 82.1 MB (82088651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aabf1673a6b603b7d1c93584062c5ca37959e57baf0818eda272903a290e186`  
		Last Modified: Tue, 17 Mar 2026 08:21:33 GMT  
		Size: 191.6 MB (191552661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:54cb92ef585b9d6c263657ed0e6b0ed4c09382af253eedc80cae411c06e7aff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16753514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4477dc70db1ea413944ec5187fdf4d212bb1c016a87b6c72622a39d8fd18f70`

```dockerfile
```

-	Layers:
	-	`sha256:0f740aaae7dbf8dbb0ae942e474e2473b604791bd2d0b5b56a4a8a337364b20f`  
		Last Modified: Tue, 17 Mar 2026 08:21:30 GMT  
		Size: 16.7 MB (16743337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95de70e68ce189a199350c70fda205809b57bd46ccbd9664dfc0a57f8b5c9459`  
		Last Modified: Tue, 17 Mar 2026 08:21:28 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4a07117c40a71eeafa1f067471830ee9ccb74bbfb1ecbdfe13343c477789d153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **468.6 MB (468648172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5eb31e6cb42fe103ddad7a3bfee8af7c4702874d08084e10bf4d7c95a1bd75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 26 Feb 2026 21:34:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:33:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:db31b4401b1ad39bc8394e302320dc063e12e2c0464e6a8103701611daac2f3e`  
		Last Modified: Tue, 24 Feb 2026 18:43:31 GMT  
		Size: 46.9 MB (46914404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ea7a6a4533bb42137b98ae7cf7eb86a1fd6eefe9d713522264d613c05e62`  
		Last Modified: Tue, 24 Feb 2026 19:09:30 GMT  
		Size: 26.8 MB (26774378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ebef486f83ee0c702c262a6d5550673a0f1b78368f99bd1ce71d5e966d05ab`  
		Last Modified: Thu, 26 Feb 2026 21:38:15 GMT  
		Size: 74.4 MB (74379205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b16e39d37471c692ac6df897b04bb474eee60d703290f4752935fdc10a24d`  
		Last Modified: Sat, 28 Feb 2026 19:49:17 GMT  
		Size: 320.6 MB (320580185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f9c0e5337687790a07200eaa00aabb33cf8944c46444832b572dd6b2d85efb5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6b0f3fdfb70563f37211e755d59a2be7a26138c5c9864d87d89778a2e301a`

```dockerfile
```

-	Layers:
	-	`sha256:92c278ac18d4279c06690a127db5174d7096668ba4c3c52040137a99c5a1957b`  
		Last Modified: Sat, 28 Feb 2026 19:48:33 GMT  
		Size: 16.9 MB (16885046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:173fb54d825398d0145365446ef33f196c28634bbdfc9c52cd0bc87d9443c491`  
		Last Modified: Sat, 28 Feb 2026 19:48:28 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:60847b6c7e35fed98d6d69287badb4874056e5d6aca9e8edcacbe82e97348829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322368930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702968fc82c180b104b1f7104c371bdcf5fba737f4a375dbed0040f131c04b88`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 23:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:33:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:17:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f87b2d0069bddaedc5a87fced2f3e4651a654b1dbe947403a098a2d5a2045522`  
		Last Modified: Mon, 16 Mar 2026 21:51:42 GMT  
		Size: 48.3 MB (48334622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892b950bdf154265cdadd06df13c221ac2b053459e6309c7b38bd12f5bf75dd0`  
		Last Modified: Mon, 16 Mar 2026 23:45:01 GMT  
		Size: 26.8 MB (26831261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa57a5767314df691e90122f9d22adfdd6c410cf68498773d14f127f4b4336a0`  
		Last Modified: Tue, 17 Mar 2026 01:34:03 GMT  
		Size: 76.5 MB (76522597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf18c3e8bd615b71717530945de442b531f91c0329af12d68e580d367bd75be`  
		Last Modified: Tue, 17 Mar 2026 02:18:59 GMT  
		Size: 170.7 MB (170680450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:982525048d91b738037211b8c3698b1c3dea4840c115f62c48ec723bc8816f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16556016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8273e2bb664c14b9deaa7c45d7200a23ba91e4adf2493221afff28609d83a5c2`

```dockerfile
```

-	Layers:
	-	`sha256:3f75262eba826d2274aca0c1d5ea4602de4233cb796067d25b4a5b255275f2d1`  
		Last Modified: Tue, 17 Mar 2026 02:18:55 GMT  
		Size: 16.5 MB (16545872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f8b1bfe0cdeba5cd148bdd6e0bf20f6720ba2e85b736d0921bd753b475dcf3a`  
		Last Modified: Tue, 17 Mar 2026 02:18:55 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json
