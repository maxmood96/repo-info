## `hylang:python3.12-alpine`

```console
$ docker pull hylang@sha256:91f2b58cfa5c4c8f0b36dfe341b847cae5245bb4a95a35a61e3c65ccb8e82d06
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

### `hylang:python3.12-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:93b9c785a82c4ead42dd02922bc0828d372807fa77dced0d8e519ac1883e5a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23470086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816e9968ff2dfffcc35924501743e4557b4871e541f11fcaebc4126fb27b25d5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:47:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:47:04 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:47:04 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:47:04 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 20:47:04 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 15 Apr 2026 20:47:04 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 15 Apr 2026 20:52:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:52:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:52:17 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:57 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:57 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254ac41e2afd13e7a1276627191463329b96d835eab35e7804fdad56d7e363d5`  
		Last Modified: Wed, 15 Apr 2026 20:52:25 GMT  
		Size: 455.7 KB (455663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd21a26fb55d22baaa317c98a4296e6a284dd39cc0f9e68ef781bb74adfd6dc7`  
		Last Modified: Wed, 15 Apr 2026 20:52:26 GMT  
		Size: 13.7 MB (13744435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4f2e6e1560fccb75f8aa9c6b7458b3179164f6378b125e533286c88351cd2a`  
		Last Modified: Wed, 15 Apr 2026 20:52:25 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1562eff9f0321ed59f898a6f8845f477a27308a667ff9b0084f5f31a5e9e122`  
		Last Modified: Wed, 27 May 2026 00:12:03 GMT  
		Size: 5.4 MB (5405549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:3e06c52b773c4e94389b91bca1c5508421f9fa4ec416a03adc83cf2c21dc72c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.4 KB (662375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e6435297d6ca88506cbd549378e423def872f28213b129c9cb043a1df2d94c`

```dockerfile
```

-	Layers:
	-	`sha256:6cc5294483512878c68b67b84cb20a14239d03d3d7adecbb64bc144543923b9d`  
		Last Modified: Wed, 27 May 2026 00:12:03 GMT  
		Size: 653.0 KB (652968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e7535b7be6aefeb279e4a9973a1bad029108e74465ebbfef92efa0cc884638`  
		Last Modified: Wed, 27 May 2026 00:12:03 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:f4c9466bad5def513f87a4b8fd3f05ec6333da0d535a4f7a6a5852b2ad57ebe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22741709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aea1085ccddf1012ce635fa154181ed5341e9f95f8bd3b1f79b96708054f7e1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:01 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:33:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:33:01 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 20:33:01 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 15 Apr 2026 20:33:01 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 15 Apr 2026 20:40:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:40:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:40:01 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:14 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:14 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9acd70edf35f4c011b86dd015dfa20cdac24055597fdc4dcdb6bd9a987e47c`  
		Last Modified: Wed, 15 Apr 2026 20:40:06 GMT  
		Size: 456.5 KB (456510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0ad7c2b5e69a3ec101dd50ec96e77749a28ab93ded503661a38cfaf7a761b3`  
		Last Modified: Wed, 15 Apr 2026 20:40:07 GMT  
		Size: 13.3 MB (13307580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e245c8bb614daf51b7b465beeda380bcb3732ba28c43b2a72488516314194ce`  
		Last Modified: Wed, 15 Apr 2026 20:40:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7340a06ccecde8ede6d330634d169249471cd07f7cef4dd3716bd9f13fc357df`  
		Last Modified: Wed, 27 May 2026 00:11:18 GMT  
		Size: 5.4 MB (5405506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:93784037dc044f9753c02b34ee430711f4365e98440d427c9b57a19e06f9a6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78589948f538dc6c4da4ed6b926f6b9348f5ac4934c932a96106a628a500a85`

```dockerfile
```

-	Layers:
	-	`sha256:2c6b4154400519b76c4338f281f5730fe3170b77470d32f0028afcc89db8fa54`  
		Last Modified: Wed, 27 May 2026 00:11:18 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:3c14d6c64f3197c31d429e0d7ab62268637842d67cd201a30ea8bd2d01177f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22052209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b016421ca628f34f115e14a3f2a9dc4ed16ceab33508cb71012650a392a2c06`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:42:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:42:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:42:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:42:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 20:42:40 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 15 Apr 2026 20:42:40 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 15 Apr 2026 20:49:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:49:50 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:49:50 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:42 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:42 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83f16a210a4ec71a02e87a4b4ba6979aa1bb1e6049c2bff7d339f6f06cdcc9d`  
		Last Modified: Wed, 15 Apr 2026 20:49:57 GMT  
		Size: 455.6 KB (455617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:854bc5c85e51653367955e32600e5ebaa821574eb5cbb23357883f4f6385cc72`  
		Last Modified: Wed, 15 Apr 2026 20:49:57 GMT  
		Size: 12.9 MB (12907550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93ec6c83c3ff8d57fca181a5197ff1794e424b75ec734b0ec12c00275eb16a4`  
		Last Modified: Wed, 15 Apr 2026 20:49:57 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7eff96905ac5196da299b04d0d744774607f20004e9bba45d6f9cb23a3c21`  
		Last Modified: Wed, 27 May 2026 00:11:48 GMT  
		Size: 5.4 MB (5405671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:173d8c0477ae9a0748e0c4721eeba1ead4b2687b3ba5a852c47269e2c180890c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.9 KB (664895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d5fbcebcce275f7760a7c36e7614800da3bea1908f56dc33eccf2ef12da16f`

```dockerfile
```

-	Layers:
	-	`sha256:936af38aae2d4cea9aecb7beb59a16426c5702349c79ef55ba8051d60b36aa51`  
		Last Modified: Wed, 27 May 2026 00:11:48 GMT  
		Size: 655.4 KB (655376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acec2b1bf3bada707d710f60aa537841fb0b8c6d042ee5c404ccf65cc655a289`  
		Last Modified: Wed, 27 May 2026 00:11:48 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:73132e33b6a45bf97cd5eecbbfb3a2fafe726563e866443890a4691cc330fe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23952665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9916a52ee558cfecea543e702279533566a190693e90e1a9b5f8ea2d836c8da8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:50:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:50:07 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:50:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:50:07 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 20:50:07 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 15 Apr 2026 20:50:07 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 15 Apr 2026 20:57:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:57:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:57:01 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:44 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:44 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3124cc6c064bced8b2c441577d9c793d290258b2eb87477d21572e5a938fb3cb`  
		Last Modified: Wed, 15 Apr 2026 20:57:07 GMT  
		Size: 457.9 KB (457915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74bec20749987ddac4cc74bd2f826b97908f1c8a71661be8e89e6e8468e634d9`  
		Last Modified: Wed, 15 Apr 2026 20:57:08 GMT  
		Size: 13.9 MB (13888939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b6ee55fad38c6a3dc2ee84c7a44ff2b3429fc3eef0d4c2a2cfeb230b0acd73`  
		Last Modified: Wed, 15 Apr 2026 20:57:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed3e4a2d2a55143b2816585461e4dda0380e0c2e96cd27b374c968a3ca06d2`  
		Last Modified: Wed, 27 May 2026 00:11:50 GMT  
		Size: 5.4 MB (5405691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:ef51dd90a5ea9b2fa4674794590ede21d40e2877edb63b7c95f38c5f579c8481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.0 KB (661981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70bf53b4b2c95ac4306aa7033465707259b72ec589cac817e32960557a09168`

```dockerfile
```

-	Layers:
	-	`sha256:ba44ff722ad520473a4c69205b7857c0c292e658419264dc8988226f1d64f3e9`  
		Last Modified: Wed, 27 May 2026 00:11:50 GMT  
		Size: 652.4 KB (652422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c27797668adeab233275075a8065985cab3f0dc2e09a62c90218fe9a2590e8`  
		Last Modified: Wed, 27 May 2026 00:11:50 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine` - linux; 386

```console
$ docker pull hylang@sha256:7a79c7e13bb4ea326c8f9f328acd413201553e0b847b88eefd559ecaf229ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23503574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7514bf58009e53c3ee87399fd3c73c0b0378ff86acff45d19e0c24d1a1aa0496`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:27:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:27:51 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:27:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:27:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 22:27:51 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 15 Apr 2026 22:27:51 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 15 Apr 2026 22:32:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:32:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:32:47 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:41 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:41 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051df14ec2707bc64f4f66c578ae7351e224a1e90bdc91cf811f202bf23376d4`  
		Last Modified: Wed, 15 Apr 2026 22:32:53 GMT  
		Size: 456.1 KB (456119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e3da77369a5157b5e1dfb6a926a5ea643b8fb0bbc493e28a98053905c0c71e`  
		Last Modified: Wed, 15 Apr 2026 22:32:54 GMT  
		Size: 14.0 MB (13951396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578ede26b8464a4425d8e85f97acc23500b5cc7aeb3dbe5036adb9547e5aceec`  
		Last Modified: Wed, 15 Apr 2026 22:32:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db62d6bdf46282f8151daecb2cdb3a267ef3a46ff97027677abb88ae0e159160`  
		Last Modified: Wed, 27 May 2026 00:10:46 GMT  
		Size: 5.4 MB (5405367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:34d3598d813240c97133335f2d436725914217a09c1cda27a62d15df795c4aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **662.3 KB (662277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad563d0902033c52371bade09531658c96e20f0f6b08a45d80d6936d7e9adba9`

```dockerfile
```

-	Layers:
	-	`sha256:23f723ac207dff2c3577c1ef8aaacf26f24a5700f528c97c34c5d64f82862140`  
		Last Modified: Wed, 27 May 2026 00:10:46 GMT  
		Size: 652.9 KB (652923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f9dfc6ae5c5ad880c100e7f8cbc44c16f932f8932e9e175eb48b0cc2afceecd`  
		Last Modified: Wed, 27 May 2026 00:10:46 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:0cf146fc250745c4ea4d74697f0f65b8ac1c7962040b91c3218da59b0679d95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.3 MB (24297433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8c2f4ca35adb4727a9ddebc0b2489124333067213db2647de532fab188b3af`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:29:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:29:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:29:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:29:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 22:29:19 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 15 Apr 2026 22:29:19 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 15 Apr 2026 22:39:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:39:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:39:40 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:23:03 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:23:03 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:23:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:23:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5188be2ff5f3202965415e6a0385e7bbfdefc53657428e80c9077bf02386c09e`  
		Last Modified: Wed, 15 Apr 2026 22:39:55 GMT  
		Size: 458.3 KB (458328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e794b0135cd63c236568b29175d327c28ab30f8b0139f9536b0acb50d628cc25`  
		Last Modified: Wed, 15 Apr 2026 22:39:55 GMT  
		Size: 14.6 MB (14602419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fe7145e06f9822bc532c59595f1de1df9edf316e1a5cde82007ff649889a03`  
		Last Modified: Wed, 15 Apr 2026 22:39:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b047a895b261bde0a28f6a472aaed311e531dae0e1046a34295d87457e11c3e0`  
		Last Modified: Wed, 27 May 2026 00:23:13 GMT  
		Size: 5.4 MB (5405510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:d23a1fc0b285461e4a1bd6e03d8af104facbb86d8de93fff7d2e15cc88c3a2bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.9 KB (661850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aced76aa8009594cb6a11e179a8301042d2ae04fdf807efae26e0f3f7a78df92`

```dockerfile
```

-	Layers:
	-	`sha256:e43903709a1f508fcaf18646fdd98fe55e4b7195cc4d075f6436779e646a928c`  
		Last Modified: Wed, 27 May 2026 00:23:13 GMT  
		Size: 652.4 KB (652375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd95024bb22f3bbf365f1d99de4f94621c2e339aaee67e68bac7a854a59a9a91`  
		Last Modified: Wed, 27 May 2026 00:23:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:d5e450f4e72e522fe130fd4733f8f9391e2d0d5a0de8687e396a840be66b450b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23183714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f630407dce201b6e470ce4ed747655ebb6509881c58d731bb5baab18b855c455`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 19:57:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 19:57:53 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2026 19:57:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 16 Apr 2026 19:57:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 16 Apr 2026 19:57:53 GMT
ENV PYTHON_VERSION=3.12.13
# Thu, 16 Apr 2026 19:57:53 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Thu, 16 Apr 2026 20:32:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 16 Apr 2026 20:32:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 16 Apr 2026 20:32:22 GMT
CMD ["python3"]
# Sat, 18 Apr 2026 06:40:34 GMT
ENV HY_VERSION=1.2.0
# Sat, 18 Apr 2026 06:40:34 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 18 Apr 2026 06:40:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 18 Apr 2026 06:40:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5938584958193c97edd29fd7dcb625012c86f6f8b1b1e786fedfa747f26cf307`  
		Last Modified: Thu, 16 Apr 2026 20:33:08 GMT  
		Size: 456.0 KB (455998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b45e4405b7d119ac05e6deb1b12f7d46181a2d767201ae327dd76149558069`  
		Last Modified: Thu, 16 Apr 2026 20:33:10 GMT  
		Size: 13.8 MB (13752130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692f1561e14bb53bd70d57a829575f18b76b4d6a571d15999ab53d2ca15a647a`  
		Last Modified: Thu, 16 Apr 2026 20:33:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1185eb90dea9f8e8cedf31d4e6c80cb1c90889cb765bf6e201442cdfe5bb1a`  
		Last Modified: Sat, 18 Apr 2026 06:41:13 GMT  
		Size: 5.4 MB (5387674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:69a8ecf0ef25cfb8754974aa17d840c4e7140969de5675cc9a7a75abc7994854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.8 KB (661845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a71e3f14b27b2fb9e00f9790756c7e8476892d98bc3849c4f4f345d9acbc843`

```dockerfile
```

-	Layers:
	-	`sha256:b770a7354012a42445bb0520f77a8733946c5af89fbdb6b956d9d6844ece2e34`  
		Last Modified: Sat, 18 Apr 2026 06:41:12 GMT  
		Size: 652.4 KB (652371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a1fd903d0aa408515584a18bfc0d43a1b8e48e496b88f2f5e2563d49f10afc`  
		Last Modified: Sat, 18 Apr 2026 06:41:12 GMT  
		Size: 9.5 KB (9474 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.12-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:dbe9ed75b9fae20d8e048b87848e17f092511045a320e7eed77f9acc33c13efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23861316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17e57114bcb203fbe538dbd27be5f45445242b558cbbcfb451f494e97f7b466`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:52:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:52:35 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:52:35 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:52:35 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 15 Apr 2026 22:52:35 GMT
ENV PYTHON_VERSION=3.12.13
# Wed, 15 Apr 2026 22:52:35 GMT
ENV PYTHON_SHA256=c08bc65a81971c1dd5783182826503369466c7e67374d1646519adf05207b684
# Wed, 15 Apr 2026 23:04:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 23:04:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 23:04:02 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:17:52 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:17:52 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:17:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:17:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17530f44152de0ad6ed44a81435a6dce19edd92bb0055e1dbf9552f43e43eeb9`  
		Last Modified: Wed, 15 Apr 2026 23:04:34 GMT  
		Size: 456.7 KB (456681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b707d06684c03bc45951e256770d82eec050bdee07335fd5b410738a27c8112f`  
		Last Modified: Wed, 15 Apr 2026 23:04:36 GMT  
		Size: 14.3 MB (14272235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04c1795d7eaeccc2caab01e89bcda395d35990eb977218bce2048799f52423a`  
		Last Modified: Wed, 15 Apr 2026 23:04:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdeb1267723b56a228bcf1cf79c3315dc39bec1b6137c09c3b157c0f0fe5d2e`  
		Last Modified: Wed, 27 May 2026 00:18:03 GMT  
		Size: 5.4 MB (5405620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:8e49b0d6f964558e203c2e7b4465a10511632f9031b2167370072a5f48cc295e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **661.7 KB (661724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0605c3173412fedeb2022597710964761a8dcfd7ef0646bc4cdfc33244e4ca`

```dockerfile
```

-	Layers:
	-	`sha256:bf95b43d2d614f5275ef20de1ab0b5b512cbad87089f8b8d0c8a77168ff63b32`  
		Last Modified: Wed, 27 May 2026 00:18:03 GMT  
		Size: 652.3 KB (652317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5d02e71a29acd9b4054343a2fb18194a6f8613c5365dfa0b9f9285abd0391a4`  
		Last Modified: Wed, 27 May 2026 00:18:03 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
