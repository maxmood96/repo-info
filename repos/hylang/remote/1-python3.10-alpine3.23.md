## `hylang:1-python3.10-alpine3.23`

```console
$ docker pull hylang@sha256:67ef56ead621c3d185090d05843278de072cf3ef5bde58d4e269a3969a9fb558
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

### `hylang:1-python3.10-alpine3.23` - linux; amd64

```console
$ docker pull hylang@sha256:ff0d1695126bac7e000d63395621405f2d540807908edbb0465de6928195871c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24894814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:246d3cd26878647faebd1d472a20e85fe054f919252575577b7b56ddfe85a194`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:25:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:25:31 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:25:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:25:31 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:25:31 GMT
ENV PYTHON_VERSION=3.10.20
# Tue, 03 Mar 2026 20:25:31 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Tue, 03 Mar 2026 20:28:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:28:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:28:28 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 21:07:35 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 21:07:35 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 21:07:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 21:07:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d02280b920b7fc9c227d58c8363d587963dd235bff43ea21360af50909dee`  
		Last Modified: Tue, 03 Mar 2026 20:28:34 GMT  
		Size: 460.9 KB (460928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7bc9bb8e807d50a5e2ca322a25ca793a856c5647f581a7ced56e6350f8f36a`  
		Last Modified: Tue, 03 Mar 2026 20:28:35 GMT  
		Size: 15.5 MB (15453180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3936a345a388bee4c24bf52d44fdac6b439653e1ffd6f5166ea8d99d59cf2f`  
		Last Modified: Tue, 03 Mar 2026 20:28:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ce857065f91dbd7ffaee1f10edc7fac20110e3e9ab91ae02304c759b9f050a`  
		Last Modified: Tue, 03 Mar 2026 21:07:41 GMT  
		Size: 5.1 MB (5118637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:4e1a182b0ccee6b1a8a15cf474b0c1acede8c4cde9200294446b763dcbe21511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.4 KB (709373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3dd2d777a0bbfbc0dde20c57a32daa7992c9f66adea9622e123a65f12637d1`

```dockerfile
```

-	Layers:
	-	`sha256:5f8afe3c97c7f989932d281f105e0b0a82ddfa0bad273e91d553967bba0b680e`  
		Last Modified: Tue, 03 Mar 2026 21:07:41 GMT  
		Size: 700.0 KB (699966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb6eb0183da4b8da40aee503d0abd610f1e86dca8083edd9d87012f66d5fbc5`  
		Last Modified: Tue, 03 Mar 2026 21:07:41 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.23` - linux; arm variant v6

```console
$ docker pull hylang@sha256:40ff21766a4a2d633e90c32c97f19790bfb7472762d5f76b5821eb0198af1208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24198978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111aeec8bc96814766e16732d1b5311ae741790f4e704cbc5fef395f60e02800`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:12:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:12:36 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:12:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:12:36 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:12:36 GMT
ENV PYTHON_VERSION=3.10.20
# Tue, 03 Mar 2026 20:12:36 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Tue, 03 Mar 2026 20:23:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:23:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:23:52 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 20:57:38 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 20:57:38 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 20:57:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 20:57:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01287a9cb556469c4385d00cb1c38f35bae8529c263c68ebfcd6e4258f2deb55`  
		Last Modified: Tue, 03 Mar 2026 20:19:44 GMT  
		Size: 461.4 KB (461441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878061a10a556cde2e0e82033494ee86a9a0773ab795e638268dd70f7e8d4d1c`  
		Last Modified: Tue, 03 Mar 2026 20:23:57 GMT  
		Size: 15.0 MB (15048702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe4755778a15875d881463c3504160f9c859ff28c5afe8aeb3d88e7359e1bb6`  
		Last Modified: Tue, 03 Mar 2026 20:23:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6f72f54c85bcca940211d13cf7c7dbb9de36ae6bb4ecd2167e8f6af6562d3f`  
		Last Modified: Tue, 03 Mar 2026 20:57:43 GMT  
		Size: 5.1 MB (5118764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:d6cefb75789723bf621040e243c88a04ca127ee59324dc4496742fe9d82d3e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3b79c60caebf1af7447d833731c92653912421b7846f5a890345002c3c8d3f`

```dockerfile
```

-	Layers:
	-	`sha256:a3ddb2a962ff35f9948a54eaa0fff9021cfb8e940f082a0fce1bf17d4be16809`  
		Last Modified: Tue, 03 Mar 2026 20:57:42 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.23` - linux; arm variant v7

```console
$ docker pull hylang@sha256:7bf24d309cb67965038b4583e8cd1a4e0f818d274dc06b55f21fb9ec6dddd673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23494745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281938757382264d42225273f84cdecff170a95f5822798da39f87aee681448a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:48:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:48:50 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:48:50 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:48:50 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:48:50 GMT
ENV PYTHON_VERSION=3.10.20
# Tue, 03 Mar 2026 20:48:50 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Tue, 03 Mar 2026 20:52:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:52:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:52:56 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 21:00:55 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 21:00:55 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 21:00:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 21:00:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3be75dd81bf7bdd3f5e5b44d758992b7cadc463500edf47892550b34b4a467`  
		Last Modified: Tue, 03 Mar 2026 20:53:03 GMT  
		Size: 460.7 KB (460743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b456520732b0048628ff7ee6791fd3d5f22b0943e5036bb428dee3daa58fe8dc`  
		Last Modified: Tue, 03 Mar 2026 20:53:03 GMT  
		Size: 14.6 MB (14633206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb60d8a73e66381131499f1645b0dd9f37450650e50f2af020482ccdf2cb006`  
		Last Modified: Tue, 03 Mar 2026 20:53:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8517732d6e9d0e79496711024588f0141fba898cb5708dd20e38580e7a2bec54`  
		Last Modified: Tue, 03 Mar 2026 21:01:02 GMT  
		Size: 5.1 MB (5118823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:e95fedcbf9470cc3ef54ab40e156f88d9c37724626488d3dcffd2fc288d8a185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **711.9 KB (711893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c631d3571b9068f66ac18b4b53567f503ca6907d234a16af0ad1a9ac2eb6f44c`

```dockerfile
```

-	Layers:
	-	`sha256:a4548f9528bf94e6c036a57f08b861b993bd23255042307cc47f524a282a0efd`  
		Last Modified: Tue, 03 Mar 2026 21:01:14 GMT  
		Size: 702.4 KB (702374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6554387743cefb8623f97745ad750f97645496ad78f5ba2b2267e40bccaf5d1`  
		Last Modified: Tue, 03 Mar 2026 21:01:03 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:fbb2ab8ee12418d6608b0375f371422f7252277e8c7ba3dff13aac8b5cc7c58c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25410522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f04682cb8022116ec45be401f2a0bf2f684728e71498777bfcabca8c3a65e3`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:28:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:28:40 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:28:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:28:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:28:40 GMT
ENV PYTHON_VERSION=3.10.20
# Tue, 03 Mar 2026 20:28:40 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Tue, 03 Mar 2026 20:32:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:32:44 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:32:44 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 21:05:30 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 21:05:30 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 21:05:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 21:05:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa14904690ebafa0dbf281b61805a1e9518470a4e06a3afa8114b04d6e4d234`  
		Last Modified: Tue, 03 Mar 2026 20:32:51 GMT  
		Size: 463.0 KB (463004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9409d64e8d3f35fda2c21f05985a02f9b9dbe61e2cbc7991baedbb728f23f39`  
		Last Modified: Tue, 03 Mar 2026 20:32:52 GMT  
		Size: 15.6 MB (15631437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32955f7bd65eeba7e6c8039e3d6527947de86d72947f2f2a6e085b26f66ec2a2`  
		Last Modified: Tue, 03 Mar 2026 20:32:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07945088ce88e5e1ee1f8c57688dbe7e4c1bc8e916f45b81a0911c796652a68`  
		Last Modified: Tue, 03 Mar 2026 21:05:36 GMT  
		Size: 5.1 MB (5118741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:318bc4e03d5b44701583cc7881ba2351d4935ede45d104fc835e77152d926075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.0 KB (708979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebd1de2257d0dc7af5dcd309f3342bff34b5e2d075f71d445bb0489c578aa96`

```dockerfile
```

-	Layers:
	-	`sha256:d6c157362efb17fb8160a341aab54c624cfe319218c4237c416c7e896f7629e8`  
		Last Modified: Tue, 03 Mar 2026 21:05:36 GMT  
		Size: 699.4 KB (699420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54625fb640da0fabda5ecd53aa7fdb9f80137996048145d990d86431d26136af`  
		Last Modified: Tue, 03 Mar 2026 21:05:35 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.23` - linux; 386

```console
$ docker pull hylang@sha256:eaa1dda9b9a20c7b8e0cfb8cec53de3ffe5776ed0b7d14c51732061e666b17a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24949134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1fe55053980f2fa6a8b9ce8ffa12d9dbd6c4e8088e4bb69ddfcdc7f96a5a07`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:24:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:24:09 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:24:09 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:24:09 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:24:09 GMT
ENV PYTHON_VERSION=3.10.20
# Tue, 03 Mar 2026 20:24:09 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Tue, 03 Mar 2026 20:27:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:27:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:27:14 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 20:59:48 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 20:59:48 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 20:59:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 20:59:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d469519e5d5a5051087dc1ee760241f997f16fd104d45740b7b793a581aaf249`  
		Last Modified: Tue, 03 Mar 2026 20:27:20 GMT  
		Size: 461.2 KB (461238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061702ea3da5963434434f05c38eecc49aef6c6f38468baf88d6ccd7983dd66c`  
		Last Modified: Tue, 03 Mar 2026 20:27:21 GMT  
		Size: 15.7 MB (15682120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565c445becd4ec034d13eee20b520421e3fc972562bb2da33109f5d1025cc638`  
		Last Modified: Tue, 03 Mar 2026 20:27:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c33b204832f44c3c386cc2fec50416b2fd06e98974d2c5a2f5fa89ce884080d`  
		Last Modified: Tue, 03 Mar 2026 20:59:54 GMT  
		Size: 5.1 MB (5118530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:37e86ce2f6d5f96c5829cb232c48d1fb90a06520bf70c6791e6abca07ba720c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.3 KB (709275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1118edb8b6208c4881c4ee5d44e198e1ee2da86f8b0ac559ef2761fc2da1c69f`

```dockerfile
```

-	Layers:
	-	`sha256:ba8e92a9378a064663981c644f4fba8d5956c18db2c7e34e506540b2ca4776d0`  
		Last Modified: Tue, 03 Mar 2026 20:59:54 GMT  
		Size: 699.9 KB (699921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd80e8417d320a03ccedadfc67c08793a9653ac366c5c4d6c880f0d752aec806`  
		Last Modified: Tue, 03 Mar 2026 20:59:53 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.23` - linux; ppc64le

```console
$ docker pull hylang@sha256:1cb38b0fc13f98849e47e71c0149f14acc2b64582d927c9be0b305b42097610b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25723455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252b192fe2bcd8511a52c973abf1c07e35c2398cbd9a1549c08360e9bf700797`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 23:13:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 23:13:33 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 23:13:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 23:13:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 23:13:33 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 23:13:33 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Thu, 05 Feb 2026 00:54:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 05 Feb 2026 00:54:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Feb 2026 00:54:34 GMT
CMD ["python3"]
# Thu, 05 Feb 2026 01:46:39 GMT
ENV HY_VERSION=1.2.0
# Thu, 05 Feb 2026 01:46:39 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 05 Feb 2026 01:46:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 05 Feb 2026 01:46:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6689bfe5e4a666fe6d4700b49a99430d84d84b190a8049b76e21eb722dacf017`  
		Last Modified: Wed, 04 Feb 2026 23:25:20 GMT  
		Size: 463.5 KB (463514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d48829577d6124794761f93f213e7df230a8c51bcb12029ed3948e3fd9061a4`  
		Last Modified: Thu, 05 Feb 2026 00:54:50 GMT  
		Size: 16.3 MB (16254891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c22871407b12d2e974817ff43d6dfdb466e965ebf951cb92b44546336afec4d`  
		Last Modified: Thu, 05 Feb 2026 00:54:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd0a0d615cd8ddf4221b12e6188ad832fea7abccb2f7b9a260b04e871eaaa8c`  
		Last Modified: Thu, 05 Feb 2026 01:46:53 GMT  
		Size: 5.2 MB (5175157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:5caacccbd0660c9326a2aeffd281029517ff6e4ff7ddd01c78d0cd3da7147396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.8 KB (708847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f003f44c91263a79a70446bb7b81e52ca3e89d0fa1e49191bad2da4f6538e5`

```dockerfile
```

-	Layers:
	-	`sha256:6b1e8ad4d2c47d53c87d75f703dc0dc6c70a6d48a1ab6837da65d2bcc8e45456`  
		Last Modified: Thu, 05 Feb 2026 01:46:53 GMT  
		Size: 699.4 KB (699373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c164d52a7e813eb6b29f99ae482460eba2d36940c765dc94f10614e200a7f93b`  
		Last Modified: Thu, 05 Feb 2026 01:46:53 GMT  
		Size: 9.5 KB (9474 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.23` - linux; riscv64

```console
$ docker pull hylang@sha256:b1386f297d07553ba456a84077809a82528878083d1d6c4328783fb6255dbf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24631126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a32426e5e6dddac451f25cf91687bcdc516980e8c818ae61f4d910ec83093a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Sat, 07 Feb 2026 06:13:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Feb 2026 06:13:14 GMT
ENV LANG=C.UTF-8
# Sat, 07 Feb 2026 06:13:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 07 Feb 2026 06:13:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 07 Feb 2026 06:13:14 GMT
ENV PYTHON_VERSION=3.10.19
# Sat, 07 Feb 2026 06:13:14 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Sat, 07 Feb 2026 11:30:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Sat, 07 Feb 2026 11:30:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 07 Feb 2026 11:30:39 GMT
CMD ["python3"]
# Sun, 08 Feb 2026 03:32:14 GMT
ENV HY_VERSION=1.2.0
# Sun, 08 Feb 2026 03:32:14 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 08 Feb 2026 03:32:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 08 Feb 2026 03:32:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e39819e3cf6d3fa245855c76541c78c7c1ca1816ad2911ff1fb7346b8637fb`  
		Last Modified: Sat, 07 Feb 2026 06:48:29 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a96e9a35e618f308b5d89b5547ce43c913bbd4b9fdfbde576211a91f492be054`  
		Last Modified: Sat, 07 Feb 2026 11:31:29 GMT  
		Size: 15.4 MB (15409764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a0973fce903c4914095a167afaceb41daa74929e2c3bc5a63bbaedf63307`  
		Last Modified: Sat, 07 Feb 2026 11:31:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31648318bbb9e5ed95cf968c187471ecb0e85f85284393515f6966c953e62d1`  
		Last Modified: Sun, 08 Feb 2026 03:32:56 GMT  
		Size: 5.2 MB (5174633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:a1f64dcd4f73aefb158d0100464b02c5f9b09e52f422c2c0636191aeb01dabfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.8 KB (708842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99b91f37da0c204d926aca394c84368c43ef73814043a9cfdb2fa9166d81e3b`

```dockerfile
```

-	Layers:
	-	`sha256:b91a9d1c474215ad4b94566c12be77d3c3d942392ce675dec2e69db288aeafae`  
		Last Modified: Sun, 08 Feb 2026 03:32:55 GMT  
		Size: 699.4 KB (699369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f0a96892ea16bd460c164384b693ec82c803f1e67aee1d20e84af0e352282`  
		Last Modified: Sun, 08 Feb 2026 03:32:55 GMT  
		Size: 9.5 KB (9473 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:83b2d1e9b6e532453e618fdf19fbc652727c6be16062e333c171072af43f33aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25179477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504f01f798dd1ea5f4b5d1e4f86c38db94a15f9250747d02d4f104fe326aea2c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:59:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:59:34 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:59:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:59:34 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:59:34 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:59:34 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 21:33:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 21:33:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 21:33:31 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 22:11:08 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 22:11:08 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 22:11:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 22:11:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29058587d68ad61f251548ba458d73678a3184e42af633f8e3042bbd6e16752d`  
		Last Modified: Wed, 04 Feb 2026 21:06:22 GMT  
		Size: 461.7 KB (461738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080087da0f29c70a355b590701cb2bb2c8bafc0a8e4ec3471d94ff3be6d28c1e`  
		Last Modified: Wed, 04 Feb 2026 21:33:45 GMT  
		Size: 15.8 MB (15816863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b1b8a6ed6396476b2a5e13e86476e16ed9a3d882b6b9615b2395863c270d31`  
		Last Modified: Wed, 04 Feb 2026 21:33:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcedfed7be1057d9d12f1c0007a87258a648986bdffd2f463c8b8740415e4c1`  
		Last Modified: Wed, 04 Feb 2026 22:11:24 GMT  
		Size: 5.2 MB (5175294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:9975d57c9929c2cfbd0c5ba1d0a93ab5b1ce51015461271622f4d77291c3b7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.7 KB (708722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb744abcf0048a51ce7fea9604e2db838b0108e48898780bb0ad3790690571d2`

```dockerfile
```

-	Layers:
	-	`sha256:a44ae471404d6ef3f34d411eae9eeb5c5fce277856cef2f55352afede2721f96`  
		Last Modified: Wed, 04 Feb 2026 22:11:24 GMT  
		Size: 699.3 KB (699315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046833dc4a572003b7382d566b91eb26d5ce9f0407a2e6838e46bc705e591255`  
		Last Modified: Wed, 04 Feb 2026 22:11:24 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
