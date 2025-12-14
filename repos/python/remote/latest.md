## `python:latest`

```console
$ docker pull python@sha256:2febcd1e225a79391d5c9a7b416125af542ffd2f686201a58ea1d5595e110c4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `python:latest` - linux; amd64

```console
$ docker pull python@sha256:f59048c479e585a6ef4aef2c25883eb40556073eccb38db574d65de27b657439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.1 MB (414139639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b058ae471b66b4c7d19426be87e375d9f091f03e5ea08684dd808966c9ae97`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:46:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:54:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:54:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:54:05 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 01:54:05 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 01:58:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libzstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 01:58:51 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 01:58:51 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd420cee8193b72cf70974a80e88896c8e58d925edd1cdc515b203ff7aa65550`  
		Last Modified: Tue, 09 Dec 2025 00:47:38 GMT  
		Size: 236.0 MB (235974801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388c30f2dc569df381ac55ed9c7bf0a3494a7383ed09b64f8c2c4ff9439b29a1`  
		Last Modified: Tue, 09 Dec 2025 01:59:18 GMT  
		Size: 6.1 MB (6084833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f8a41ae1eca164f1c6ac9c8b0f444f478e31ceece03a5283b4e9eaec9513e`  
		Last Modified: Tue, 09 Dec 2025 01:59:19 GMT  
		Size: 29.4 MB (29397726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d5b01339430c5cd5004ca11b1673730eaf84ff0d2aedf058500d76ae7a1c03`  
		Last Modified: Tue, 09 Dec 2025 01:59:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:eb2ba7f900193360bcb0c2c457e709995f2023963d9569fbc8d7db08f7b135de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17775416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0ce049534d94d88ba1f3f6a774c0f4f57581968537ce43a617cba2e800208d`

```dockerfile
```

-	Layers:
	-	`sha256:65675e4eae1b11f11363ac3fa94258251c8d67dfb2a04a5cb6e7fdbd6bc09b04`  
		Last Modified: Tue, 09 Dec 2025 04:06:44 GMT  
		Size: 17.8 MB (17750498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2773ed9691054bca3db0f3e629b60bad29e3e734bfccaebbe8548f9c70162061`  
		Last Modified: Tue, 09 Dec 2025 04:06:45 GMT  
		Size: 24.9 KB (24918 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; arm variant v5

```console
$ docker pull python@sha256:a87ec6ff1e2fff0d38c1ef55aee2c70764abec0306e7bdd86e96cbdd1cba18d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.7 MB (376731331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdef48eb78242f29ee12c897b4083a293ed4f83aad12a2dd889e35df44e23b12`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:55:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:18:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:15:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:08:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 04:08:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:08:08 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 04:08:08 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 04:18:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libzstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 04:18:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 04:18:05 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:123c232a33b986aeccb984e885244b48200c4eb4f9a811e3df109a416dc71f80`  
		Last Modified: Mon, 08 Dec 2025 22:16:56 GMT  
		Size: 47.4 MB (47448721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbaeb213e9fa41da55c6b895ce8273281464b3351c9fcf26aed8d0fc7484a18`  
		Last Modified: Mon, 08 Dec 2025 23:55:26 GMT  
		Size: 24.3 MB (24345927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4936999457f9b45cd7af5bc334afc3525d9cd25bc796f9420e78292f7e4e6d8`  
		Last Modified: Tue, 09 Dec 2025 01:18:47 GMT  
		Size: 65.3 MB (65318096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbe24d4bd7124e2e25624c6cb817a4ea96874b5b05fa82ee85e637d69cc11d3`  
		Last Modified: Tue, 09 Dec 2025 02:16:29 GMT  
		Size: 205.7 MB (205708128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd631e379b84f368fdffc97224324698d8abdc68b427537e386544c3de36cfe3`  
		Last Modified: Tue, 09 Dec 2025 04:18:37 GMT  
		Size: 5.8 MB (5805821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30053d18fc1f7539490a7ab084782c53cfd396ff43151865a372eb0ee97abb3`  
		Last Modified: Tue, 09 Dec 2025 04:18:38 GMT  
		Size: 28.1 MB (28104388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3955f1b9489986747817a912e225110bae786d024de2c74d48f5c58022463c0b`  
		Last Modified: Tue, 09 Dec 2025 04:18:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:6b1ab5e477776500d393531ba6a8bb5cbdef0c77807857072217c9c4b3fd5449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17537809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddbe36949984e0f5ea11415e34421693f9098d9d1d906ec4645b7c9659627af`

```dockerfile
```

-	Layers:
	-	`sha256:69226a861a5befda21019b0b72a4af52f64498d59ea93eab3a45497b861e99ed`  
		Last Modified: Tue, 09 Dec 2025 07:06:46 GMT  
		Size: 17.5 MB (17512754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ab3cc1f52d426e549dec9b7c4f1567385c38c40db7bc17c4b098410ad9f8400`  
		Last Modified: Tue, 09 Dec 2025 07:06:47 GMT  
		Size: 25.1 KB (25055 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; arm variant v7

```console
$ docker pull python@sha256:9fefb466ee4e68e3853cecbcfd9e889107dc2050e51e50b471fad97b8203a636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358793088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510eac0820083c3032473cdf70f9084cd256d7170b2369aed13b77576b5e4d15`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:19:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:42:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 04:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:42:33 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 04:42:33 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 04:50:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libzstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 04:50:51 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 04:50:51 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:c4eba7a08ba9825cabd599d8641314a004d500b627e05a38640b9d3c0bf389ef`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 45.7 MB (45718282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6ad1d8bb6e8d2c91990f13409d4d822c19a3b9fb5463aa9033cd860aaa4822`  
		Last Modified: Tue, 09 Dec 2025 00:07:27 GMT  
		Size: 23.6 MB (23620171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067e549495a4594bb4406cebf8990f1500f9fbae204461f2b793444540c774bf`  
		Last Modified: Tue, 09 Dec 2025 01:33:43 GMT  
		Size: 62.7 MB (62713415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f0a24772dec0e72cc1a314a0c6613a5577b09b7b6c8368604b9a163a31aa5`  
		Last Modified: Tue, 09 Dec 2025 02:20:05 GMT  
		Size: 193.3 MB (193258585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e378172273637ea16fc4eb42853db1a5a0bd8fd40c558abdcac18ef0914fc535`  
		Last Modified: Tue, 09 Dec 2025 04:51:18 GMT  
		Size: 5.5 MB (5493668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14cafff0dc93d046500df06a1cb07953a26995cb9d2f7b25c3bc79e7b0cb14e`  
		Last Modified: Tue, 09 Dec 2025 04:51:21 GMT  
		Size: 28.0 MB (27988718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f032bca042ef47c3e048b8ff3aaf22e0a2bfcaf336401961786444791c696d1e`  
		Last Modified: Tue, 09 Dec 2025 04:51:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:15124788c91db5ef9509d3ea99cda8afd87c22fc971b30f82ea4b993459d4bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17543636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2653e6a5227b872dd24154b1bf0516b30ec8326b926e28239e4434a8783c8150`

```dockerfile
```

-	Layers:
	-	`sha256:f890c2939c4054e828d254b78540b9e3ff3b9aeca26ecfdf9b1dee578f48f821`  
		Last Modified: Tue, 09 Dec 2025 07:07:01 GMT  
		Size: 17.5 MB (17518580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6051775eb8196ecda5f413c90a1046dc7f8a384452e8fb8e3be9bef6e1a1d568`  
		Last Modified: Tue, 09 Dec 2025 07:07:02 GMT  
		Size: 25.1 KB (25056 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; arm64 variant v8

```console
$ docker pull python@sha256:361d44b305c5933e1bfa0fdd4073c3047af9acdc18809f8e9cad3266ffbd5370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 MB (403009767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b9072063ed8ca0e7e34e19ee44988947a265bb16c99b7946333a57a9765e96`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:16:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:43:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:43:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:43:40 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 02:43:40 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 02:49:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libzstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 02:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 02:49:13 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2b4af09d0743acafc293109ad1b191f5a03a36cd1dddf8454458ced3631f5d`  
		Last Modified: Tue, 09 Dec 2025 01:17:36 GMT  
		Size: 226.1 MB (226108094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261701ec7f37177f36e71754e9af1a85f0573259824ed2c0f92e6f4cac837334`  
		Last Modified: Tue, 09 Dec 2025 02:49:43 GMT  
		Size: 6.2 MB (6199249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f3c990e70d17694532d119b58478ad9b85de64b31c36a1116d5a5d7a60b5`  
		Last Modified: Tue, 09 Dec 2025 02:49:46 GMT  
		Size: 28.4 MB (28445994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a68c1cd21d099117fb9ff14c32b523696032fd3ee10184955f311246451ee35`  
		Last Modified: Tue, 09 Dec 2025 02:49:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:f11b396299b399da04c5469bf9834f5fb0531cfaf950af58d966003a1570ccb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17859970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee39ea1840209ba3f735b2a978a24deaa66a2192f302dffda329ba4d1c1a41ba`

```dockerfile
```

-	Layers:
	-	`sha256:19d27243b1ff5a8c4971df5417f016edaed2631ad07723e4359634ac61d84a45`  
		Last Modified: Tue, 09 Dec 2025 04:07:23 GMT  
		Size: 17.8 MB (17834870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:392cd64f57d4c7528549f0dc4045695ab98438b9db58a82dfca389899200dee1`  
		Last Modified: Tue, 09 Dec 2025 04:07:24 GMT  
		Size: 25.1 KB (25100 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; 386

```console
$ docker pull python@sha256:58d03bfdd0cee434adbc62f8d70889fe9d0188f3b96e4bdbdbf9f48fd721f0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422346998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9edb688cc88b4bbe0002732b670cb548f1d2e2c0102b153fd08bf31e3af83e9`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:17:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:28:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:28:08 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 02:28:08 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 02:34:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libzstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 02:34:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 02:34:01 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798fea9bbf98ef639c9ca23d745bec44c0d7b28fbd93792d4578fc5b43e7569`  
		Last Modified: Mon, 08 Dec 2025 23:14:38 GMT  
		Size: 26.8 MB (26776300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d1731e98c6e5aff4c28a002263af9a4fc5c06d23cbc860d258dafbd603ef2`  
		Last Modified: Tue, 09 Dec 2025 00:24:53 GMT  
		Size: 69.8 MB (69794656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9ce1752769ca8894b138e7f67dcb0e328629def6e6854ee6c1fc3ea4e6dac`  
		Last Modified: Tue, 09 Dec 2025 01:19:01 GMT  
		Size: 240.1 MB (240068858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873b054d097554829e17903eeabcec486d977908dfa98aa884807664765e9d9`  
		Last Modified: Tue, 09 Dec 2025 02:34:30 GMT  
		Size: 6.4 MB (6446169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c225357839bb0afc99434855a448354223b2325d35cc6198eadc75edf5ce8b`  
		Last Modified: Tue, 09 Dec 2025 02:34:31 GMT  
		Size: 28.5 MB (28459118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cba0b0629bf59211334219bb7c32501ef5042716547247494518cf6b345bf1`  
		Last Modified: Tue, 09 Dec 2025 02:34:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:47ff2100e64f88f2dd2952efc3a3653479a1775d7bd092235743100c98907c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17744890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3fc6fcd5b3e1d2afb48788e5f663c968172ac60743f4ac124ae458cac0d830`

```dockerfile
```

-	Layers:
	-	`sha256:3136ca23f66127fead3ea68c5af75427347c021d57a58ea02f7887015246d078`  
		Last Modified: Tue, 09 Dec 2025 04:07:39 GMT  
		Size: 17.7 MB (17720028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b8fc0f415d2ff6fcf5c9ce216ec4de332ee7fda029da7db860ed229297b5f5f`  
		Last Modified: Tue, 09 Dec 2025 04:07:40 GMT  
		Size: 24.9 KB (24862 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; ppc64le

```console
$ docker pull python@sha256:7ef3dd485f0309159b25a08027127a55f73331c82365975be964ed1290a9b27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.3 MB (420315137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c9fb07cd8c18cbda0b44178662cb50b9ea552a12fb805a4d3266fed39dddaa`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 04:34:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 11:16:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 11:16:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 11:16:18 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 11:16:18 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 11:25:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libzstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 11:25:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 11:25:01 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc59b593a33ee8746f94dd61c3d4d2abec3c25d3c7e93e36a9043ee716aacde`  
		Last Modified: Tue, 09 Dec 2025 04:45:03 GMT  
		Size: 231.1 MB (231106988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab19f0d68330a51adb2637a7f80b07d3f145a45744f0c91fdf7b2077970e605a`  
		Last Modified: Tue, 09 Dec 2025 11:23:46 GMT  
		Size: 6.8 MB (6821385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede7766ca179f00a1f7c1bff5a71eb28ae0d45bc6830f29dd72ef97985e96ffa`  
		Last Modified: Tue, 09 Dec 2025 11:26:11 GMT  
		Size: 29.3 MB (29259176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6409f258cd0fe6af5ac3beae29ccdf8e5de0f9c50b2826c0985088165d8d46c1`  
		Last Modified: Tue, 09 Dec 2025 11:26:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:3378f2ce84f71233e845d30f059679f1e52d9654c6bf51fef332b98709689a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17761201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2657c4122a520d9c821d4134bf4e82537d82979480aead3dbadce76e7f5a2fbf`

```dockerfile
```

-	Layers:
	-	`sha256:9a5103afc39a859cda9d2c73f6b3110ebfddfa65487a8fb1ed30b6869997924d`  
		Last Modified: Tue, 09 Dec 2025 13:09:56 GMT  
		Size: 17.7 MB (17736211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1374360f786e7ed13fcd2b33c624a37e1dfb8fc98c0a90df4980c600cb3b5aa`  
		Last Modified: Tue, 09 Dec 2025 13:09:57 GMT  
		Size: 25.0 KB (24990 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; riscv64

```console
$ docker pull python@sha256:accbd26d2b03cbe94e690770755cccb2e5edcdd282bbaec7c12226f9c5686af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.1 MB (500089377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3133cbca491ec271dc00ad2d5bd38c87a85556872329042556a17da89ce0b260`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 21:51:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Sun, 23 Nov 2025 22:35:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 23 Nov 2025 22:35:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Sun, 23 Nov 2025 22:35:41 GMT
ENV PYTHON_VERSION=3.14.1
# Sun, 23 Nov 2025 22:35:41 GMT
ENV PYTHON_SHA256=8dfa08b1959d9d15838a1c2dab77dc8d8ff4a553a1ed046dfacbc8095c6d42fc
# Wed, 03 Dec 2025 02:51:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libzstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 02:51:04 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 02:51:04 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0946283142630ddc0be55b717109fdc10f4f3806b47ec32301b162ca5d92b2`  
		Last Modified: Sat, 22 Nov 2025 22:12:30 GMT  
		Size: 322.9 MB (322888286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6821013f8a831aa52f2eb6b549214fa0dbe882726ad6d6a5e3589c62b5d03f4`  
		Last Modified: Mon, 24 Nov 2025 00:28:49 GMT  
		Size: 10.4 MB (10380091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221e0e3519f833610123976b0735277999736c8eefcc61505d2688e9a44d00cc`  
		Last Modified: Wed, 03 Dec 2025 02:59:55 GMT  
		Size: 27.4 MB (27434858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81974c354a6ea0976496217b91d80711a50273f202c4fb1aaee74949ee63df78`  
		Last Modified: Wed, 03 Dec 2025 02:59:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:d6c5f0173c64a66ddc7e940e3caf4e5bad76fec661ea927b2f4f333bb1e54bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17831683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ca0659c2a4df77d4de443c53e6fd7c9a7330d134a8d3207942cc45f4de7601`

```dockerfile
```

-	Layers:
	-	`sha256:9bcc372b6e5cf06879d8020d4d7c62963283ee166a89baea6f49ff0bf60dc1bd`  
		Last Modified: Wed, 03 Dec 2025 04:08:23 GMT  
		Size: 17.8 MB (17806692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0984c573f8e688ca25d062aea107708ccda5d5360f7a2091ee8dfa9cb02a410`  
		Last Modified: Wed, 03 Dec 2025 04:08:24 GMT  
		Size: 25.0 KB (24991 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - linux; s390x

```console
$ docker pull python@sha256:5aa0c19c57de80ea1637fbad3e849cdceb061188b9ec2bf35e8cfe8387b32ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.4 MB (386377372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0cd32bcfe0f0ce7db11618d54f43ac1a2766e582173d226cf7b86089a0d8d7`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:57:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 05:40:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 05:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libbluetooth-dev 		tk-dev 		uuid-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 05:40:36 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 05:40:36 GMT
ENV PYTHON_SHA256=ce543ab854bc256b61b71e9b27f831ffd1bfd60a479d639f8be7f9757cf573e9
# Tue, 09 Dec 2025 05:47:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libzstd-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		bin="$(readlink -ve /usr/local/bin/python3)"; 	dir="$(dirname "$bin")"; 	mkdir -p "/usr/share/gdb/auto-load/$dir"; 	cp -vL Tools/gdb/libpython.py "/usr/share/gdb/auto-load/$bin-gdb.py"; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 09 Dec 2025 05:47:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 09 Dec 2025 05:47:24 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d6b6af65161fdf6adbca5b49fba0d0a414708fb199521ee78075952e4ba4ca`  
		Last Modified: Tue, 09 Dec 2025 02:59:04 GMT  
		Size: 206.5 MB (206478489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbf1f322a1d3c90e655e956dbadc345962c506eec6fc0e320c58430665ca9b5`  
		Last Modified: Tue, 09 Dec 2025 05:48:07 GMT  
		Size: 6.3 MB (6329419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168563b5cc07eb2ed5783b528e7b7d7af5076dd09f90c54d75b52776d57d5d92`  
		Last Modified: Tue, 09 Dec 2025 05:48:08 GMT  
		Size: 28.8 MB (28812444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec42efd3f09b2cc5da1b0ab3255c977f4692b786f944de6b2e9617f34caabf9e`  
		Last Modified: Tue, 09 Dec 2025 05:48:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:latest` - unknown; unknown

```console
$ docker pull python@sha256:ea71cc554a989ac5d722a71ad3c4afb6168ea553b989ff7bf9fde8412b20aac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17552630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a465f77b29a3abf0fd473cc0833f6f182dbbe7fb75ad7aa21ab77e59cb94c28e`

```dockerfile
```

-	Layers:
	-	`sha256:949fabc8b421ec2ed04ec8d0dd2b36f19d8e996dcf0f391d6cf1bbbdadfab8d5`  
		Last Modified: Tue, 09 Dec 2025 07:08:07 GMT  
		Size: 17.5 MB (17527713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78397f67ad809d3a6c454d727b8ed9229e0155b8cb99176c5fd197d02772d31c`  
		Last Modified: Tue, 09 Dec 2025 07:08:08 GMT  
		Size: 24.9 KB (24917 bytes)  
		MIME: application/vnd.in-toto+json

### `python:latest` - windows version 10.0.26100.7462; amd64

```console
$ docker pull python@sha256:3b76eba607d383bdf2e9eabd7cae9166c98e72170854004a36f2559d18845146
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3314118316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc9bf5cd658a2f0587fc32c2689f2df84637386d7ff21765037e1a6dcc5f09e`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:36:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:48:39 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Dec 2025 20:48:39 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 20:48:40 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 09 Dec 2025 20:49:20 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:49:21 GMT
CMD ["python"]
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
	-	`sha256:13a705a6e8ee03f99b80a0bf2257b33ccbf03d0695038a45544f551b47f1bad3`  
		Last Modified: Tue, 09 Dec 2025 20:46:08 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf2ec845e36092f35025b446f4a84789d0001875a44461df70da99007d8c432`  
		Last Modified: Tue, 09 Dec 2025 20:49:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea37b5eb971dd19514c3870274b3fd9711466e67cccb7a7f24a91c38b0362fa`  
		Last Modified: Tue, 09 Dec 2025 20:49:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d417a9df3ccce81c9113e8703f978f15412ac84a925185238929e01cb6766e38`  
		Last Modified: Tue, 09 Dec 2025 20:49:36 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c61149ef6a0674515ed5e1b6e541ff115a9eb10b693013a24c76c520c72142`  
		Last Modified: Tue, 09 Dec 2025 20:49:40 GMT  
		Size: 61.0 MB (60991350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572b5e0dfab25e9a33e424ed104eaf77ebbbb399d910a48202a88479848d285b`  
		Last Modified: Tue, 09 Dec 2025 20:49:36 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:latest` - windows version 10.0.20348.4529; amd64

```console
$ docker pull python@sha256:df01bda7abbbc0b2da909c3c6fe23d51e65555ac345b82e97c476811fe0cc469
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1840811837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d71dc5151de73e1e4d1351aaa94cce6d2243cfc42e5dd8b3497cacd6ecbe4ec`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:46:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Dec 2025 20:46:50 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 20:46:51 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 09 Dec 2025 20:47:32 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:47:33 GMT
CMD ["python"]
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
	-	`sha256:34587e3124c2354fd0c0ebc422da5a49bd90585ddb565123a6a607568a27d77f`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73959298aa0c72f2ef4c2adaca9c6319ad8f57fb3ad3139a3ffb6f2bcc4a5b3`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6b048b9df31de6a2a4089f32d19b21bd49c1d7b7f74b76ccb3aa9c0bc59fa8`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee5ca9163acd37c8180f34b414cf06699edfa777c693d18342d5ef32acf65d1`  
		Last Modified: Tue, 09 Dec 2025 20:47:56 GMT  
		Size: 60.9 MB (60925935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00182617a1921b03d51762122e1f5fba52b8fc8b81bb5dce8c52a89e1006f37f`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
