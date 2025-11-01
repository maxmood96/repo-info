## `hylang:1-python3.9-alpine`

```console
$ docker pull hylang@sha256:7f135350793ad47d941581de4f652e51e3fb383a0f9351e33a55f8ca370ef3c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `hylang:1-python3.9-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:8bc1fd8ba7f9fd5e5ff3820e613030c9e16df3635d2f66dea8ea8eef6388859c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23385626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cce9bbf2e77c599498b169eededb5c2b5774dbe983d459fa1e9d0fc788f4f84a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:15:18 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:15:18 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:15:18 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:15:18 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:15:18 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:15:18 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:16:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:16:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:16:28 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:57:18 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:57:18 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:57:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:57:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9008197b8dd9d9b4c7a87e38fa66c8bceb4f7d87df8e9061284b123459f9451`  
		Last Modified: Fri, 31 Oct 2025 23:16:49 GMT  
		Size: 456.9 KB (456919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27711589a568cd76752066b7f5d51377b4eb3d501cf866ff9a2933d7c3db806d`  
		Last Modified: Fri, 31 Oct 2025 23:16:52 GMT  
		Size: 15.4 MB (15402499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9806928fa0da94a3d2440c42430d7caa253e6f05e8669881cee924ceecabe3b3`  
		Last Modified: Fri, 31 Oct 2025 23:16:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191c8857353551f683faa7b9b524d1d69cfb63b72cd78e3c4595e86d9c33515f`  
		Last Modified: Fri, 31 Oct 2025 23:57:31 GMT  
		Size: 3.7 MB (3723509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:8c9cef82c84e69d98446ad26c2fcd5f902cd3ff797309adc578a31ca32998ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.3 KB (709280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4e598a2b0beeb10ebf0f695c8b127c85ef79cbf8bfceaacd1e527156ca2ab8`

```dockerfile
```

-	Layers:
	-	`sha256:e174091dbe00eb3dbbf4ca68b7d05bf7cb32d45f0edf441843a36c599a3f1b34`  
		Last Modified: Sat, 01 Nov 2025 02:19:04 GMT  
		Size: 699.9 KB (699893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9413050f862d2b0dddb557bbf369fa9e340ea8d16765b3e7c8f4172b32ce621`  
		Last Modified: Sat, 01 Nov 2025 02:19:05 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:6091246e3593b87b757538bb1faec7bcc8221e9ec6bf4e977fb014db6a20d6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22632787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a99e61f7cbb1f25364fc1e29b506fc05f5cccfc0eac587a86f46555f2e0d69`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:13:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:13:15 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:13:15 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:13:15 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:13:15 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:13:15 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:14:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:14:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:14:47 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:56:36 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:56:36 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:56:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:56:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6770e33aa969011d62ca40dc7194752466266c0f564695667f7b5a009b29b9f6`  
		Last Modified: Fri, 31 Oct 2025 23:15:01 GMT  
		Size: 457.7 KB (457739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d0905f4874ae0c0c51cf78356014e1edaf2c5445a40d2c9e914d313f983f68`  
		Last Modified: Fri, 31 Oct 2025 23:15:02 GMT  
		Size: 14.9 MB (14947119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff29d56deb4d64381aef7bf4d56f7c19c12e98699e05ed3b9cd3008fd123808`  
		Last Modified: Fri, 31 Oct 2025 23:15:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08aa647d1cd40dd30739ea8f81e79a37b9d6e73bf3977219b40bbca1594a4d1d`  
		Last Modified: Fri, 31 Oct 2025 23:56:46 GMT  
		Size: 3.7 MB (3723600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:a9315f3c9cd14a735c332890b30f0a22eaf254161607cfcd9eb0e5cfebccaf39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50efb6cb391439dd022678b22183d12707d948ee801a569141c52f0b96a80a16`

```dockerfile
```

-	Layers:
	-	`sha256:b5c22a9ea88ba3104df8e2999efb07864c7be9065e0dcddbf930255e4fe69257`  
		Last Modified: Sat, 01 Nov 2025 02:19:08 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:2ed6488a0252b068d1e982723a89f9e1714715a518bf01c96debf425d03e65de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21959032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594edd1a6c9e98acbfe1a225a60e6d48bf93ecd34984d1588d4fb3a99b5ee261`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:15:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:15:50 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:15:50 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:15:50 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:15:50 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:15:50 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:17:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:17:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:17:16 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:57:16 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:57:16 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:57:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:57:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d45d7e997cf909dc084bd30c499032dd5029e8f96c24e7659f6889cbf0afb45`  
		Last Modified: Fri, 31 Oct 2025 23:17:33 GMT  
		Size: 456.9 KB (456939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdeba935aa7741345eccaad605c41b62da49f9440f6489851576e232dfac13a`  
		Last Modified: Fri, 31 Oct 2025 23:17:34 GMT  
		Size: 14.6 MB (14556634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8c18a56d6393af3f246082c76c36fddd6d361159d5c4d9c3cf310231d3d535`  
		Last Modified: Fri, 31 Oct 2025 23:17:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de70e6842c1cdd096404754afba70c4ca91d305ac29000c68b8682383dabd7d`  
		Last Modified: Fri, 31 Oct 2025 23:57:29 GMT  
		Size: 3.7 MB (3723656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:55321e6012016e56ab197e995a5e06070f0b14297061128cea7d0e37cf08f1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7b8fabaacc399cee00e9f0f059c0466fad695475bff76c1c61d0420f0154ec`

```dockerfile
```

-	Layers:
	-	`sha256:f590add439dde42b7907fd9b442c2aada6c0f0738aeb2a94ae655cbcd403e9f9`  
		Last Modified: Sat, 01 Nov 2025 02:19:11 GMT  
		Size: 703.0 KB (702951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:183eb7a17feb9bb1527d885c92411c5b6771a022ca20eb6c481377638d53687d`  
		Last Modified: Sat, 01 Nov 2025 02:19:12 GMT  
		Size: 9.5 KB (9499 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b97bf40fe704da961c96883c3429af4d22e9332d6fa6b42b25a1a35b7aef5893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23791624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0cde9a6cbce94d877418ea810482ec1d3c8c63d927a93b0c2e838b58e5a412`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:15:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:15:02 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:15:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:15:02 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:15:02 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:15:02 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:16:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:16:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:16:23 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:55:10 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:55:10 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:55:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:55:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee686342b8ed076bf791f466e05379cdd5739d9a89b3aedcb03c00793f8c5d0`  
		Last Modified: Fri, 31 Oct 2025 23:16:49 GMT  
		Size: 459.0 KB (459015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba316076990e2b86e4f940b61f11d084cb714837e0c898d3a3da6e22bee66e`  
		Last Modified: Fri, 31 Oct 2025 23:16:50 GMT  
		Size: 15.5 MB (15470663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328b92a71e2216fad5b69a929cc673a94f3bf73dad6a56c6277afb097c79bdc1`  
		Last Modified: Fri, 31 Oct 2025 23:16:49 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625961162685b7aca5c26faf0b2ee88d20d389a159cda056c4cc223f9a359d27`  
		Last Modified: Fri, 31 Oct 2025 23:55:22 GMT  
		Size: 3.7 MB (3723626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:bf0f0b972e17547d5d1ea8e925692e2199a84dc396d44348bba7d5b65787389c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.5 KB (709536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00876257de0f87c5e686a3d8eb9b6d2ed97cf9be740187caa5a34d9b740d8f79`

```dockerfile
```

-	Layers:
	-	`sha256:cea38d41a7098a96b4a4102991da03f4079bbf85f93be39325d23bae1917a700`  
		Last Modified: Sat, 01 Nov 2025 02:19:15 GMT  
		Size: 700.0 KB (699997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3fa5f653bbb3fc45c3d324d6f8b95b317e7f7fb5206f22b35e0eb4f0b3a58b`  
		Last Modified: Sat, 01 Nov 2025 02:19:16 GMT  
		Size: 9.5 KB (9539 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine` - linux; 386

```console
$ docker pull hylang@sha256:fdb5f25a0ef88b3c9983fc1f4916aae9a60c07ec3ece5051c4deadc0cbb04cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23428781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64d9d276df2d6cf9b53bdcb726df6844bb297abe6f322dc625868c50bdafe5d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 31 Oct 2025 23:15:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Oct 2025 23:15:21 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 23:15:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 31 Oct 2025 23:15:21 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 31 Oct 2025 23:15:21 GMT
ENV PYTHON_VERSION=3.9.25
# Fri, 31 Oct 2025 23:15:21 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:16:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:16:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:16:37 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:56:33 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:56:33 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:56:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:56:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb45f051102b421b6ab2d47f37c72ce701768886d97969d27edd0f7721742e8`  
		Last Modified: Fri, 31 Oct 2025 23:16:52 GMT  
		Size: 457.4 KB (457382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341b3fc8355a75d4e231efa6e8eb781878f9bd88f5814315d284e17569f9081f`  
		Last Modified: Fri, 31 Oct 2025 23:16:54 GMT  
		Size: 15.6 MB (15628778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cea79372ff1e176725f6c950af143d1e6483964b520ce7d5666cb0f1fb72f5`  
		Last Modified: Fri, 31 Oct 2025 23:16:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2ca7f5c6184b1caade3b0981a2c9e976cd74611865a12f4d80eed2e8023dfc`  
		Last Modified: Fri, 31 Oct 2025 23:56:46 GMT  
		Size: 3.7 MB (3723442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:abf0f8ba64863fc1f406d4d2827c976c8f5c29a2fd4b21e0d6e762a7220200ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.2 KB (709183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de32506a9f9b74450c073c0f53a8dac5281763800c964a3478d8727826614c3`

```dockerfile
```

-	Layers:
	-	`sha256:c1d956ff5ec47ff7a3dbd6281265d36a4113bee8995a9f52468d6426805afd6a`  
		Last Modified: Sat, 01 Nov 2025 02:19:20 GMT  
		Size: 699.8 KB (699848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23136f8fae4d96674bbdc63c79e3c83af35c814c1dc67af57b4808366f602b88`  
		Last Modified: Sat, 01 Nov 2025 02:19:21 GMT  
		Size: 9.3 KB (9335 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:dc2359f20ef6e06f45bac73521500b45b3aa3967fd59ed0904e6caf33032bde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24015624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1485840c994456839f6c0b4f6ad34aeb8361388cc8f2987cd9c33b687a5c0125`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 08:19:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 08:19:42 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 08:19:42 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 08:19:42 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 08:19:42 GMT
ENV PYTHON_VERSION=3.9.25
# Thu, 09 Oct 2025 08:19:42 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:47:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:47:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:47:46 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:57:38 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:57:38 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:57:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:57:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d59558aec49aa561bba128776098134d977c895162d47f6feb60e130039a68`  
		Last Modified: Thu, 09 Oct 2025 08:28:28 GMT  
		Size: 459.4 KB (459435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0942dbf5c9f2570c7077c73ba958b6a3ef39f6b79a1d44a50c895fd2c580c77d`  
		Last Modified: Fri, 31 Oct 2025 23:48:26 GMT  
		Size: 16.1 MB (16100044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7681c7589aed2c664fa298a578f35a0d6de107c90038398e283404dede4248`  
		Last Modified: Fri, 31 Oct 2025 23:48:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6543f57a1d2b0bb585329a4caa77e82c95dce2450c288f175f1584c790c8523f`  
		Last Modified: Fri, 31 Oct 2025 23:58:01 GMT  
		Size: 3.7 MB (3723657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:45a684183c04231d6d91fbcfa584dbfa68d5256025e1d820c8e20e79e7361616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.5 KB (707455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd20f983dead58c1d9f8b471f8e916d6219b00fd76a25ba23179c87e64aa17a`

```dockerfile
```

-	Layers:
	-	`sha256:404712be681914041745dcfb46f55408d48219309508a0fcba4298af5c365125`  
		Last Modified: Sat, 01 Nov 2025 02:19:24 GMT  
		Size: 698.0 KB (698000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec13cedd271cce3689c330ea44f51d7925e6547b951e60015f00d4fd3a62187`  
		Last Modified: Sat, 01 Nov 2025 02:19:24 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:02c4af0beb7910cb42a01e3e9222fce50f1263b13dd72dda4c674690664cc53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23114320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f3ad67a3fbd9125507d5d92bc5a21ed44a2cf269dbde9c89cc939c19d39983`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Oct 2025 17:21:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 17:21:20 GMT
ENV LANG=C.UTF-8
# Mon, 13 Oct 2025 17:21:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 13 Oct 2025 17:21:20 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 13 Oct 2025 17:21:20 GMT
ENV PYTHON_VERSION=3.9.25
# Mon, 13 Oct 2025 17:21:20 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Sat, 01 Nov 2025 02:35:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Sat, 01 Nov 2025 02:35:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 01 Nov 2025 02:35:22 GMT
CMD ["python3"]
# Sat, 01 Nov 2025 03:30:10 GMT
ENV HY_VERSION=1.1.0
# Sat, 01 Nov 2025 03:30:10 GMT
ENV HYRULE_VERSION=1.0.0
# Sat, 01 Nov 2025 03:30:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 01 Nov 2025 03:30:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879bd470fd11b0111acf6d20db06ac6a0b955448eb55f42b1ca31bc17c8f4dd9`  
		Last Modified: Mon, 13 Oct 2025 17:53:31 GMT  
		Size: 457.3 KB (457271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3338c9ae03ef7b81d39bd66383292f3d470118788eb80877010a25e41b88196`  
		Last Modified: Sat, 01 Nov 2025 02:36:23 GMT  
		Size: 15.4 MB (15416961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c0022c2a4c47b9864dadbec5062f4ee3db602b8955d79ace2072c670aa29be`  
		Last Modified: Sat, 01 Nov 2025 02:36:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34030729b2a6c38c52386ee4a961299439335e7d2485d8e58f28debabc638caa`  
		Last Modified: Sat, 01 Nov 2025 03:30:56 GMT  
		Size: 3.7 MB (3724601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:71375f6d104ad43e765ab251f54e2651de5b5b1d33236b9f7e67c71dcaf13c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.4 KB (707449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e91aae5d9b16a09c6ed187b4c43c6409426f9a872d0b2671844b2e6c3e2ac20`

```dockerfile
```

-	Layers:
	-	`sha256:5cac48e477078ea77dc8ae52d57770ba390d71a4d14c181bd8d26be34bd18290`  
		Last Modified: Sat, 01 Nov 2025 05:18:39 GMT  
		Size: 698.0 KB (697996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfa0a5a4a346a2289995e0f4f0f705b74a128c0b4ca6473312ec34df1434786c`  
		Last Modified: Sat, 01 Nov 2025 05:18:40 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:1117b5edc3385ee30636c3bfb7565ca57dd6c652a0114f252095e8a51817ccaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23624789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d120df110836364f5d489cc6481df870c9bb9245b070d3933e2ac95842adf17f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 09 Oct 2025 12:53:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 12:53:16 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 12:53:16 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 09 Oct 2025 12:53:16 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 12:53:16 GMT
ENV PYTHON_VERSION=3.9.25
# Thu, 09 Oct 2025 12:53:16 GMT
ENV PYTHON_SHA256=00e07d7c0f2f0cc002432d1ee84d2a40dae404a99303e3f97701c10966c91834
# Fri, 31 Oct 2025 23:34:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 31 Oct 2025 23:34:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 31 Oct 2025 23:34:11 GMT
CMD ["python3"]
# Fri, 31 Oct 2025 23:56:31 GMT
ENV HY_VERSION=1.1.0
# Fri, 31 Oct 2025 23:56:31 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 31 Oct 2025 23:56:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 31 Oct 2025 23:56:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4929a7616ec9e65e89e8fc96cf51868212bfa5dfaa51e5a68686d2f0903e035`  
		Last Modified: Thu, 09 Oct 2025 13:00:09 GMT  
		Size: 457.9 KB (457909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6536e0150704925e7859f01f27abdd3ef94f770f6e8d323cfc612406a926880`  
		Last Modified: Fri, 31 Oct 2025 23:34:28 GMT  
		Size: 15.8 MB (15794004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15090ab8f0fe02bc7d562aa19a1eb7415f837ab57d76102306a6f576936fed46`  
		Last Modified: Fri, 31 Oct 2025 23:34:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f897631540aaa7d831821925026809f5c8ebb3a644c6c06504bc8e1c40014f2`  
		Last Modified: Fri, 31 Oct 2025 23:56:43 GMT  
		Size: 3.7 MB (3723384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:336addcb164c2f04f7f8ebc0e282d020342149487ad0f9aa2b82934101d53503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.3 KB (707329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc4a38a5f6b65b38e1c406af4aba5cc494a5c7de270f8ab570f6f490af3bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:a90fa586f51ac6126589e934c79601a161ae16e6a23255b8d8320545197e89fb`  
		Last Modified: Sat, 01 Nov 2025 02:19:30 GMT  
		Size: 697.9 KB (697942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113b7fd7b0c90c3a3f52e80dbd8922d6294d5b7ff038f2daf69a59051b640803`  
		Last Modified: Sat, 01 Nov 2025 02:19:31 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.in-toto+json
