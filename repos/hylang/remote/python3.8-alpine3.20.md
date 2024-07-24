## `hylang:python3.8-alpine3.20`

```console
$ docker pull hylang@sha256:689ea2ffe6c71e606698224f4287534c33f3883ac4b75f9a32609d2b0d5abb0e
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

### `hylang:python3.8-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:35b299eae06667183760ca5242c9c35a0c6dd347a0ce66efaadc56a16e43074e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21900212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d4959e69462519d4bb34cb2aee33b0566dd032b76b01e65ec4b614f8b71332`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 01:49:54 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836bb7ea00ffeec6ee055b7a17bde2fa239377e041faa8f22e5a63b6a2f48deb`  
		Last Modified: Mon, 22 Jul 2024 23:09:46 GMT  
		Size: 461.8 KB (461810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d5b5966ffc16017127434f17aefd6bcb881180e61aea2673eec51712cf5cd4`  
		Last Modified: Mon, 22 Jul 2024 23:09:46 GMT  
		Size: 11.4 MB (11361715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df3bbf99283de4dbc7873b8a2c4969b4256e67f8d11dbd6723dc41fa53b8329`  
		Last Modified: Mon, 22 Jul 2024 23:09:46 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddfd8ed15fbe6c86f7139b36472f82e482f670f95e2cdba8782352cfc488a92`  
		Last Modified: Mon, 22 Jul 2024 23:09:46 GMT  
		Size: 2.7 MB (2697385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a598bc8594b39eca9c1bed4474c97d7f10362f1e0e850e879fc4b0a3f23f9`  
		Last Modified: Tue, 23 Jul 2024 00:08:42 GMT  
		Size: 3.8 MB (3756180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:c181b94581504640991472e0696ccefa3f152b9443713795cd8675dabdcc5e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.1 KB (669073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61f82d30f93b84a82b57e9ec99a4ef46c46a6d2765bbdaeb76d21a78581ee24`

```dockerfile
```

-	Layers:
	-	`sha256:7e1f708bdc789967bc00b93194237a9b74573c67eb027f46633c87ced7922374`  
		Last Modified: Tue, 23 Jul 2024 00:08:42 GMT  
		Size: 660.6 KB (660573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50522f2fb3ac648e01b2db50ade197a61437d3e78e3960cafa7947af98683793`  
		Last Modified: Tue, 23 Jul 2024 00:08:42 GMT  
		Size: 8.5 KB (8500 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:cdbf30c971e4dc495bb7398675f688fd9c5ffb5fd3e6a2f255e380812c0ea4dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21316065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6765954e2380290c69e096dbdaff9761b0395817c9717c86e30cbb0ff417c24`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 01:49:54 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc40886e816061a64b6be7bdf7c340dfcbc54c7657f624b135742461c31364e`  
		Last Modified: Tue, 23 Jul 2024 10:28:47 GMT  
		Size: 462.6 KB (462574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb9b925a145ad1c87b5ecc3d59f3dacb50338a9cdd977f18cf1a452244d8c7b`  
		Last Modified: Tue, 23 Jul 2024 10:47:52 GMT  
		Size: 11.0 MB (11034580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663b04c977cbbdc0674ecaccd7363975c0c820a868fcecf541daeab844cfd155`  
		Last Modified: Tue, 23 Jul 2024 10:47:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60afc5d3cdba734dabd4d06c40f89ae744948db3abb79e0e7f4a4508cca501a4`  
		Last Modified: Tue, 23 Jul 2024 10:47:52 GMT  
		Size: 2.7 MB (2697311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef89c2d9c7288e59461a54c2fc10092f32da6e7a2f72d70fc73848cc0a4758e4`  
		Last Modified: Tue, 23 Jul 2024 13:02:44 GMT  
		Size: 3.8 MB (3756184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:d93c2c5de7ef7615179b43db41fddb6e73a75ae1cccbfe5e5926a25f33563698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c51e3992410c1fac570cb71515d2ab68d96550260f70257ac4a0b206e04905b`

```dockerfile
```

-	Layers:
	-	`sha256:4c4cf63d8d16ed3147a86d6a142160c8ceb1f8941783b5717d7f5500fd256e10`  
		Last Modified: Tue, 23 Jul 2024 13:02:43 GMT  
		Size: 8.4 KB (8369 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:0d8afb5a77df2c674ae219ccd505b16681d5bd9ce2b35dd16711db39ddd74425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22588055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d66c95d6992bedd7cffb2638137b506aacf842ccb859b3fda7e0de851024017`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67fbf7b03239e69ea5cefa1b3bcbeb41abb2359ce6e7c757b9818b1d72bef20`  
		Last Modified: Wed, 03 Jul 2024 07:06:27 GMT  
		Size: 463.2 KB (463183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4992ad3b4d201d972eb764216ca5e39645df2650140369fed5716ab3533903`  
		Last Modified: Wed, 03 Jul 2024 08:51:12 GMT  
		Size: 12.6 MB (12576235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7051c38e4326780ce9afa08e1336f3547f88ed5c0bfeedf93651e5a160f979`  
		Last Modified: Wed, 03 Jul 2024 08:51:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e0232fe4491d75ee723142cedd2996e8a5796239bcad879eb7bd183fc20c7b`  
		Last Modified: Wed, 10 Jul 2024 19:27:07 GMT  
		Size: 2.7 MB (2697322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456bd0b0d249de18953c3a613fb25c43b59965f3f1ba6439d130d4d559cdca85`  
		Last Modified: Wed, 10 Jul 2024 20:16:24 GMT  
		Size: 3.8 MB (3756231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:8a046d2ce613668a80c3757da2ea4007ec623da3b88f33d18bd1ff69ed2c1836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.7 KB (662667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0bf10333594ffd501daeb13f821937c0e65f60bb917fec43e12cf5ef598b9d6`

```dockerfile
```

-	Layers:
	-	`sha256:867a5e7c47eb8882bd60e74f46ffcc1a4ea79d8acb6aa992d439bf08871083e2`  
		Last Modified: Thu, 11 Jul 2024 17:03:51 GMT  
		Size: 654.1 KB (654079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0b1dbb036b13982cacc8fb131a6564821a02fac7afe868e75ff13503348a44`  
		Last Modified: Thu, 11 Jul 2024 17:03:51 GMT  
		Size: 8.6 KB (8588 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:17f65862aaaf5f0270be7f511def552298fee12e504788c44e0f21d81aa3b730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22463203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e3ee4c33bf3e643dea0e1cc2a4ceb6d172ec0970c278d6adb1db440cfdc6ca`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 01:49:54 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2711f91d5f9c677eb6883af3f381a64f628a585ad46fcfcfeecf39228185c2b2`  
		Last Modified: Wed, 24 Jul 2024 04:24:38 GMT  
		Size: 463.8 KB (463841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348639857ceb6b9f7b6f01b42fb2ed7f6566b471faafe3024c271068e154da77`  
		Last Modified: Wed, 24 Jul 2024 06:52:35 GMT  
		Size: 11.5 MB (11458810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d11aecfce439641f87f8069ce5add166588045c54d75f7382ef781d62962ff`  
		Last Modified: Wed, 24 Jul 2024 06:52:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106bc2f68e8c91ad9d3aaac666e12570d4e185e13baa8e98e75d6c94103bff85`  
		Last Modified: Wed, 24 Jul 2024 06:52:35 GMT  
		Size: 2.7 MB (2697295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a9f12394ceedc1e9cbc30b613b73abde15779a806ddb87c0af551252aabff5`  
		Last Modified: Wed, 24 Jul 2024 15:37:13 GMT  
		Size: 3.8 MB (3756096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:13e41c3637c19ffc1a7171c6b01bc191187864343726c21c48a051a1e4c00ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.5 KB (669526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dc55a93a6aaa91a850f57e7f37454620ad43c839205164c3112556f131910b`

```dockerfile
```

-	Layers:
	-	`sha256:fe93792204e3236229b97d919a8561a21c66a540fb5992072a35ba94fff21497`  
		Last Modified: Wed, 24 Jul 2024 15:37:12 GMT  
		Size: 660.6 KB (660629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6df9f16cf24256226587ae96cbeb1c1a8f5b80476750306e1a9bbf063c0902d`  
		Last Modified: Wed, 24 Jul 2024 15:37:12 GMT  
		Size: 8.9 KB (8897 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:28cf5a34909022fe0fa2dced5650911575d5b79ddcabb5168768028b0a20a8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21977392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eeb6d3389cb816a1e4e6719948cb6c7606b3018b9581b1437e2ecce28cc6752`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 01:49:54 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfe863ab6c0e46decd5d3efd9fe4c8412543609c2dc172b0c0d81f53cb71b87`  
		Last Modified: Mon, 22 Jul 2024 22:10:41 GMT  
		Size: 462.2 KB (462197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ba181033bbcd78b4b9f9021fdaed0fb4c8e56335eae80989969cca80ea3e21`  
		Last Modified: Mon, 22 Jul 2024 22:10:42 GMT  
		Size: 11.6 MB (11593616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ec97a04d5c906ae987a95a559aab6643166d2b46bd1e26f699e30fe03d900b`  
		Last Modified: Mon, 22 Jul 2024 22:10:41 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55655954f727b86cf7960f2b681e04bb9e44301b36e6e14e9f94782ad87855e0`  
		Last Modified: Mon, 22 Jul 2024 22:10:41 GMT  
		Size: 2.7 MB (2697329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4196495a8b47f789407b66026f5658684d2539de596aafa4ee2593927a8cc1`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 3.8 MB (3755950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:e158768c93722a8b0fe1b5d86d81eedffbc61a21ad70de8e8c90053c2af09c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.0 KB (669016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5c6bd6c932eb624490df4559ea4d5ca663c7c9f8f66c84019302e20422f12a`

```dockerfile
```

-	Layers:
	-	`sha256:40955456e32f6972d6173022f4c898da30a51fa7f49c070030b51ca64ee4944e`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 660.5 KB (660548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47a2bc01ef8efe0edb39bfafd8123496bef118b6f23e113e8daa6b0304798b4f`  
		Last Modified: Mon, 22 Jul 2024 23:08:42 GMT  
		Size: 8.5 KB (8468 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:612d80182427f1bdbedb05bace4443d9c1a58f15b372f75b4b98ca951b2f0baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24604532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6418b635df4a4fc591ac15496f5c74aaa25411b1a0cc5ff906cda1edc71cf7ee`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dda537e2a89e050c4a6baee145aa8999cb1aeb295d4b29f95940b9351c2e3`  
		Last Modified: Wed, 03 Jul 2024 13:15:42 GMT  
		Size: 466.0 KB (465998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09212bc29ebab8e325b8b8a68dc45c63560693164191e56dab1ee761f5368640`  
		Last Modified: Wed, 03 Jul 2024 16:54:28 GMT  
		Size: 14.1 MB (14113022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f06fe6cd0d968abbb73c9378fb82d23c8616d47ca432e4b1ddc3e9e752d041f`  
		Last Modified: Wed, 03 Jul 2024 16:54:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149bce38fde7e4441856bf305fe86171daedfe68569a57812e4f8cafc8bda4fe`  
		Last Modified: Wed, 10 Jul 2024 22:35:03 GMT  
		Size: 2.7 MB (2697312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5850ab7aee3a0c39d88b26946d024f6214a525171ff58c340fabbf8ef8b944e0`  
		Last Modified: Wed, 10 Jul 2024 23:28:23 GMT  
		Size: 3.8 MB (3756271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:64821677f0e141905b598e89cb5c638641a6ae738a7f4a619c894b4a41c2a3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.1 KB (658098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959a5a68c39a18e336e53553eff81285841facbe44dc6e23effd80a77e97d4e0`

```dockerfile
```

-	Layers:
	-	`sha256:a0bd9131b8d5cbbe02e35822c24ec55a22fd8d5726a54524d25063ae3deb372f`  
		Last Modified: Thu, 11 Jul 2024 17:09:18 GMT  
		Size: 649.5 KB (649545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f416ea5d95eee47b737b9b325a0c48043d9237ef260de00052e097cbbaba81`  
		Last Modified: Thu, 11 Jul 2024 17:09:17 GMT  
		Size: 8.6 KB (8553 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; riscv64

```console
$ docker pull hylang@sha256:f8b1ccc94bf0248e2315793d913d68a4807b2943d0a1c26bfbaf4db1217e9258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21631421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3be37aca2dc9c5ab4807176de30ccc70dab3980f4be48316ae1fd871165ef0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 08 Jul 2024 01:49:54 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace253365c23ecfdc250ca83142af637ab9336949fe86ecef247d97e45417502`  
		Last Modified: Wed, 24 Jul 2024 03:05:52 GMT  
		Size: 462.5 KB (462505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b6013f9f34a13fae3c9d2d66ec3d832c9fbe06428bffe1546ec83f9139e4b9`  
		Last Modified: Wed, 24 Jul 2024 04:20:23 GMT  
		Size: 11.3 MB (11343493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7910ba2d15c5cbd6d28967d0d4b26da80ac4f7da17e1a81fcaa1e4ef91d8aa`  
		Last Modified: Wed, 24 Jul 2024 04:20:20 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4545cf20feaf6074491bd04da283a0f03b51bb494136deb120fcd8228a522cee`  
		Last Modified: Wed, 24 Jul 2024 04:20:22 GMT  
		Size: 2.7 MB (2697331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15dccbf1a9fa9b2b228403a792b09c61aebbcaa89a1ea4d073f66b2a5e0d2e0`  
		Last Modified: Wed, 24 Jul 2024 14:21:59 GMT  
		Size: 3.8 MB (3757190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:966d5f39f5554f966d8c4513d86ed703ddbfe3331ca693590980e38b140a1074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.2 KB (667205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66acdceef857e9fbe01534c091e33ddfc0a9d524a0e1888c18dc949fc2579d51`

```dockerfile
```

-	Layers:
	-	`sha256:64fa5a2c566520447a73704853efb1ce0667d1cc5db24d6a3bcd715ab158e17c`  
		Last Modified: Wed, 24 Jul 2024 14:21:58 GMT  
		Size: 658.6 KB (658649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c66ba212c8b902400c5ae4afd59c75b83d866edcfc9c3a1e2d9becaec2f445b4`  
		Last Modified: Wed, 24 Jul 2024 14:21:58 GMT  
		Size: 8.6 KB (8556 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:381528998e96db157c8dbe347370a9c323ef8c13b17f0c79142c7289170ac240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24188932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae98d5fa2b0215d42d4213b4f99ae92a2b9fc96f1cc714ad697de02ed07027ff`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jul 2024 01:49:54 GMT
ENV LANG=C.UTF-8
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Mon, 08 Jul 2024 01:49:54 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Mon, 08 Jul 2024 01:49:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 08 Jul 2024 01:49:54 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81372ec9eec545e9af2e05c16da4cf7ebcaa676e104e5924b51839f59c80730c`  
		Last Modified: Wed, 03 Jul 2024 05:10:43 GMT  
		Size: 464.2 KB (464153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b8e71379b6888c52f0ac7161585c2358586b49495a21ce9faa32f053884d1`  
		Last Modified: Wed, 03 Jul 2024 06:35:42 GMT  
		Size: 13.8 MB (13809460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45722d661bf93d4b9228032440d31212d5ba6528581ccbe33ef209f53f407bf`  
		Last Modified: Wed, 03 Jul 2024 06:35:41 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a85e7c2e1a837ed709b0836a2a394310527ffcb4ca5bb4593d25bfc43c1529`  
		Last Modified: Wed, 10 Jul 2024 19:30:54 GMT  
		Size: 2.7 MB (2697208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8601a2023717bddf3690cb4c0a13b86d8265bf4985e92cc1cc1294b8b546f810`  
		Last Modified: Wed, 10 Jul 2024 20:18:23 GMT  
		Size: 3.8 MB (3756025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:de1f0689ae7901109f5e74bb8d12869b58bc449e1cd104e26e9cc664381ff12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.0 KB (658023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355f6ea297fa766930e2bdbf4e5abf99cbe7ac382892d17ba7d6529520da5eb3`

```dockerfile
```

-	Layers:
	-	`sha256:38473b87412de3cf2ec16fdd912b67e90a339e478fc7e4a20ef0760e7a7562f8`  
		Last Modified: Thu, 11 Jul 2024 17:07:39 GMT  
		Size: 649.5 KB (649511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91cc46de878921013cc6a2884fbb89916d2c1425936007634f806982bca74603`  
		Last Modified: Thu, 11 Jul 2024 17:07:39 GMT  
		Size: 8.5 KB (8512 bytes)  
		MIME: application/vnd.in-toto+json
