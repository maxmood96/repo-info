## `hylang:0-python3.10-alpine3.20`

```console
$ docker pull hylang@sha256:d337bd8714a1535e46314cf9ce3a1e69df937d351193e992240d6fd62568cfd1
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

### `hylang:0-python3.10-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:d9e5fd1b322fed4e0734b371c89f52855d5c3eeb2e9be3a60b099629e81d7668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23553261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f37dcd7e3ffa1dd3c7b228f9074212bb344b5f897d9b7f2c8e19a85f784798`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 21:49:12 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sun, 07 Jul 2024 21:49:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:1717f0165ffa072906ac73c9e4f5e3a3dbee324bfa2f234870f1530bf97b4a5b`  
		Last Modified: Mon, 22 Jul 2024 23:15:05 GMT  
		Size: 461.8 KB (461804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2781bbec29c7c89632af77b943bc6138e91539bc79069532581314b11a960a4a`  
		Last Modified: Mon, 22 Jul 2024 23:15:05 GMT  
		Size: 12.2 MB (12215124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e125cf812e71195178cdd9570559dcca866561707e7eef31e45c32ee963ef78`  
		Last Modified: Mon, 22 Jul 2024 23:15:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55a234a52774b0ff8d878af7eca2d196dd013cc749ae0fe114d178758269b1f`  
		Last Modified: Mon, 22 Jul 2024 23:15:05 GMT  
		Size: 3.1 MB (3080751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbde4bb7fc51e6321d70ea596f50054ed5d4424b76bde1356288294788b3d5cd`  
		Last Modified: Tue, 23 Jul 2024 00:08:25 GMT  
		Size: 4.2 MB (4172461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a5a11809668eedbc6a00ff2a9e8f37ae8113b2a002c5614322d07c33770a38ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.7 KB (666665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbe267d9a695dc85ca2222a8a28a18fee92c246e9000d4bb41b6841986965c4`

```dockerfile
```

-	Layers:
	-	`sha256:34dfcbd4b1e5e9c58cd76e8435b41504a3d393e897a74145160752269fd414f8`  
		Last Modified: Tue, 23 Jul 2024 00:08:25 GMT  
		Size: 658.2 KB (658153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8074430e5224ea6236af5d1c9e99f74e0323f24a6b6f332e27150d7a7965c0c9`  
		Last Modified: Tue, 23 Jul 2024 00:08:25 GMT  
		Size: 8.5 KB (8512 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:ad8f055e49929ab6365877ff07fdfe83ea2f0c710b547059595011df94bcf9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22951327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0b674ad7aebcaf4c9aff6d1f00b67c5f564b454f45ab194c7b898af11c59cc`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 21:49:12 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Sun, 07 Jul 2024 21:49:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:bf482409f93435e3c9760a8dc3d483a4ab7432241496dce62198ba61c74f3005`  
		Last Modified: Tue, 23 Jul 2024 10:28:47 GMT  
		Size: 11.9 MB (11869398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c0bd85f000ad75273aa65e31f7a9a4abbfd2fc13dd8c1da7cb712cbf3c0664`  
		Last Modified: Tue, 23 Jul 2024 10:28:46 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949816fd65737fe38fe1f26c38fe43c8442e9fe6cd563b0a068f35dd29d9cb90`  
		Last Modified: Tue, 23 Jul 2024 10:28:47 GMT  
		Size: 3.1 MB (3080734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e68df2fc06dac8158d17b14753bb25ea731e9a7248ed5705a5194b0ac0d80bf`  
		Last Modified: Tue, 23 Jul 2024 13:00:31 GMT  
		Size: 4.2 MB (4173203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:e7c08d0fb2894421bfc5ce39c6b70ead48c3b66d50becd3f708479b6078cc541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1b8b4b0c54c1c788880bb564e986796c5e7a85714874d35510a1b6538b0bd7`

```dockerfile
```

-	Layers:
	-	`sha256:a3fc283a9a503a92199394bce28578249edcbae2bc781ee97db9508c81a966f1`  
		Last Modified: Tue, 23 Jul 2024 13:00:30 GMT  
		Size: 8.4 KB (8380 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:f61c28eb398de794768c4be9c268dfbd676dbbca7603f22ed8dde1ca9b037dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22259637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891956e8e24d30839c5d366e117e799e8902186fea856265252bfc14468ed283`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 21:49:12 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Sun, 07 Jul 2024 21:49:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef77f3591f9a13a2d038b8d57b659d41ac91d2de7301c4ab9e6c12c44d058c`  
		Last Modified: Wed, 24 Jul 2024 09:43:23 GMT  
		Size: 461.8 KB (461753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363a64389d7eafbca19f38b1c976a8e584e696e756f8499d73f406363830f96e`  
		Last Modified: Wed, 24 Jul 2024 12:22:45 GMT  
		Size: 11.4 MB (11449116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8f859caadcaded5f0d0c690672b8f6d8d02d19ed9cba382601ad0ce64f5d69`  
		Last Modified: Wed, 24 Jul 2024 12:22:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d509b825447f063cb46092d7a0196fb8b50c5a0dafb2f5e7873d6435221984`  
		Last Modified: Wed, 24 Jul 2024 12:22:45 GMT  
		Size: 3.1 MB (3080741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97038a075e94765452f4dffe8438101c9df2b52f4b3ea0224068a7d4b2a1d008`  
		Last Modified: Wed, 24 Jul 2024 19:19:00 GMT  
		Size: 4.2 MB (4172841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:462ac7d18b0595b6438d34ff2c700bac388a890152f118dcf0123ef5f7bd54d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.7 KB (669653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bf4aca5e84bdd913729d625ab630b96987384a817f528c35f1e7c43d3be1c4`

```dockerfile
```

-	Layers:
	-	`sha256:377d128ade249a48e55c0d5c95a4ca681bf63c38c43578cd5e0b39e8258ca304`  
		Last Modified: Wed, 24 Jul 2024 19:19:00 GMT  
		Size: 661.1 KB (661053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32a03ab63207ad05928094c4beec8faf1ab9fa2444c8ea73767a52a7cd20dfc4`  
		Last Modified: Wed, 24 Jul 2024 19:19:00 GMT  
		Size: 8.6 KB (8600 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5791ac804582b86630200be79cbc2d1c78d5899b3dba8b7cfbe98cbccc626ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24104782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68abbf616b0fc65beff51c55b3359c2179184f098a36071da44843e950ecabe`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 21:49:12 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sun, 07 Jul 2024 21:49:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:80328aefd956aeaa08972bdfa8c8c00197b42211f1e94cbc9c01112849b47983`  
		Last Modified: Wed, 24 Jul 2024 06:18:57 GMT  
		Size: 12.3 MB (12300301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d60c26d809fc1992aed0f5f20a7c5749d8657a7ac8bfd846a2f248eb569d0c`  
		Last Modified: Wed, 24 Jul 2024 06:18:56 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e4a570a1bb417c7114803fd4368420b8aa6024b2c13029b9aa6550790eb795`  
		Last Modified: Wed, 24 Jul 2024 06:18:57 GMT  
		Size: 3.1 MB (3080703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ceac151b1a87bfb60728b198925493a8a40134700fbc3a6d04f3c17b89bc7b`  
		Last Modified: Wed, 24 Jul 2024 15:33:04 GMT  
		Size: 4.2 MB (4172775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:21a3f853a34091fa68180cdbd2a325ca18fce6ba15e64f8e2f7f439e2055101e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.1 KB (667118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0a214f2be9ef1a7f03f7476048a30e56349c8104d930b7cae44f144b5ea172`

```dockerfile
```

-	Layers:
	-	`sha256:126f83976c691a48c428321c6e957f6384b94f280cdb44825ee018600d1f4385`  
		Last Modified: Wed, 24 Jul 2024 15:33:04 GMT  
		Size: 658.2 KB (658209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d35339b48828d9946f6a2b3049388dcc9c47f5547e6cf9977b454570e755a6e0`  
		Last Modified: Wed, 24 Jul 2024 15:33:04 GMT  
		Size: 8.9 KB (8909 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:99823423fe59524326ca7c51ea605c71d34c07a3c0221dbdf33c2d94a3d75b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23627081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e788e4c20a8542c6120a245b94cdf723374c0c0fca6ec9adc658cdd3bcc5ce`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 21:49:12 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sun, 07 Jul 2024 21:49:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:bfb80fd789d4aaaa1d5934f85d820bb8992cc462cfdda11c720dca2a75ecfbc9`  
		Last Modified: Mon, 22 Jul 2024 22:21:32 GMT  
		Size: 462.2 KB (462201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88dab2be5ab4e765f8a9e579208b0dd65161d38a6ec1313e5fa200c4e276f4e`  
		Last Modified: Mon, 22 Jul 2024 22:21:33 GMT  
		Size: 12.4 MB (12443400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d6b0875f6953effa55c550417d03b169da2d56473564eff1953245718246cb`  
		Last Modified: Mon, 22 Jul 2024 22:21:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ecb9a80ae0dbd505607444639bb48ebe3ba133b39f368be52984a5f37c5cfb`  
		Last Modified: Mon, 22 Jul 2024 22:21:33 GMT  
		Size: 3.1 MB (3080562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a4790926017b459e4e8002b2e8472b24102193384bc0ef230802b1fb0d678a`  
		Last Modified: Mon, 22 Jul 2024 23:08:26 GMT  
		Size: 4.2 MB (4172618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7a64a7b8ec1567d4626330160bca3ee7f3de6d7cbefee100d8997a75dcbf9f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.6 KB (666607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c78c69d6ea0d6f517f791a725fe546b5652b06f95329df437615aa719d10fa3`

```dockerfile
```

-	Layers:
	-	`sha256:e3bc72e0f8fe2d1a77654779888fec8156e9c8a5f966df385546ec88fb69d224`  
		Last Modified: Mon, 22 Jul 2024 23:08:26 GMT  
		Size: 658.1 KB (658128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa98af090c9407789d6900d95072ee34e2d12329048a907712ba9f90fb06bcda`  
		Last Modified: Mon, 22 Jul 2024 23:08:26 GMT  
		Size: 8.5 KB (8479 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:75db8a15571dcd8684445bb73403201079d3df737c63b1b09820074436a13bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24018194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1728770017394c8cc16833ff0edadd86a61bff381a546c475a7be260036f5de`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 21:49:12 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sun, 07 Jul 2024 21:49:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd9dca3c71557146b76d34caf51ce31845024af597b3e49a8a753cc001f0db0`  
		Last Modified: Wed, 24 Jul 2024 06:19:23 GMT  
		Size: 464.2 KB (464224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55297e38d96eef6ebcc89bc384d8d93d17342a8d1299846790a68a3fb45068f`  
		Last Modified: Wed, 24 Jul 2024 08:57:55 GMT  
		Size: 12.7 MB (12728623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43c848c8be777ce4cead2fe3d7ce8abc902e5b63fc0fd89c3975df26c10318c`  
		Last Modified: Wed, 24 Jul 2024 08:57:54 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfcbcac83e5846ad7bc95f249b7b0bbc9b0f4ea7556be83ddfd6c7c0fecec16`  
		Last Modified: Wed, 24 Jul 2024 08:57:55 GMT  
		Size: 3.1 MB (3080750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c8ddba64f82545fbec319d1a1b9d0d2834890a9f2f492ac3da444ac71cd07f`  
		Last Modified: Thu, 25 Jul 2024 02:09:11 GMT  
		Size: 4.2 MB (4172808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:331cb42edd998c36d9ed40cd3902af5c07b90246161021387e0fbe6126f05e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.8 KB (664801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47716c526c7f602fce9f2c6d479cb0bc55d0387bd8ef6aaefbd4e4e83882cee`

```dockerfile
```

-	Layers:
	-	`sha256:b077b3e38c7b927d3ab0a7809ffe8824854a5c72ec5887f82f5bc663878d22df`  
		Last Modified: Thu, 25 Jul 2024 02:09:10 GMT  
		Size: 656.2 KB (656233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f63ca05510af6169edf047cd2360ef4b6c13bf50904c45b8b5d2d21849965e9`  
		Last Modified: Thu, 25 Jul 2024 02:09:10 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.20` - linux; riscv64

```console
$ docker pull hylang@sha256:269a63c87220e364a6a6f35b4c88efc503fcf2a4a6caebcdf8b6715593f2164e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23596710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf66e0f9e6eff309c6167c18dd0c88814a26eb8422113125bae052021589340`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 21:49:12 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Sun, 07 Jul 2024 21:49:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:8177f7da4e814e87466b3701ce38fd2e1b2c2b4a4b4e05255ea6c4971abdcac3`  
		Last Modified: Wed, 24 Jul 2024 03:05:55 GMT  
		Size: 12.5 MB (12508245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4f9f3301f78dfbe594e02aa395e4349d9637f288a1d5e2bb95fb96c06099d5`  
		Last Modified: Wed, 24 Jul 2024 03:05:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b977a594757fbb4c551b7705f6e7bf485e471244a66d7fc0980376191a40fb4`  
		Last Modified: Wed, 24 Jul 2024 03:05:53 GMT  
		Size: 3.1 MB (3080772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2324666e97832f55e34f71e41ca304ee84c327f8507436bd8d87e73b8c5f6619`  
		Last Modified: Wed, 24 Jul 2024 14:09:53 GMT  
		Size: 4.2 MB (4174283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:c38ea06a409fd0cf7f3248086fd15b272e9f5f129ed03c2cab5c2befc820fb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.8 KB (664797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcaa4a092f79640395be3d7c0f98ecd8293bfd78688b343fbe036653a3fdcf8b`

```dockerfile
```

-	Layers:
	-	`sha256:c3dcb632b0d75cd749464fc22e59feebba503bfa949bf11e14c447f0a300a350`  
		Last Modified: Wed, 24 Jul 2024 14:09:52 GMT  
		Size: 656.2 KB (656229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce49b3b3f54cf8207b4d883b4eb2a31987d0acdf3109923df825cf44b04a8fc4`  
		Last Modified: Wed, 24 Jul 2024 14:09:52 GMT  
		Size: 8.6 KB (8568 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:3659fbb1a402a3b36a748307cac9d87b41f106ded5aca468ef0471c94ea05253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23672301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b72a0df39ac0fc743af3a55c273327e8387455a269d7e70308b33d9cb1efa9`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 21:49:12 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sun, 07 Jul 2024 21:49:12 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 21:49:12 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_VERSION=3.10.14
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 21:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 21:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 21:49:12 GMT
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
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baecdfe02d59eacf44954894e7c2146a3d5c7099ff70061111d0789211a6fae0`  
		Last Modified: Wed, 24 Jul 2024 05:44:07 GMT  
		Size: 462.7 KB (462738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bfcabee8c8f3ef38e35ba9d5f9ec182260c67df9dda8a5c2d474ed58f60ef7`  
		Last Modified: Wed, 24 Jul 2024 07:45:30 GMT  
		Size: 12.5 MB (12494496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1372eac71890a54ee4f3784debe5a8b19cac41c4a16325ab3ec12145ab4a7d35`  
		Last Modified: Wed, 24 Jul 2024 07:45:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b495960033b8e2a6b98222e786f2351df72fae32b002d7319f201ef4f6090a65`  
		Last Modified: Wed, 24 Jul 2024 07:45:30 GMT  
		Size: 3.1 MB (3080709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce949fd4027f9ce0e4801c21f149c32eb406c03820d963cbc0aba1040d1ce1d7`  
		Last Modified: Wed, 24 Jul 2024 16:36:09 GMT  
		Size: 4.2 MB (4173062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:4863c4be44bffc0f2ac783ba71922c45ba663ff2fe7fdf3857eebb452651f15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.7 KB (664723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d39c87346f605b1bf48b3afef0143cf1a275e56d4b4c35ccb53ae50807b86b3`

```dockerfile
```

-	Layers:
	-	`sha256:2e3a99f428e0d0b188f654880801a84047e130c123eed3e79b1bedc754d8a753`  
		Last Modified: Wed, 24 Jul 2024 16:36:09 GMT  
		Size: 656.2 KB (656199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6396c2ee1e191a88c4420d7f8683f92ffe463a682d31fe37e6c5b3c8db4cedb4`  
		Last Modified: Wed, 24 Jul 2024 16:36:09 GMT  
		Size: 8.5 KB (8524 bytes)  
		MIME: application/vnd.in-toto+json
