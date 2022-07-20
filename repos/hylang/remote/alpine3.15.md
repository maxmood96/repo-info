## `hylang:alpine3.15`

```console
$ docker pull hylang@sha256:4c3de71e69e6c174198fe4c61777298f44c5940c688605b8d3145c3cc6f1d1c0
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

### `hylang:alpine3.15` - linux; amd64

```console
$ docker pull hylang@sha256:ae3fe6f73e969f67d1b9685d877e17d1792b212b8c3301e1596548573f185fb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22455888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6af62571b73b4686be1ecfd6131468c370435e219e08eedb28a62f7c51a538`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 00:55:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 00:55:49 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 00:55:50 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 20 Jul 2022 00:55:50 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 Jul 2022 01:15:10 GMT
ENV PYTHON_VERSION=3.10.5
# Wed, 20 Jul 2022 01:27:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 20 Jul 2022 01:27:15 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 20 Jul 2022 01:27:15 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 20 Jul 2022 01:27:16 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 20 Jul 2022 01:27:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Wed, 20 Jul 2022 01:27:16 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Wed, 20 Jul 2022 01:27:23 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 20 Jul 2022 01:27:23 GMT
CMD ["python3"]
# Wed, 20 Jul 2022 05:20:11 GMT
ENV HY_VERSION=0.24.0
# Wed, 20 Jul 2022 05:20:11 GMT
ENV HYRULE_VERSION=0.2
# Wed, 20 Jul 2022 05:20:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 20 Jul 2022 05:20:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104c00f00fd409ba0bcd53013de4550f2fa8c11643bf08c73bfe912dfaa7173f`  
		Last Modified: Wed, 20 Jul 2022 01:46:17 GMT  
		Size: 667.0 KB (667029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bb4199dd008e2d8181fc9170df6149312411b8ad72b2751ebabec1546b0c21`  
		Last Modified: Wed, 20 Jul 2022 01:46:40 GMT  
		Size: 12.2 MB (12249175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282d7b44528b2363df9590c02dfa89d03dc8c8e07641f9e99b04feadcbeedd4f`  
		Last Modified: Wed, 20 Jul 2022 01:46:38 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72eaecd995e7165a04a2bdc7e310fd9c109a1d235624018e46a0501f9fa82f22`  
		Last Modified: Wed, 20 Jul 2022 01:46:38 GMT  
		Size: 2.9 MB (2871726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f1f5aa0cb6c5baea603e60833c910f35b224b9dc0ab2566af76239171d91b81`  
		Last Modified: Wed, 20 Jul 2022 05:23:58 GMT  
		Size: 3.9 MB (3853081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.15` - linux; arm variant v6

```console
$ docker pull hylang@sha256:8790119119f5c5e79c18aecd74a14858eedcd423174d99976901714f22d0735e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23156652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d63fd7d1760178d30e125e3cafb8a840d7e61d170d971cf94411bceb95827c4`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 07:16:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 07:16:39 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 07:16:42 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 07:16:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 07 Jun 2022 19:39:46 GMT
ENV PYTHON_VERSION=3.10.5
# Tue, 07 Jun 2022 20:10:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 07 Jun 2022 20:10:33 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 07 Jun 2022 20:10:33 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 07 Jun 2022 20:10:34 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 07 Jun 2022 20:10:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Tue, 07 Jun 2022 20:10:34 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Tue, 07 Jun 2022 20:10:53 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 07 Jun 2022 20:10:54 GMT
CMD ["python3"]
# Thu, 23 Jun 2022 19:51:09 GMT
ENV HY_VERSION=0.24.0
# Thu, 23 Jun 2022 19:51:10 GMT
ENV HYRULE_VERSION=0.2
# Thu, 23 Jun 2022 19:52:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 23 Jun 2022 19:52:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c148f0a21858ba6d892e5c2be6f7a4cdc7017f1eb8f0dfe07a2aa14cdcf6d2`  
		Last Modified: Tue, 05 Apr 2022 11:23:18 GMT  
		Size: 672.6 KB (672638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bed3099c2a9c4f0f3ea0f090e616727c745fb188a97f966e8c2a9d697332398`  
		Last Modified: Tue, 07 Jun 2022 20:15:36 GMT  
		Size: 13.1 MB (13136569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c321a596dcbf0e16d485f40da1b5b34c1683d86402aad557eca2d1203f13fde4`  
		Last Modified: Tue, 07 Jun 2022 20:15:28 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ca899865506ad8da06e6217b7015da9495ba1bd0b146010efb231938ff2086`  
		Last Modified: Tue, 07 Jun 2022 20:15:30 GMT  
		Size: 2.9 MB (2871800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9948a40019cbc28aa0181cd7826e2191a27bb13fc068ca32111c8be36880fa`  
		Last Modified: Thu, 23 Jun 2022 19:58:39 GMT  
		Size: 3.9 MB (3853442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.15` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c0610391f598b1eb7c0e8fc92d8b62a5a1d105586e6a41e38dd986eb8b502bfa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22332823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f59f40c69a09a970b70c0c1336fe1ee921e678bd21de4b81f91d6d8f7b2538d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 11:15:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 11:15:50 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 11:15:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 11:15:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 07 Jun 2022 21:59:34 GMT
ENV PYTHON_VERSION=3.10.5
# Tue, 07 Jun 2022 22:33:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 07 Jun 2022 22:33:53 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 07 Jun 2022 22:33:54 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 07 Jun 2022 22:33:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 07 Jun 2022 22:33:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Tue, 07 Jun 2022 22:33:56 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Tue, 07 Jun 2022 22:34:17 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 07 Jun 2022 22:34:18 GMT
CMD ["python3"]
# Sat, 25 Jun 2022 06:21:48 GMT
ENV HY_VERSION=0.24.0
# Sat, 25 Jun 2022 06:21:48 GMT
ENV HYRULE_VERSION=0.2
# Sat, 25 Jun 2022 06:22:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 25 Jun 2022 06:22:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5594b60729afc7fdfa6de04dfddfc5560d7ca2510331911a8b6c27a5fd65f469`  
		Last Modified: Tue, 05 Apr 2022 15:18:31 GMT  
		Size: 664.5 KB (664505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8499b49b080305990d68b565a5d2c7e8194360aa589909ed2f44a3ddb747d9`  
		Last Modified: Tue, 07 Jun 2022 22:48:08 GMT  
		Size: 12.5 MB (12518707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2d1df707b3059f6662654ca0987bce78c26e5a325e26a3f286a36c852418c0`  
		Last Modified: Tue, 07 Jun 2022 22:48:03 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcad617cbc89d4143e6627a4c3dbf92178675c4df7e3dcf247708fea51cc2d0`  
		Last Modified: Tue, 07 Jun 2022 22:48:05 GMT  
		Size: 2.9 MB (2871698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbf190fc151152a4c121b007abb1f8d486822e610ad7fa87c6b0692a7da0e0d`  
		Last Modified: Sat, 25 Jun 2022 06:39:23 GMT  
		Size: 3.9 MB (3853358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:022652e43f2dde755e208dd789133d66f5c1e4bf1aedc6e427649da0453f6c33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23855254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa022df8298886d03d8f0732a7066ad9e056393992f587289ad7edabb27b66`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 04:43:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 04:43:56 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 04:43:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 04:43:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 07 Jun 2022 19:54:02 GMT
ENV PYTHON_VERSION=3.10.5
# Tue, 07 Jun 2022 20:08:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 07 Jun 2022 20:08:17 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 07 Jun 2022 20:08:18 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 07 Jun 2022 20:08:19 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 07 Jun 2022 20:08:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Tue, 07 Jun 2022 20:08:21 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Tue, 07 Jun 2022 20:08:29 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 07 Jun 2022 20:08:30 GMT
CMD ["python3"]
# Thu, 23 Jun 2022 23:46:14 GMT
ENV HY_VERSION=0.24.0
# Thu, 23 Jun 2022 23:46:15 GMT
ENV HYRULE_VERSION=0.2
# Thu, 23 Jun 2022 23:46:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 23 Jun 2022 23:46:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c8fe6b300068ece063b73d7ea69bef331e0698246ebbe2abe966cf6685e1ef`  
		Last Modified: Tue, 05 Apr 2022 06:41:57 GMT  
		Size: 668.4 KB (668392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b274a401d241eaa5acfaa5c414e1115b1fc7d896298fef00b5b9fa9b208c1d4`  
		Last Modified: Tue, 07 Jun 2022 20:15:27 GMT  
		Size: 13.7 MB (13747857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03fb4869011a9fbae542404f97730a5bdc6994b96d94cfdd478526837d6c20e`  
		Last Modified: Tue, 07 Jun 2022 20:15:25 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f974ae2512775846e3e8ec579e5dea4a4f0dc964c79d4a96ab64cb92c41df7d3`  
		Last Modified: Tue, 07 Jun 2022 20:15:25 GMT  
		Size: 2.9 MB (2871492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dad45fba3eecf76cd5951c9d049f6e334e79dda32cc70dcc24f93f491ccf695`  
		Last Modified: Fri, 24 Jun 2022 00:00:44 GMT  
		Size: 3.9 MB (3850804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.15` - linux; 386

```console
$ docker pull hylang@sha256:1ffa50d3fc32adda9e9d98cada4c9af5c37abb963e3212557e89baac8d8e4824
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22677650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a495f355d9c8933957f59674d21be0d7cdc1fc129d52c85d946d0712c00255c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 19 Jul 2022 22:38:32 GMT
ADD file:3c11e12b5c10a13cce2dec1d5ae8d7c6a61e0ccc2b4b44b6cf5b80b97eed9869 in / 
# Tue, 19 Jul 2022 22:38:32 GMT
CMD ["/bin/sh"]
# Wed, 20 Jul 2022 01:05:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Jul 2022 01:05:30 GMT
ENV LANG=C.UTF-8
# Wed, 20 Jul 2022 01:05:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 20 Jul 2022 01:05:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 Jul 2022 01:25:03 GMT
ENV PYTHON_VERSION=3.10.5
# Wed, 20 Jul 2022 01:37:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 20 Jul 2022 01:37:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 20 Jul 2022 01:37:06 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 20 Jul 2022 01:37:07 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 20 Jul 2022 01:37:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Wed, 20 Jul 2022 01:37:09 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Wed, 20 Jul 2022 01:37:17 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 20 Jul 2022 01:37:18 GMT
CMD ["python3"]
# Wed, 20 Jul 2022 03:30:14 GMT
ENV HY_VERSION=0.24.0
# Wed, 20 Jul 2022 03:30:15 GMT
ENV HYRULE_VERSION=0.2
# Wed, 20 Jul 2022 03:30:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 20 Jul 2022 03:30:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8bbe360ea5d414165050aeceb6ca82ed372606830e0addd5df0d1000146ab250`  
		Last Modified: Tue, 19 Jul 2022 22:39:24 GMT  
		Size: 2.8 MB (2819359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fad5fdc3628ec3ae8e826916d0011c98c35fdae07ae64520a9a3abb5e03a8c`  
		Last Modified: Wed, 20 Jul 2022 01:59:58 GMT  
		Size: 674.8 KB (674836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8256bcd1973120bf361920ec0ecfdadbaf47359c54837b1b9ae14caee642fe`  
		Last Modified: Wed, 20 Jul 2022 02:00:35 GMT  
		Size: 12.5 MB (12460874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3bbdda5532881fa472e6f97b16bd30beb8f032971d437ed243eb01862c68c1`  
		Last Modified: Wed, 20 Jul 2022 02:00:33 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a096bcbfb54b38059a35a8a673784980fc0a837d69306726b29311bd7f2efe5b`  
		Last Modified: Wed, 20 Jul 2022 02:00:33 GMT  
		Size: 2.9 MB (2871509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285c505f78161faab9b16a50233246b0b9f7b288ff33298b8ada773c0aa25cf`  
		Last Modified: Wed, 20 Jul 2022 03:38:00 GMT  
		Size: 3.9 MB (3850837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.15` - linux; ppc64le

```console
$ docker pull hylang@sha256:54041fdb392fe952eb1376d670319d60b0686ccdaed22f96ebd208f65470c536
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24211971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2dd7df9239308f54097445998d004ac805d5ba230b302eaebc31514c637f1c9`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:30 GMT
ADD file:960cf6f9d3d1cfcb36c2d67dd4c3eaba7db1d0c7afe97968512248d7f234ad47 in / 
# Tue, 05 Apr 2022 00:23:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 16:00:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 16:00:44 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 16:00:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 05 Apr 2022 16:00:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 07 Jun 2022 20:36:16 GMT
ENV PYTHON_VERSION=3.10.5
# Tue, 07 Jun 2022 20:58:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 07 Jun 2022 20:58:16 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 07 Jun 2022 20:58:25 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 07 Jun 2022 20:58:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 07 Jun 2022 20:58:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Tue, 07 Jun 2022 20:58:47 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Tue, 07 Jun 2022 20:59:17 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 07 Jun 2022 20:59:22 GMT
CMD ["python3"]
# Fri, 24 Jun 2022 19:05:00 GMT
ENV HY_VERSION=0.24.0
# Fri, 24 Jun 2022 19:05:05 GMT
ENV HYRULE_VERSION=0.2
# Fri, 24 Jun 2022 19:06:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 24 Jun 2022 19:06:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1877acf2d48ed8bcb5bd9756a95aca0c077457be7cf4fcef25807f4e9be88db1`  
		Last Modified: Mon, 04 Apr 2022 19:09:49 GMT  
		Size: 2.8 MB (2811186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383b0511332251ebc07b3b84ac239f2c956371bd46dbe7229965dd10db503224`  
		Last Modified: Tue, 05 Apr 2022 19:05:19 GMT  
		Size: 676.5 KB (676534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43e5b7376c2b4f4031b29ecf7ee4d922b9e5851a24de0daf429a74a3ab800322`  
		Last Modified: Tue, 07 Jun 2022 21:07:29 GMT  
		Size: 14.0 MB (13998385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c30d989c217b126581de6fc2d192a41f5c592c37b9b06c1cac27f7566c1b944`  
		Last Modified: Tue, 07 Jun 2022 21:07:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ad66316d6adbbed04382cec8dde3cc7c119207e084d40c59bfa20bf380bc2e`  
		Last Modified: Tue, 07 Jun 2022 21:07:27 GMT  
		Size: 2.9 MB (2871709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed76f40446600bc81b11f8b41630ae0ff194b8fe32cd4cf80a2e087898e27f75`  
		Last Modified: Fri, 24 Jun 2022 19:24:06 GMT  
		Size: 3.9 MB (3853926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.15` - linux; s390x

```console
$ docker pull hylang@sha256:4b7c6ed79ed63c38fa70b248c156c36ccc8a6fe4b3af0aa810f8fc27e05064d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22206734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2351484c2785462279d938be8d733ea7d2726b8be7a58637546c00def53a7a2`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 19 Jul 2022 22:41:55 GMT
ADD file:9671b14d87fd7602279c1b3d1148babaa2c411e4ab0570d294d95324fa19210c in / 
# Tue, 19 Jul 2022 22:41:56 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 23:43:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 23:43:39 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 23:43:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 23:43:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 Jul 2022 00:08:24 GMT
ENV PYTHON_VERSION=3.10.5
# Wed, 20 Jul 2022 00:28:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 20 Jul 2022 00:28:41 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 20 Jul 2022 00:28:43 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 20 Jul 2022 00:28:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 20 Jul 2022 00:28:44 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Wed, 20 Jul 2022 00:28:45 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Wed, 20 Jul 2022 00:28:54 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 20 Jul 2022 00:28:57 GMT
CMD ["python3"]
# Wed, 20 Jul 2022 06:29:26 GMT
ENV HY_VERSION=0.24.0
# Wed, 20 Jul 2022 06:29:26 GMT
ENV HYRULE_VERSION=0.2
# Wed, 20 Jul 2022 06:29:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 20 Jul 2022 06:29:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ef614dc1febe442e84bcc0f287628aea0f6547a0f322d7bed0a46ffabd5e0a50`  
		Last Modified: Tue, 19 Jul 2022 22:43:17 GMT  
		Size: 2.6 MB (2600789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419e43a45321b88539b62ef9c20295d0aca1152bc94775af95b63fa6b9492b1c`  
		Last Modified: Wed, 20 Jul 2022 01:00:34 GMT  
		Size: 672.6 KB (672592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce0914a684026d73142fb3ba70b006cb656802826e5fb36f2d8b9366f775214`  
		Last Modified: Wed, 20 Jul 2022 01:01:13 GMT  
		Size: 12.2 MB (12208528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4bcc4743bc72bbef6c82ad0ce13e209e9183d25d86f5977fa02ed20b2ddd0`  
		Last Modified: Wed, 20 Jul 2022 01:01:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5e987af1977cf25f16ff2fa9881add656e0696c33a90bbeec3a8d7ddd1647a4`  
		Last Modified: Wed, 20 Jul 2022 01:01:12 GMT  
		Size: 2.9 MB (2871711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a000c9a996c386347d5e6fba4620a9649e4efe5771d1a70dbcde16624e4587`  
		Last Modified: Wed, 20 Jul 2022 06:36:55 GMT  
		Size: 3.9 MB (3852885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
