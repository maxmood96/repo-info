## `hylang:python3.11-alpine3.20`

```console
$ docker pull hylang@sha256:d4e709a456c387e9cd490a96daa1d2320119ed77ef9eaea41c213784064265dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `hylang:python3.11-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:724366b108a9468aebd63ecd7f3ed1781b022cd78e264ea3d43afa5438f8673d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26087381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4a3d3b04dd815f2c35c2d50a8ab90fbb1d3fe8689f7595888bb7fe1f566863`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.11.9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8433896d5d0a8102565aa0aece9c227502fc549b6835f6f04fe88a035bac62d5`  
		Last Modified: Thu, 27 Jun 2024 00:13:12 GMT  
		Size: 463.2 KB (463229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54353c9750d391ca5b6a1141a37a284a2c55ccab5686b6c4e78bea7f53ae49c2`  
		Last Modified: Thu, 27 Jun 2024 00:13:12 GMT  
		Size: 12.7 MB (12672262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bafa4723f8f470024f83b1bdb622f1fd47f3ab9e73bf0199ce6fbfca4ce63e3f`  
		Last Modified: Thu, 27 Jun 2024 00:13:12 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78da16b983ac898c5d3dba227289a4b2c59a7c40e972aa33a0a562fd4d5aadc0`  
		Last Modified: Thu, 27 Jun 2024 00:13:12 GMT  
		Size: 3.1 MB (3129979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457af2132d3197da7ff271d1926041fbb14af7bcff215f593b0d782398b5001a`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 6.2 MB (6197839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:99e8abdda2c28cb6740d4438f7968ef7ad72eee0703b026803a4d96e26a4e4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.7 KB (657655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8f3cc7f14271c544f7793079849573ae6fd7e3428e46fb9ef0b5edec34057f`

```dockerfile
```

-	Layers:
	-	`sha256:44efa5cb4c294a93acbe5d4690fd1ea9435ff5d62bcb41d81272f29153eaab65`  
		Last Modified: Thu, 27 Jun 2024 00:59:44 GMT  
		Size: 649.1 KB (649146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e96bea8441453f84132fdad6d1d9653b94971b49886685b3cfebb0bc828ab8ef`  
		Last Modified: Thu, 27 Jun 2024 00:59:43 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:bda30b6350d49f8e1c8fbb0804aaa91bfe7803058a5921286ce527e969c814c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25431982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26f24e354723bb17dcb10122aec1a2fef44444e58c0aa139e99fc0acb94cf2c`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.11.9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1690c05b67bd96f09afbaf8ed50bd1d5ce45e8ce028ec45d793a1932e33c9f9d`  
		Last Modified: Thu, 27 Jun 2024 00:58:57 GMT  
		Size: 463.9 KB (463884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98a683153fb4386c1d68a680c72de04087a9af0e6ca6a4f3c9dec9b7f8f8250`  
		Last Modified: Thu, 27 Jun 2024 01:37:06 GMT  
		Size: 12.3 MB (12272958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda56ee314512e1337dbe517646c36d7ee6eecfbd30a196c46e54bb368f694de`  
		Last Modified: Thu, 27 Jun 2024 01:37:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fa95af60c9c792e9817951389efb17c68a06ae3b67c094f303b2fa4e60c3ee`  
		Last Modified: Thu, 27 Jun 2024 01:37:06 GMT  
		Size: 3.1 MB (3129989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad29cdaa9712125052740fb5f0a4f3c631a2d6e3419dafb89d382e56cf2025c`  
		Last Modified: Thu, 27 Jun 2024 02:33:53 GMT  
		Size: 6.2 MB (6197768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:080ebc54c864eac646b4f6748797dc63152faeba5200f495e849ef86c3e6c202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b72d28e14b7e2b05d527832f36da141397186842c7536d3ed97c6cb59c46cf`

```dockerfile
```

-	Layers:
	-	`sha256:57a7f7899db55a3c357c0a55c2042c5240da32a20a6e797070dfb51d0446946e`  
		Last Modified: Thu, 27 Jun 2024 02:33:52 GMT  
		Size: 8.4 KB (8378 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8cfd198223a54119291faaf7b61fc51c772a9458764c55225ca5da259564a132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24734834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bab074d6c3cf034154c51ac1564fd22c9e4de715f42230680d963fd5eeceee6`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.11.9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c708927d89b7745e9f553175dbb9d585894c9c0f2cd91946e4c0e12199a4f89f`  
		Last Modified: Thu, 20 Jun 2024 22:54:46 GMT  
		Size: 463.1 KB (463099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2406f24a60cb24846214b23ea307349f16026afe6114190f4a2cca33cc64ed66`  
		Last Modified: Thu, 20 Jun 2024 22:55:23 GMT  
		Size: 11.8 MB (11848727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba671be270f2877c58622928a492ef34e700370de78d6d6163bef0b78bccdee`  
		Last Modified: Thu, 20 Jun 2024 22:55:21 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e89129fbd5b97d28a0f1f243ef937c08a1abf5b193d05c30bf994ecd35573a`  
		Last Modified: Thu, 20 Jun 2024 22:55:22 GMT  
		Size: 3.1 MB (3129989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7502fbb9e4f795fb8d705f5ce174caa78852237ce497543246b849825fd3c4`  
		Last Modified: Fri, 21 Jun 2024 12:14:26 GMT  
		Size: 6.2 MB (6197923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:253bc883c339861ca779e9597c48ef6ae2c9771ac567fb4e98d1954673594dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.2 KB (660209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624c4076e30ed2fe1b2d734fb110dade623244746ff60a3bc4e87510a00ecdfd`

```dockerfile
```

-	Layers:
	-	`sha256:c584cb125e164d051fd8c58a7e3a524662a2f9279506392b9bdab52d0bfce295`  
		Last Modified: Fri, 21 Jun 2024 12:14:26 GMT  
		Size: 651.8 KB (651760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143427257f30ffa24a0382adb4b001f9927d17fcd3c1bff41bf185a96e6bf039`  
		Last Modified: Fri, 21 Jun 2024 12:14:25 GMT  
		Size: 8.4 KB (8449 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:dbb895e4771e13b092a26694151d2cf1c5091cd10a2d4a5527502c1c4b2f13a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26640567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14858a86c6babdcace04131dd9f6c2fdee8f911525644fa755166b310789fceb`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.11.9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e0a54ce1bdfb371b942c96830ed8a81f953669f02f93cbf826a148112789ee`  
		Last Modified: Thu, 20 Jun 2024 22:33:07 GMT  
		Size: 465.5 KB (465483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b63f47bcf0befe162c76aa7efcaa05de208fc0bb83af9bc30cbb2c8b9809c1`  
		Last Modified: Thu, 20 Jun 2024 22:33:44 GMT  
		Size: 12.8 MB (12758194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddfde8986f4bef2e85b0a745cd02c2b5e4442eaa5809a0a16772de9cf1285e4`  
		Last Modified: Thu, 20 Jun 2024 22:33:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef7231fb3dd46741ae9bce900ec29b62d152172bc0d8da898af40b74f14befb`  
		Last Modified: Thu, 20 Jun 2024 22:33:43 GMT  
		Size: 3.1 MB (3129969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05acc646c8283a33ff1bf7a66af65b490b9c21db08a9bb57a46624c040116d3f`  
		Last Modified: Fri, 21 Jun 2024 15:29:42 GMT  
		Size: 6.2 MB (6197879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7d235786bc390f84581c8db6a203aa9ebd6da444a055c67f85e2a2c4c2672489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.9 KB (657892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35035c2c22c469ccdabd7270d72d26dde47fad5cdfc693a211ab77e288cfb41`

```dockerfile
```

-	Layers:
	-	`sha256:10c4172faa15782286ffde3814c3dcaa812441faa236610a10800385353ee2f9`  
		Last Modified: Fri, 21 Jun 2024 15:29:42 GMT  
		Size: 649.2 KB (649202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a45e0519c0134c830ba77c21f32ca9c7ecfd676968c9b70cf8a459d4ecdbdd`  
		Last Modified: Fri, 21 Jun 2024 15:29:42 GMT  
		Size: 8.7 KB (8690 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:742445445b0b20ecf90c183994cbc112f091ed076c93b82f5ceed56c6ab5312d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26130005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d426b118ea90bee17dda9cc8ded7c7bbdc4ae3bbf565a4931feee0ea7bc86b`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.11.9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7561584ac9544d43ac35e50a0716798d2030f3b92ba8f14fb41a88e0946f4fe`  
		Last Modified: Thu, 27 Jun 2024 00:15:23 GMT  
		Size: 463.6 KB (463615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a900ac26828a88a2a7dc1075d92d0c4507ffa05bdaf9e4de60e46638c273f4`  
		Last Modified: Thu, 27 Jun 2024 00:15:23 GMT  
		Size: 12.9 MB (12868916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7f4587807bb4b4ac7a7930e4fa0c2e374e75afdac578188147ce80883e7c2`  
		Last Modified: Thu, 27 Jun 2024 00:15:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03c4d42778d6a81244aa1ca6addce1e692a53c78a7d693d6f007ee1375a087`  
		Last Modified: Thu, 27 Jun 2024 00:15:23 GMT  
		Size: 3.1 MB (3130001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7190f37bd96f89e4457f17f8fa021e07a707cb44e73d080db1ae8a86ca699c9`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 6.2 MB (6197775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:dc2e1cfb6ffabd9c8a660a59cb72c14e77ada1a70f4fdbc8c9acf100c512ef82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.6 KB (657597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52573f09626652ed9ab93e57119297a3d8377fb2de680d456bac50e06fd93c7a`

```dockerfile
```

-	Layers:
	-	`sha256:4b47a5255b78ffe414af52bb50a21106f3098ea1bf35d4e84614eeb8125bc2cd`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 649.1 KB (649121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95298313d548abc3bada60e69db8013f7cb3b8f9978f5e8b991a891ec741fad8`  
		Last Modified: Thu, 27 Jun 2024 00:59:45 GMT  
		Size: 8.5 KB (8476 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:ceabd61da9ae136ad84df9cd52da4ec86187103c44bf9dcb693e2e32f49a197f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26535207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293e8d9b279c0af5f4f99e9ec1375aa77d62761e0b3dc65278f9fbba44b0db22`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.11.9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bd453c8be5405b60b60e6f4ed670d0b55e922008cf221fce0ac80e3689940f`  
		Last Modified: Thu, 20 Jun 2024 23:19:38 GMT  
		Size: 465.8 KB (465849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc2cb2addfdc1938b76d750ba652c949ba1d299535bceb0750fae383d45502a`  
		Last Modified: Thu, 20 Jun 2024 23:20:14 GMT  
		Size: 13.2 MB (13169563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5291371b25ebdbdc9f88328fb24c0ba2140879cff46417718573a0cc3477493`  
		Last Modified: Thu, 20 Jun 2024 23:20:12 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f20c94eaeff518b957db50ec4f21d2250f168cc39a8c4c996f83eed1655281`  
		Last Modified: Thu, 20 Jun 2024 23:20:13 GMT  
		Size: 3.1 MB (3129987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18999f0fddd2642130fb76ffe79852a61fe6f9757ccb0a9680b0a06a029ad42a`  
		Last Modified: Fri, 21 Jun 2024 05:59:55 GMT  
		Size: 6.2 MB (6197867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:60f82b74d31845bf7d27f77819fd02e7149692698b9bf13c9d97c851dd0e8072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 KB (655643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdd1fa8b248e48449933cbc4b4518c431523b9b770735be5b5bfe60371c3802`

```dockerfile
```

-	Layers:
	-	`sha256:b9a95ad8ac311d34ad986b85ca3fc35b05887ab178e88e05303d86763962ef5f`  
		Last Modified: Fri, 21 Jun 2024 05:59:55 GMT  
		Size: 647.2 KB (647226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3927ce4468ec16e844382225e628fc5f99146660f16c54b7b8778a8b9fffed0f`  
		Last Modified: Fri, 21 Jun 2024 05:59:55 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:e7ede01821f1fbea5cfb871b28163703bad96366274171ca77cab4560e6cf1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28402414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2032a546f82c80459a41d1a6d1281d71c31d0cd5cea1c44e7a94838699c4b99`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 May 2024 09:33:51 GMT
ENV LANG=C.UTF-8
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_VERSION=3.11.9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Sat, 25 May 2024 09:33:51 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Sat, 25 May 2024 09:33:51 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b21c33714fac5d281268dfd5fc94d1ad978120d3d01be27cc5775a2e39bc0f`  
		Last Modified: Fri, 07 Jun 2024 22:31:52 GMT  
		Size: 464.1 KB (464083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7194bfcf87d1c3b9b31dae6765a8e470bdb4e4c4403b48c8ecbc2e5ec9f6a2b5`  
		Last Modified: Fri, 14 Jun 2024 19:29:21 GMT  
		Size: 15.2 MB (15150020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa7247924882aa5f5e737a1f575adbdfeff37a22b1d8b9050bad8373f007ac70`  
		Last Modified: Fri, 14 Jun 2024 19:29:19 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c381599b67ca3efc672b889ba3f433d72da29a239f74c7772cbc9b70ba1fc6`  
		Last Modified: Fri, 14 Jun 2024 19:29:19 GMT  
		Size: 3.1 MB (3129961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9079039c6af3d8f3a6697c36d04e4e11e0ba84e5b9a85108457f5b6971eda8be`  
		Last Modified: Fri, 14 Jun 2024 20:04:47 GMT  
		Size: 6.2 MB (6197768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:5645c96ef4b42c6790027dfe48a6fe61b8ecb673858a16d2ad0f672bff612074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **655.6 KB (655570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053c35830a65524b8dd53c2f262b59e573e28e588d472fe72d6cd9d3d2ead072`

```dockerfile
```

-	Layers:
	-	`sha256:4908011518efade57affe78b3bbbe75a718cd759458c599aa060b0f22a80e781`  
		Last Modified: Fri, 14 Jun 2024 20:04:46 GMT  
		Size: 647.2 KB (647191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48d7978a7b25ee4e93e024c369e03e80afda8da4a126f0cf9ec3a04699d8b713`  
		Last Modified: Fri, 14 Jun 2024 20:04:46 GMT  
		Size: 8.4 KB (8379 bytes)  
		MIME: application/vnd.in-toto+json
