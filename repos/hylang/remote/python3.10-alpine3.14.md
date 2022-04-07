## `hylang:python3.10-alpine3.14`

```console
$ docker pull hylang@sha256:7c40c818346b50e8858e74822e880a38f79e896fb15d464a7856af6e3f0f39f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hylang:python3.10-alpine3.14` - linux; amd64

```console
$ docker pull hylang@sha256:9c1dc8dc2b800159fe0f2fea85d44b01581c5336833eb23c0a7d3b9f3c690dff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21751112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963b37e2aeef0dd0ac1bcea0d4ee1aaf2390618b03ba9d154e10b6f7f04e9efd`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 06:01:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 08:10:25 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 08:10:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 08:10:26 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 05 Apr 2022 08:44:07 GMT
ENV PYTHON_VERSION=3.10.4
# Tue, 05 Apr 2022 08:57:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 05 Apr 2022 08:57:35 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 05 Apr 2022 08:57:36 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 05 Apr 2022 08:57:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 05 Apr 2022 08:57:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 05 Apr 2022 08:57:36 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 05 Apr 2022 08:57:43 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 05 Apr 2022 08:57:43 GMT
CMD ["python3"]
# Tue, 05 Apr 2022 15:48:36 GMT
ENV HY_VERSION=1.0a4
# Tue, 05 Apr 2022 15:48:36 GMT
ENV HYRULE_VERSION=0.1
# Tue, 05 Apr 2022 15:48:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 05 Apr 2022 15:48:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6202aa870befe19a5b6da7484e3ac1b39b0762008cbc7ed14e11815e9ac4668`  
		Last Modified: Tue, 05 Apr 2022 09:38:32 GMT  
		Size: 666.7 KB (666689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddafefb14b74461ca1bf1a35878b530925f060058a05b763aaf7b2e7f7e8c77`  
		Last Modified: Tue, 05 Apr 2022 09:39:17 GMT  
		Size: 12.3 MB (12276242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1227a5c81da2083bd8dd38c6c9e3b98905ddea32ab69edbae212dab3e3e0e152`  
		Last Modified: Tue, 05 Apr 2022 09:39:15 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72d23cf14026358f4ffeeefd1a2acf3753748a41bf0b7aad4a8b5d9edcbadd4`  
		Last Modified: Tue, 05 Apr 2022 09:39:16 GMT  
		Size: 2.9 MB (2871639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed27b22917a0d2fb2bca46a7ac30a887e6242315cbac9951972bf48bdce9d0c`  
		Last Modified: Tue, 05 Apr 2022 15:51:34 GMT  
		Size: 3.1 MB (3117936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.14` - linux; arm variant v6

```console
$ docker pull hylang@sha256:da67cd5acbd6ec90b0a50a55833b446dacc143044d5f3d35a60b5768af44a539
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21174110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a614d59132b435487caf594802c66af88169a9c7eace8ee403e042997b7efc2`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 08:03:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 08:03:43 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 08:03:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 08:03:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 05 Apr 2022 09:22:32 GMT
ENV PYTHON_VERSION=3.10.4
# Thu, 07 Apr 2022 03:43:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Thu, 07 Apr 2022 03:43:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Thu, 07 Apr 2022 03:43:54 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 07 Apr 2022 03:43:54 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 07 Apr 2022 03:43:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Thu, 07 Apr 2022 03:43:55 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Thu, 07 Apr 2022 03:44:14 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 07 Apr 2022 03:44:14 GMT
CMD ["python3"]
# Thu, 07 Apr 2022 05:45:23 GMT
ENV HY_VERSION=1.0a4
# Thu, 07 Apr 2022 05:45:24 GMT
ENV HYRULE_VERSION=0.1
# Thu, 07 Apr 2022 05:45:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 07 Apr 2022 05:45:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c092face47a2112c72860166b813286834ab14f8f92854ffc9f489eca2acbe8`  
		Last Modified: Tue, 05 Apr 2022 11:23:43 GMT  
		Size: 672.5 KB (672521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d30ac63b1967a1ac51a0a8cfbb86f360a01652f78e970242d9cc1270b4657df`  
		Last Modified: Thu, 07 Apr 2022 05:14:26 GMT  
		Size: 11.9 MB (11885381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a35b381d087d873752add3f9c8cac662bbf1605da484635dd58ce7a83711e3`  
		Last Modified: Thu, 07 Apr 2022 05:14:18 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42499ab71077efb5d240c11d3752040b9cd67854cae308d4e97cda2095406317`  
		Last Modified: Thu, 07 Apr 2022 05:14:21 GMT  
		Size: 2.9 MB (2871686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1140d418c093188e83670711dd47d0b95695a5f1e272ee3702865134e4d823`  
		Last Modified: Thu, 07 Apr 2022 05:50:43 GMT  
		Size: 3.1 MB (3118230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.14` - linux; arm variant v7

```console
$ docker pull hylang@sha256:68675be83b453f2603464572b1010c248013dac074375c0d44cad4ea95f49696
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20438201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8a5897816136af0ae1c70c84d0398b15d11e85e7f8257bf4deb320784307cb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 12:02:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 12:02:01 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 12:02:04 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 12:02:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 05 Apr 2022 13:19:58 GMT
ENV PYTHON_VERSION=3.10.4
# Tue, 05 Apr 2022 13:48:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 05 Apr 2022 13:49:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 05 Apr 2022 13:49:00 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 05 Apr 2022 13:49:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 05 Apr 2022 13:49:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 05 Apr 2022 13:49:02 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 05 Apr 2022 13:49:18 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 05 Apr 2022 13:49:18 GMT
CMD ["python3"]
# Wed, 06 Apr 2022 02:27:48 GMT
ENV HY_VERSION=1.0a4
# Wed, 06 Apr 2022 02:27:49 GMT
ENV HYRULE_VERSION=0.1
# Wed, 06 Apr 2022 02:27:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 06 Apr 2022 02:27:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3106007b2bf37305f1ef428030e7ce4df21b1481c0b001c8ff496c2177affc`  
		Last Modified: Tue, 05 Apr 2022 15:18:56 GMT  
		Size: 664.5 KB (664465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9cab0d795226a14fff10b3dcaa939483973519d07ed6ad2a32ee89eaf2009b`  
		Last Modified: Tue, 05 Apr 2022 15:20:32 GMT  
		Size: 11.4 MB (11355440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7d3f40351e9097fbc2f8ffabafc41fa4709923110ae1e5bd498fe360221f2f`  
		Last Modified: Tue, 05 Apr 2022 15:20:25 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7cfc5dcbd5bad765ec8de88e96507b89e43f8665f8525ccdac412cd6981980`  
		Last Modified: Tue, 05 Apr 2022 15:20:28 GMT  
		Size: 2.9 MB (2871817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4e97d5e1271b1ca8f540121467204cabd448dae6d15c68d956f5924a0e8c16`  
		Last Modified: Wed, 06 Apr 2022 02:37:05 GMT  
		Size: 3.1 MB (3118275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:3ab5590cfd5ef19f623515d538c71a698529152c06e32471067a94b83761aaee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21755887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98a6434ab516223d0191ee8f1df48bb3fed7a55854dcae09b386b4e676a230c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:07:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 05:07:01 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 05:07:03 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 05:07:04 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 05 Apr 2022 05:46:30 GMT
ENV PYTHON_VERSION=3.10.4
# Tue, 05 Apr 2022 06:01:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 05 Apr 2022 06:01:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 05 Apr 2022 06:01:12 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 05 Apr 2022 06:01:13 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 05 Apr 2022 06:01:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 05 Apr 2022 06:01:15 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 05 Apr 2022 06:01:22 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 05 Apr 2022 06:01:23 GMT
CMD ["python3"]
# Tue, 05 Apr 2022 17:30:50 GMT
ENV HY_VERSION=1.0a4
# Tue, 05 Apr 2022 17:30:50 GMT
ENV HYRULE_VERSION=0.1
# Tue, 05 Apr 2022 17:30:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 05 Apr 2022 17:30:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d5c20c24764c1957d965bf2629678511b31309d3e5bd85ee06a19e1df4b9eb`  
		Last Modified: Tue, 05 Apr 2022 06:42:15 GMT  
		Size: 668.3 KB (668287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b863495583594e7041638d1e495f58585c793141ef2b99f96027444caced7315`  
		Last Modified: Tue, 05 Apr 2022 06:43:11 GMT  
		Size: 12.4 MB (12382126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a99b8ed6cc7d32e4c458198a891408b30670b1354f726e840232446cf1840fb`  
		Last Modified: Tue, 05 Apr 2022 06:43:10 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3056c04a878a2ae853c52696cf60de26fa789e05c62e061430684707ff950636`  
		Last Modified: Tue, 05 Apr 2022 06:43:10 GMT  
		Size: 2.9 MB (2871525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2eba1bc8285ed6a1d66c7ce1486a34a157744bba76ca1bebd5377fbedae9ac`  
		Last Modified: Tue, 05 Apr 2022 17:36:06 GMT  
		Size: 3.1 MB (3116326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.14` - linux; 386

```console
$ docker pull hylang@sha256:dc9e7bd5eb4fff061ea7ad97f53240542428cdb83acf5f5780503f10ee587a7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21974423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179cddc0996ffcf0621ac6a8e8cb857b000aff7861a0a0a3663d30fc11435615`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:32 GMT
ADD file:6508514d43b69774a3307679ef8f6dba0faf707e62ad6c6c1c8cf40d84e12d1d in / 
# Mon, 04 Apr 2022 23:38:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:59:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 04:59:51 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 04:59:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 04:59:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 05 Apr 2022 05:31:06 GMT
ENV PYTHON_VERSION=3.10.4
# Thu, 07 Apr 2022 03:59:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Thu, 07 Apr 2022 03:59:11 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Thu, 07 Apr 2022 03:59:12 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 07 Apr 2022 03:59:13 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 07 Apr 2022 03:59:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Thu, 07 Apr 2022 03:59:15 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Thu, 07 Apr 2022 03:59:23 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 07 Apr 2022 03:59:24 GMT
CMD ["python3"]
# Thu, 07 Apr 2022 06:36:29 GMT
ENV HY_VERSION=1.0a4
# Thu, 07 Apr 2022 06:36:29 GMT
ENV HYRULE_VERSION=0.1
# Thu, 07 Apr 2022 06:36:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 07 Apr 2022 06:36:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c11e5e1035714514f6e237dffd1836a4d03b48af64e55a8e08f9bd9e998e24a9`  
		Last Modified: Mon, 04 Apr 2022 23:39:35 GMT  
		Size: 2.8 MB (2821213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215ecdd17ee697ca711b6420aaeee57970412708c0d0c25f8a6c10cf57f07002`  
		Last Modified: Tue, 05 Apr 2022 06:24:35 GMT  
		Size: 674.6 KB (674589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d945912e642f1d5aad6021300677669b792b231ec1610074cf0265edd1b07d3`  
		Last Modified: Thu, 07 Apr 2022 06:08:40 GMT  
		Size: 12.5 MB (12490589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3684401cb34c3397de8c4f5f784aaf7047cfadb34b8c9bd4a37c86a8e3be9b6b`  
		Last Modified: Thu, 07 Apr 2022 06:08:39 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47186a1aad7715801e6102f69d45b9c9a193b6ff5aa4ac7de34abc93ecb69dc0`  
		Last Modified: Thu, 07 Apr 2022 06:08:39 GMT  
		Size: 2.9 MB (2871478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6723a92a9d8a132b4e2880be95460b301bbd090bdf49dfc91abdda5c935ac2`  
		Last Modified: Thu, 07 Apr 2022 06:43:02 GMT  
		Size: 3.1 MB (3116322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.14` - linux; ppc64le

```console
$ docker pull hylang@sha256:a4a72afd60435bf666f16d91bab8df76768ac854d74a513f1697f357516c0349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22063230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67814525ce5d5d47bbffa9ebba8820f31640f3a33bd5134dbc5050d929cc7bba`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 16:34:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 16:34:31 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 16:34:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 16:34:41 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 05 Apr 2022 17:31:33 GMT
ENV PYTHON_VERSION=3.10.4
# Tue, 05 Apr 2022 17:52:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 05 Apr 2022 17:52:58 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 05 Apr 2022 17:53:02 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 05 Apr 2022 17:53:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 05 Apr 2022 17:53:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 05 Apr 2022 17:53:15 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 05 Apr 2022 17:53:35 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 05 Apr 2022 17:53:40 GMT
CMD ["python3"]
# Wed, 06 Apr 2022 03:16:25 GMT
ENV HY_VERSION=1.0a4
# Wed, 06 Apr 2022 03:16:28 GMT
ENV HYRULE_VERSION=0.1
# Wed, 06 Apr 2022 03:17:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 06 Apr 2022 03:17:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60ada6e38c11c96e48223b00e85ed8734a57312657ff8d2a373f5ec559b3aec`  
		Last Modified: Tue, 05 Apr 2022 19:05:40 GMT  
		Size: 676.4 KB (676427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f39238e740eb4f7b252204ed5a61077ab33fd79115956a22e8581e895eeea2e`  
		Last Modified: Tue, 05 Apr 2022 19:06:45 GMT  
		Size: 12.6 MB (12582108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f83b3757133a836a66df8852d19570613113e8956004ccc829bfd3f11610eb8`  
		Last Modified: Tue, 05 Apr 2022 19:06:42 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3315667575d014896e5e85409d2356a76effa590306b3e8c3a9448d409133e2d`  
		Last Modified: Tue, 05 Apr 2022 19:06:43 GMT  
		Size: 2.9 MB (2871766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7709fd93ba4e99a4e992bdee49abb7769ca90cf3557bade6eed5a6678f1c7526`  
		Last Modified: Wed, 06 Apr 2022 03:25:50 GMT  
		Size: 3.1 MB (3118527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.14` - linux; s390x

```console
$ docker pull hylang@sha256:de1c6fa9053e57a80688df7f2cfd5b2059c257f8e78943b6e121a08924427aee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21513185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401f95a090240f2900ad7e80c687b4ad0b9bf6392a698b1421bfc0bc9f3cf903`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:41:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 04:41:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 04:41:18 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 04:41:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 05 Apr 2022 05:09:55 GMT
ENV PYTHON_VERSION=3.10.4
# Thu, 07 Apr 2022 03:07:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Thu, 07 Apr 2022 03:07:13 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Thu, 07 Apr 2022 03:07:13 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Thu, 07 Apr 2022 03:07:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 07 Apr 2022 03:07:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Thu, 07 Apr 2022 03:07:14 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Thu, 07 Apr 2022 03:07:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 07 Apr 2022 03:07:20 GMT
CMD ["python3"]
# Thu, 07 Apr 2022 05:24:33 GMT
ENV HY_VERSION=1.0a4
# Thu, 07 Apr 2022 05:24:33 GMT
ENV HYRULE_VERSION=0.1
# Thu, 07 Apr 2022 05:24:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 07 Apr 2022 05:24:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d253464dc85c5cf8aa9aac3b36322787444bb45a3610d2ffc14ecfeaf8cff11`  
		Last Modified: Tue, 05 Apr 2022 05:59:14 GMT  
		Size: 672.5 KB (672460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6505679dd769731d2bfa23a44f209666b76134781509ab469658c6ebd6a69139`  
		Last Modified: Thu, 07 Apr 2022 04:51:40 GMT  
		Size: 12.2 MB (12246799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a877ae9eda36e5bba3cfcc2e3b53a59c3a42163583b5a5feec7a443bb4c515`  
		Last Modified: Thu, 07 Apr 2022 04:51:39 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4b7f58994e27093579a7b8482bedb215ce4db7087d6bd42b03534e098fe8ac`  
		Last Modified: Thu, 07 Apr 2022 04:51:39 GMT  
		Size: 2.9 MB (2871693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee30c94c14431fe789213d5ca9bdfda1f6cafb5c482f557bf6139108321f53a`  
		Last Modified: Thu, 07 Apr 2022 05:30:57 GMT  
		Size: 3.1 MB (3117925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
