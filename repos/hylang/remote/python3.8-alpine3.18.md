## `hylang:python3.8-alpine3.18`

```console
$ docker pull hylang@sha256:6eeee31e6b0167fb49e177c3aa3156e571686fdbd80899899abf9b621294039b
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
$ docker pull hylang@sha256:825801d0002aea8cb10ec94347ab22b3184730cd47ef382f4ce3e983472977ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 MB (25152331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104930dafde3c5c2812d2fb075d4b8d8d3afae9a15c46233894dfd075845d693`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
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
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279ddce74df1089fd8408c1df4817404bf1429d5e1c26eba71dbe75693396243`  
		Last Modified: Tue, 05 Dec 2023 18:23:57 GMT  
		Size: 622.7 KB (622711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129509a1a2c78b1ea25decd48b85c7e74b0be9cbbd7250f04407c9b797d7921b`  
		Last Modified: Thu, 18 Jan 2024 23:51:45 GMT  
		Size: 14.8 MB (14806998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b172bfe993db12563a62f1751e170b89a8003300fab87e6e346b660a4b3f96`  
		Last Modified: Thu, 18 Jan 2024 23:51:43 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a47aa6c30eaaceac307916d48ee7c29a67c717b2850682ac4609fa78b2d0fd`  
		Last Modified: Thu, 18 Jan 2024 23:51:44 GMT  
		Size: 2.9 MB (2851738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca402227983f394692abf0449e3a7a9d5969896bbe5e0d8a786c396f596171f`  
		Last Modified: Fri, 19 Jan 2024 19:41:58 GMT  
		Size: 3.7 MB (3723770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:a02fb8c7190dfcbfb1ffa1052cc391118e6df0852d7cb82418a57843129fdf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 KB (8987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67868f5504adbac74bbabb651ab138308a54e9b8c3950c523dc845a2552be9d`

```dockerfile
```

-	Layers:
	-	`sha256:8c06f29995f70ab24a6c388ffda9472092290a4a50ce9847d0cd3a489c1a2843`  
		Last Modified: Fri, 19 Jan 2024 19:41:57 GMT  
		Size: 9.0 KB (8987 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; arm variant v7

```console
$ docker pull hylang@sha256:1f61cfaafbc2599ab71158e9d1b4694527ea4ecab279dc44647dc6924c229547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24386016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ab5976a687c96278bfae00663912ea7acceb4ddd5e14530f3d84a473e935a1`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
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
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6a3a8c72a8c1864813c622206dfebfe27ffe4515ca4764f1a5863c084c385a`  
		Last Modified: Tue, 05 Dec 2023 19:30:47 GMT  
		Size: 621.8 KB (621783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7944b3b97cc600de01d4407bf1e74a35599481b1d42090bd3b3d7be5db64b90`  
		Last Modified: Fri, 19 Jan 2024 04:12:34 GMT  
		Size: 14.3 MB (14287369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9400a60e6c499c7ae7cd71e614a999fde4fb750c72d23ceb3547dc9f51e7b`  
		Last Modified: Fri, 19 Jan 2024 04:12:31 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651d165b854bc44c86bb2dc0bfa5511ebad2884308e630c744d99793cd18dd58`  
		Last Modified: Fri, 19 Jan 2024 04:12:34 GMT  
		Size: 2.9 MB (2851687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f9410da523145ba896db1f04271cdd7c197a71e34979a75819aa6e015fc8e7`  
		Last Modified: Fri, 19 Jan 2024 10:29:39 GMT  
		Size: 3.7 MB (3723929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:e7c51a3962a49e6920e413bf165342ada4f81f220adfa939e3b3b807a0705efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.1 KB (875059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2beb78428779d526f227fb6d0ddc5215546e97cec6af2a15d36c8d2d9f05bfc`

```dockerfile
```

-	Layers:
	-	`sha256:1ef76961c7c1b8320616eb15b789a930fe459770b362f4de07f5849ebb7467c1`  
		Last Modified: Fri, 19 Jan 2024 10:29:38 GMT  
		Size: 865.9 KB (865857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e84180fad459b65a07c3141aa12559273e4ac917ff560c018c2e6643115260bd`  
		Last Modified: Fri, 19 Jan 2024 10:29:38 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:fc0f5d344827d5a5393ce1fb7a1d886ff1f2a028bc800f9aa5c8b6919891206c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (25950994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145977f555a12d8cdc4e3e8c2f6dfe15841dd69e5ab1c65c8c5304a34e2894a2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
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
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7687c947765812cb62b6294a5779d27f0df3310e38c77b4524b2be89bd39260`  
		Last Modified: Tue, 05 Dec 2023 18:58:51 GMT  
		Size: 624.5 KB (624520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be55aea7a7bd40a445dea3bbd04927ad600aa0eb9b0cfca8e84b76665d72ca8`  
		Last Modified: Fri, 19 Jan 2024 00:20:41 GMT  
		Size: 15.4 MB (15417787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da67a406d739b1437401db2d294ae989aefd224d134331590e983d5f227db49b`  
		Last Modified: Fri, 19 Jan 2024 00:20:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2b498b2d9bd29ff820e7e60846473dd300330538f3bb07836a80884ecf009e`  
		Last Modified: Fri, 19 Jan 2024 00:20:40 GMT  
		Size: 2.9 MB (2851705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733ee880a7f6f24dbccafb72fee6d280579f0f989f0e1af437616a98010e14e3`  
		Last Modified: Fri, 19 Jan 2024 04:38:41 GMT  
		Size: 3.7 MB (3723709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:56d461aae021a33bdf8a83f1169bb788922d3e189420c569cc5a784f5d00b1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037a771b51a9dd9153f5089c5851153aa303b3dd0ede6dbf01f49ee8bcb1e879`

```dockerfile
```

-	Layers:
	-	`sha256:3a606be977b9b20469094befb4f41713b14157745f15b269bf80cc556828a8a4`  
		Last Modified: Fri, 19 Jan 2024 04:38:41 GMT  
		Size: 863.4 KB (863356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:148c6e1944f8d07ff776371ce95b849593f848e24f664c3196fa4b8772da38c1`  
		Last Modified: Fri, 19 Jan 2024 04:38:40 GMT  
		Size: 9.1 KB (9142 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; 386

```console
$ docker pull hylang@sha256:7bdcfa03c79315ff06c11cae80ab04691a3a8bb7bb33cbe710a13f882ccfc698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25842402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530e47e54ac11f0a5f318b51a44110e3c4d4be195d3860573718d93e47a30934`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:44 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Fri, 01 Dec 2023 02:03:44 GMT
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
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffea944196344a71c68c27de834d0fcdc5eec752152b9f6fc6497ce5b6747f8f`  
		Last Modified: Tue, 05 Dec 2023 19:39:13 GMT  
		Size: 622.2 KB (622214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17af6a034582d1cbd56cd352faf647ea39963576a45399125b725914f4f8a1dc`  
		Last Modified: Fri, 19 Jan 2024 01:26:13 GMT  
		Size: 15.4 MB (15405692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1470d867065ae322b9c13d71c28f79f8a7cbc19438ff8bdbb3a358b9fa89b34`  
		Last Modified: Fri, 19 Jan 2024 01:26:10 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8a3c1486e909a068ec96807f99758b1c9faaac829b0882abf25db9ed72a7e2`  
		Last Modified: Fri, 19 Jan 2024 01:26:11 GMT  
		Size: 2.9 MB (2851691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e22c74c54b52eb03fa2de606cf77ae18b36a01bcb6f827b9a4f2e8d49e2d3d5`  
		Last Modified: Fri, 19 Jan 2024 02:50:52 GMT  
		Size: 3.7 MB (3723731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:131f8cb3f3928d838996109805bf4768f99be2d86f2b6300432a1340c686a924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.4 KB (872423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea31639952e47b897087f5be0f6e2520e811ab68ad474aa96a4c7611394a22dc`

```dockerfile
```

-	Layers:
	-	`sha256:8e0683fe7c7616873fa92ef2fd1f76ecc1cfb932ea6ca6ecb7657edf841c77d7`  
		Last Modified: Fri, 19 Jan 2024 02:50:51 GMT  
		Size: 863.3 KB (863320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b666a29fb2e2e974f16059c47d67a28aa55e9fe74a312fbe52532420ee1b59`  
		Last Modified: Fri, 19 Jan 2024 02:50:51 GMT  
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
$ docker pull hylang@sha256:86bc1fd2940a6efbc8e5b0beb7081e6c004bfdfd9f8b1ae5ceedd1ab502aa124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25714912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c006a5c6302cbe6625a5d002ea6f6bcb8d6f76f73b11eda43de439cd98efc9c1`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
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
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607af03b9a228e95db0cdffe1efee657c6cfa8771fb312b60948c7b142bfb77a`  
		Last Modified: Tue, 05 Dec 2023 19:11:08 GMT  
		Size: 622.8 KB (622835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b3b07e1f1bf72f9616ab0721d2ec1cea130c4057c10307d33cd34d2308cfae`  
		Last Modified: Fri, 19 Jan 2024 18:36:42 GMT  
		Size: 15.3 MB (15299124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c37c970e57ea4c206c0ff5e328e9ec2f8630d0b1d741912b107beb022107509`  
		Last Modified: Fri, 19 Jan 2024 18:36:40 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712be616faa79d3645dd34a243b2730204d0aedf5916e2282e9d7c165623890b`  
		Last Modified: Fri, 19 Jan 2024 18:36:41 GMT  
		Size: 2.9 MB (2851704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb30d46afb709584768605ffe8dff38d882bb85d66f3bb041ab24fbb5bbd823`  
		Last Modified: Sun, 21 Jan 2024 06:54:09 GMT  
		Size: 3.7 MB (3723552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:c93a433d7473f6d76d656229ad3f0d7c445cee5aa49e8b82524b7167cd239bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.8 KB (870835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d2f25a05244a316ca5a1af005b3e565d3dc96efd0f8ed5f65abea9695154b2`

```dockerfile
```

-	Layers:
	-	`sha256:91582d66e9a6230790462b8b2c3985295a1da68f5d587fa4076e5876c80effe3`  
		Last Modified: Sun, 21 Jan 2024 06:54:08 GMT  
		Size: 861.7 KB (861703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f68ec4a559bfcd6663674193863bc511bc8ca3f1ae8147c8c24d75bf05dc23d`  
		Last Modified: Sun, 21 Jan 2024 06:54:08 GMT  
		Size: 9.1 KB (9132 bytes)  
		MIME: application/vnd.in-toto+json
