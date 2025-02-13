## `python:3-alpine`

```console
$ docker pull python@sha256:bb2c06f24622d10187d0884b5b0a66426a9c8511c344492ed61b5d382bd6018c
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

### `python:3-alpine` - linux; amd64

```console
$ docker pull python@sha256:6300bc7fef25b31114828045c8747aa649ffe83fd31391d611f064328eb6607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16634844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf03fe1f23ae12769dc7dfc3c1b2987115f41cbd8f4f49f6354817bd2b2aa2b`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465162ce757d18adee28732d5e0da71931baf4ac30cb47fb7ac1215533db8f88`  
		Last Modified: Fri, 07 Feb 2025 01:06:49 GMT  
		Size: 458.8 KB (458760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f470c1f353a748be125ee58f1ed0956578047a2b4d0331e7a2ea0d047e01a1`  
		Last Modified: Thu, 06 Feb 2025 23:34:30 GMT  
		Size: 12.5 MB (12534120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f2ebd6b42b7d5aff69075a40418bab899deb82279cc3da8ddda6ceec153aab`  
		Last Modified: Thu, 06 Feb 2025 23:34:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:96d624b37a4dd47b746153f50d0fec35f0df3e1772896bc4592597ba0ae55120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.1 KB (645144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe103f491bbc8a2881a6fb4d38eb3f000969e049a272700f10e272e355cd9ed1`

```dockerfile
```

-	Layers:
	-	`sha256:c358054b84d79def816b85550c261aed00c35c70bbda0d6504657f71ae87a26c`  
		Last Modified: Fri, 07 Feb 2025 01:16:26 GMT  
		Size: 621.3 KB (621289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272da05be0b517e4503b1c2cfb26a8adc16a6ffce542243d788335f67842d794`  
		Last Modified: Fri, 07 Feb 2025 01:16:27 GMT  
		Size: 23.9 KB (23855 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; arm variant v6

```console
$ docker pull python@sha256:076257f9a5f0a128dec34f42f80f5cef531ef3715d4d709adfd9fcb388235ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15977429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d2b45652c7da0c437d0a171540a7ba92fc3c2583f61177afdcdc8d9298bca2`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2dec769123af1f5a0c91c72bfe4e9f0159b1fda485ecb156007cf295004a14`  
		Last Modified: Tue, 14 Jan 2025 22:30:03 GMT  
		Size: 459.6 KB (459577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97fca3022e00e4b0806142cd8691a23c0c39b328af79902a01739c0bf7646b1`  
		Last Modified: Fri, 07 Feb 2025 01:12:09 GMT  
		Size: 12.2 MB (12153725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6d2cbc8bb1b54ee5b3d749b14b3917d537c5bbf4673822dbbd25fd2d368f1a`  
		Last Modified: Fri, 07 Feb 2025 01:12:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:15d463c8becca2a3bf068cfdcb4b244d1e78a7e047a95aca42c92fa66b847e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 KB (23774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c68ea4d4dc9ce22f06167b4988b58eabae4f2d141c6d453dabb5e55f24933d2`

```dockerfile
```

-	Layers:
	-	`sha256:f0429e2f307ceab6c850f6250e9819afd550da9205ebb7a3c4b2747f1432087a`  
		Last Modified: Fri, 07 Feb 2025 01:16:38 GMT  
		Size: 23.8 KB (23774 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; arm variant v7

```console
$ docker pull python@sha256:e843cb634d24a8a86d24a92157bab828c92e54c404d517671922ee8916630c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15390976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1953da04b5fc243ab439ed78a0e3edf1507868ba88404b616bcad595dd973f`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52fed4f44c67cbc108822cb67f010dfbf3a64ce27abbeff6c7c380b97b0a0f4`  
		Last Modified: Tue, 14 Jan 2025 22:30:03 GMT  
		Size: 458.7 KB (458718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e174fd7bb980b1f79f8f60c5e9ebfba122b26ddb87742696a8326080c6e57c38`  
		Last Modified: Fri, 07 Feb 2025 04:16:14 GMT  
		Size: 11.8 MB (11834896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7269383cab7eca56571adcd2148868e6b900e8da1d32fc8319857660698c5aaf`  
		Last Modified: Fri, 07 Feb 2025 05:06:41 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:7cd2b887f351883aeea59a43daab13a9bda73f8e4e9e2dfc605ae023a04f2a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.2 KB (648159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c0fa88d41ba869ae8f68b534879e9f1da1bd22241252e21d6c30af6b75d7cd`

```dockerfile
```

-	Layers:
	-	`sha256:fc79f1c2e64cc64efd26498df07e0fbb6e37f6af1ddafec06d3daca9a710df15`  
		Last Modified: Fri, 07 Feb 2025 04:16:23 GMT  
		Size: 624.2 KB (624170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da564a931310ca0d982ec46259fffdc6786a01e0b69484731e286c49f481d844`  
		Last Modified: Fri, 07 Feb 2025 04:16:25 GMT  
		Size: 24.0 KB (23989 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; arm64 variant v8

```console
$ docker pull python@sha256:b8abf817e72649c26716027081010036008d93b4344ec32c0cf66e8a9bb47291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17007906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabbea52047c8332369849de8288d9a1ea870579ce0f0a4260f77202a8b2a9e1`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d7468fbe113a6e37718cb11746a5cb65868b0f17928d7442639cc0f54f4a60`  
		Last Modified: Fri, 07 Feb 2025 04:06:44 GMT  
		Size: 460.8 KB (460844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19b94151f971279b2c59813e9b755e4cac9ed3bcbbb93932ccc096ec002f1cb`  
		Last Modified: Fri, 07 Feb 2025 04:06:45 GMT  
		Size: 12.6 MB (12554456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ed9b1ba37d67de201976655346dd1e94a254bbd16dca79d01f59de58886055`  
		Last Modified: Fri, 07 Feb 2025 04:06:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:01aeff7457b2cbe3102cd565bb276cc83be6b879d5f071a4922859b06c157181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.4 KB (645430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27db28bbfcd02239295ede63140debba3cd3000ade5f5f4fb775f118341bb251`

```dockerfile
```

-	Layers:
	-	`sha256:41da8a566f34f778af7cc3a78d44be48d57e09ad31f8b7e9c5c93eb5f84c3c93`  
		Last Modified: Fri, 07 Feb 2025 04:16:43 GMT  
		Size: 621.4 KB (621393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:726a261577b71d8a7800205643bbccc590550e7f1e1a569d58396fbaf25fb4aa`  
		Last Modified: Fri, 07 Feb 2025 04:16:45 GMT  
		Size: 24.0 KB (24037 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; 386

```console
$ docker pull python@sha256:71f8320da036180a64f4dd3ae5a9d5b943be382af05a7267b5c22c05d8fee625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16708568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdb67c580205143a0256be2391bf784cda0de8f6f4fc11f4894726a9c4e1c85`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acb8008336673a902ef2c1ed187f226031dd3513bd3453910dd5bc562623eae`  
		Last Modified: Fri, 07 Feb 2025 01:16:45 GMT  
		Size: 459.2 KB (459188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4116ed83f96d1b1a470e8a6c803b936fd58c4813bb5bfffc804dcdccc6dac5a5`  
		Last Modified: Fri, 07 Feb 2025 01:16:48 GMT  
		Size: 12.8 MB (12786007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1416b41bf16686a7025454870f1d4a5fcfc820484c27adc4670ba9e232804174`  
		Last Modified: Fri, 07 Feb 2025 01:16:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:fdfc8b3efee824f635816f30691d8ff1b58ba9479b95d78fdd2f1cad358e0f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **645.0 KB (645043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b39f6b7a34fa9141df9cdc0d79cb9d9f12f793aea0ca6ecff9e5ef778dfd52`

```dockerfile
```

-	Layers:
	-	`sha256:c0648eabcd3ff59bbcdf672f6b2dbdd47c1853854ef28e61e6c5e061aa50c129`  
		Last Modified: Fri, 07 Feb 2025 01:16:56 GMT  
		Size: 621.2 KB (621244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f59be18e203dfb1f9cc05d2929353fb3c5b5d72e6283a827c2f593fdf62eceae`  
		Last Modified: Fri, 07 Feb 2025 01:16:58 GMT  
		Size: 23.8 KB (23799 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; ppc64le

```console
$ docker pull python@sha256:daa5ca8cc36256be4b2231aa2876b77e15d33ba0ab03d61b8bd781bbc57fe088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17296202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5696f5e212fa6110f9d9dc5e430e08d64299a3b4e649bf41fe62a98fe9c2358d`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78682beede19196d68ea8312fad482211dddc22810f3e520b446a72a6396fc56`  
		Last Modified: Tue, 14 Jan 2025 22:15:40 GMT  
		Size: 461.3 KB (461293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c25c30c74985ee8caef3a07238f2f5aa85f2d2fc20c4b64a82624e8d45e3e7`  
		Last Modified: Fri, 07 Feb 2025 03:01:55 GMT  
		Size: 13.3 MB (13261058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bef4f3f8f99c8717cedc980410f7fae8bdd9d3c3618dff80f6207bec4b7cebc`  
		Last Modified: Fri, 07 Feb 2025 03:01:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:16ffb02369a2048355636979d81f7642f8777c5346a14c83a7daa1dc32e32f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.3 KB (643323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d15a2eeb92be638b4cb860eae4bcb5ab189228ad4b314f60424d96c6624f288`

```dockerfile
```

-	Layers:
	-	`sha256:d88b7242e93b7ef10c387b92618fc1471ec834fbb6ac9adceb28c173f2b429a5`  
		Last Modified: Fri, 07 Feb 2025 01:17:12 GMT  
		Size: 619.4 KB (619396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:977e4bfcecc25583bca1122b3dff54fc40872e12c34f2b53c7c4237178aef442`  
		Last Modified: Fri, 07 Feb 2025 06:40:35 GMT  
		Size: 23.9 KB (23927 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-alpine` - linux; s390x

```console
$ docker pull python@sha256:fd1d77c4ff2edaba54c513aa493d46eb75640d90142f616d02ded379837f9e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16923255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f95f51ca4f0e21ad77edbfa4ccd4a395a16b037879cfe50843ccce517212bd`
-	Default Command: `["python3"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_VERSION=3.13.2
# Tue, 04 Feb 2025 23:51:20 GMT
ENV PYTHON_SHA256=d984bcc57cd67caab26f7def42e523b1c015bbc5dc07836cf4f0b63fa159eb56
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 23:51:20 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560126eea99dc7dc8a2cdfd7e7f15c796c369f9a2a3c057c6afd6ff6a9320525`  
		Last Modified: Fri, 07 Feb 2025 01:17:16 GMT  
		Size: 459.7 KB (459689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd5e29954514d2568821cbd69cbeabcbdcc4059142849df3312283fa627747f`  
		Last Modified: Fri, 07 Feb 2025 01:17:18 GMT  
		Size: 13.0 MB (12996450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b5eeac16a1b86600291830e2928b70774a1debccc46dc2ec540e2c33455aeb`  
		Last Modified: Fri, 07 Feb 2025 01:17:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-alpine` - unknown; unknown

```console
$ docker pull python@sha256:9c79c7e26b80c6c0a32598a01085f7b643d583d105ff50e5449160bd53b3bbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.2 KB (643193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52420dd79a2defb04831a35d3f5b024c8dd2ddcacbc71139e9133977c7867ca6`

```dockerfile
```

-	Layers:
	-	`sha256:11d8d9f9ce9a72604c8bedf135b96de7f517779a8ab70c1a3279b4559a64814f`  
		Last Modified: Fri, 07 Feb 2025 01:17:27 GMT  
		Size: 619.3 KB (619338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827a712133807753ae21f36fa7e4a6a96de8d33e67ffe5c11df50ed173f05c5e`  
		Last Modified: Fri, 07 Feb 2025 03:02:16 GMT  
		Size: 23.9 KB (23855 bytes)  
		MIME: application/vnd.in-toto+json
