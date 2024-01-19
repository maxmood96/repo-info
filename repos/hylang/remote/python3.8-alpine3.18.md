## `hylang:python3.8-alpine3.18`

```console
$ docker pull hylang@sha256:5ab455513e440da01e65644468a62fdeeb821d4746df1488d93dcbac7fa19f60
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

### `hylang:python3.8-alpine3.18` - linux; amd64

```console
$ docker pull hylang@sha256:1b55060462f528991f9a3d41b3ed437f6329e42ce38e09ff3f5318176e8eaad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26051609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42fea06c4981f24c805bb7adb7efab802126f39eff05ce9c485e42fb6ab75ee`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5363d7c7ad3a7983ab3c7d72572f8e9abe624da19a7d1f5047d5896858545b35`  
		Last Modified: Tue, 05 Dec 2023 19:53:56 GMT  
		Size: 622.3 KB (622321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbb6be09fb2fac1f8087ee72971398d91ec1f1c05d7a4d8e3ebeec0e2a85fb7`  
		Last Modified: Fri, 19 Jan 2024 00:14:28 GMT  
		Size: 15.5 MB (15451287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1966658e4b5c54e5b33a06203051e9c40e5b2b07c51e677f62b24d9c2daf5ba`  
		Last Modified: Fri, 19 Jan 2024 00:14:26 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2c35e88e3c38a06531ba23650efc31418a406b648d73ea38504427f3592576`  
		Last Modified: Fri, 19 Jan 2024 00:14:27 GMT  
		Size: 2.9 MB (2851687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3d0fd86a9133e8789da8cc60f2b07471f0a76c30d406e2c09af13a2b31d411`  
		Last Modified: Fri, 19 Jan 2024 00:51:11 GMT  
		Size: 3.7 MB (3723649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:4b7d8a81d15d65c9e2bc2a2be2366f57ec6fbe4fc866899dfd9eb90c232f4a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ed0de502da656efc364db3f09ebaba6642b4c54876577dfb707128fb55bac7`

```dockerfile
```

-	Layers:
	-	`sha256:1203f4df5d9ea1f473879f318f47598c3c884f9bac4498d7962fa59381bef707`  
		Last Modified: Fri, 19 Jan 2024 00:51:11 GMT  
		Size: 863.3 KB (863345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39858e03b8b218b6734b078713e3322b22bd141ea0826f9827e23aa150120d4`  
		Last Modified: Fri, 19 Jan 2024 00:51:11 GMT  
		Size: 9.1 KB (9131 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; arm variant v6

```console
$ docker pull hylang@sha256:e9ff603b9e093315b173314293d134b9461e7d46c385c1d9c6a6ec5b1afff72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23327562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb29dba6a8f78aa2bcc5bc49d86a9b5e5e6a709c74df23ec0547ddf6db1142f`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 20:47:05 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 20:47:05 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_VERSION=3.8.18
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020e6d725b1f9117d8a0fd87888f83e8a35c75b310a29e508a21850a48d9f10d`  
		Last Modified: Fri, 01 Dec 2023 11:12:14 GMT  
		Size: 622.9 KB (622885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13ba64069d0e198925d4e51f765dfca5e24414ac800ac912ac531a167b78b02`  
		Last Modified: Fri, 01 Dec 2023 11:13:07 GMT  
		Size: 13.0 MB (12982607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ec20d9b22a06eab963b706e28e59f1d7c8a2edfb5be76284142988be2da338`  
		Last Modified: Fri, 01 Dec 2023 11:13:06 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68124a5722affc32d92e0b3dc6eeb0b721483440abeb5e8b1446681a1b90c5d`  
		Last Modified: Fri, 01 Dec 2023 11:13:06 GMT  
		Size: 2.9 MB (2851257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba89eae4ea009a737fc2ff351175b4d23b6eb5e2eab0c781f9de4f41597c401`  
		Last Modified: Mon, 08 Jan 2024 20:12:29 GMT  
		Size: 3.7 MB (3723715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:fbd3d011dc3b87ccc26c53c9966d460dae82cfa7d6e761e670e879fa5aa75749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 KB (8987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4d1c51a63e57f9a161107bbf03772b927c9ff89fb711a3f3606e8e900b768b`

```dockerfile
```

-	Layers:
	-	`sha256:61607376d2e32d4695dca4fa4a36f0431fcdf9a2c727102fd2fd7f86aabaa018`  
		Last Modified: Mon, 08 Jan 2024 20:12:29 GMT  
		Size: 9.0 KB (8987 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; arm variant v7

```console
$ docker pull hylang@sha256:fd8f447320c733c0845fe9b2ce302dd593ba89e52080ec900cf97035a184b394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22641542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:595bc4f280109a3d22b9e02bdb87df5465eb3586e54cc329bc672ce6f39539b0`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 20:47:05 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 20:47:05 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_VERSION=3.8.18
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff7e5a1e11ebe03d6acf7eb6082639d0e9d0e1385daeca0fd59c2a5245ba99f`  
		Last Modified: Fri, 01 Dec 2023 02:30:12 GMT  
		Size: 621.9 KB (621938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1128ab987f2c76fec3fd40b402e0803c4a59b04b677706961c87e9480ff1520`  
		Last Modified: Fri, 01 Dec 2023 02:31:25 GMT  
		Size: 12.5 MB (12542891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae30c859fd05ab01a8c42c8ac55eab99f1f32077303a96d8ced1278376e224`  
		Last Modified: Fri, 01 Dec 2023 02:31:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5101f9cf5c74d2c7aae4485a5625d7672954e24e967f5ef67247a90524623c7c`  
		Last Modified: Fri, 01 Dec 2023 02:31:25 GMT  
		Size: 2.9 MB (2851409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5b3dcd939c1afa75fac9710384c6b4318fe96f199c1983344a0d698061eca7`  
		Last Modified: Sat, 06 Jan 2024 05:00:29 GMT  
		Size: 3.7 MB (3724070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:3d8925dc3c5677ffb0a9dc43aeca97d1ecc89c3748be71de274bf313c086dacd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **874.3 KB (874257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0599e32852f97980b626cbcd7c90712972f676e517e8cb27d5027aab718b19`

```dockerfile
```

-	Layers:
	-	`sha256:d054db670d5387d9386b97f4f6913597975d2ecdb6e7e7b05f50e7bd25c75257`  
		Last Modified: Sat, 06 Jan 2024 05:00:29 GMT  
		Size: 865.9 KB (865873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9748bfa5f1b226c126394ca33879c694b07ce19af1686e05b0c56324d7d12d0`  
		Last Modified: Sat, 06 Jan 2024 05:00:28 GMT  
		Size: 8.4 KB (8384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:beeb05ffd5af1ba877af27adbd7c8849723cac33cb985ac2ad20984b61af078a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26375325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cc43db4db7e59e983d4af12257c3531edff6b19a2be5d0e6a8691edc017510`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 20:47:05 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_VERSION=3.8.18
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ed61460a111aaef7891660426e3a7b7b0f79c5767cc5d231b761daea57733`  
		Last Modified: Wed, 29 Nov 2023 05:41:29 GMT  
		Size: 624.7 KB (624729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e48b31ea544a634a87727859fdf0298125e8d56ad9cad6ff0532100c920b3b`  
		Last Modified: Wed, 29 Nov 2023 05:44:08 GMT  
		Size: 15.8 MB (15843340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27208895e86b12f41d98b0a959a468752f930fe8bcf2e54936034599a01ceec2`  
		Last Modified: Wed, 29 Nov 2023 05:44:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb09c705bb9111962148af3a33b4ea3386557e69f1961689566cb2396cda53`  
		Last Modified: Wed, 29 Nov 2023 05:44:08 GMT  
		Size: 2.9 MB (2851426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19497945d6b039e5160edebc32db779b0aff913d531e352c52d12c7fceca1213`  
		Last Modified: Sat, 06 Jan 2024 00:43:21 GMT  
		Size: 3.7 MB (3723771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:f35f323ee070bea4cd5bcc1839d08372355746986784395145444ddfc94c5206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.6 KB (872563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e810d614dce301f1f1879b4da60c4dcc38e1732dc0e51fc8c488d76c4a687216`

```dockerfile
```

-	Layers:
	-	`sha256:b9d5c874ac351bbcccfc3c50bcaebc8ad65863cb2ff2aacc58a17ece99dcad59`  
		Last Modified: Sat, 06 Jan 2024 00:43:21 GMT  
		Size: 864.2 KB (864239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15b81848556ad3bebf82161a3fa68a96b3d5e19bba87664a34058d177d7cb897`  
		Last Modified: Sat, 06 Jan 2024 00:43:21 GMT  
		Size: 8.3 KB (8324 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; 386

```console
$ docker pull hylang@sha256:b976b8da5273aaf41a9e103dd5f3fc4b9dbd8d1274da249f6d3c6ea4138bebea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23827591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bab36adc43f9690d9a0e7489d8b5a72fd92c425ca5e5b13dbe4f346e868b21`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 20:47:05 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 20:47:05 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_VERSION=3.8.18
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf5d54f9b80cc86c8bf93637d018e9432b6daf1aa4841e0302b2e9c5e4697a4`  
		Last Modified: Fri, 01 Dec 2023 07:08:31 GMT  
		Size: 622.3 KB (622335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2985ee17f93a079212c17311f189cdbbbf6dcfb523d80ca694e97138c39b190`  
		Last Modified: Fri, 01 Dec 2023 07:09:46 GMT  
		Size: 13.4 MB (13391101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d211a4c316dcc0b02e359063b6151d82a380ec0fce2f8391784992a2ed9d1cb6`  
		Last Modified: Fri, 01 Dec 2023 07:09:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c32dd96b485096c272bd9fe12da04597aefd517c18f70fd1828a4968bf7736`  
		Last Modified: Fri, 01 Dec 2023 07:09:45 GMT  
		Size: 2.9 MB (2851368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5d589077ecaeabf40be467c48e879dda6a0760e9da2214588980b71f86ec43`  
		Last Modified: Fri, 05 Jan 2024 23:55:50 GMT  
		Size: 3.7 MB (3723728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:959550e5e6806b59989ac4bd50de74eb477fa06925d13e343fe414190424f6ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.4 KB (872439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef96a395151b1c188f25734d673dcab6ab607e6f32ffa601d6485c9a604a706`

```dockerfile
```

-	Layers:
	-	`sha256:a18d5acba90666b3cb6edfd3a3a5a8f7051b63199d8e224b74d24374c3c78446`  
		Last Modified: Fri, 05 Jan 2024 23:55:50 GMT  
		Size: 863.3 KB (863336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bf59cd9337df8194a1d8d482705161de6a5fc378b23c1d74d27e028b9bece9f`  
		Last Modified: Fri, 05 Jan 2024 23:55:50 GMT  
		Size: 9.1 KB (9103 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; ppc64le

```console
$ docker pull hylang@sha256:1415c3be2bb826b3b618d7a9674abd42472677e2ccb65f19ff910c8e0f081884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26244071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c353370db34bf2b76a864cb483a5ef05bdffaeba3b247739c9962e5dd4da4634`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:04 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Thu, 30 Nov 2023 23:19:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 19:34:36 GMT
ENV LANG=C.UTF-8
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_VERSION=3.8.18
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Tue, 19 Dec 2023 19:34:36 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Tue, 19 Dec 2023 19:34:36 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Tue, 19 Dec 2023 19:34:36 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c450107b1f651e0d5357ddca15f10b7fe2195f41771b1c55d96c62001069b127`  
		Last Modified: Tue, 05 Dec 2023 20:02:45 GMT  
		Size: 624.9 KB (624906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abccb94f1af3e9bbfa0a1ddf7770be19c7b34512378aa608502799fc3f8f7bd5`  
		Last Modified: Fri, 19 Jan 2024 00:41:18 GMT  
		Size: 15.7 MB (15695082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7805cb3eb79642c5fc1951b2f7afefa57d02d6857e85ed46c7c10ec01a0a2ba`  
		Last Modified: Fri, 19 Jan 2024 00:41:15 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08978d2993e8ba556a68a11def6422a048b4b10984f820860adee977aba14d56`  
		Last Modified: Fri, 19 Jan 2024 00:41:16 GMT  
		Size: 2.9 MB (2851675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1353a50ad069b151a4dd2e0accd31a3f2adc4d228474f41bd4f2894a99c4f6c0`  
		Last Modified: Fri, 19 Jan 2024 02:36:52 GMT  
		Size: 3.7 MB (3723844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:7f8d2e4b3856e44efb4ec076c0fc282177df7077441e9cec05c0c541f4366d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.9 KB (870913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9d96a8298da877f19397fa5e5c747246752da3e1274215c85f13a40446f412`

```dockerfile
```

-	Layers:
	-	`sha256:616003ae2c46466dba930cdbbc139fc81a52ec92b7dd57bb5113799e875165d4`  
		Last Modified: Fri, 19 Jan 2024 02:36:52 GMT  
		Size: 861.7 KB (861743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721f9da28546794be95158d60b7ab86d0a7f7e36365f6f8fc68a845a2387b870`  
		Last Modified: Fri, 19 Jan 2024 02:36:52 GMT  
		Size: 9.2 KB (9170 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; s390x

```console
$ docker pull hylang@sha256:9e44cde29d5487c899e0bd778240b286f9e3ec3af090e3d37419bf0e6fdfd1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23769251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04353cec4695ff5b44cc35195cd97d4f922f000584989b32839b8ae5bada56a4`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 20:47:05 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 20:47:05 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_VERSION=3.8.18
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 20:47:05 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 20:47:05 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 20:47:05 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a35e8347eed15bdf065db4baf4be15e7227287d9f94ad22890350f3290e439`  
		Last Modified: Fri, 01 Dec 2023 02:09:37 GMT  
		Size: 623.0 KB (622975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00add8fe9a79e5ee3d3e50c08331af432125342f1af76c8a3a91116cd2332c03`  
		Last Modified: Fri, 01 Dec 2023 02:10:33 GMT  
		Size: 13.4 MB (13353516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f94b0bab44d718915df27399ef4204e9830a1e190d6a6a4004a816a28fb7cc`  
		Last Modified: Fri, 01 Dec 2023 02:10:33 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb45073e69c0eb1cd1a20c2768a4cc2b58630ad6adbf8c81634347a29c39b09`  
		Last Modified: Fri, 01 Dec 2023 02:10:33 GMT  
		Size: 2.9 MB (2851401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d0541e1a7f6fa2801ecb4ae7060429f32f0b1e2426c410f8a1f0fcc17ee93e2`  
		Last Modified: Sat, 06 Jan 2024 00:35:18 GMT  
		Size: 3.7 MB (3723676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:80a45d64d04c0301c8b8eed186c9963ef8488748d5a5c9ed192d25f641ee9f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.0 KB (870033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be9f88ce4173e523976f9e316627859b818a2ed31006405e5b51231dd0b9534`

```dockerfile
```

-	Layers:
	-	`sha256:eeb5d2baf5aee0a6af9930c4802066973dc10290bf6487e6b4a0eb4d1d757245`  
		Last Modified: Sat, 06 Jan 2024 00:35:17 GMT  
		Size: 861.7 KB (861719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:995cd95821b48010960794638630bbf3e433cc9c956b9a8769a0f7733f7f2a51`  
		Last Modified: Sat, 06 Jan 2024 00:35:17 GMT  
		Size: 8.3 KB (8314 bytes)  
		MIME: application/vnd.in-toto+json
