## `pypy:latest`

```console
$ docker pull pypy@sha256:3bf59a6e7c8b790969e0925e6c055cd3eab5ed71f9c376c90b17ba23b3ea9d25
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `pypy:latest` - linux; amd64

```console
$ docker pull pypy@sha256:63d3a9cf8d17a6827852fd2abf8285c117664f2b2ff5a6c7f97f03972beb64da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.8 MB (415769759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b1429da9a3010a12f7ec0b8a9db563f78e288d678aeb063aef791290fd6721`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:50:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:50:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:50:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 05:50:55 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:50:55 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 05:50:55 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 13 Jan 2026 05:50:55 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:21 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d823e3848f3d74363d9b5b44f39f2d2f81a99a37d8c7fb54831a489a32e999`  
		Last Modified: Tue, 13 Jan 2026 05:12:51 GMT  
		Size: 236.0 MB (236001828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27dfc56fe6e11a7c0f2244e27358f51abf7ee319af0320d4b12df73d940312a`  
		Last Modified: Tue, 13 Jan 2026 05:51:21 GMT  
		Size: 3.0 MB (2976575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba919d63ec9b8e58592828327dfc72585add39c9c3b1cff1a7e2741403aecde`  
		Last Modified: Tue, 13 Jan 2026 05:51:25 GMT  
		Size: 34.1 MB (34105549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:latest` - unknown; unknown

```console
$ docker pull pypy@sha256:9e7bc2649c9a794a48147e3ab4e964b208bf13136124a07a433f61288b7d4e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3ee4ebdc0cfab58260d1685335a8da9e893d6c6bd8f88c45fff1965e67c2bc`

```dockerfile
```

-	Layers:
	-	`sha256:31dda0a9d6bea6f5ce6e5c5a3fe846b17f794716487b87cda3c6fb96f85b21c7`  
		Last Modified: Tue, 13 Jan 2026 07:40:49 GMT  
		Size: 17.5 MB (17532987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b89fbd718e72ac32e160b3d88feaf356242aa190929637dbc6076438a3823311`  
		Last Modified: Tue, 13 Jan 2026 07:40:50 GMT  
		Size: 24.9 KB (24921 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:latest` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:6a4610acffef34b140bc8249df9b910e79720fca2522308623ccb9805d3cb135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.8 MB (403801584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a684d8a043002385efbffd97a79eb894c93081465b70f9ca676fcb14ffb34914`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:52:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:49:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:49:56 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 05:49:56 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:49:56 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 05:49:56 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 13 Jan 2026 05:49:56 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fffeb567ed4215b503f814aeaab9fa5a2e701d3efa35d4c285b3cf111e9cb4a`  
		Last Modified: Tue, 13 Jan 2026 05:16:01 GMT  
		Size: 226.1 MB (226143857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25a6a26a04b02c15a3633fe5ae4e1a550e02ff0f6e9037d2a5fc3a32e0298d2`  
		Last Modified: Tue, 13 Jan 2026 05:50:25 GMT  
		Size: 3.0 MB (2975987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2680d98922249b82553d8c1146caecea5e467572c778ba970f5ec5084b6c42`  
		Last Modified: Tue, 13 Jan 2026 05:50:27 GMT  
		Size: 32.4 MB (32419508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:latest` - unknown; unknown

```console
$ docker pull pypy@sha256:0c61bc41abee96f4847e4b75e42ac9da7bc5f9f9bb41422ca135e51b09c26d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17642673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218fee3408a790140ee11e3cb425ac34b12a2a461eb5278cd604348a6d549a8c`

```dockerfile
```

-	Layers:
	-	`sha256:1eef7d7f15c41a8d2e3ba0dc317d23a6830566240a5afb5bc1c8b4716d5f5f9e`  
		Last Modified: Tue, 13 Jan 2026 07:41:08 GMT  
		Size: 17.6 MB (17617465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34950d2cbb6b86f530cf7dd2acedc24de85caaba3f06b2e89f27793846807333`  
		Last Modified: Tue, 13 Jan 2026 07:41:09 GMT  
		Size: 25.2 KB (25208 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:latest` - linux; 386

```console
$ docker pull pypy@sha256:4137f9ca7810ac0c5cabf2871a8d5365721eca84ca8250b1783402473d4893a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.1 MB (421051616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b73a4cb54f5be3b7744bff84d921fd268b3a68b9389dbf69188e335c1325bf4`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:56:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:35:16 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:35:16 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:35:16 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 13 Jan 2026 04:35:16 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 13 Jan 2026 04:35:16 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:47 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:58 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c438693622c619054710e61f4e49c9f44709996e7ac1c8577527c38f87d008f`  
		Last Modified: Tue, 13 Jan 2026 04:02:03 GMT  
		Size: 240.1 MB (240108789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77290150ea126caf219959d7266e62169de25ccef9f833290520a19a4478c7b`  
		Last Modified: Tue, 13 Jan 2026 04:35:42 GMT  
		Size: 3.1 MB (3113541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21fd219324857121c5b59a47b4f0f46144f25f092a25ec10f2077609d530388`  
		Last Modified: Tue, 13 Jan 2026 04:35:43 GMT  
		Size: 30.4 MB (30448928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:latest` - unknown; unknown

```console
$ docker pull pypy@sha256:3c649b9c1a63824848ff6acd8043ce9b19fc2e2dea0dcb6f354844f4e7a5b592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17527312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d419daa6e7c1f0b1de7260500434e84d55d859fc92d120a5cde157f62aef5e75`

```dockerfile
```

-	Layers:
	-	`sha256:fbdc53de2dffb39305be1a3f8f7a238848c9edfa94887b072b08306b4717550f`  
		Last Modified: Tue, 13 Jan 2026 07:41:27 GMT  
		Size: 17.5 MB (17502495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f2664032e2c7e5e9ac2f95129bda6d480e1cbb90cb841155213976981f257e4`  
		Last Modified: Tue, 13 Jan 2026 07:41:28 GMT  
		Size: 24.8 KB (24817 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:latest` - windows version 10.0.26100.7462; amd64

```console
$ docker pull pypy@sha256:d78d1c70147b62fac499ebbe520f4d78fed5cb16f0e38e7e053ee45929760e78
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3299665001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05264528f71ac02ede073d26428336c31a98b85ba3ce6de90c618abcf3fafcf8`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:35:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:48:31 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:40 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:40 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 09 Dec 2025 20:49:16 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:49:17 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f987c501e4c8afb4e2888125887f3223de31afb60e4470196dd3ee0c043dc67`  
		Last Modified: Tue, 09 Dec 2025 20:44:28 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66c9dabbb84f1d63c86643f1762692500b8bfaf4ad924f7f76041929966c240`  
		Last Modified: Tue, 09 Dec 2025 20:49:34 GMT  
		Size: 359.1 KB (359117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87eebde2aed919da13827b407a0aa2941128169fa9168a781ec9be16e9c5640`  
		Last Modified: Tue, 09 Dec 2025 20:49:35 GMT  
		Size: 15.5 MB (15525127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ec101dd10c7b6a4824abece4584b7b5cdf430ef8f0b6a4d22dcc44c57c2f9f`  
		Last Modified: Tue, 09 Dec 2025 20:49:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda1887a2a6402ac7f36423d88dff0d9d0fec3ca35930b2a989856673cd3d413`  
		Last Modified: Tue, 09 Dec 2025 20:49:38 GMT  
		Size: 30.7 MB (30656424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd6be9226bbdcfa8815695c7212348a0ef06c26c5e924f556160c4875046841`  
		Last Modified: Tue, 09 Dec 2025 20:49:34 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:latest` - windows version 10.0.20348.4529; amd64

```console
$ docker pull pypy@sha256:01486489230197921430c448b0174dd8d1affb66605cc416d7f71ab64b026475
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1826569978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65388beaa660a7b54ef3216398782f7941bd537f9c0da7b3f82bf132aedc7fd0`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:45:36 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:45 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:45:46 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 09 Dec 2025 20:46:24 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:46:25 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768ea431b13531bd18fa519503dcde235d1371c06640fff6c434a8dc2f78f370`  
		Last Modified: Tue, 09 Dec 2025 20:40:48 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec050c56559e408db965fe2de7696d5bc66616743cc4cec14444cc5bf332b281`  
		Last Modified: Tue, 09 Dec 2025 20:46:42 GMT  
		Size: 487.3 KB (487263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5f0940222982a508cabd6d6820d8ee2293b5da2636346849dbc3a14eced2d1`  
		Last Modified: Tue, 09 Dec 2025 20:46:43 GMT  
		Size: 15.5 MB (15529718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789dc98a0cf13a91045eefe8f95c211fabceae83c0c66a4e2e4a2bd0c2ac7558`  
		Last Modified: Tue, 09 Dec 2025 20:46:41 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e901f0a820c780add1e883808971df167f558e932b21c6e37079232831df700f`  
		Last Modified: Tue, 09 Dec 2025 20:46:45 GMT  
		Size: 30.7 MB (30669781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449f4f44c0a177bd9ff16414ce04b5d72898fa021782fee433376e188e4ec784`  
		Last Modified: Tue, 09 Dec 2025 20:46:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
