## `hylang:python3.10-alpine3.16`

```console
$ docker pull hylang@sha256:8385b889b0a90831c15e06513c94644a512cede80fd9c9d1bceb513b5d4222ce
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

### `hylang:python3.10-alpine3.16` - linux; amd64

```console
$ docker pull hylang@sha256:3c19517f079e8aaf570312f403f3e67d108e10e96f4cafe9ac935fad5d981fc2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24810271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d81fcffb4fdefd26f6f9119d613c9560de07847d4eb50f5cdc8ebdc86faf2d`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:56:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:39:07 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:39:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:57:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Feb 2023 02:11:15 GMT
ENV PYTHON_VERSION=3.10.10
# Thu, 09 Feb 2023 02:20:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Thu, 09 Feb 2023 02:20:42 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 09 Feb 2023 02:20:42 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 09 Feb 2023 02:20:42 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 09 Feb 2023 02:20:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Thu, 09 Feb 2023 02:20:42 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Thu, 09 Feb 2023 02:20:49 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 09 Feb 2023 02:20:49 GMT
CMD ["python3"]
# Thu, 09 Feb 2023 02:53:40 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 02:53:41 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 02:53:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 02:53:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e124a36b9ab9caae9b9b43bffcb6f6d9f126ab89cf2a8b20b9a6f912df03d36`  
		Last Modified: Sat, 12 Nov 2022 07:47:59 GMT  
		Size: 661.8 KB (661831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd71263ccb2dea1d6e07966a253c68d4850ffbddcc4868195354f06efdb3b94`  
		Last Modified: Thu, 09 Feb 2023 02:27:32 GMT  
		Size: 14.2 MB (14165311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08ec9473861e220fec3de6abdbbd30f081fe36db9be02a40e93526a116163d8`  
		Last Modified: Thu, 09 Feb 2023 02:27:30 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bb172450832d4b682c9b0b9d9ce19023b7e8956900eb23f72d66722701357a`  
		Last Modified: Thu, 09 Feb 2023 02:27:31 GMT  
		Size: 3.1 MB (3056455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dea77eafffc8a2b989d359bab2907d379883b5c8538e42c912f3e480891b56a`  
		Last Modified: Thu, 09 Feb 2023 03:06:06 GMT  
		Size: 4.1 MB (4120174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.16` - linux; arm variant v6

```console
$ docker pull hylang@sha256:85ba42678b84fc4a43379aaf63239b18f5fa5ff074422a8645e1fba917da32a3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24099787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493ecb3423c764bfcd30d332662ae43bc00fa67a0bf3b6876df20b53ad64ce72`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 12 Nov 2022 03:49:18 GMT
ADD file:493290ed8856fa13463defe63da0d30ab3de5dde042c87ef7c0701d66ebb8892 in / 
# Sat, 12 Nov 2022 03:49:18 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:28:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 06:28:49 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 06:28:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 06:55:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Feb 2023 01:25:59 GMT
ENV PYTHON_VERSION=3.10.10
# Thu, 09 Feb 2023 01:39:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Thu, 09 Feb 2023 01:39:18 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 09 Feb 2023 01:39:18 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 09 Feb 2023 01:39:18 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 09 Feb 2023 01:39:18 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Thu, 09 Feb 2023 01:39:18 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Thu, 09 Feb 2023 01:39:27 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 09 Feb 2023 01:39:27 GMT
CMD ["python3"]
# Thu, 09 Feb 2023 02:10:33 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 02:10:33 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 02:10:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 02:10:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9616ea8c1de4a90b1a50591336485e88ae5c2346e0d778bdbe69b00647bf8e39`  
		Last Modified: Sat, 12 Nov 2022 03:50:12 GMT  
		Size: 2.6 MB (2615105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe974d15ab7b1ace1e4997a68bcfb22f2652af9f902f110d0a90fbdd2ef2053`  
		Last Modified: Sat, 12 Nov 2022 08:03:00 GMT  
		Size: 666.2 KB (666196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1b76274a5a37e5b5f3f66922954d60cf2113672545a99aa3ba0375af28c262`  
		Last Modified: Thu, 09 Feb 2023 01:53:22 GMT  
		Size: 13.6 MB (13644350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be900e4ea3ed4e7f22005387ef869bafd3541d26a550b9ef3c4e4a13a04910a3`  
		Last Modified: Thu, 09 Feb 2023 01:53:19 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6849dccdcf323f429a661c47b70fdff1499606b263e1772717bd804d78f74e0b`  
		Last Modified: Thu, 09 Feb 2023 01:53:20 GMT  
		Size: 3.1 MB (3056223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd18562c2aadf551fcacc68d229336509fca788b070818db9b6b3bdf9064eb55`  
		Last Modified: Thu, 09 Feb 2023 02:18:58 GMT  
		Size: 4.1 MB (4117682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.16` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c9d26df943e6e73a02ccc4933d3e90e63742a8813bfe5f1145fef1e64cbc704e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22000153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769f77ff2a3fcade6aea9b2dd1f264ae4516b3b3563d135c541dd78a5dec7fa0`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 12 Nov 2022 03:57:24 GMT
ADD file:0b4a628f529226f5ec9d357ca63138bd2d22411a889c780ac8d395d761e07b2c in / 
# Sat, 12 Nov 2022 03:57:24 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 08:12:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:12:04 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:12:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:38:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 08 Dec 2022 03:40:11 GMT
ENV PYTHON_VERSION=3.10.9
# Sat, 04 Feb 2023 05:07:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 04 Feb 2023 05:07:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 04 Feb 2023 05:07:03 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Sat, 04 Feb 2023 05:07:04 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 04 Feb 2023 05:07:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Sat, 04 Feb 2023 05:07:04 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Sat, 04 Feb 2023 05:07:11 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Sat, 04 Feb 2023 05:07:11 GMT
CMD ["python3"]
# Sat, 04 Feb 2023 09:26:56 GMT
ENV HY_VERSION=0.25.0
# Sat, 04 Feb 2023 09:26:56 GMT
ENV HYRULE_VERSION=0.2.1
# Sat, 04 Feb 2023 09:27:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 04 Feb 2023 09:27:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e44ba29d168a7f7c9e914f3724614df9e070aa6ef9b9ba5c9004db3c071f403a`  
		Last Modified: Sat, 12 Nov 2022 03:58:16 GMT  
		Size: 2.4 MB (2418788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb04c1ebc7f7005f359b85d4698d031de9ca4a4e8bc776ac6faa3f052b3a3f1`  
		Last Modified: Sat, 12 Nov 2022 10:03:05 GMT  
		Size: 659.3 KB (659291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c339a9a3582618f3003e15e47123de8337ff90bab8b98d9ab50d1f282329b9dd`  
		Last Modified: Sat, 04 Feb 2023 06:50:12 GMT  
		Size: 11.7 MB (11734046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f321f95adc87e1f08ca5af39c762d03a72ff72ead49ac67ba157eb77e83177`  
		Last Modified: Sat, 04 Feb 2023 06:50:09 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94a423be252785064c203e622e8a39bb7a44f53460d9cfa7d621c3e9cc90a39`  
		Last Modified: Sat, 04 Feb 2023 06:50:10 GMT  
		Size: 3.1 MB (3056302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd0d56d84e208ac1a097c8fd664ce68ef036c08300d4cb972c9c621d4b1974`  
		Last Modified: Sat, 04 Feb 2023 09:41:16 GMT  
		Size: 4.1 MB (4131496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:942000b14d6a2d779a6d0b3724c5466d71969b794a9dd0cdb12dc83765ad74f1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24725536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e1cd00d06d8aea4f269ef75ac6910d1d19af852c5de6b68d5a22d745017d7d`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 12 Nov 2022 03:39:38 GMT
ADD file:57d621536158358b14d15155826ef2dd4ca034278044111ec0aaf6717016e569 in / 
# Sat, 12 Nov 2022 03:39:38 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:23:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 08:16:58 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 08:16:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 08:35:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Feb 2023 02:47:26 GMT
ENV PYTHON_VERSION=3.10.10
# Thu, 09 Feb 2023 02:57:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Thu, 09 Feb 2023 02:57:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 09 Feb 2023 02:57:01 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 09 Feb 2023 02:57:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 09 Feb 2023 02:57:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Thu, 09 Feb 2023 02:57:02 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Thu, 09 Feb 2023 02:57:07 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 09 Feb 2023 02:57:07 GMT
CMD ["python3"]
# Thu, 09 Feb 2023 03:25:24 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 03:25:24 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 03:25:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 03:25:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6875df1f535433e5affe18ecfde9acb7950ab5f76887980ff06c5cdd48cf98f4`  
		Last Modified: Sat, 12 Nov 2022 03:40:05 GMT  
		Size: 2.7 MB (2707756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e190eeb0612a6514b857c64886ec8f64d8e235210be5682cf6abbc5bd172b135`  
		Last Modified: Sat, 12 Nov 2022 09:21:43 GMT  
		Size: 663.1 KB (663101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f940b038002c5cf439efc1307784fb438d7167203cffb0e18ce37638e64de3`  
		Last Modified: Thu, 09 Feb 2023 03:04:12 GMT  
		Size: 14.2 MB (14177702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6803f6eedee6cf0ef4284e43d25309db8d51adf6c2a2e188310a1f99a02c2f97`  
		Last Modified: Thu, 09 Feb 2023 03:04:10 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5722f921ed00882edfa8edd608246eb7d2ee0fb45247aec9f0f149449f2b10ed`  
		Last Modified: Thu, 09 Feb 2023 03:04:11 GMT  
		Size: 3.1 MB (3056495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f1627a55f8d224a3efba6a1232dc05a8361698a11b47aec416a479e2cbe9a5`  
		Last Modified: Thu, 09 Feb 2023 03:37:06 GMT  
		Size: 4.1 MB (4120251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.16` - linux; 386

```console
$ docker pull hylang@sha256:7e1f2328a7b4d013af30310d92de93a370cf9ff0327e75b52006fe0e447df2c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23419842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3926b7d07e63fc44bc4609b218dd0bfe2b9a0965f0254e14f6436fd7ae9bce`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 05:29:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 05:29:12 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 05:29:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 05:50:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 08 Dec 2022 02:30:53 GMT
ENV PYTHON_VERSION=3.10.9
# Sat, 04 Feb 2023 03:42:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 04 Feb 2023 03:42:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 04 Feb 2023 03:42:27 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Sat, 04 Feb 2023 03:42:28 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 04 Feb 2023 03:42:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Sat, 04 Feb 2023 03:42:30 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Sat, 04 Feb 2023 03:42:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Sat, 04 Feb 2023 03:42:38 GMT
CMD ["python3"]
# Sat, 04 Feb 2023 07:29:10 GMT
ENV HY_VERSION=0.25.0
# Sat, 04 Feb 2023 07:29:11 GMT
ENV HYRULE_VERSION=0.2.1
# Sat, 04 Feb 2023 07:29:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 04 Feb 2023 07:29:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a152a67ad9fd5011f8da356e104e14cdbd9cd925941bb6c241b50471eef5a520`  
		Last Modified: Sat, 12 Nov 2022 06:51:44 GMT  
		Size: 669.6 KB (669609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9e1d061939a7ccc68c1808442c3d8d3598967b5ae7487a147f8ebeb651bd46`  
		Last Modified: Sat, 04 Feb 2023 05:13:05 GMT  
		Size: 12.8 MB (12755962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217183889ac4d4b457e6b293d39127c90aa7bc2a98462fdc9a3f0651c1049da0`  
		Last Modified: Sat, 04 Feb 2023 05:13:03 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fd7aefd6d16ff7ba72687cfbb98db8b0c2e9facbc7d3dd64cf2ad2b312436e`  
		Last Modified: Sat, 04 Feb 2023 05:13:04 GMT  
		Size: 3.1 MB (3054256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a7e5f934f585a09b222d8d5d53b6eb315011e4a8870bce7bf6b662a2cb759dc`  
		Last Modified: Sat, 04 Feb 2023 07:43:34 GMT  
		Size: 4.1 MB (4131436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.16` - linux; ppc64le

```console
$ docker pull hylang@sha256:05741cd6aa436a63d16f88d66b94dbceaef11b234b8c179c5f62839f64ce877c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23514003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c1637a8b4895d050e1b0405689e66a8c3dabc8563826b8341616e619c14b6f`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 09:09:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 09:09:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 09:09:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 09:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 08 Dec 2022 05:07:46 GMT
ENV PYTHON_VERSION=3.10.9
# Sat, 04 Feb 2023 06:46:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 04 Feb 2023 06:46:57 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 04 Feb 2023 06:46:58 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Sat, 04 Feb 2023 06:46:59 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 04 Feb 2023 06:46:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Sat, 04 Feb 2023 06:46:59 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Sat, 04 Feb 2023 06:47:10 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Sat, 04 Feb 2023 06:47:11 GMT
CMD ["python3"]
# Sat, 04 Feb 2023 09:19:10 GMT
ENV HY_VERSION=0.25.0
# Sat, 04 Feb 2023 09:19:10 GMT
ENV HYRULE_VERSION=0.2.1
# Sat, 04 Feb 2023 09:19:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 04 Feb 2023 09:19:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0578c681eac19aa83cc60a5d383147a7c56a35a3ac13286945daa470f25157e`  
		Last Modified: Sat, 12 Nov 2022 11:31:49 GMT  
		Size: 670.3 KB (670297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5d89a32ed85b89d1eba56e19c3d908fe19a875b6b5b6097d09aa39bca625a0`  
		Last Modified: Sat, 04 Feb 2023 08:12:41 GMT  
		Size: 12.9 MB (12851536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e12ef241386a9abf61c2be69267812cec58457ded0fedc3a8728b042e1051a5`  
		Last Modified: Sat, 04 Feb 2023 08:12:38 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b542bb923c02404cdbfb70ae43cdde21edc9bb6885e174082ac05a0d92ac063c`  
		Last Modified: Sat, 04 Feb 2023 08:12:39 GMT  
		Size: 3.1 MB (3056488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa7b3b4beffc953d5f3ddbd27094ab8291be05f635ce7776cb398f76f783b3d`  
		Last Modified: Sat, 04 Feb 2023 09:31:56 GMT  
		Size: 4.1 MB (4133891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-alpine3.16` - linux; s390x

```console
$ docker pull hylang@sha256:196b6a8ba7bad29328f443f0ae695f472f8c195e497f2b65818c00aa5f64c4a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24400178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49b4574b5a42a6451683884465f2f28164f6d5f4694b9c6cd3a1012fcf81f6b`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 12 Nov 2022 03:42:05 GMT
ADD file:b78ae95cbacd853e398f187adaf3be51d9e301a66de8f7a4b6c60a9733075cb5 in / 
# Sat, 12 Nov 2022 03:42:06 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:00:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 12 Nov 2022 07:00:48 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 07:00:49 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 12 Nov 2022 07:20:25 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Feb 2023 01:37:10 GMT
ENV PYTHON_VERSION=3.10.10
# Thu, 09 Feb 2023 01:46:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Thu, 09 Feb 2023 01:46:58 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Thu, 09 Feb 2023 01:46:58 GMT
ENV PYTHON_PIP_VERSION=22.3.1
# Thu, 09 Feb 2023 01:46:58 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 09 Feb 2023 01:46:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1a96dc5acd0303c4700e02655aefd3bc68c78958/public/get-pip.py
# Thu, 09 Feb 2023 01:46:59 GMT
ENV PYTHON_GET_PIP_SHA256=d1d09b0f9e745610657a528689ba3ea44a73bd19c60f4c954271b790c71c2653
# Thu, 09 Feb 2023 01:47:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Thu, 09 Feb 2023 01:47:06 GMT
CMD ["python3"]
# Thu, 09 Feb 2023 02:21:52 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 02:21:53 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 02:22:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 02:22:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cff16a5ffe2df97bc1d10b021c5ceb98bdb36a18a1d70395590444ac204a9b2b`  
		Last Modified: Sat, 12 Nov 2022 03:43:06 GMT  
		Size: 2.6 MB (2591126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5323c5f174ca07f8bb576c8d074a71044032b97762887d3e339d13ee241569b9`  
		Last Modified: Sat, 12 Nov 2022 08:14:42 GMT  
		Size: 666.6 KB (666646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47d21c9eb70c8fc10c8e977a80f53a4754f3055f20d623a2688ee2d0842d3ce`  
		Last Modified: Thu, 09 Feb 2023 01:54:17 GMT  
		Size: 14.0 MB (13965496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99ab795c74876c20ce0e461f1f2e533fa61221eaf4eccecae48c84e6fa48365`  
		Last Modified: Thu, 09 Feb 2023 01:54:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713b9a285d97ebc104d5152ab55c747039f2008c356f687d75e730d97e61bef2`  
		Last Modified: Thu, 09 Feb 2023 01:54:16 GMT  
		Size: 3.1 MB (3056423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4f3a23e9c9d32cb36dd9121bca3974503216f8ee1d84456c30775f725ba4ba`  
		Last Modified: Thu, 09 Feb 2023 02:32:25 GMT  
		Size: 4.1 MB (4120258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
